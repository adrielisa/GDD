# Sistemas del Juego

## Descripción de la sección

Los sistemas son conjuntos de reglas y componentes que trabajan juntos: combate, inventario, IA, diálogo, progresión, economía, misiones, etc.

## Inventario de sistemas

| Sistema                             | Propósito                                                                                                                                               | Dependencias                                                                 | Estado |
| ----------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------- | ---------------------------------------------------------------------------- | ------ |
| Daño, Salud y Combate               | Gestionar puntos de vida del protagonista y enemigos, detección de _hitbox/hurtbox_ y eventos de muerte.                                                | Capas de colisión 2D, Animador, Sistema de Efectos/Game Feel.                |        |
| Controlador del Jugador y Movilidad | Procesar entradas del usuario, físicas de movimiento lateral, saltos y rebote vertical                                                                  | Motor de físicas 2D (`Rigidbody2D`, `Collider2D`), Input System.             |        |
| Sistema de IA de Hordas Menores     | Controlar el patrullaje, detección y embestida de las criaturas sobre la plataforma.                                                                    | Raycasts de suelo/borde, Transform del Jugador, Sistema de Daño.             |        |
| Cámara Reactiva y Encuadre          | Encuadrar de forma dinámica al protagonista en movimiento rápido, aplicar amortiguación y confinar la visión dentro de los límites de cada micro-arena. | `Transform` del Jugador, colliders de confinamiento de zona, Cinemachine 2D. |        |
| Gestor de Nivel y Flujo del Prólogo | Orquestar el avance del prólogo, activación de barreras en micro-arenas, eventos de derrota forzada inicial y cinemática final.                         | Triggers de escenario, UI Manager, Estados del Jugador.                      |        |

## Plantilla de sistema

### Plantilla de Sistema 01: Daño, Salud y Combate

- **Nombre:** Daño, Salud y Combate
    
- **Objetivo:** Administrar los valores de vida de Eon y de las criaturas, validar colisiones de ataque/vulnerabilidad, procesar la ventana de Choque de Tinta (_Parry_) y despachar eventos de daño o muerte.
    
- **Entradas:** Señales de colisión entre colliders en capas `Hitbox` y `Hurtbox`, identificador del atacante y daño asignado.
    
- **Procesamiento / reglas:**
    
    - Si un `Hitbox` de Eon y un `Hitbox` enemigo se tocan dentro de una ventana de 0.08 s, se anula el daño y se detona el Choque de Tinta (_Parry_).
        
    - Al recibir daño válido, se resta el valor a la salud actual de la entidad.
        
    - Si la entidad dañada es Eon, se activan 0.7 s de invulnerabilidad temporal (_i-frames_) con parpadeo de sprite.
        
    - Si la vida llega a 0, se apagan los colliders de la entidad y se llama a su rutina de muerte.
        
    - En cada impacto exitoso, se llama al efecto de congelación temporal (_hitstop_) y sacudida de pantalla.
        
- **Salidas:** Eventos `OnHealthChanged`, `OnParryTriggered`, `OnEntityDeath`, señal de activación de sacudida de cámara.
    
- **Estados posibles:** `Vulnerable`, `Invulnerable`, `HitStun`, `Dead`.
    
- **Dependencias:** Capas de colisión 2D, Animador, Sistema de Efectos/Game Feel.
    
- **Interacciones:** Informa al _Controlador del Jugador_ o a la _IA de Criaturas_ para aplicar aturdimiento y retroceso; notifica a la _Cámara Reactiva_ para aplicar vibración.
    
- **Datos que necesita:** Daño del ataque, vector de retroceso (_knockback_), duración de aturdimiento.
    
- **Datos que genera:** Puntos de salud restantes, estado de vida/muerte, posición de impacto para partículas.
    
- **Riesgos:** Registro doble de daño en un mismo fotograma o desincronización de cajas de colisión.
    
- **Criterios de aceptación:** Un impacto descuenta vida solo una vez, aplica retroceso en dirección opuesta al golpe y activa los cuadros de invulnerabilidad sin trabar la animación.

### Plantilla de Sistema 02: Controlador del Jugador y Movilidad

- **Nombre:** Controlador del Jugador y Movilidad
    
- **Objetivo:** Interpretar los comandos del jugador para controlar el desplazamiento lateral de Eon, las físicas de salto, el rebote aéreo descendente y las cancelaciones de animación mediante dash.
    
- **Entradas:** Ejes direccionales, botones de Salto, Ataque y Desplazamiento Fantasma (_Dash_) desde el Input System.
    
- **Procesamiento / reglas:**
    
    - El movimiento horizontal aplica aceleración directa con frenado inmediato al soltar la palanca.
        
    - Presionar ataque con dirección "Abajo" en el aire activa la caída en picada; si impacta un objetivo vivo, resetea la velocidad vertical con un impulso ascendente de rebote.
        
    - El Desplazamiento Fantasma (_Dash_) mueve a Eon a velocidad fija horizontal durante 0.15 s, ignora colisiones con enemigos y puede cancelar cualquier fotograma de ataque en tierra o aire.
        
    - Solo se permite 1 Dash aéreo hasta tocar el suelo o conectar un rebote.
        
- **Salidas:** Modificación de `velocity` en `Rigidbody2D`, cambio de parámetros en el Animator (`Speed`, `IsGrounded`, `IsDashing`), activación de `Hitboxes`.
    
- **Estados posibles:** `Idle`, `Run`, `Jump`, `Fall`, `Dash`, `DownStab`, `HitStun`.
    
- **Dependencias:** Motor de físicas 2D (`Rigidbody2D`, `Collider2D`), Input System, Sistema de Daño.
    
- **Interacciones:** Envía activación de hitboxes al _Sistema de Daño_; recibe bloqueos de control durante cinemáticas del _Gestor de Nivel_.
    
- **Datos que necesita:** Velocidad de carrera, fuerza de salto, fuerza de rebote vertical, duración del dash.
    
- **Datos que genera:** Posición global de Eon, vector de velocidad actual, orientación del sprite (Facing Direction).
    
- **Riesgos:** Atascos en esquinas de plataformas durante el dash o rebotes aéreos infinitos fuera del encuadre de cámara.
    
- **Criterios de aceptación:** El control responde inmediatamente a las entradas, el dash cancela los ataques en el fotograma solicitado y el rebote aéreo solo se activa al colisionar con entidades válidas.
    

### Plantilla de Sistema 03: Sistema de IA de Hordas Menores

- **Nombre:** Sistema de IA de Hordas Menores
    
- **Objetivo:** Manejar las rutinas de patrulla, detección y agresión de las criaturas básicas (Mímicos Monetarios, Crías de Gato-dragón) y del subjefe mediante máquinas de estados finitos simples.
    
- **Entradas:** Coordenadas de posición de Eon, colisiones de `Raycast2D` contra bordes de plataformas y paredes.
    
- **Procesamiento / reglas:**
    
    - Los enemigos patrullan horizontalmente hasta detectar un muro o un vacío mediante raycasts.
        
    - Si Eon entra en su radio de visión frontal, el enemigo pausa su marcha por 0.3 s (destello visual de advertencia) e inicia su embestida.
        
    - Las unidades voladoras ajustan su altura siguiendo un patrón oscilatorio y se lanzan en picada al tener a Eon en su cono inferior.
        
    - Si la entidad entra en estado `HitStun` por recibir daño, su temporizador de ataque se reinicia.
        
- **Salidas:** Modificación de posición/fuerza en el `Rigidbody2D` del enemigo, activación de animaciones y encendido de hitboxes hostiles.
    
- **Estados posibles:** `Patrol`, `Alert`, `Charge`, `Stunned`, `Dead`.
    
- **Dependencias:** Raycasts de suelo/borde, `Transform` del Jugador, Sistema de Daño.
    
- **Interacciones:** Consulta la posición de Eon; activa hitboxes que evalúa el _Sistema de Daño_; reporta su muerte al _Gestor de Nivel_.
    
- **Datos que necesita:** Radio de alerta, velocidad de carga, distancia del raycast de borde, tiempo de preparación de golpe (_windup_).
    
- **Datos que genera:** Estado actual de la criatura, hitboxes de daño en fotogramas específicos.
    
- **Riesgos:** Enemigos saltando accidentalmente al vacío o quedándose encallados corriendo contra paredes.
    
- **Criterios de aceptación:** Las criaturas detienen su avance antes de caer de plataformas no deseadas y muestran un aviso visual claro antes de soltar cualquier golpe.
    

### Plantilla de Sistema 04: Cámara Reactiva y Encuadre

- **Nombre:** Cámara Reactiva y Encuadre
    
- **Objetivo:** Mantener el foco sobre Eon con suavizado cinemático, anticipar su dirección de avance (_lookahead_), delimitar la vista dentro de cada arena y ejecutar sacudidas en los impactos.
    
- **Entradas:** `Transform` de Eon, volumen de confinamiento activo de la sala, llamadas de evento de impacto/parry.
    
- **Procesamiento / reglas:**
    
    - Sigue a Eon en los ejes X e Y con amortiguación suave (_damping_) para evitar saltos bruscos.
        
    - Si Eon corre continuamente en una dirección por más de 0.2 s, la cámara desplaza su centro ligeramente hacia adelante para mejorar la visibilidad.
        
    - Al entrar en una micro-arena, la cámara bloquea sus límites dentro del `PolygonCollider2D` de confinamiento asignado.
        
    - Al recibir un evento de golpe o parry, aplica un impulso de ruido (_Cinemachine Impulse_) proporcional a la fuerza del impacto.
        
- **Salidas:** Matriz de vista y proyección de la cámara principal (`Transform` de la cámara en escena).
    
- **Estados posibles:** `FollowPlayer`, `LockedInArena`, `ScreenShake`, `CinematicFocus`.
    
- **Dependencias:** `Transform` del Jugador, colliders de confinamiento de zona, Cinemachine 2D.
    
- **Interacciones:** Recibe llamadas de vibración desde el _Sistema de Daño_; recibe cambios de confinamiento desde el _Gestor de Nivel_.
    
- **Datos que necesita:** Coordenadas de Eon, límites del confinado de la sala, amplitud y frecuencia de sacudida.
    
- **Datos que genera:** Rectángulo de visión visible en pantalla (_frustum_ 2D).
    
- **Riesgos:** Salidas de encuadre hacia zonas vacías fuera del escenario o vibraciones excesivas que desorienten al jugador.
    
- **Criterios de aceptación:** La cámara no muestra zonas fuera del mapa al llegar a los extremos y las sacudidas duran menos de 0.2 s sin perder el foco del personaje.
    

### Plantilla de Sistema 05: Gestor de Nivel y Flujo del Prólogo

- **Nombre:** Gestor de Nivel y Flujo del Prólogo
    
- **Objetivo:** Controlar la progresión secuencial de los 15 minutos de juego, administrando la derrota inicial scriptada, el cierre de puertas en arenas de combate y la pantalla de cierre de la demo.
    
- **Entradas:** Señales de cruce de `BoxCollider2D` en modo trigger, eventos `OnEntityDeath` de los enemigos dentro de cada sector.
    
- **Procesamiento / reglas:**
    
    - En la escena inicial (minuto 0), monitorea la vida del coloso; al llegar al umbral de derrota, bloquea controles y desata la transición de caída.
        
    - Al ingresar a una micro-arena, activa barreras de colisión mágicas a los extremos e inicia el seguimiento de bajas.
        
    - Cuenta los enemigos eliminados en el área activa; al llegar a cero, desactiva las barreras y permite el paso.
        
    - Tras derrotar al Guardián Caído final, pausa el juego y muestra la interfaz de cierre con la ilustración final.
        
- **Salidas:** Activación/desactivación de GameObjects de barreras, bloqueo/desbloqueo de controles de Eon, llamadas al Canvas de UI.
    
- **Estados posibles:** `IntroBossEvent`, `LinearTraversal`, `ArenaFight`, `OutroEvent`.
    
- **Dependencias:** Triggers de escenario, UI Manager, Estados del Jugador, Sistema de Daño.
    
- **Interacciones:** Deshabilita temporalmente el _Controlador del Jugador_ en eventos narrativos; escucha bajas emitidas por el _Sistema de Daño_.
    
- **Datos que necesita:** Identificadores de triggers de zona, cantidad de enemigos por arena, prefabs de barreras de contención.
    
- **Datos que genera:** Índice de arena activa, estado de superación del prólogo.
    
- **Riesgos:** Una arena queda cerrada para siempre si un enemigo muere fuera de la detección del trigger.
    
- **Criterios de aceptación:** Cada arena cierra sus muros inmediatamente al cruzar el umbral y los retira de inmediato en el fotograma en que muere la última criatura.

## Relaciones entre sistemas

Describe qué sistemas dependen de otros y qué información intercambian.

#### Detalle de dependencias e intercambio de información

- **Controlador del Jugador y Movilidad $\leftrightarrow$ Daño, Salud y Combate:**
    
    - **Información que envía el Controlador:** Activa y orienta las cajas de colisión (`Hitbox`) según la animación en curso (tajo horizontal, caída descendente, dash). Envía las coordenadas del impacto.
        
    - **Información que devuelve el Sistema de Daño:** Notifica si el golpe conectó exitosamente para habilitar el _Rebote Aéreo_ (impulso vertical) o si Eon recibió un impacto para forzar el estado `HitStun`, descontar salud e iniciar los fotogramas de invulnerabilidad (_i-frames_).
        
- **IA de Hordas Menores $\leftrightarrow$ Daño, Salud y Combate:**
    
    - **Información que envía la IA:** Enciende los `Hitboxes` hostiles durante los cuadros activos de embestida o picada, y expone su `Hurtbox` para ser golpeada.
        
    - **Información que devuelve el Sistema de Daño:** Aplica retroceso (_knockback_), resta vida a la criatura, interrumpe su comportamiento con aturdimiento (`HitStun`) o ejecuta el evento de muerte cuando la salud llega a cero.
        
- **Daño, Salud y Combate $\leftrightarrow$ IA de Hordas Menores (Resolución de Choque / Parry):**
    
    - Si el `Hitbox` del arma de Eon y el `Hitbox` del ataque enemigo colisionan simultáneamente en la ventana de choque, el Sistema de Daño anula el daño mutuo y envía a la IA enemiga una orden directa de aturdimiento prolongado (1.2 s).
        
- **Daño, Salud y Combate $\rightarrow$ Cámara Reactiva y Encuadre:**
    
    - **Información enviada:** Cada impacto crítico, tajo aéreo o _Choque de Tinta_ despacha un pulso con dos variables: **Amplitud** (fuerza del temblor) y **Frecuencia** (rapidez de vibración). La cámara traduce estos datos en un movimiento reactivo de lente sin perder el seguimiento central de Eon.
        
- **Daño, Salud y Combate $\rightarrow$ Gestor de Nivel y Flujo del Prólogo:**
    
    - **Información enviada:** Cuando un enemigo agota su salud, el Sistema de Daño despacha el evento global `OnEntityDeath` junto con el identificador del enemigo. El Gestor de Nivel descuenta esa baja del contador interno de la micro-arena activa.
        
- **Gestor de Nivel y Flujo del Prólogo $\rightarrow$ Cámara Reactiva y Encuadre:**
    
    - **Información enviada:** Al cruzar el umbral de una zona de combate, el Gestor de Nivel actualiza la referencia del `Cinemachine Confiner` al nuevo `PolygonCollider2D` de la arena. Esto restringe el encuadre de la cámara dentro de los límites visuales de la pelea.
        
- **Gestor de Nivel y Flujo del Prólogo $\rightarrow$ Controlador del Jugador:**
    
    - **Información enviada:** Órdenes booleanas de interrupción (`EnableControl(false)` / `EnableControl(true)`). Se usan para congelar el movimiento del jugador durante la cinemática de caída inicial del minuto 0 y la pantalla final de cierre del prólogo.


> **Navegación:** [[00 - Índice]] · ← [[02 - Mecánicas]] · [[04 - Controles]] →
