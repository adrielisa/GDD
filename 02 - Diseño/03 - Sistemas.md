	# Sistemas del Juego

## Inventario de sistemas

| Sistema | Propósito | Dependencias | Estado |
| --- | --- | --- | --- |
| Daño, salud y combate | Vida y escudo de Eon y enemigos, *hitbox*/*hurtbox*, instakill y eventos de muerte. | Capas de colisión 2D, Animator, efectos/*game feel*. | En prototipo |
| Controlador del jugador y movilidad | Entradas, movimiento lateral, salto, doble salto, dash, ataques y habilidades activas. | `Rigidbody2D`, `Collider2D`, Input System, Inventario. | En prototipo |
| IA de enemigos comunes | Patrulla, detección y ataque de Aurion y Earthlem; reaparición. | Raycasts, `Transform` de Eon, sistema de daño. | En prototipo |
| IA de jefes | Patrones, fases y avisos de los tres jefes y La Entidad. | Sistema de daño, gestor de mundo, cámara. | En prototipo (Chasko; Driller provisional) |
| Inventario y equipamiento | Guardar habilidades y potenciadores; 3 ranuras de cada tipo; descripciones. | UI, guardado, controlador del jugador. | En prototipo (habilidades) |
| Economía de XP y tienda | Ganar XP y gastarla con el mercader. | Daño (muertes), UI, guardado. | Por implementar |
| Cámara reactiva y encuadre | Seguir a Eon, confinar la vista en arenas y aplicar sacudidas. | Cinemachine 2D, gestor de mundo. | En prototipo (seguimiento ajustado a píxel y sacudidas) |
| Gestor de mundo y progreso | Zonas, puntos de control, arenas de jefe, barreras y cinemáticas. | Triggers, UI, guardado, inventario. | En prototipo (puntos de control y arenas con muros) |
| Elementos de entorno | Géiseres, cañones, puertas entre escenas. | Físicas 2D, controlador del jugador. | En prototipo (géiseres) |
| Guardado | Persistir progreso entre sesiones. | Todos los anteriores. | Por implementar |

## Sistema 01: Daño, salud y combate

- **Objetivo:** administrar vida y escudo, validar colisiones de ataque y despachar eventos de daño y muerte.
- **Entradas:** colisiones entre capas `Hitbox` y `Hurtbox`, identificador del atacante, daño y bandera `isInstakill`.
- **Reglas:**
    - El daño normal se resta primero del escudo (si Eon tiene Coraza) y después de la vida.
    - Con Espinas punzantes equipada, cada golpe recibido de un enemigo tiene un 30 % de probabilidad de devolverle el 50 % del daño.
    - Un ataque **instakill** ignora escudo y dash; deja la vida en 0 y no activa Espinas punzantes.
    - Tras recibir daño, Eon tiene 0,7 s de invulnerabilidad con parpadeo rojo.
    - Vida y escudo **solo se restauran** al tocar un punto de control, al vencer a un jefe o al reaparecer. No hay curación en el campo.
    - Si la vida llega a 0 se apagan los colliders y se llama a la rutina de muerte.
    - Si el arma de Eon y la *hitbox* de un enemigo común chocan en el mismo fotograma, se anula el daño mutuo y solo recibe daño el enemigo (no aplica a jefes).
- **Salidas:** `OnHealthChanged`, `OnShieldChanged`, `OnEntityDeath`, `OnPlayerDeath`.
- **Estados:** `Vulnerable`, `Invulnerable`, `Petrified`, `HitStun`, `Dead`.
- **Riesgos:** daño registrado dos veces en un fotograma; instakill aplicado sin aviso visible.
- **Criterios de aceptación:** un impacto descuenta una sola vez, respeta la prioridad escudo → vida y la vida nunca sube fuera de un punto de control o de la muerte de un jefe.

## Sistema 02: Controlador del jugador y movilidad

- **Objetivo:** convertir las entradas en movimiento, salto, dash, ataques y habilidades, consultando qué está equipado.
- **Entradas:** dirección, Salto, Ataque (`Enter`), Dash, Tajo ardiente (`J`), Interactuar, Inventario.
- **Reglas:**
    - Movimiento con aceleración inmediata y frenado al soltar.
    - Doble salto, Tajo ardiente, Dash cortante y Espinas punzantes solo funcionan equipados.
    - Dash de 0,20 s y 4 u; 1 aéreo por salto; recarga de 1,2 s.
    - Abajo + Ataque en el aire ejecuta el ataque descendente; al impactar rebota y recupera el dash aéreo.
    - Los potenciadores equipados modifican los valores de forma permanente (vida máxima, daño, velocidad, recargas).
    - Durante cinemáticas, tienda e inventario el control queda bloqueado.
- **Salidas:** `velocity` del `Rigidbody2D`; parámetros del Animator (`Speed`, `IsGrounded`, `IsDashing`, `AirJumps`, `IsPetrified`); activación de *hitboxes*.
- **Estados:** `Idle`, `Run`, `Jump`, `DoubleJump`, `Fall`, `Dash`, `Attack`, `DownStab`, `FireSlash`, `Petrified`, `HitStun`, `Locked`.
- **Riesgos:** atascos en esquinas durante el dash; rebotes infinitos fuera de cámara.
- **Criterios de aceptación:** respuesta inmediata, dash que cancela ataques en el fotograma pedido y habilidades que solo funcionan equipadas.

## Sistema 03: IA de enemigos comunes

- **Objetivo:** rutinas de patrulla, detección, ataque y reaparición.
- **Reglas:**
    - Los terrestres patrullan hasta detectar un muro o un vacío con raycasts y nunca saltan al vacío.
    - Al detectar a Eon pausan 0,3 s con un destello de aviso antes de atacar.
    - Los voladores oscilan en altura y embisten cuando Eon entra en su cono.
    - Al recibir daño entran en `HitStun` y reinician su temporizador de ataque.
    - Reaparecen en sus posiciones iniciales cuando Eon descansa en un punto de control o vuelve a entrar a la zona.
- **Estados:** `Patrol`, `Alert`, `Attack`, `Stunned`, `Dead` (más `Buried` en Earthlem).
- **Salidas:** al morir sueltan orbes de XP.
- **Criterios de aceptación:** ningún enemigo cae de su plataforma por error, todos avisan antes de golpear y reaparecen correctamente.

## Sistema 04: IA de jefes

- **Objetivo:** ejecutar los patrones de cada jefe con fases y avisos.
- **Reglas comunes:**
    - Cada jefe tiene una tabla de ataques con peso, recarga y requisito de fase.
    - Nunca repite el mismo ataque más de 2 veces seguidas.
    - El cambio de fase ocurre por porcentaje de vida y va acompañado de una pausa protegida de 1,5 s en la que ni el jefe ni Eon reciben daño.
    - Los ataques instakill tienen aviso mínimo de 1,5 s y un sonido exclusivo.
    - Al morir: cinemática corta, habilidad guardada en el inventario, vida y escudo de Eon restaurados y apertura de la arena.
- **Datos:** vida, fases, tabla de ataques, ventanas de vulnerabilidad. Detalle por jefe en [[03 - Enemigos y NPC]].
- **Riesgos:** ataques superpuestos imposibles de esquivar; instakill sin salida.
- **Criterios de aceptación:** cada ataque se puede evitar **sin necesidad de ninguna habilidad concreta**, ya que el jugador decide qué equipar.

## Sistema 05: Inventario y equipamiento

- **Objetivo:** guardar lo obtenido y decidir qué se usa.
- **Reglas:**
    - **Habilidades:** se guardan todas las obtenidas; ninguna se descarta. Solo **3** pueden estar equipadas.
    - **Potenciadores:** se guardan todos los comprados; solo **3** pueden estar equipados. Los equipados están **siempre activos**; no hay botones de uso.
    - Al seleccionar cualquier habilidad o potenciador, el inventario muestra su **función** y, si la tiene, su **tecla de control**.
    - Una habilidad recién obtenida se guarda en el inventario y se avisa al jugador para que decida si la equipa.
    - El inventario se abre con `Tab` / `View`. Se puede cambiar el equipamiento en cualquier momento **fuera de una arena de jefe**.
- **Salidas:** habilidades activas al controlador; modificadores de los potenciadores equipados; iconos al HUD.
- **Riesgos:** aplicar dos veces el modificador de un potenciador al reequiparlo.
- **Estado en el prototipo:** las habilidades ya se guardan, se equipan (máximo 3) y se aplican al controlador; el cambio se bloquea con los muros de una arena cerrados. Se manejan desde el menú de pausa (ver [[04 - Controles]]). Faltan los potenciadores, el guardado entre sesiones y los iconos en el HUD.
- **Criterios de aceptación:** nunca hay más de 3 habilidades ni 3 potenciadores equipados; los cambios se reflejan de inmediato en el control, los valores y el HUD.

## Sistema 06: Economía de XP y tienda

- **Objetivo:** convertir el combate en potenciadores.
- **Reglas:**
    - Cada enemigo suelta su XP como orbes al morir; los jefes dan cantidades mayores. Codicia aumenta un 25 % la XP obtenida.
    - La XP no sube niveles. Tope de 9999. Se conserva al morir.
    - El mercader está en la antesala de cada jefe. Cada potenciador se compra una sola vez; los ya comprados aparecen como «Adquirido».
    - La compra se bloquea si falta XP.
- **Criterios de aceptación:** el contador del HUD y el de la tienda coinciden siempre; una compra descuenta una sola vez y el potenciador aparece en el inventario.

## Sistema 07: Cámara reactiva y encuadre

- **Reglas:**
    - Seguimiento en X e Y con amortiguación y *lookahead* hacia la dirección de avance.
    - En arenas de jefe la cámara se confina a los límites de la arena y, si el jefe es muy grande (Jefe 3, La Entidad), se aleja para mostrarlo.
    - Sacudida de cámara en impactos fuertes. **No es configurable** ni se puede desactivar.
- **Estados:** `FollowPlayer`, `LockedInArena`, `ScreenShake`, `CinematicFocus`.
- **Criterios de aceptación:** nunca muestra zonas fuera del mapa y siempre deja ver el aviso de un ataque instakill.

## Sistema 08: Gestor de mundo y progreso

- **Objetivo:** controlar el recorrido de las zonas, los puntos de control, las arenas y los eventos narrativos.
- **Reglas:**
    - Registra jefes derrotados y habilidades obtenidas.
    - El camino principal nunca exige una habilidad concreta; las rutas opcionales pueden pedir Doble salto o Tajo ardiente y muestran una pista visual.
    - Los puntos de control restauran vida y escudo y hacen reaparecer a los enemigos comunes.
    - Al cruzar la entrada de una arena de jefe se cierran sus límites:
        - **Jefe 1, Jefe 3 y La Entidad:** barreras **invisibles**.
        - **Jefe 2:** la sala del templo ya está cerrada por sus muros; al empezar el combate las **puertas** se sellan.
    - Al morir el jefe, las barreras se retiran.
    - Las zonas superadas siguen accesibles para volver a acumular XP.
    - Tras el Jefe 3 reproduce la ilustración de la serpiente petrificada y activa el puente hacia la isla final.
    - Tras La Entidad, bloquea el control y lanza el final y los créditos.
- **Estados:** `Intro`, `Exploration`, `BossArena`, `Cinematic`, `Ending`.
- **Riesgos:** una arena que queda cerrada si el jefe muere fuera del trigger.
- **Criterios de aceptación:** cada arena se cierra al entrar y se abre en el fotograma en que muere el jefe.

## Sistema 09: Elementos de entorno

- **Géiser:** ciclo reposo/aviso/erupción; lanza a Eon por un arco fijo hacia un punto destino. Ver [[02 - Mecánicas]].
- **Cañón:** solo en la isla final; dispara al interactuar y daña a La Entidad.
- **Puertas entre escenas:** la del templo del Mago (en Eretz) se usa con Interactuar y funde a negro hacia `Ruina_Mago`; las de dentro llevan de vuelta a Eretz. Ninguna funciona durante un combate de jefe.

## Relaciones entre sistemas

- **Controlador ↔ Daño:** el controlador activa las *hitboxes* de espada, descendente, Tajo ardiente y Dash cortante; el sistema de daño confirma impactos (para el rebote), aplica el daño recibido y, con Espinas punzantes, decide si devuelve parte al atacante.
- **Inventario → Controlador:** indica qué habilidades están equipadas y qué modificadores aplican los potenciadores.
- **Tienda → Inventario:** cada compra añade el potenciador al inventario.
- **Daño → Economía:** `OnEntityDeath` genera los orbes de XP del enemigo.
- **IA de jefes → Gestor de mundo:** la muerte del jefe guarda la habilidad, restaura a Eon, abre la arena y registra el progreso.
- **Gestor de mundo → Cámara:** cambia el confinamiento al entrar a una arena y activa el foco cinemático.
- **Gestor de mundo → IA de enemigos:** ordena la reaparición al usar un punto de control.
- **Todos → Guardado:** el progreso se escribe al tocar un punto de control, al derrotar un jefe, al comprar y al cambiar el inventario.

> **Navegación:** [[00 - Índice]] · ← [[02 - Mecánicas]] · [[04 - Controles]] →
