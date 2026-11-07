# True Hero — GDD completo

**Versión 0.2.1 · 7 de noviembre de 2026.**


---

## True Hero: resumen del diseño

**GDD 0.2.1 · 7 de noviembre de 2026.**

Eon, el héroe de la profecía, ya perdió contra La Entidad. Despierta solo en la costa de Kastleland sin su equipo legendario y emprende la revancha: recorre zonas explorables, derrota enemigos que le dan XP, cambia esa XP por potenciadores permanentes con un mercader que aparece antes de cada jefe y vence a tres jefes que le devuelven sus habilidades. Al caer el tercero, su cuerpo petrificado forma el puente hacia la isla final, donde Eon vuelve a enfrentar a La Entidad.

### Recorrido

```text
Cómic (derrota de Eon) → Costa → Jefe 1 → Bosque → Ruinas → Jefe 2 → Archipiélago → Jefe 3
   → Puente de la Serpiente → Isla Final → La Entidad → Final
```

### De un vistazo

| Área | Contenido |
| --- | --- |
| Control | Mover, salto, dash (`Shift`), ataque con espada (`Enter`), ataque descendente, Tajo ardiente (`J`), Escama pétrea (`K`). |
| Vida | Sin curación en el campo: vida y escudo se restauran solo en puntos de control y al vencer a un jefe. |
| Economía | XP de los enemigos → potenciadores del mercader. Los enemigos reaparecen; se puede volver a zonas superadas. |
| Potenciadores | 6, permanentes y pasivos; **3 equipados**, siempre activos, sin botones. |
| Habilidades | Doble salto (Jefe 1), Tajo ardiente y Dash cortante (Jefe 2), Escama pétrea (Jefe 3). **3 equipadas**; ninguna se descarta. |
| Inventario | Muestra la función y el control de cada habilidad y potenciador. |
| Enemigos | Aurion, Earthlem y Vestigio. |
| Jefes | Camarón serpiente (costa), Mago oscuro (ruinas planas), Serpiente gigante (islas de tierra flotante), La Entidad (isla final). |
| Mundo | 5 zonas explorables con rutas opcionales; géiseres entre islas. |

### Jefes

| Jefe | Lo esencial | Entrega |
| --- | --- | --- |
| Camarón serpiente | Libera camaroncitos voladores, embiste y muerde; antes de su ráfaga de agua instakill aparece una plataforma de agua para ponerse a salvo. Límites invisibles. | Doble salto |
| Mago oscuro | Arena plana sin plataformas, cerrada por pilares de las ruinas. Llamaradas del cielo, ola de picos de magma de la que hay que huir, escudo periódico, cráneos de fuego teledirigidos y teletransporte al otro extremo. | Tajo ardiente + Dash cortante |
| Serpiente gigante | Rodea islas flotantes; su cuerpo deja caer baba; tocar la cabeza es instakill. Al morir se petrifica y forma el puente. Límites invisibles. | Escama pétrea |
| La Entidad | Ascenso por islas con géiseres y cañones; cara a cara en la cumbre; fase final. Límites invisibles. | Victoria |

### Pendiente

- Cerrar la fase 3 de La Entidad.
- Nombres de jefes, camaroncitos y Vestigio.
- Asignar roles del equipo.

### Dónde consultar cada parte

- [[02 - Mecánicas]] y [[03 - Sistemas]]: reglas y valores.
- [[04 - Controles]]: mapa de teclas.
- [[06 - Economía y Recursos]]: XP y potenciadores.
- [[02 - Niveles]]: zonas.
- [[03 - Enemigos y NPC]]: enemigos, jefes y mercader.
- [[03 - Registro de Decisiones]]: qué se decidió y por qué.


---

## Ficha del Proyecto

### Información general

| Campo                        | Información                                                                                                                                 |
| ---------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------- |
| **Nombre del proyecto**      | True Hero                                                                                                                                   |
| **Nombre clave**             | Revancha                                                                                                                                    |
| **Versión del GDD**          | 0.2.1                                                                                                                                       |
| **Estado del proyecto**      | Preproducción (diseño cerrado de la estructura; prototipo en curso)                                                                         |
| **Equipo**                   | García Velázquez Marco Damián<br>González Cruz Celeste<br>Rodríguez Pacheco Adriel Isaí<br>Trujillo Torres Sergio Joel<br>Vargas Pérez Joel |
| **Responsable del proyecto** | González Cruz Celeste                                                                                                                       |
| **Fecha de inicio**          | 05 / Octubre / 2026                                                                                                                         |
| **Última actualización**     | 07 / Noviembre / 2026                                                                                                                       |
| **Repositorio**              | https://github.com/adrielisa/GDD                                                                                                            |

### Identidad del videojuego

| Elemento | Decisión |
| --- | --- |
| Género principal | Plataformas 2D |
| Subgéneros | Acción y aventura · exploración por zonas · combate contra jefes |
| Plataforma objetivo | PC |
| Modo de juego | 1 jugador |
| Perspectiva | Lateral 2D (*side-scroller*) |
| Clasificaciones y etiquetas | Fantasía medieval, pixel art, jefes, progresión por habilidades. Consulta [[06 - Clasificaciones y Etiquetas]]. |
| Tecnología principal | Unity (Editor y Runtime), C#, Clip Studio para sprites y assets, Claude como apoyo de productividad y auditoría. |

### Elevator Pitch

> _¿Qué pasa cuando el héroe elegido ya perdió?_ Eon, el héroe de la profecía, fue derrotado por La Entidad. Ahora recorre un mundo en ruinas, derrota a tres jefes para arrebatarles sus habilidades, cambia la experiencia de cada combate por potenciadores permanentes con el mercader y vuelve a la isla final por su revancha.

### Resumen en cifras

| Contenido | Cantidad |
| --- | ---: |
| Zonas explorables | 5 (más la isla final) |
| Jefes normales | 3 |
| Jefe final | 1 (La Entidad) |
| Enemigos comunes | 3 (Aurion, Earthlem, Vestigio) |
| Habilidades obtenibles | 4 |
| Ranuras de habilidad | 3 |
| Potenciadores en catálogo | 6 |
| Ranuras de potenciador | 3 |

### Estado actual

- [x] Concepto definido
- [x] Alcance inicial definido
- [x] Mecánica principal definida
- [ ] Prototipo funcional
- [ ] Vertical slice (Costa + Jefe 1)
- [ ] Producción
- [ ] Pruebas
- [ ] Versión final

### Criterio de éxito del proyecto

- **Mínimo entregable:** la Costa jugable de principio a fin: despertar de Eon, enemigos comunes, mercader en la antesala, combate contra el Jefe 1 y obtención del doble salto en el inventario.
- **Objetivo completo:** los tres jefes, las zonas explorables, la cinemática de la serpiente petrificada y la batalla final contra La Entidad.


---

## Visión del Juego

### Concepto central

True Hero empieza donde otras historias terminan: el héroe profetizado ya peleó contra la calamidad y perdió. Eon fue derrotado por **La Entidad**, un titán cósmico que arrasó el 98 % de la civilización de Eretz. El juego no cuenta cómo cumple su destino, sino cómo se gana una segunda oportunidad.

Eon despierta solo en la costa de Kastleland, sin su armadura ni su arma legendaria. Para volver a enfrentar a La Entidad recorre zonas explorables, derrota enemigos que le dan **puntos de experiencia (XP)** y vence a **tres jefes** que custodian habilidades. Cada jefe vencido le devuelve una habilidad; la XP se cambia por **potenciadores permanentes** con un mercader que aparece antes de cada jefe. Cuando cae el tercer jefe, su cuerpo petrificado se convierte en el puente hacia la isla final, donde espera La Entidad.

La fantasía que el jugador vive es la **revancha ganada a pulso**: la profecía no bastó, pero el esfuerzo, la preparación y lo aprendido en cada combate sí.

### Experiencia deseada

- **Quiero que el jugador se sienta:** vulnerable al inicio, porque sabe que el héroe ya perdió; después, cada vez más capaz, hasta sentirse listo para la revancha.
- **Quiero que el jugador piense:** «Ya sé cómo me venció. Esta vez llego preparado».
- **Quiero que el jugador haga:** explorar, esquivar ataques, aprender los patrones de cada jefe y decidir qué habilidades y potenciadores llevar.
- **Quiero que el jugador recuerde:** a cada jefe por su forma de pelear, el momento en que la serpiente se petrifica y abre el camino, y el combate final contra La Entidad.

### Fantasía del jugador

Ser el héroe caído que no acepta la derrota y vuelve más fuerte, no por destino, sino por lo que consiguió en el camino.

### Propuesta de valor

- Un protagonista que empieza derrotado: el cómic inicial muestra la caída de Eon y el control se entrega justo después.
- Tres jefes con identidad propia (una serpiente-camarón en la costa, un mago oscuro entre ruinas y una serpiente gigante entre islas de tierra flotante), cada uno con una habilidad que cambia la forma de jugar.
- Una decisión constante: solo caben **3 habilidades** y **3 potenciadores** equipados a la vez.
- Un mundo medieval de fantasía con estética colorida y carisma en los diseños.

### Características principales

1. **Revancha estructurada:** tres jefes antes de volver a enfrentar a La Entidad.
2. **Habilidades por jefe:** Doble salto, Tajo ardiente, Dash cortante y Escama pétrea. Ninguna se descarta; el jugador elige cuáles equipar.
3. **XP para el mercader:** los enemigos comunes sueltan XP que se cambia por potenciadores permanentes. Los enemigos reaparecen y se puede volver a zonas superadas para acumular más.
4. **Vida que se gana:** no hay curación en el campo; vida y escudo solo se restauran en puntos de control o al vencer a un jefe.
5. **Géiseres:** el cruce entre ciertas islas se hace con géiseres que lanzan a Eon por el aire.

### Diferenciadores

- Rompe el cliché del héroe que progresa en línea recta: la historia empieza con su fracaso.
- El jugador arma su propio equipo de tres habilidades y tres potenciadores para cada desafío.
- Los ataques más peligrosos (instakill) siempre ofrecen una salida legible: la plataforma de agua del Jefe 1 o evitar la cabeza de la serpiente del Jefe 3.

### Límites del concepto

- No es multijugador.
- No es un mundo abierto: las zonas están conectadas en un orden principal con rutas opcionales.
- No hay subida de nivel del personaje; la XP solo se gasta con el mercader.
- No hay aliados, acompañantes ni rescate de personajes.
- No hay objetos de curación ni objetos que recoger aparte de la XP.


---

## Público y Plataforma

### Público objetivo

| Elemento | Decisión |
| --- | --- |
| Edad aproximada | +12 años |
| Experiencia esperada | Casual a intermedia; se esperan varios intentos por jefe. |
| Intereses relevantes | Juegos de acción, plataformas 2D, combates contra jefes y fantasía medieval. |
| Conocimientos previos | Ninguno. Los controles se enseñan en la Costa antes del primer jefe. |

### Plataforma

| Elemento                | Decisión          |
| ----------------------- | ----------------- |
| Plataforma principal    | PC                |
| Plataformas secundarias | —                 |
| Método de entrada       | Teclado / Control |
| Resolución objetivo     | 1920 × 1080 (Full HD) |
| Relación de aspecto     | 16:9              |
| Rendimiento objetivo    | 60 FPS estables   |
| Conexión requerida      | No                |

### Restricciones de plataforma

- Todo debe jugarse con teclado sin ratón; el ratón solo es opcional en menús.
- Los mandos de Xbox y PlayStation usan el mismo mapa a través del Input System de Unity.
- El guardado es local y no requiere cuenta ni conexión.

### Sesión de juego

| Medida | Estimación |
| --- | --- |
| Sesión típica | 15 a 20 minutos (una zona y su jefe). |
| Combate contra un jefe | 2 a 4 minutos por intento. |
| Duración total | 45 a 60 minutos para un jugador que lo termina por primera vez. |

### Modelo de distribución

Gratuito.

### Consideraciones

- [x] Controles adaptados a la plataforma
- [ ] Interfaz legible a 1080p y en ventana
- [ ] Rendimiento verificado en un equipo de gama media
- [ ] Resoluciones 16:9 alternativas (1280 × 720, 2560 × 1440)
- [x] Guardado local compatible


---

## Pilares de Diseño

### Pilar 1 — La revancha se gana

**Descripción:** Eon ya perdió una vez. Todo lo que el jugador consigue (habilidades, potenciadores, conocimiento de los patrones) debe sentirse como preparación para volver a enfrentar a La Entidad.

**Cómo se refleja en el juego:**

- Cada jefe entrega una habilidad que se vuelve útil en la zona siguiente y en la batalla final.
- La silueta de La Entidad se ve en el horizonte de todas las zonas, como recordatorio constante.
- El mercader convierte la XP de los enemigos básicos en potenciadores; pelear en el camino tiene sentido.

### Pilar 2 — Amenaza legible

**Descripción:** Los ataques pueden ser duros, incluso letales, pero siempre se anuncian y siempre tienen una respuesta.

**Cómo se refleja en el juego:**

- Toda acción hostil tiene una preparación visible (brillo, sonido o sombra en el suelo) antes de hacer daño.
- Los ataques instakill tienen una salida clara: la plataforma de agua ante la ráfaga del Jefe 1 o mantenerse lejos de la cabeza de la serpiente del Jefe 3.
- Los jefes repiten patrones reconocibles para que cada intento enseñe algo.

### Pilar 3 — Fluidez de combate en movimiento

**Descripción:** Moverse y atacar ocurren en un mismo flujo. Saltar, hacer dash y golpear se encadenan sin pausas.

**Cómo se refleja en el juego:**

- El dash cancela la recuperación del ataque y, con el dash cortante, también hace daño.
- El mago oscuro obliga a correr para escapar de los picos de magma; la serpiente gigante obliga a saltar entre plataformas.
- Los géiseres mantienen el ritmo al cruzar entre islas.

### Pilar 4 — Fantasía medieval colorida

**Descripción:** Un mundo de fantasía clásica en ruinas, con colores vivos y diseños con carisma.

**Cómo se refleja en el juego:**

- Eon usa capa, armadura ligera y espada.
- Los jefes y enemigos tienen siluetas reconocibles y un punto brillante que indica peligro.
- Costas, bosques, ruinas e islas flotantes mantienen una paleta saturada aun en un mundo destruido.

### Reglas de decisión

Antes de incorporar una característica importante, preguntar:

- ¿Refuerza la preparación para la revancha?
- ¿El jugador puede leer la amenaza a tiempo?
- ¿Justifica el costo de desarrollo dentro del alcance de [[01 - Alcance]]?
- ¿Complica innecesariamente otro sistema?


---

## Jugabilidad

### Bucle principal de juego

```text
Explorar la zona → Derrotar enemigos comunes (XP) → Llegar a la antesala del jefe
      → Intercambiar XP por potenciadores con el mercader → Preparar inventario (3 habilidades, 3 potenciadores)
      → Vencer al jefe → Guardar su habilidad en el inventario → Siguiente zona
      (opcional: volver a zonas superadas para acumular más XP)
```

Tras el tercer jefe el bucle se cierra: la serpiente petrificada abre el paso a la isla final y el jugador enfrenta a La Entidad con todo lo reunido.

### Bucles por escala

| Escala | Qué hace el jugador | Qué obtiene |
| --- | --- | --- |
| Segundo a segundo | Corre, salta, hace dash y encadena tajos; lee avisos de ataque. | Esquivar daño y conectar golpes. |
| Minuto a minuto | Despeja tramos con enemigos, cruza géiseres, administra su vida hasta el siguiente punto de control. | XP. |
| Por zona | Explora la zona, compra potenciadores y vence a su jefe. | Una habilidad nueva y acceso a la zona siguiente. |
| Partida completa | Reúne habilidades y potenciadores y vuelve a la isla final. | La revancha contra La Entidad. |

### Acciones principales del jugador

| Acción | Propósito | Resultado |
| --- | --- | --- |
| Ataque con espada | Eliminar enemigos. | Combo de hasta 3 tajos; los enemigos sueltan XP al morir. |
| Ataque descendente | Golpear desde el aire. | Daña al objetivo y rebota a Eon hacia arriba. |
| Salto | Navegar plataformas y evitar ataques rasantes. | Con el Doble salto equipado alcanza rutas más altas. |
| Dash | Esquivar y reposicionarse. | Breve invulnerabilidad; con el Dash cortante también hace daño. |
| Tajo ardiente | Atacar a distancia (Jefe 2). | Tajo de fuego que sale de la espada y atraviesa enemigos. |
| Escama pétrea | Defenderse (Jefe 3). | Reduce el daño; el bloqueo perfecto aturde al atacante. |
| Interactuar | Mercader, puntos de control y cañones. | Abre la tienda, guarda y restaura vida, dispara. |
| Montar un géiser | Cruzar entre islas. | Lanzamiento en arco hacia la isla siguiente. |

### Experiencia de los primeros minutos

El cómic inicial termina con la derrota de Eon. El control empieza cuando despierta solo en la playa. En el primer minuto el jugador camina, salta y se cruza con los primeros Aurion; aprende el combo y el dash mientras recoge su primera XP. Al final de los Acantilados, justo antes del primer jefe, encuentra al mercader y descubre que esa XP compra potenciadores. La silueta de La Entidad se ve en el horizonte del mar.

### Experiencia a largo plazo

Cada jefe entrega una habilidad que cambia la forma de pelear y de moverse, y la batalla final promete la revancha que el cómic dejó pendiente. Las ranuras limitadas obligan a probar combinaciones distintas, y volver a zonas anteriores permite reunir XP para completar el catálogo del mercader.

### Condición de victoria

- **Por zona:** derrotar al jefe de la zona.
- **Del juego:** derrotar a La Entidad en la isla final.

### Condición de derrota

- La salud de Eon llega a 0 (el escudo, si lo tiene, se gasta primero).
- Un ataque instakill conecta: ráfaga de agua del Jefe 1 o contacto con la cabeza de la serpiente del Jefe 3.
- Caer al vacío resta 25 HP y devuelve a Eon al último suelo seguro. Si eso deja la salud en 0, cuenta como derrota.

Al ser derrotado, Eon reaparece en el último punto de control con la vida y el escudo completos y conserva su XP. Ver [[07 - Reglas y Estados del Juego]].

### Ritmo

- **Exploración:** tramos de plataformas con rutas opcionales que se abren con habilidades.
- **Acción:** encuentros de 10 a 20 segundos con grupos pequeños de enemigos.
- **Tensión:** sin curación en el campo, cada golpe recibido cuenta hasta el siguiente punto de control.
- **Descanso:** puntos de control y la antesala de cada jefe, donde está el mercader.
- **Desafío:** combates contra jefes de 2 a 4 minutos con fases.
- **Recompensa:** la habilidad de cada jefe y la restauración completa de vida al vencerlo.
- **Historia:** ambiental (ruinas, estandartes caídos, la silueta del titán) y diálogos breves con el mercader.

### Principios de interacción

- **Legibilidad de bordes:** los límites transitables y los precipicios tienen siluetas y colisiones alineadas.
- **Un botón de contexto:** mercader, puntos de control y cañones usan `E` y muestran un aviso al entrar en su zona.
- **Avisos antes del daño:** ningún ataque hostil hace daño sin una preparación visible de al menos 0,4 s; los instakill, de al menos 1,5 s.


---

## Mecánicas

Los valores de esta página son la referencia de diseño para implementar y balancear. Si cambian en Unity, se actualizan aquí y en [[03 - Registro de Decisiones]].

### Valores base de Eon

| Parámetro | Valor |
| --- | ---: |
| Vida máxima | 100 HP (130 con el potenciador Vigor) |
| Escudo máximo | 0 SP (50 con el potenciador Coraza) |
| Velocidad de carrera | 7 u/s |
| Altura de salto | 3 u |
| Daño por tajo | 10 / 10 / 15 (combo de 3) |
| Invulnerabilidad tras recibir daño | 0,7 s |

**Vida y escudo no se recuperan durante la exploración ni el combate.** No hay objetos de curación ni de escudo. Ambos se restauran por completo solo al **tocar un punto de control** o al **vencer a un jefe** (también al reaparecer tras una derrota).

### Mecánicas principales

#### Movimiento lateral

- Aceleración inmediata y frenado al soltar la dirección; no hay inercia de deslizamiento.
- En el aire se conserva el control horizontal completo.

#### Salto

- **Activación:** pulsar Salto en contacto con el suelo.
- **Reglas:**
    - Impulso vertical inmediato; soltar el botón antes corta el ascenso (salto variable).
    - *Jump buffer* de 0,1 s: si se pulsa justo antes de aterrizar, el salto sale al tocar el suelo.
    - *Coyote time* de 0,1 s tras salir de un borde.
    - Sin la habilidad **Doble salto** equipada no hay segundo salto en el aire.
- **Estados:** `Idle`/`Run` → `InAir_Ascending` → `InAir_Falling` → `Landing` → `Idle`/`Run`.
- **Caso límite:** al chocar con un techo, la velocidad vertical se anula y empieza la caída.

#### Dash

- **Propósito:** esquivar en el último momento y reposicionarse sin bloqueos pasivos.
- **Activación:** pulsar Dash en tierra o en el aire.
- **Reglas:**
    - Desplazamiento horizontal de 4 u durante 0,20 s.
    - Invulnerabilidad durante todo el recorrido frente a ataques y proyectiles, **excepto los instakill**.
    - Atraviesa enemigos comunes sin daño por contacto.
    - Recarga de 1,2 s desde que termina.
    - 1 dash aéreo por salto; se restablece al tocar suelo o al conectar un ataque descendente.
- **Interacciones:** cancela la recuperación del combo de espada. Con **Dash cortante** equipado, daña a cada enemigo atravesado.
- **Casos límite:** contra un muro la velocidad pasa a cero en el punto de contacto. La invulnerabilidad no evita la caída al vacío.

#### Ataque básico (espada)

- **Activación:** pulsar Ataque (`Enter`) en tierra o en el aire.
- **Reglas:**
    - En tierra encadena hasta 3 tajos (10, 10 y 15 de daño).
    - Cada tajo activa una *hitbox* frontal durante 0,10 s.
    - Al conectar se aplica *hitstop* de 0,05 s y retroceso leve a enemigos comunes.
    - Recuperación de 0,1 s al final del combo; se puede cancelar con dash.
    - No se puede atacar durante el aturdimiento por daño recibido.
- **Caso límite:** si el arco toca a varios enemigos, todos reciben daño.

#### Ataque descendente

- **Activación:** Abajo + Ataque (`S` + `Enter`) en el aire.
- **Reglas:** golpe vertical de 12 de daño. Si impacta a un enemigo, Eon rebota hacia arriba y recupera su dash aéreo.

### Habilidades (obtenidas de jefes)

- Cada jefe entrega su habilidad (el Jefe 2 entrega dos). **Ninguna se descarta:** todas se guardan en el inventario.
- Hay **3 ranuras de habilidad**. El jugador decide cuáles equipar; solo las equipadas funcionan. Ninguna es obligatoria, ni siquiera el Doble salto.
- Al ver una habilidad en el inventario se muestra siempre su **control y su función**.

| Habilidad | Origen | Tipo | Control | Efecto |
| --- | --- | --- | --- | --- |
| **Doble salto** | Jefe 1 | Pasiva | Salto en el aire | Segundo salto en el aire (80 % de la altura del primero). Se restablece al tocar suelo. |
| **Tajo ardiente** (ataque arcano) | Jefe 2 | Activa | `J` | La espada lanza un tajo ardiente en forma de media luna que viaja en horizontal: 15 de daño, 14 u/s, alcance 8 u, recarga 1,2 s. Atraviesa a los enemigos comunes. |
| **Dash cortante** | Jefe 2 | Pasiva | Dash | El dash inflige 20 de daño a cada enemigo que atraviesa (una vez por enemigo y por dash). |
| **Escama pétrea** | Jefe 3 | Activa | `K` (mantener) | Eon petrifica su cuerpo y se cubre (detalle abajo). |

#### Escama pétrea (detalle)

- Mantener `K`: Eon se petrifica y se cubre hasta 1 s; recibe un 70 % menos de daño y no puede moverse.
- **Bloqueo perfecto:** si el golpe llega en los primeros 0,25 s, el daño se anula y el atacante queda aturdido 1 s.
- Recarga de 3 s desde que se suelta.
- **No bloquea ataques instakill** ni evita la caída al vacío.
- Sinergias: el bloqueo perfecto aturde al Earthlem y rompe la guardia del Vestigio.

### Potenciadores

- Se compran con XP al mercader, una sola vez cada uno, y son **permanentes**.
- **No se activan con ningún botón:** mientras están equipados en el inventario, su efecto está siempre activo.
- Hay **3 ranuras de potenciador** en el inventario. Los demás quedan guardados, sin efecto, hasta que se equipen.
- Al ver un potenciador en el inventario se muestra siempre su función.
- Catálogo y precios en [[06 - Economía y Recursos]].

### Mecánicas secundarias

- **Interacción:** `E` / Botón `Y` frente al mercader y los puntos de control.
- **Experiencia:** los enemigos sueltan su XP en forma de orbes dorados que se atraen hacia Eon cuando está a 3 u o menos.
- **Géiseres:** Eon se coloca sobre un géiser y, durante la erupción, sale lanzado en un arco fijo hacia la isla destino.
    - Ciclo: reposo 1,5 s → aviso (burbujeo y vapor) 0,5 s → erupción 1,0 s.
    - Durante el vuelo se conserva un control horizontal leve (±1 u) para corregir el aterrizaje.
    - Sustituyen por completo a los trampolines.
- **Cañones (isla final):** al interactuar, disparan contra La Entidad. Recarga de 6 s por cañón.
- **Reaparición de enemigos:** los enemigos comunes reaparecen al descansar en un punto de control o al volver a entrar a una zona. Se puede regresar a zonas ya superadas para acumular más XP.


---

## Sistemas del Juego

### Inventario de sistemas

| Sistema | Propósito | Dependencias | Estado |
| --- | --- | --- | --- |
| Daño, salud y combate | Vida y escudo de Eon y enemigos, *hitbox*/*hurtbox*, instakill y eventos de muerte. | Capas de colisión 2D, Animator, efectos/*game feel*. | Por implementar |
| Controlador del jugador y movilidad | Entradas, movimiento lateral, salto, doble salto, dash, ataques y habilidades activas. | `Rigidbody2D`, `Collider2D`, Input System, Inventario. | En prototipo |
| IA de enemigos comunes | Patrulla, detección y ataque de Aurion, Earthlem y Vestigio; reaparición. | Raycasts, `Transform` de Eon, sistema de daño. | Por implementar |
| IA de jefes | Patrones, fases y avisos de los tres jefes y La Entidad. | Sistema de daño, gestor de mundo, cámara. | Por implementar |
| Inventario y equipamiento | Guardar habilidades y potenciadores; 3 ranuras de cada tipo; descripciones. | UI, guardado, controlador del jugador. | Por implementar |
| Economía de XP y tienda | Ganar XP y gastarla con el mercader. | Daño (muertes), UI, guardado. | Por implementar |
| Cámara reactiva y encuadre | Seguir a Eon, confinar la vista en arenas y aplicar sacudidas. | Cinemachine 2D, gestor de mundo. | Por implementar |
| Gestor de mundo y progreso | Zonas, puntos de control, arenas de jefe, barreras y cinemáticas. | Triggers, UI, guardado, inventario. | Por implementar |
| Elementos de entorno | Géiseres, cañones, plataforma de agua, pilares de las ruinas. | Físicas 2D, controlador del jugador. | Por implementar |
| Guardado | Persistir progreso entre sesiones. | Todos los anteriores. | Por implementar |

### Sistema 01: Daño, salud y combate

- **Objetivo:** administrar vida y escudo, validar colisiones de ataque y despachar eventos de daño y muerte.
- **Entradas:** colisiones entre capas `Hitbox` y `Hurtbox`, identificador del atacante, daño y bandera `isInstakill`.
- **Reglas:**
    - El daño normal se resta primero del escudo (si Eon tiene Coraza) y después de la vida.
    - Con Escama pétrea activa, el daño normal se reduce un 70 %; en bloqueo perfecto se anula y aturde al atacante.
    - Un ataque **instakill** ignora escudo, dash y Escama pétrea; deja la vida en 0.
    - Tras recibir daño, Eon tiene 0,7 s de invulnerabilidad con parpadeo rojo.
    - Vida y escudo **solo se restauran** al tocar un punto de control, al vencer a un jefe o al reaparecer. No hay curación en el campo.
    - Si la vida llega a 0 se apagan los colliders y se llama a la rutina de muerte.
    - Si el arma de Eon y la *hitbox* de un enemigo común chocan en el mismo fotograma, se anula el daño mutuo y solo recibe daño el enemigo (no aplica a jefes).
- **Salidas:** `OnHealthChanged`, `OnShieldChanged`, `OnEntityDeath`, `OnPlayerDeath`.
- **Estados:** `Vulnerable`, `Invulnerable`, `Petrified`, `HitStun`, `Dead`.
- **Riesgos:** daño registrado dos veces en un fotograma; instakill aplicado sin aviso visible.
- **Criterios de aceptación:** un impacto descuenta una sola vez, respeta la prioridad escudo → vida y la vida nunca sube fuera de un punto de control o de la muerte de un jefe.

### Sistema 02: Controlador del jugador y movilidad

- **Objetivo:** convertir las entradas en movimiento, salto, dash, ataques y habilidades, consultando qué está equipado.
- **Entradas:** dirección, Salto, Ataque (`Enter`), Dash, Tajo ardiente (`J`), Escama pétrea (`K`), Interactuar, Inventario.
- **Reglas:**
    - Movimiento con aceleración inmediata y frenado al soltar.
    - Doble salto, Tajo ardiente, Dash cortante y Escama pétrea solo funcionan equipados.
    - Dash de 0,20 s y 4 u; 1 aéreo por salto; recarga de 1,2 s.
    - Abajo + Ataque en el aire ejecuta el ataque descendente; al impactar rebota y recupera el dash aéreo.
    - Los potenciadores equipados modifican los valores de forma permanente (vida máxima, daño, velocidad, recargas).
    - Durante cinemáticas, tienda e inventario el control queda bloqueado.
- **Salidas:** `velocity` del `Rigidbody2D`; parámetros del Animator (`Speed`, `IsGrounded`, `IsDashing`, `AirJumps`, `IsPetrified`); activación de *hitboxes*.
- **Estados:** `Idle`, `Run`, `Jump`, `DoubleJump`, `Fall`, `Dash`, `Attack`, `DownStab`, `FireSlash`, `Petrified`, `HitStun`, `Locked`.
- **Riesgos:** atascos en esquinas durante el dash; rebotes infinitos fuera de cámara.
- **Criterios de aceptación:** respuesta inmediata, dash que cancela ataques en el fotograma pedido y habilidades que solo funcionan equipadas.

### Sistema 03: IA de enemigos comunes

- **Objetivo:** rutinas de patrulla, detección, ataque y reaparición.
- **Reglas:**
    - Los terrestres patrullan hasta detectar un muro o un vacío con raycasts y nunca saltan al vacío.
    - Al detectar a Eon pausan 0,3 s con un destello de aviso antes de atacar.
    - Los voladores oscilan en altura y embisten cuando Eon entra en su cono.
    - Al recibir daño entran en `HitStun` y reinician su temporizador de ataque.
    - Reaparecen en sus posiciones iniciales cuando Eon descansa en un punto de control o vuelve a entrar a la zona.
- **Estados:** `Patrol`, `Alert`, `Attack`, `Stunned`, `Dead` (más `Buried` en Earthlem y `Guard` en Vestigio).
- **Salidas:** al morir sueltan orbes de XP.
- **Criterios de aceptación:** ningún enemigo cae de su plataforma por error, todos avisan antes de golpear y reaparecen correctamente.

### Sistema 04: IA de jefes

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

### Sistema 05: Inventario y equipamiento

- **Objetivo:** guardar lo obtenido y decidir qué se usa.
- **Reglas:**
    - **Habilidades:** se guardan todas las obtenidas; ninguna se descarta. Solo **3** pueden estar equipadas.
    - **Potenciadores:** se guardan todos los comprados; solo **3** pueden estar equipados. Los equipados están **siempre activos**; no hay botones de uso.
    - Al seleccionar cualquier habilidad o potenciador, el inventario muestra su **función** y, si la tiene, su **tecla de control**.
    - Una habilidad recién obtenida se guarda en el inventario y se avisa al jugador para que decida si la equipa.
    - El inventario se abre con `Tab` / `View`. Se puede cambiar el equipamiento en cualquier momento **fuera de una arena de jefe**.
- **Salidas:** habilidades activas al controlador; modificadores de los potenciadores equipados; iconos al HUD.
- **Riesgos:** aplicar dos veces el modificador de un potenciador al reequiparlo.
- **Criterios de aceptación:** nunca hay más de 3 habilidades ni 3 potenciadores equipados; los cambios se reflejan de inmediato en el control, los valores y el HUD.

### Sistema 06: Economía de XP y tienda

- **Objetivo:** convertir el combate en potenciadores.
- **Reglas:**
    - Cada enemigo suelta su XP como orbes al morir; los jefes dan cantidades mayores. Codicia aumenta un 25 % la XP obtenida.
    - La XP no sube niveles. Tope de 9999. Se conserva al morir.
    - El mercader está en la antesala de cada jefe. Cada potenciador se compra una sola vez; los ya comprados aparecen como «Adquirido».
    - La compra se bloquea si falta XP.
- **Criterios de aceptación:** el contador del HUD y el de la tienda coinciden siempre; una compra descuenta una sola vez y el potenciador aparece en el inventario.

### Sistema 07: Cámara reactiva y encuadre

- **Reglas:**
    - Seguimiento en X e Y con amortiguación y *lookahead* hacia la dirección de avance.
    - En arenas de jefe la cámara se confina a los límites de la arena y, si el jefe es muy grande (Jefe 3, La Entidad), se aleja para mostrarlo.
    - Sacudida de cámara en impactos fuertes. **No es configurable** ni se puede desactivar.
- **Estados:** `FollowPlayer`, `LockedInArena`, `ScreenShake`, `CinematicFocus`.
- **Criterios de aceptación:** nunca muestra zonas fuera del mapa y siempre deja ver el aviso de un ataque instakill.

### Sistema 08: Gestor de mundo y progreso

- **Objetivo:** controlar el recorrido de las zonas, los puntos de control, las arenas y los eventos narrativos.
- **Reglas:**
    - Registra jefes derrotados y habilidades obtenidas.
    - El camino principal nunca exige una habilidad concreta; las rutas opcionales pueden pedir Doble salto o Tajo ardiente y muestran una pista visual.
    - Los puntos de control restauran vida y escudo y hacen reaparecer a los enemigos comunes.
    - Al cruzar la entrada de una arena de jefe se cierran sus límites:
        - **Jefe 1, Jefe 3 y La Entidad:** barreras **invisibles**.
        - **Jefe 2:** **pilares de las ruinas** que emergen del suelo y bloquean el paso; se hunden al morir el jefe.
    - Al morir el jefe, las barreras se retiran.
    - Las zonas superadas siguen accesibles para volver a acumular XP.
    - Tras el Jefe 3 reproduce la ilustración de la serpiente petrificada y activa el puente hacia la isla final.
    - Tras La Entidad, bloquea el control y lanza el final y los créditos.
- **Estados:** `Intro`, `Exploration`, `BossArena`, `Cinematic`, `Ending`.
- **Riesgos:** una arena que queda cerrada si el jefe muere fuera del trigger.
- **Criterios de aceptación:** cada arena se cierra al entrar y se abre en el fotograma en que muere el jefe.

### Sistema 09: Elementos de entorno

- **Géiser:** ciclo reposo/aviso/erupción; lanza a Eon por un arco fijo hacia un punto destino. Ver [[02 - Mecánicas]].
- **Cañón:** solo en la isla final; dispara al interactuar y daña a La Entidad.
- **Plataforma de agua:** solo en el combate del Jefe 1; aparece antes de la ráfaga y se disuelve después.
- **Pilares de las ruinas:** solo en la arena del Jefe 2; cierran los extremos durante el combate.

### Relaciones entre sistemas

- **Controlador ↔ Daño:** el controlador activa las *hitboxes* de espada, descendente, Tajo ardiente y Dash cortante, y el estado de Escama pétrea; el sistema de daño confirma impactos (para el rebote) y aplica el daño recibido.
- **Inventario → Controlador:** indica qué habilidades están equipadas y qué modificadores aplican los potenciadores.
- **Tienda → Inventario:** cada compra añade el potenciador al inventario.
- **Daño → Economía:** `OnEntityDeath` genera los orbes de XP del enemigo.
- **IA de jefes → Gestor de mundo:** la muerte del jefe guarda la habilidad, restaura a Eon, abre la arena y registra el progreso.
- **Gestor de mundo → Cámara:** cambia el confinamiento al entrar a una arena y activa el foco cinemático.
- **Gestor de mundo → IA de enemigos:** ordena la reaparición al usar un punto de control.
- **Todos → Guardado:** el progreso se escribe al tocar un punto de control, al derrotar un jefe, al comprar y al cambiar el inventario.


---

## Controles

La prioridad es la inmediatez: respuesta sin latencia percibida, una acción por botón y retroalimentación audiovisual instantánea.

### Mapa de controles

| Acción | Teclado | Control (Xbox / PS) |
| --- | --- | --- |
| Mover izquierda / derecha | `A` / `D` | Stick izquierdo / cruceta |
| Mirar abajo / dirigir ataque descendente | `S` | Stick izquierdo abajo |
| Saltar (y doble salto) | `Espacio` o `W` | `A` / Cruz |
| Ataque con espada | `Enter` | `X` / Cuadrado |
| Ataque descendente | `S` + `Enter` en el aire | Abajo + `X` / Cuadrado |
| Dash | `Shift izquierdo` | `RB` / `R1` |
| Tajo ardiente (ataque arcano) | `J` | `B` / Círculo |
| Escama pétrea (petrificación) | `K` (mantener) | `LB` / `L1` (mantener) |
| Interactuar | `E` | `Y` / Triángulo |
| Inventario | `Tab` | `View` / `Share` |
| Pausa | `Escape` | `Start` / `Options` |

- Los **potenciadores no tienen controles**: funcionan siempre mientras están equipados en el inventario.
- Las habilidades pasivas (Doble salto, Dash cortante) no tienen botón propio: modifican Salto y Dash.
- Si una habilidad activa no está equipada, su botón no hace nada.
- El inventario muestra el control y la función de cada habilidad, y la función de cada potenciador.

### Principios de control

- **Consistencia:** salto, aceleración y dash son idénticos en todas las zonas.
- **Tolerancia de entrada:** *buffer* de 0,10 s para Ataque, Salto y Dash al terminar una animación o al aterrizar.
- **Sin combinaciones complejas:** no hay medias lunas ni dobles toques; la única combinación es Abajo + Ataque.
- **Pulsación accidental:** la tecla que cierra la tienda o el inventario no se reutiliza como ataque o salto en el mismo fotograma.

### Reasignación

No se incluye reasignación de teclas en esta versión. Salto tiene dos teclas (`Espacio`/`W`).

### Entrada y retroalimentación

| Entrada | Acción | Visual | Sonido | Sensación |
| --- | --- | --- | --- | --- |
| Ataque (tierra) | Tajo horizontal | Estela en media luna cian/blanca. | *Whoosh* agudo. | Avance de 0,5 u. |
| Abajo + Ataque (aire) | Golpe descendente | Estela vertical, punta brillante. | Silbido descendente. | Caída acelerada; rebote si impacta. |
| Salto en el aire (con Doble salto) | Segundo salto | Ráfaga de aire bajo los pies. | Soplo corto. | Impulso algo menor que el primero. |
| Dash | Desplazamiento | Silueta residual; con Dash cortante, estela roja. | Corte de aire; con Dash cortante, tajo metálico. | Velocidad súbita con *hitstop* si corta a un enemigo. |
| `J` | Tajo ardiente | Media luna de fuego naranja que sale de la espada. | Tajo con chisporroteo. | Retroceso mínimo de Eon. |
| `K` (mantener) | Escama pétrea | El cuerpo de Eon se vuelve gris piedra; destello blanco en el bloqueo perfecto. | Crujido de roca; golpe seco en el bloqueo perfecto. | Eon queda inmóvil. |
| Recibir daño | Impacto y retroceso | Parpadeo rojo 0,7 s. | Golpe sordo y quejido. | Empuje en X; sin control 0,15 s. |
| Aviso instakill | — | Brillo intenso y sombra en el área de impacto. | Sonido exclusivo grave. | La cámara no se mueve para no tapar el aviso. |


---

## Progresión

Eon no sube de nivel. Progresa de dos formas: **habilidades** que entregan los jefes y **potenciadores** permanentes que compra con XP. De cada tipo puede tener **3 equipados**; lo demás queda guardado en el inventario. También progresa el jugador: cada intento contra un jefe le enseña sus patrones.

### Progresión general

| Etapa | Zona | Qué aprende o consigue el jugador |
| --- | --- | --- |
| Inicio | Cómic del prólogo | Eon ya perdió contra La Entidad. Motivo de la revancha. |
| Introducción | Playa del Despertar | Movimiento, salto, combo, dash. Primeros Aurion y primera XP. |
| Desarrollo 1 | Acantilados → antesala (mercader) → **Jefe 1** | Primer potenciador. Leer avisos y usar el entorno (plataforma de agua). Obtiene **Doble salto**. |
| Desarrollo 2 | Bosque → Ruinas → antesala → **Jefe 2** | Earthlem y Vestigio. Obtiene **Tajo ardiente** y **Dash cortante**: ya tiene 3 habilidades. |
| Dominio | Archipiélago → antesala → **Jefe 3** | Géiseres y plataformas flotantes. Obtiene **Escama pétrea**: con 4 habilidades y 3 ranuras, elige su equipo. |
| Clímax | Puente de la Serpiente → antesala → Isla Final | Combina todo contra La Entidad. |
| Final | — | Revancha cumplida; créditos. |

En cualquier momento tras vencer a un jefe, el jugador puede volver a zonas anteriores para acumular XP con los enemigos que reaparecen.

### Desbloqueos

| Desbloqueo | Requisito | Efecto |
| --- | --- | --- |
| Tienda del mercader | Llegar a la antesala del Jefe 1 | Compra de potenciadores; el mercader vuelve a aparecer antes de cada jefe. |
| Doble salto | Derrotar al Jefe 1 | Segundo salto aéreo; abre rutas opcionales altas. |
| Tajo ardiente | Derrotar al Jefe 2 | Ataque a distancia; activa interruptores lejanos de rutas opcionales. |
| Dash cortante | Derrotar al Jefe 2 | El dash hace daño. |
| Acceso al Archipiélago | Derrotar al Jefe 2 | Se activan los géiseres que conectan las Ruinas con las islas. |
| Escama pétrea | Derrotar al Jefe 3 | Bloqueo y contraataque. |
| Isla Final | Derrotar al Jefe 3 | La serpiente se petrifica y su cuerpo forma el puente. |
| Nuevos potenciadores | Llegar a cada antesala | El catálogo del mercader crece (ver [[06 - Economía y Recursos]]). |

Ninguna habilidad es obligatoria para avanzar por el camino principal: el jugador decide qué equipar.

### Curva de dificultad

| Tramo | Elementos nuevos | Presión |
| --- | --- | --- |
| Playa | Aurion sueltos | Baja; se aprende sin castigo. |
| Acantilados | Grupos de Aurion; precipicios | Media-baja. |
| Jefe 1 | Esbirros voladores, embestidas, primer instakill con salida clara | Media. |
| Bosque | Earthlem; plataformas verticales | Media. |
| Ruinas | Vestigio; combinaciones Earthlem + Aurion | Media-alta. |
| Jefe 2 | Arena plana sin plataformas; ataques que exigen correr; escudo y teletransporte | Alta. |
| Archipiélago | Géiseres, islas pequeñas, enemigos en espacios reducidos | Alta. |
| Jefe 3 | Jefe grande con cuerpo dañino, lluvia de baba, cabeza instakill | Muy alta. |
| La Entidad | Fases con todo lo anterior; Vestigios como refuerzos | Máxima. |

Sin curación en el campo, la distancia entre puntos de control es parte de la dificultad: aumenta ligeramente en cada zona.

### Curva de aprendizaje

- Antes del Jefe 1 el jugador debe dominar salto y dash: la Playa y los Acantilados obligan a usarlos.
- Antes del Jefe 2 debe saber pelear contra enemigos con defensa (Earthlem, Vestigio).
- Antes del Jefe 3 debe dominar el cruce con géiseres y las plataformas pequeñas.
- Antes de La Entidad debe haber elegido su equipo de 3 habilidades y 3 potenciadores.


---

## Economía y Recursos

La economía gira en torno a un solo recurso de intercambio: los **puntos de experiencia (XP)**. Los enemigos los sueltan al morir y el mercader los cambia por potenciadores permanentes.

### Recursos

| Recurso | Obtención | Uso | Límite | Pérdida / recarga |
| --- | --- | --- | --- | --- |
| **Salud (HP)** | Se restaura por completo en puntos de control, al vencer a un jefe y al reaparecer. | Mantener a Eon con vida. | 100 HP (130 con Vigor). | Se pierde con el daño. No hay curación durante la exploración ni el combate. En 0, derrota. |
| **Escudo (SP)** | Solo con el potenciador Coraza equipado. Se restaura igual que la vida. | Absorber daño antes que la vida. | 50 SP. | Se gasta con cada impacto. |
| **XP** | Enemigos comunes y jefes. | Comprar potenciadores. | 9999. | Solo al gastarse. **Se conserva al morir.** |
| **Potenciadores** | Compra única con el mercader. | Efecto pasivo permanente mientras están equipados. | 3 equipados. | Nunca se pierden. |
| **Habilidades** | Derrotar jefes. | Nuevas acciones o mejoras de movimiento. | 3 equipadas. | Nunca se pierden ni se descartan. |

### Fuentes de XP

| Fuente | XP |
| --- | ---: |
| Aurion | 10 |
| Vestigio | 25 |
| Earthlem | 30 |
| Camaroncito (esbirro del Jefe 1) | 1 |
| Jefe 1 | 200 |
| Jefe 2 | 300 |
| Jefe 3 | 400 |

- Los enemigos comunes **reaparecen** al descansar en un punto de control o al volver a entrar a una zona. Tras vencer a un jefe, el jugador puede regresar a zonas anteriores para acumular más XP.
- Un recorrido directo reúne unos 1400 XP antes de la isla final. Comprar los 6 potenciadores (1500 XP) exige volver a pelear en zonas anteriores.

### Catálogo de potenciadores

Todos son **permanentes**: se compran una vez y, mientras ocupan una de las **3 ranuras** del inventario, su efecto está siempre activo. No usan botones. El inventario muestra la función de cada uno.

| Potenciador | Efecto | Precio | Disponible desde |
| --- | --- | ---: | --- |
| **Vigor** | +30 de vida máxima (100 → 130). | 200 XP | Antesala del Jefe 1 |
| **Filo** | +25 % de daño en espada, ataque descendente, Tajo ardiente y Dash cortante. La estela de la espada se tiñe de rojo. | 250 XP | Antesala del Jefe 1 |
| **Codicia** | +25 % de XP obtenida. | 150 XP | Antesala del Jefe 1 |
| **Coraza** | Otorga un escudo de 50 SP que absorbe daño antes que la vida; se restaura junto con la vida. | 250 XP | Antesala del Jefe 2 |
| **Celeridad** | +20 % de velocidad de carrera y −40 % de recarga del dash. | 300 XP | Antesala del Jefe 2 |
| **Foco arcano** | Tajo ardiente con −50 % de recarga y +50 % de daño. Solo tiene efecto si Tajo ardiente está equipado. | 350 XP | Antesala del Jefe 3 |

El catálogo de cada antesala incluye también los potenciadores de antesalas anteriores que el jugador no haya comprado. En la antesala de la Isla Final, el mercader regala uno de los que falten (una sola vez).

### Fuentes y sumideros

**Fuentes**

- **Combate:** enemigos comunes (XP), que reaparecen.
- **Jefes:** una gran cantidad de XP y su habilidad.
- **Puntos de control y jefes vencidos:** restauran vida y escudo.

**Sumideros**

- **Tienda del mercader:** potenciadores.
- **Daño:** consume escudo y vida hasta el siguiente punto de control.

### Reglas

1. **Escudo antes que vida:** la vida no baja mientras quede al menos 1 SP.
2. **Instakill:** ignora escudo, la invulnerabilidad del dash y la Escama pétrea.
3. **Sin curación en campo:** vida y escudo solo se restauran en puntos de control, al vencer a un jefe o al reaparecer.
4. **Persistencia:** XP, potenciadores y habilidades se conservan al ser derrotado.
5. **Reaparición de enemigos:** los enemigos comunes reaparecen; los jefes derrotados no.

### Balance

**Comportamientos que queremos incentivar**

- Pelear en el camino: la XP de los enemigos es la única vía hacia los potenciadores.
- Cuidar la vida entre puntos de control: no hay curación en el campo.
- Elegir: 3 ranuras de habilidad y 3 de potenciador para catálogos de 4 y 6.
- Volver a zonas superadas para completar el catálogo.

**Comportamientos que queremos evitar**

- **Farmear dentro de un combate de jefe:** los camaroncitos dan solo 1 XP.
- **Ganar sin aprender al jefe:** los potenciadores ayudan, pero el instakill sigue siendo letal.


---

## Reglas y Estados del Juego

### Estados principales

- **Menú principal:** nueva partida, continuar, configuración, créditos y salir.
- **Carga:** transición entre escenas; inicializa assets, reinicia *pools* de objetos y coloca entidades.
- **Prólogo (cómic):** secuencia de viñetas que termina con la derrota de Eon; se puede omitir.
- **Jugando (exploración):** control directo de Eon en una zona.
- **Arena de jefe:** variante de Jugando con límites cerrados, cámara confinada y equipo fijado.
- **Inventario:** simulación pausada; permite ver la descripción de todo lo obtenido y cambiar habilidades y potenciadores equipados (fuera de una arena de jefe).
- **Tienda:** simulación pausada mientras se compra con el mercader.
- **Cinemática:** ilustraciones fijas o breves (habilidad obtenida, serpiente petrificada, final). Control bloqueado.
- **Pausa:** `Time.timeScale = 0`; reanudar, volver al último punto de control, configuración o salir al menú.
- **Derrota:** animación de colapso y opción de reaparecer en el último punto de control o salir al menú.
- **Victoria:** al derrotar a La Entidad; lleva al final y a los créditos.
- **Créditos:** desde el menú o tras la victoria.

### Transiciones

| Estado origen | Evento | Estado destino | Condición |
| --- | --- | --- | --- |
| Menú principal | `OnNewGame` | Prólogo | Nueva partida (con confirmación si existe un guardado). |
| Menú principal | `OnContinue` | Carga | Existe guardado; carga la zona del último punto de control. |
| Menú principal | `OnShowCredits` | Créditos | Selección manual. |
| Prólogo | `OnPrologueEnd` | Carga | Última viñeta o mantener `Escape`/`Start` 1,5 s. |
| Carga | `OnSceneLoaded` | Jugando | Zona lista. |
| Jugando | `OnEnterBossArena` | Arena de jefe | Eon cruza el trigger de entrada; se cierran los límites. |
| Arena de jefe | `OnBossDefeated` | Cinemática | Muere el jefe y Eon sigue vivo. |
| Cinemática | `OnCinematicEnd` | Jugando | Habilidad guardada; vida y escudo restaurados; se abren los límites. |
| Jugando | `OnInventoryPressed` | Inventario | — (dentro de una arena, solo lectura). |
| Inventario | `OnInventoryClosed` | Estado previo | — |
| Jugando | `OnInteractSeller` | Tienda | Antesala de un jefe. |
| Tienda | `OnShopClosed` | Jugando | — |
| Jugando / Arena de jefe | `OnPausePressed` | Pausa | `Escape` / `Start`. |
| Pausa | `OnResumePressed` | Estado previo | — |
| Pausa | `OnRestartCheckpoint` | Carga | Volver al último punto de control. |
| Pausa | `OnExitToMenu` | Carga | Confirmación previa. |
| Jugando / Arena de jefe | `OnPlayerDeath` | Derrota | Vida en 0 o instakill. |
| Derrota | `OnRetryCheckpoint` | Carga | — |
| Derrota | `OnExitToMenu` | Carga | — |
| Arena de jefe (Isla Final) | `OnFinalBossDefeated` | Victoria | Muere La Entidad con Eon vivo. |
| Victoria | `OnVictoryEnd` | Créditos | Termina la secuencia final. |
| Créditos | `OnCreditsEnd` | Menú principal | Fin del desplazamiento u omisión. |

### Reglas globales

- **Sin curación en el campo:** vida y escudo solo se restauran al tocar un punto de control, al vencer a un jefe o al reaparecer tras una derrota.
- **Pausa absoluta:** pausa, inventario y tienda detienen el tiempo de juego, los enemigos y las animaciones; los menús usan `Time.unscaledDeltaTime`.
- **Cinemáticas seguras:** durante introducciones de jefe, cambios de fase y cinemáticas, Eon y los enemigos son invulnerables.
- **Puntos de control:** al descansar o reaparecer, Eon vuelve al último punto visitado con vida y escudo completos, y los enemigos comunes reaparecen.
- **Equipo fijado en arena:** al entrar a una arena de jefe no se pueden cambiar habilidades ni potenciadores.
- **Límites de arena:** invisibles en los combates contra el Jefe 1, el Jefe 3 y La Entidad; en el del Jefe 2, pilares de las ruinas que bloquean el paso.
- **Zonas reabiertas:** tras vencer a un jefe, las zonas anteriores siguen accesibles y sus enemigos reaparecen.
- **Persistencia:** XP, potenciadores, habilidades y jefes derrotados se guardan.

### Casos especiales

- **Derrota dentro de una arena:** el jefe vuelve a su vida completa y Eon reaparece en el punto de control de la antesala.
- **Muerte simultánea:** si Eon y el jefe llegan a 0 en el mismo fotograma, prevalece la **victoria**.
- **Instakill y defensas:** escudo, dash y Escama pétrea no protegen del instakill.
- **Caída al vacío:** −25 HP y regreso al último suelo seguro. En la arena del Jefe 3, el «último suelo seguro» es la plataforma central.
- **Habilidad nueva:** se guarda en el inventario sin descartar ninguna. Un aviso invita a abrir el inventario para equiparla.
- **Salir durante una cinemática de entrega:** la habilidad ya cuenta como obtenida y se guarda.


---

## Premisa y Trama

### Premisa

Eon, el héroe profetizado para salvar Eretz, ya enfrentó a La Entidad y perdió. Cuando cayó, el poder que lo hacía legendario se rompió en fragmentos que absorbieron las criaturas más fuertes de Kastleland. Para volver a enfrentar al titán, Eon debe derrotar a tres de ellas, recuperar esos poderes como habilidades y llegar a la isla final por su revancha.

### Sinopsis

En un mundo más allá de la Vía Láctea existe el planeta Eretz (nombre de la Tierra en hebreo). Durante miles de años sus pueblos esperaron al héroe que vencería a la calamidad del fin del mundo: Eon. Equipado con las mejores armas y armaduras, Eon ascendió por un archipiélago flotante para enfrentar a La Entidad, un ser colosal que emergió del océano liberando aberraciones. La profecía no bastó: el titán destrozó su arma, lo arrojó al abismo y desató un ataque que aniquiló al 98 % de la civilización y fragmentó la geografía.

Días después, Eon despierta solo en una playa entre ruinas. No tiene su armadura ni su espada legendaria, y su poder ya no le pertenece: se repartió entre las criaturas que sobrevivieron al cataclismo. Con la espada que le queda, Eon recorre la costa, los bosques, las ruinas y las islas de tierra flotante. Cada enemigo vencido le da experiencia que un mercader errante, que aparece siempre antes de cada gran combate, acepta a cambio de potenciadores; cada jefe vencido le devuelve una habilidad.

Al derrotar a la tercera criatura, una serpiente gigante que rodea las islas flotantes, su cuerpo se petrifica y forma un puente hacia la isla final. Allí, Eon enfrenta de nuevo a La Entidad. Esta vez no lo sostiene una profecía, sino todo lo que aprendió y ganó en el camino.

### Estructura narrativa

#### Acto 1 — La caída del elegido (prólogo en cómic)

**Contexto:** el mundo de Eretz, Kastleland, la calamidad y la profecía.

**Enfoque narrativo:** el cómic presenta al héroe y termina con su derrota ante La Entidad. El jugador no controla esa batalla: empieza el juego sabiendo que Eon ya perdió.

#### Acto 2 — La revancha se prepara

**Contexto:** el despertar en la costa y el recorrido por Kastleland en ruinas.

**Enfoque narrativo:** Eon, debilitado y solo, se abre paso entre enemigos. Antes de la primera gran pelea encuentra al mercader, que desde entonces aparece antes de cada jefe. Derrota a la serpiente-camarón de la costa (recupera el doble salto) y al mago oscuro de las ruinas (recupera el tajo ardiente y el dash cortante).

#### Acto 3 — El puente de piedra

**Contexto:** el Archipiélago de Tierra, la serpiente gigante y la isla final.

**Enfoque narrativo:** Eon vence a la serpiente gigante y recupera la escama pétrea; el cuerpo de la serpiente se petrifica y abre el camino hacia la isla final. La revancha contra La Entidad cierra el arco: el héroe no gana por estar destinado, sino porque decidió volver.

### Eventos principales

| Orden | Evento | Participación del jugador | Consecuencia |
| --- | --- | --- | --- |
| 1 | La caída del elegido | Lee el cómic del prólogo (o lo omite). | Se establece que Eon perdió y por qué busca la revancha. |
| 2 | El despertar | Controla a Eon en la Playa del Despertar. | Aprende los controles con un héroe debilitado. |
| 3 | El mercader | Lo encuentra en la antesala del Jefe 1. | Descubre que la XP sirve para comprar potenciadores. |
| 4 | La marea viva | Derrota al Jefe 1 en la Arena de la Marea. | Recupera el **Doble salto**. |
| 5 | Las ruinas en llamas | Derrota al Jefe 2 en las Ruinas Abandonadas. | Recupera el **Tajo ardiente** y el **Dash cortante**; se activan los géiseres hacia el Archipiélago. |
| 6 | La serpiente de piedra | Derrota al Jefe 3 en el Archipiélago de Tierra. | Recupera la **Escama pétrea**. Cinemática: la serpiente se petrifica y forma el puente. |
| 7 | La revancha | Cruza el puente y enfrenta a La Entidad. | Victoria: final y créditos. |

### Final

**La revancha:** Eon derrota a La Entidad en la isla final. El titán cae al mar del que emergió y el cielo de Eretz se despeja por primera vez desde el cataclismo. La profecía se equivocó en cómo, pero no en quién: el héroe sí salvó al mundo, solo que tuvo que perder primero.

> [!warning] Spoilers
> Si el documento se comparte con jugadores de prueba, conviene separar esta sección.


---

## Mundo

### Concepto del mundo

**Época:** medieval ficticia.

**Planeta:** Eretz.

![[Pasted image 20260929141034.png|135]]

**Continente donde transcurre el juego:** Kastleland.

![[Pasted image 20260929141048.png|258]]

### Contexto

Eretz es un planeta formado por siete grandes continentes. Durante miles de años vivieron casi aislados entre sí, por lo que las culturas y tecnologías son distintas en cada uno. El juego transcurre por completo en **Kastleland**; los demás continentes son contexto del mundo y no aparecen como zonas jugables.

#### Afrikka

Es la tierra más antigua del planeta: un desierto implacable de tierra roja y cañones profundos, donde el calor evaporó los antiguos mares y dejó solo llanuras agrietadas de polvo y sal.

En contraste, por sus cielos flota **Baltia**: una isla gigantesca del tamaño de varios países, suspendida a cientos de metros de altura, que se desplaza lentamente con el viento. Baltia es un paraíso verde de manantiales, bosques frutales luminosos y criaturas pacíficas. Su paso arroja una sombra constante sobre el desierto: mientras el cielo exhibe una abundancia inalcanzable, la tierra firme se consume en la sequía.

Esa desigualdad convirtió a la isla en la mayor maldición política de Afrikka. Desde hace siglos, sus diez naciones pelean por controlarla. Como ninguna puede conquistarla de forma permanente, los ejércitos siguen su sombra por el desierto con arpones colosales, cadenas y cometas de abordaje para trepar a la roca flotante, saquear agua y alimentos, y eliminar a cualquier facción rival que llegue primero.

#### Amerikka

Un continente colosal de selvas tropicales infinitas y ríos largos, con una vegetación tan espesa que la luz apenas toca el suelo. Sus pueblos aprendieron a convivir con la naturaleza y levantaron ciudades de piedra blanca entre las raíces de árboles gigantescos. Sus 21 naciones mantienen una gran alianza en la que la guerra entre humanos está prohibida.

La razón es **El Gran Verano**: cada dos décadas, el verano se prolonga un año entero. El calor hace hervir la selva y miles de bestias arrasan los asentamientos. Durante los diecinueve años de calma, los 21 países acumulan recursos y entrenan guerreros para defender las murallas.

Tras el despertar de La Entidad y el fracaso de la profecía, el Gran Verano se volvió permanente. Con hordas atacando sin tregua y reservas agotándose en semanas, la alianza empezó a fracturarse y algunas naciones cerraron sus puertas al resto.

#### Aasia

Una tierra de contrastes extremos: montañas nevadas, tierras fértiles, desiertos de niebla y costas de mar morado. Esa diversidad impulsó a sus 14 naciones a liderar la ciencia de Eretz; fueron las primeras en construir navíos capaces de cruzar los océanos. En la superficie, los reinos compiten en una carrera de innovación donde el prestigio no se hereda, sino que se gana construyendo herramientas que empujen los límites de la exploración.

Ese progreso tuvo un costo. En los abismos subterráneos vive una civilización que rechaza las máquinas de la superficie. Durante generaciones, las 14 naciones usaron las fosas y cavernas como vertedero de chatarra e inventos fallidos. Hartos de ver su hogar envenenado, los habitantes del subsuelo iniciaron una guerra silenciosa contra puertos y centros de investigación.

El ataque de La Entidad arrasó los grandes laboratorios y abrió las compuertas hacia las profundidades. Hoy los sobrevivientes defienden su tecnología de las aberraciones del vacío y del contraataque de los moradores del subsuelo.

#### Kastleland

Kastleland se considera el centro de Eretz por su posición geográfica. Sus tierras fértiles, de castillos de piedra y valles verdes, se dividen en 10 reinos donde el linaje define el poder. El honor de una familia se mide por la reputación en combate de sus miembros; desde niños, los jóvenes se forman en academias de caballeros que compiten en torneos para demostrar qué linaje tiene la mejor técnica.

Esa obsesión tiene una raíz sagrada: los textos antiguos profetizaron que de esas academias saldría el héroe destinado a salvar al mundo de la calamidad final. Por generaciones, los 10 reinos canalizaron sus mejores recursos hacia esa promesa.

Tras la derrota de Eon en la cumbre del archipiélago, el corazón de Kastleland quedó hecho pedazos. Los linajes casi se extinguieron y las academias quedaron en escombros. La certeza de ser el «pueblo elegido» se convirtió en vergüenza. Sobre esas ruinas camina Eon en busca de su revancha.

#### Oseania

Un megacontinente formado por 17 islas-país. *Pendiente de desarrollar; no aparece en el juego.*

#### Kalaharia y Vaskia

*Pendientes de desarrollar; no aparecen en el juego.*

### Reglas especiales del mundo

- **Los fragmentos del héroe:** al caer Eon, su poder se dividió y fue absorbido por criaturas poderosas. Vencerlas devuelve ese poder en forma de habilidades. Por eso los jefes «entregan» habilidades.
- **La experiencia se puede intercambiar:** la energía que liberan las criaturas al morir (XP) es tangible; el mercader sabe destilarla en potenciadores.
- **Los Vestigios:** soldados sin rostro, blancos como La Entidad, nacidos de su ataque. Cuanto más cerca de la isla final, más abundan.
- **Géiseres:** el cataclismo fracturó la corteza; en las islas brotan géiseres lo bastante potentes para lanzar a una persona de una isla a otra.

### Historia del mundo

#### Antes del juego

Los reinos de Kastleland preparan durante siglos al héroe de la profecía. La Entidad emerge del océano, Eon asciende el archipiélago flotante para enfrentarla y pierde. El ataque del titán arrasa el 98 % de la civilización.

#### Durante el juego

Eon despierta solo en la costa días después. La Entidad permanece en la isla final, visible desde todo Kastleland. Las criaturas que absorbieron el poder de Eon dominan la costa, las ruinas y el archipiélago.

#### Después del juego

La Entidad es derrotada y el cielo se despeja. El mundo sigue en ruinas, pero la amenaza ha terminado. Queda abierta la reconstrucción y el destino de los demás continentes.

### Lugares

| Lugar | Descripción | Función jugable | Importancia narrativa |
| --- | --- | --- | --- |
| Playa del Despertar | Arena gris, restos de naves y estandartes. | Tutorial de movimiento y combate. | Eon despierta solo tras su derrota. |
| Acantilados de la Costa | Rocas, cuevas marinas y faros caídos. | Exploración con rutas opcionales; antesala del Jefe 1, donde aparece el mercader. | Camino hacia la guarida del Jefe 1. |
| Arena de la Marea | Playa abierta con el mar a un lado. | Combate contra el Jefe 1. | Primer fragmento recuperado. |
| Bosque de Raíces | Árboles altos, raíces colosales, armaduras de caballeros antiguos. | Plataformas verticales; primer Earthlem. | Restos de los caballeros que marcharon con Eon. |
| Ruinas Abandonadas | Antigua academia de caballeros arrasada; suelo plano de piedra y pilares. | Exploración y combate contra el Jefe 2. | Símbolo de la profecía rota. |
| Archipiélago de Tierra | Islas de tierra y roca flotando sobre el vacío, unidas por géiseres. | Exploración aérea; combate contra el Jefe 3. | Último guardián. |
| Puente de la Serpiente | El cuerpo petrificado del Jefe 3. | Camino hacia la isla final. | El precio de la revancha hecho piedra. |
| Isla Final | La cumbre donde Eon perdió. | Batalla contra La Entidad. | Cierre del arco. |

### Facciones

| Facción | Objetivo | Relación con el jugador |
| --- | --- | --- |
| La Entidad y los Vestigios | Terminar la destrucción de Eretz. | Hostil. |
| Criaturas con fragmentos (jefes) | Conservar el poder que absorbieron. | Hostil; entregan habilidades al ser vencidas. |
| Fauna corrompida (Aurion, Earthlem) | Sobrevivir y defender su territorio. | Hostil; fuente de XP. |
| El mercader | Sobrevivir comerciando. | Aliado comercial. |

### Coherencia del mundo

- Ningún personaje recuerda a Eon como héroe legendario; los pocos que lo reconocen lo tratan con ironía.
- La Entidad siempre se ve en el horizonte; nunca aparece fuera de la isla final hasta el combate.
- Las habilidades solo se obtienen de jefes; no se compran.
- No hay aliados reclutables ni acompañantes: Eon avanza solo.


---

## Personajes

Las cifras de combate de jefes y enemigos están en [[03 - Enemigos y NPC]]; aquí se describe su identidad y su papel.

### Protagonista: Eon

![[Default Sprite.png|178]]

| Campo | Descripción |
| --- | --- |
| Rol | Héroe caído en busca de revancha. |
| Función jugable | Personaje controlado: espada, salto, dash y las habilidades que recupera. |
| Función narrativa | El elegido que falló y decide volver por mérito propio. |
| Descripción física | Joven espadachín ligeramente musculoso, de cabello azul, con capa y armadura ligera dañada. |
| Personalidad | Antes, confiado hasta la arrogancia; ahora, terco y con humor seco. |
| Motivación | Corregir su derrota y demostrar que no necesita una profecía. |
| Objetivo | Derrotar a La Entidad. |
| Conflicto | La vergüenza de haber fallado frente a todo un mundo que creía en él. |
| Relaciones | Viaja solo; el mercader lo trata con burla y respeto a partes iguales. |
| Arco | De «estoy destinado a ganar» a «voy a ganar porque me preparé». |
| Habilidades | Espada, salto, dash; recupera Doble salto, Tajo ardiente, Dash cortante y Escama pétrea. |
| Debilidades | Sin armadura legendaria: 100 HP, sin escudo propio y sin forma de curarse en el campo. |
| Tono | Frases breves, decididas, con autocrítica. |

### Antagonista: La Entidad

![[Pasted image 20261016153614.png]]

| Campo | Descripción |
| --- | --- |
| Rol | Titán cósmico y jefe final. |
| Función jugable | Batalla final en la isla donde Eon perdió. |
| Función narrativa | La calamidad que la profecía anunciaba. |
| Descripción física | Humanoide colosal de color gris claro, sin rostro. |
| Personalidad | Indiferente; no habla, no se burla. Actúa como una fuerza de la naturaleza. |
| Objetivo | Acabar con la humanidad. |
| Habilidades | Golpes de zona sobre las islas, ondas y la invocación de Vestigios. |
| Debilidad | Los cañones de la isla final y los puntos que expone en su última fase. |

### Jefes

| Jefe | Zona | Identidad | Habilidad que entrega |
| --- | --- | --- | --- |
| **Jefe 1 — Camarón serpiente** *(nombre provisional)* | Arena de la Marea (costa) | Crustáceo alargado como una serpiente marina; acorazado, de antenas largas. Absorbió el fragmento de agilidad de Eon. Libera camaroncitos voladores. | Doble salto |
| **Jefe 2 — Mago oscuro** *(nombre provisional)* | Ruinas Abandonadas | Antiguo hechicero de la academia que tomó el fragmento de poder arcano. Domina el fuego, el magma y el teletransporte. | Tajo ardiente y Dash cortante |
| **Jefe 3 — Serpiente gigante** *(nombre provisional)* | Archipiélago de Tierra | Serpiente segmentada colosal que rodea las islas flotantes, inspirada en el Devorador de mundos de Terraria. Al morir se petrifica. | Escama pétrea |

### Enemigos comunes

| Enemigo | Identidad |
| --- | --- |
| **Aurion** | Criatura voladora de núcleo brillante; hostigador aéreo. |
| **Earthlem** | Gólem de roca camuflado bajo tierra; tanque terrestre. |
| **Vestigio** *(nombre provisional)* | Guerrero humanoide sin rostro, todo blanco, con forma parecida a La Entidad. Porta un arma. Es un eco del titán. |
| **Camaroncitos** *(sin nombre)* | Esbirros del Jefe 1; pequeños camarones que persiguen a Eon en el aire. |

### NPC: el mercader (Seller)

| Campo | Descripción |
| --- | --- |
| Rol | Comerciante ambulante. |
| Función jugable | Aparece en la antesala de cada jefe, empezando por el primero, y cambia XP por potenciadores permanentes. |
| Función narrativa | Ex soldado de una academia de caballeros de Kastleland que desertó el día del ataque. Representa a la gente común que sobrevive. |
| Descripción física | Hombre de mediana edad, robusto, piel curtida, barba descuidada y una enorme mochila metálica llena de frascos, reliquias y chatarra. |
| Personalidad | Cínico y burlón en la superficie; en secreto, quiere que Eon gane. |
| Motivación | Sobrevivir y, sin admitirlo, redimir su deserción. |
| Conflicto | Abandonó a su escuadrón para salvarse. |
| Relaciones | Regaña a Eon, pero siempre lo espera antes de cada pelea. |
| Arco | Empieza cobrando cada punto de XP; antes de la isla final le regala un potenciador. |
| Habilidades | Destilar la energía de las criaturas (XP) en potenciadores; tasar reliquias. |
| Debilidades | Lento por su carga; nunca se acerca a donde hay pelea. |
| Tono | Áspero y seco. |


---

## Diálogos y Narrativa

### Métodos narrativos

- **Cómic guiado (*motion comic*):** prólogo de 5 páginas; la cámara avanza de viñeta en viñeta al ritmo del jugador.
- **Ilustraciones fijas:** entrega de cada habilidad, la serpiente petrificada y el final.
- **Diálogo:** cuadros de texto con retrato (*bust-up*) y escritura progresiva, con el mercader y en momentos clave de Eon.
- **Texto ambiental:** inscripciones en ruinas y estandartes caídos.
- **Descripciones:** el inventario y la tienda describen cada habilidad y potenciador.
- **Entorno:** la silueta de La Entidad en el horizonte de cada zona.
- **Audio:** música melancólica en exploración y percusión intensa en los jefes.

### Prólogo (cómic)

- **Participantes:** narrador en tercera persona y Eon.
- **Objetivo:** presentar el mundo y establecer que Eon ya perdió.
- **Páginas:**
    1. **El mundo:** Eretz antes del cataclismo.
    2. **El continente:** Kastleland, sus 10 reinos y sus academias.
    3. **La calamidad:** La Entidad emerge del océano.
    4. **La profecía:** Eon asciende el archipiélago, equipado con armas legendarias.
    5. **La caída:** el titán destroza su espada y lo arroja al abismo; la onda arrasa el continente.
- **Controles:** `Espacio` / `A` avanza; mantener `Escape` / `Start` 1,5 s omite el prólogo.
- **Consecuencia:** fundido a negro; Eon despierta solo en la Playa del Despertar y el control pasa al jugador.

### Escenas de diálogo

#### El despertar

- **Contexto:** primer momento jugable.
- **Contenido:** Eon despierta entre la espuma, aturdido: *«Perdí… ¿Cuánto tiempo estuve fuera?»* Se mira las manos vacías y ve a La Entidad en el horizonte: *«Sigue ahí. Bien. Así sé a dónde volver.»*

#### El mercader

- **Primer encuentro (antesala del Jefe 1):** *«Vaya, el héroe de la profecía sigue respirando. Esas criaturas sueltan algo más útil que tu destino: experiencia. Tráemela y te doy con qué pelear. Lo que te venda es tuyo para siempre.»*
- **Compra exitosa:** *«Trato hecho. Póntelo antes de entrar; guardado en la mochila no te sirve de nada.»*
- **XP insuficiente:** *«No regalo nada por lástima, muchacho. Vuelve cuando hayas peleado un poco más.»*
- **Encuentros siguientes (antesala de cada jefe):** *«Otra vez tú. Lo que vive ahí adelante tiene algo tuyo. Ve y recupéralo.»*
- **Antes de la isla final:** *«Toma. Este va por mi cuenta… y por los que no se quedaron a pelear.»* (regala un potenciador)

#### Entrega de habilidad

- **Contexto:** al vencer a cada jefe, un fragmento de luz vuelve a Eon.
- **Contenido:** ilustración breve, nombre de la habilidad, su control y su función, y el aviso *«Se guardó en tu inventario (Tab)»*.

#### La serpiente petrificada

- **Contexto:** al vencer al Jefe 3.
- **Contenido:** ilustración fija del cuerpo de la serpiente convirtiéndose en piedra y formando un camino hacia la isla final. Eon: *«Un puente. Gracias por nada.»*

#### La revancha

- **Contexto:** al llegar a la isla final.
- **Contenido:** Eon ve a La Entidad de frente. *«La última vez tenía una profecía. Esta vez tengo algo mejor: sé cómo pegas.»*

### Tono

- **Lenguaje:** solemne y reflexivo en el narrador; directo, coloquial y decidido en Eon y el mercader.
- **Humor:** ironía sobre la profecía fallida; sin comedia absurda.
- **Formalidad:** registro alto en el cómic; informal en los diálogos.
- **Estilo:** frases breves y contundentes, al estilo del anime de acción.

### Decisiones narrativas

| Decisión | Opciones | Consecuencia |
| --- | --- | --- |
| Inicio del prólogo | A) Leer viñeta por viñeta. B) Omitir. | Quien quiere la historia la recibe; quien quiere acción entra directo a la Playa. |
| Diálogos del mercader | A) Leer. B) Omitir con `Escape`. | El primer encuentro siempre muestra al menos cómo funciona la tienda. |

### Localización

- **Español (Latinoamérica):** idioma base y único de esta versión.


---

## Estructura del Contenido

El juego es un recorrido por zonas conectadas en un orden principal, con rutas opcionales que se abren con habilidades. Cada bloque termina en una antesala con el mercader y un jefe que entrega una habilidad. Las zonas superadas siguen abiertas para volver a acumular XP.

### Estructura

```text
True Hero
├── Prólogo: cómic «La caída del elegido» (derrota de Eon)
├── Bloque 1 — La Costa
│   ├── Playa del Despertar (tutorial)
│   ├── Acantilados de la Costa (zona explorable)
│   ├── Antesala: mercader + punto de control
│   └── Arena de la Marea → Jefe 1: Camarón serpiente → Doble salto
├── Bloque 2 — Tierra adentro
│   ├── Bosque de Raíces (zona explorable)
│   ├── Ruinas Abandonadas (zona explorable)
│   ├── Antesala: mercader + punto de control
│   └── Patio de la Academia → Jefe 2: Mago oscuro → Tajo ardiente + Dash cortante
├── Bloque 3 — El cielo roto
│   ├── Archipiélago de Tierra (zona explorable con géiseres)
│   ├── Antesala: mercader + punto de control
│   └── Anillo de Islas → Jefe 3: Serpiente gigante → Escama pétrea
│       └── Cinemática: la serpiente se petrifica
└── Final
    ├── Puente de la Serpiente
    ├── Antesala: mercader (regalo) + punto de control
    └── Isla Final → La Entidad → Final y créditos
```

### Cantidad estimada

| Tipo | Cantidad |
| --- | ---: |
| Bloques | 3 + final |
| Zonas explorables | 5 |
| Arenas de jefe | 4 |
| Jefes normales | 3 |
| Jefe final | 1 |
| Enemigos comunes | 3 (+ esbirros del Jefe 1) |
| NPC | 1 (mercader) |
| Habilidades | 4 |
| Potenciadores | 6 |
| Puntos de control | ~10 (2 por zona, 1 en cada antesala) |
| Apariciones del mercader | 4 (una antesala por jefe) |

### Dependencias

| Contenido | Requiere antes |
| --- | --- |
| Mercader | Llegar a la antesala del Jefe 1. |
| Jefe 1 | Salto, dash y combo enseñados en la Playa y los Acantilados. |
| Jefe 2 | Earthlem y Vestigio presentados en Bosque y Ruinas. |
| Archipiélago de Tierra | Jefe 2 derrotado (activa los géiseres). |
| Jefe 3 | Géiseres y plataformas pequeñas dominados en el Archipiélago. |
| Isla Final | Jefe 3 derrotado (puente petrificado). |
| Rutas opcionales | Doble salto o Tajo ardiente equipados (nunca obligatorias). |


---

## Niveles y zonas

Cada zona tiene una ruta principal que se puede completar sin ninguna habilidad concreta y rutas opcionales que piden Doble salto o Tajo ardiente. Las rutas opcionales ofrecen atajos y grupos de enemigos que dan más XP. No hay objetos que recoger aparte de la XP.

Antes de cada jefe hay una **antesala** con el mercader y un punto de control. Las zonas superadas siguen abiertas: sus enemigos reaparecen y se puede volver a acumular XP.

### Resumen de zonas

| Zona | Duración | Enemigos | Rutas opcionales | Puntos de control |
| --- | --- | --- | --- | --- |
| Playa del Despertar | 3 min | Aurion | — | Inicio |
| Acantilados de la Costa | 6 min | Aurion | Cueva superior (Doble salto): grupo de Aurion | Mitad y antesala del Jefe 1 |
| Arena de la Marea | 3 min | Jefe 1, camaroncitos | — | — |
| Bosque de Raíces | 8 min | Aurion, Earthlem | Copa de los árboles (Doble salto): atajo | Entrada y salida |
| Ruinas Abandonadas | 7 min | Earthlem, Vestigio | Torre sellada (Tajo ardiente: interruptor lejano): atajo y Vestigios | Mitad y antesala del Jefe 2 |
| Patio de la Academia | 3 min | Jefe 2 | — | — |
| Archipiélago de Tierra | 9 min | Aurion, Vestigio, Earthlem | Islas altas (Doble salto + géiser): grupo de enemigos | Mitad y antesala del Jefe 3 |
| Anillo de Islas | 4 min | Jefe 3 | — | — |
| Puente e Isla Final | 6 min | La Entidad, Vestigios | — | Antesala de la Isla Final |

### Playa del Despertar

- **Objetivo principal:** enseñar movimiento, salto, combo y dash con un Eon debilitado.
- **Objetivos secundarios:** presentar la XP y la silueta de La Entidad.
- **Duración:** 3 minutos. **Dificultad:** baja.
- **Mecánicas introducidas:** movimiento, salto, ataque, ataque descendente, dash.
- **Enemigos:** 4 Aurion aislados.
- **Recompensas:** XP.
- **Entrada:** fin del prólogo. **Salida:** borde derecho hacia los Acantilados.
- **Eventos:** despertar de Eon.

```text
Despertar → Primeros Aurion → Punto de control → Acantilados
```

### Acantilados de la Costa

- **Objetivo principal:** llegar a la antesala del Jefe 1.
- **Objetivos secundarios:** explorar cuevas marinas y faros caídos.
- **Duración:** 6 minutos. **Dificultad:** media-baja.
- **Mecánicas utilizadas:** saltos sobre precipicios, dash aéreo, rebote sobre Aurion.
- **Enemigos:** grupos de 2–3 Aurion.
- **Puntos de control:** mitad del recorrido y antesala.
- **Eventos:** en la antesala aparece el mercader por primera vez y abre la tienda.

```text
Entrada → Faro caído → Cuevas marinas → Punto de control → Antesala (mercader) → Arena de la Marea
                         └── Cueva superior (Doble salto, opcional)
```

### Arena de la Marea (Jefe 1)

- Playa plana de 30 u de ancho con el mar en el lado derecho. Sin plataformas fijas: las plataformas de agua solo aparecen durante la ráfaga.
- **Límites invisibles** a ambos lados mientras dura el combate.

### Bosque de Raíces

- **Objetivo principal:** atravesar el bosque hasta las Ruinas.
- **Duración:** 8 minutos. **Dificultad:** media.
- **Mecánicas:** plataformas verticales sobre raíces (alcanzables con salto y dash).
- **Enemigos:** Aurion, primer Earthlem.
- **Puntos de control:** entrada y salida.
- **Entrada:** salida de la Arena de la Marea. **Salida:** camino hacia las Ruinas.

### Ruinas Abandonadas

- **Objetivo principal:** llegar al Patio de la Academia.
- **Objetivos secundarios:** explorar aulas derrumbadas y torres.
- **Duración:** 7 minutos. **Dificultad:** media-alta.
- **Enemigos:** Earthlem, primer Vestigio.
- **Puntos de control:** mitad del recorrido y antesala (mercader).

### Patio de la Academia (Jefe 2)

- Arena **completamente plana**, 36 u de ancho, sin plataformas, dentro de las ruinas.
- Al entrar, **pilares de piedra de las ruinas** emergen del suelo en ambos extremos y bloquean el paso; se hunden al morir el jefe. Es la única arena con límites visibles.
- Al vencer al jefe se activan los géiseres que llevan al Archipiélago.

### Archipiélago de Tierra

- **Objetivo principal:** cruzar las islas hasta el Anillo de Islas.
- **Duración:** 9 minutos. **Dificultad:** alta.
- **Mecánicas introducidas:** géiseres; combate en islas pequeñas sobre el vacío.
- **Enemigos:** Aurion, Vestigio, Earthlem.
- **Puntos de control:** mitad del recorrido y antesala (mercader).

```text
Géiser de las Ruinas → Isla 1 → Géiser → Isla 2 (punto de control) → Géiser → Islas 3–4 → Antesala (mercader) → Anillo de Islas
                                                      └── Islas altas (opcional)
```

### Anillo de Islas (Jefe 3)

- 7 plataformas de tierra flotantes en dos alturas, separadas a distancias que se cubren con salto y dash (el Doble salto facilita, pero no es necesario). La serpiente las rodea y las atraviesa.
- **Límites invisibles** a los lados; el vacío inferior aplica la regla de caída.
- Al vencer: ilustración de la serpiente petrificada; su cuerpo forma el Puente de la Serpiente.

### Puente de la Serpiente e Isla Final (La Entidad)

- **Puente:** tramo corto y sin enemigos sobre el cuerpo de piedra; termina en la última antesala, donde el mercader regala un potenciador.
- **Isla Final:** combate en fases con **límites invisibles**. La primera fase recupera la estructura del encuentro original (islas ascendentes, géiseres en lugar de trampolines, cañones y el titán al fondo). Detalle en [[03 - Enemigos y NPC]].

### Criterios de calidad

- El objetivo de cada zona se entiende sin texto.
- La ruta principal nunca exige una habilidad concreta; las rutas opcionales muestran qué falta.
- La distancia entre puntos de control es justa, porque no hay curación en el campo.
- Cada zona enseña lo que su jefe va a exigir.


---

## Enemigos y NPC

El juego tiene tres enemigos comunes (Aurion, Earthlem y Vestigio), los esbirros del Jefe 1, tres jefes normales y La Entidad. El enemigo Driller queda descartado. Las cifras son la referencia de diseño; se ajustan en pruebas y se registran en [[03 - Registro de Decisiones]].

### Resumen de enemigos comunes

| Enemigo | Vida | Velocidad | Daño principal | Zonas | XP |
| --- | ---: | --- | --- | --- | ---: |
| Aurion | 20 HP | 2,5 u/s patrulla; 7 u/s embestida | Embestida 15; contacto 10 | Costa, Bosque, Archipiélago | 10 |
| Earthlem | 80 HP | 1,2 u/s | Puño 20; onda 15; emerger 10 | Bosque, Ruinas, Archipiélago | 30 |
| Vestigio | 50 HP | 3 u/s | Combo 18; estocada 22 | Ruinas, Archipiélago, Isla Final | 25 |
| Camaroncito | 5 HP | 3 u/s en el aire | Contacto 8 | Arena de la Marea | 1 |

### Aurion

- **Rol:** hostigador aéreo.
- **Comportamiento:** flota a media altura. Al detectar a Eon su núcleo se vuelve rojo, carga 0,5 s y embiste en línea recta hacia la posición registrada. Si falla, queda aturdido 0,8 s a ras de suelo y luego vuelve a subir.
- **Detección:** 6 u horizontales y 4 verticales con línea de visión.
- **Defensas:** ninguna.
- **Debilidad:** un ataque descendente sobre él lo destruye y recupera el dash aéreo de Eon.
- **Recompensa:** 10 XP.

```text
Patrullar → Detectar (núcleo rojo, 0,5 s) → Embestir → [falla] Aturdido 0,8 s → Volver a altura
```

### Earthlem

- **Rol:** tanque terrestre que bloquea el paso.
- **Comportamiento:** camuflado como roca plana. Cuando Eon se acerca a 3,5 u, emerge levantando escombros. Si Eon se aleja más de 8 u, se entierra y reaparece más cerca.
- **Ataques:**
    - *Barrido de roca:* tajo horizontal tras 0,4 s de preparación; 20 de daño.
    - *Aplastamiento sísmico:* golpe al suelo con ambos puños; onda rasante de 3 u (hay que saltarla); 15 de daño.
- **Defensas:** coraza frontal; los golpes de frente hacen 50 % del daño. La espalda recibe daño completo.
- **Debilidades:** gira despacio; un dash para quedar a su espalda permite castigarlo. Con Dash cortante, el propio dash le hace daño completo. Con Escama pétrea, un bloqueo perfecto contra el barrido lo aturde 1 s.
- **Recompensa:** 30 XP.

```text
Enterrado → Detecta a 3,5 u → Emerge → Barrido / Aplastamiento → [Eon a más de 8 u] Se entierra
```

### Vestigio *(nombre provisional)*

- **Rol:** guerrero cuerpo a cuerpo.
- **Descripción:** humanoide sin rostro, todo blanco, con una silueta que recuerda a La Entidad. Porta una lanza-espada blanca. Es un eco del titán.
- **Comportamiento:** patrulla su plataforma; al ver a Eon se acerca hasta 3 u y elige un ataque.
- **Ataques:**
    - *Combo de dos tajos:* preparación de 0,5 s (el arma brilla); 18 de daño por tajo.
    - *Estocada:* avanza 3 u tras 0,7 s de preparación; 22 de daño.
- **Guardia:** tras recibir 2 golpes frontales seguidos, levanta el arma 1,2 s y bloquea todo daño frontal.
- **Debilidades:** la guardia no cubre la espalda ni el Dash cortante; el Tajo ardiente y el bloqueo perfecto de la Escama pétrea rompen la guardia y lo aturden 0,5 s.
- **Recompensa:** 25 XP.

```text
Patrullar → Detectar → Acercarse → Combo / Estocada → [2 golpes frontales recibidos] Guardia 1,2 s
```

### Jefe 1 — Camarón serpiente *(nombre provisional)*

- **Arena:** Arena de la Marea, playa plana de 30 u con el mar a la derecha. Límites invisibles.
- **Vida:** 500 HP. **Fases:** 1 (100–50 %) y 2 (menos de 50 %).
- **Descripción:** crustáceo alargado con cuerpo de serpiente marina. Pasa la mayor parte del tiempo en el agua; solo se le puede golpear con la espada cuando su cuerpo está sobre la arena.
- **Recompensa:** 200 XP y **Doble salto**.

| Ataque | Aviso | Regla | Daño |
| --- | --- | --- | --- |
| **Invocar camaroncitos** | Chapoteo y burbujas. | Libera 3 camaroncitos (4 en fase 2) que persiguen a Eon en el aire a 3 u/s. Máximo 6 vivos. Recarga 12 s. | 8 por contacto |
| **Embestida corta** | Ojos brillantes y cuerpo recogido 0,6 s. | Se lanza 5 u sobre la arena hacia Eon. Después queda varado 1,5 s: **ventana de castigo**. | 20 |
| **Mordida** | Mandíbulas abiertas 0,4 s. | Solo si Eon está a 2,5 u de la cabeza. | 25 |
| **Ráfaga de agua** | Se eleva en la orilla e inhala 2 s; agua girando en la boca y sonido exclusivo. | Al empezar el aviso **emerge una plataforma de agua** a 2,5 u de altura (alcanzable con salto simple) en una de tres posiciones. La ráfaga barre toda la arena a ras de suelo hasta 2 u de altura durante 1,5 s. La plataforma se disuelve 1 s después. Tras la ráfaga queda agotado 3 s en la orilla: **ventana de castigo**. Cada 20 s (15 s en fase 2). | **Instakill** |

- **Fase 2:** más esbirros, ráfagas más frecuentes y los camaroncitos siguen persiguiendo a Eon mientras está sobre la plataforma de agua.
- **Regla de diseño:** la ráfaga nunca se lanza si no hay una plataforma de agua visible.

```text
Agua (invoca / se acerca) → Embestida → Varado 1,5 s (castigo) → Agua
                    └── cada 20 s: Aviso + plataforma de agua → Ráfaga (instakill) → Agotado 3 s (castigo)
```

#### Camaroncitos *(sin nombre)*

- Esbirros voladores pequeños. 5 HP: mueren con un golpe o un ataque descendente (que además rebota a Eon).
- Persiguen a Eon en el aire; al tocarlo hacen 8 de daño y retroceden 1 s antes de volver a perseguir.
- Desaparecen al morir el jefe.

### Jefe 2 — Mago oscuro *(nombre provisional)*

- **Arena:** Patio de la Academia, suelo de piedra **totalmente plano** de 36 u, sin plataformas, dentro de unas ruinas abandonadas. Al empezar, **pilares de las ruinas** emergen en ambos extremos y bloquean el paso; se hunden al morir el jefe.
- **Vida:** 700 HP. **Fases:** 1 (100–40 %) y 2 (menos de 40 %).
- **Descripción:** hechicero encapuchado que flota a ras de suelo. Se puede golpear con la espada siempre que no tenga el escudo activo.
- **Recompensa:** 300 XP, **Tajo ardiente** y **Dash cortante** (se guardan los dos en el inventario).

| Ataque | Aviso | Regla | Daño |
| --- | --- | --- | --- |
| **Lluvia de llamaradas** | Círculos de luz naranja en el suelo 0,8 s. | 5 llamaradas (7 en fase 2) caen del cielo; 2 apuntan a la posición prevista de Eon. Radio de 1 u. | 20 |
| **Picos de magma** | El suelo se agrieta y brilla 0,5 s antes de cada pico. | Una ola de picos nace junto al mago y avanza hacia el extremo opuesto a 6 u/s (Eon corre a 7 u/s). Cada pico mide 2,5 u y dura 1 s. La ola se detiene a 2 u del pilar del extremo: hay que **correr y alejarse** del mago hasta esa zona segura. Saltar sobre el frente no sirve: los picos de detrás siguen activos. | 18 por pico |
| **Escudo arcano** | Esfera violeta que se forma en 0,5 s. | Cada 15 s, durante 4 s, bloquea todo daño. Los golpes rebotan y empujan levemente a Eon. Mientras dura, el mago lanza cráneos. | — |
| **Cráneos de fuego** | Llamas en sus manos 0,6 s. | 3 cráneos (4 en fase 2) que persiguen a Eon en el aire a 3,5 u/s con giro limitado. Duran 6 s. Se destruyen con un golpe. | 15 |
| **Teletransporte** | Humo negro en el punto de destino 0,5 s antes. | Tras cada 3 ataques (2 en fase 2) desaparece y reaparece en el **extremo opuesto** de la arena. Al reaparecer queda expuesto 1 s. | — |

- **Fase 2:** se teletransporta con más frecuencia y puede combinar llamaradas con la ola de picos.

```text
Ataque 1 → Ataque 2 → Ataque 3 → Teletransporte al extremo opuesto (expuesto 1 s) → …
   └── cada 15 s: Escudo 4 s + Cráneos de fuego
```

### Jefe 3 — Serpiente gigante *(nombre provisional)*

- **Arena:** Anillo de Islas, 7 plataformas de tierra flotantes en dos alturas sobre el vacío. Límites invisibles.
- **Vida:** 1200 HP compartidos por todo el cuerpo. **Fases:** 1 (100–50 %) y 2 (menos de 50 %).
- **Descripción:** serpiente segmentada colosal (cabeza + ~18 segmentos + cola) que da vueltas entre y a través de las plataformas, al estilo del Devorador de mundos de Terraria.
- **Recompensa:** 400 XP, **Escama pétrea** y cinemática de petrificación.

| Elemento / ataque | Aviso | Regla | Daño |
| --- | --- | --- | --- |
| **Cabeza** | Ojos y mandíbula brillantes; silueta siempre visible. | Tocarla es **instakill**. No recibe daño. | **Instakill** |
| **Cuerpo** | — | Cada segmento recibe daño de espada, Tajo ardiente, ataque descendente (con rebote) y Dash cortante. Tocarlo hace daño. | 15 por contacto |
| **Cola** | Punta de color distinto. | Punto débil: recibe el doble de daño. | 15 por contacto |
| **Recorrido** | — | Trayectorias en bucle, en ocho y zambullidas verticales a 6 u/s (8 u/s en fase 2). Puede atravesar las plataformas. | — |
| **Lluvia de baba** | El segmento se hincha y gotea 0,4 s antes. | Cada segmento deja caer gotas de baba en momentos aleatorios (cada 2–4 s; máximo 6 gotas a la vez en pantalla). Caen en vertical. | 10 |
| **Embestida de cabeza** | Rugido y flecha en el borde de la pantalla 1,5 s. | La cabeza sale de pantalla y cruza la arena en línea recta hacia la posición de Eon a 14 u/s. | **Instakill** (cabeza) |

- **Fase 2:** más velocidad, gotas más frecuentes (cada 1,5–3 s) y embestidas dobles.
- **Al morir:** el cuerpo se detiene, se petrifica (ilustración fija) y forma el Puente de la Serpiente hacia la isla final.

### La Entidad (jefe final)

- **Arena:** Isla Final. La fase 1 retoma el encuentro ya diseñado del titán (islas ascendentes, cañones, titán al fondo), con géiseres en lugar de trampolines. Límites invisibles.
- **Vida:** 2000 HP *(valor provisional; ajustar con el encuentro existente)*.
- **Recompensa:** victoria y final.

| Fase | Vida | Desarrollo |
| --- | --- | --- |
| **1. Ascenso** | 100–60 % | Eon sube por 3 islas unidas por géiseres. La Entidad, al fondo, golpea zonas del suelo marcadas con sombra 1,2 s (30 de daño) y envía hasta 3 Vestigios. Cada isla tiene un **cañón**: al interactuar dispara 150 de daño; recarga 6 s. |
| **2. Cumbre** | 60–25 % | Cara a cara. La Entidad apoya las manos en la cumbre; los núcleos del dorso de cada mano son puntos débiles. Barrido de mano (saltar o doble salto; 25), onda de choque rasante (20) e invocación de Vestigios. |
| **3. Revancha** | Menos de 25 % | Su rostro se abre y expone el núcleo. Combina los ataques anteriores a mayor velocidad. *(Detalle pendiente de cerrar con el equipo.)* |

### NPC

#### Mercader (Seller)

- **Función:** cambia XP por potenciadores permanentes (compra única de cada uno).
- **Ubicación:** aparece por primera vez en la antesala del Jefe 1 y desde entonces en la antesala de cada jefe: Acantilados, Ruinas, Archipiélago y final del Puente de la Serpiente.
- **Interacción:** `E` / `Y` dentro de su zona; congela el movimiento y abre la tienda. Cancelar cierra el menú.
- **Condiciones:**
    - La antesala no tiene enemigos.
    - El catálogo crece al avanzar (ver [[06 - Economía y Recursos]]).
    - Los potenciadores ya comprados aparecen como «Adquirido».
    - En la antesala de la Isla Final regala uno de los potenciadores que falten (una vez).
- **Información:** pistas sobre el jefe de la zona en su diálogo.


---

## Objetos y Coleccionables

Solo hay tres tipos de elementos que el jugador obtiene: **XP**, **potenciadores** y **habilidades**. No hay objetos de curación ni de escudo: la vida y el escudo se restauran únicamente en puntos de control y al vencer a un jefe.

### 1. Experiencia (XP)

- **Tipo:** recurso de intercambio.
- **Obtención:** los enemigos sueltan su XP como orbes dorados al morir; los jefes entregan una cantidad mayor.
- **Uso:** comprar potenciadores al mercader.
- **Reglas:** los orbes se atraen hacia Eon a 3 u o menos y se suman al contacto; no desaparecen mientras Eon siga en la zona. Tope de 9999. Se conserva al morir.
- **Aspecto:** esfera dorada pequeña que gira; el contador del HUD rebota al sumar.

### 2. Potenciadores (permanentes)

- **Tipo:** mejoras pasivas permanentes.
- **Obtención:** compra única al mercader, en la antesala de cada jefe.
- **Uso:** se equipan en una de las **3 ranuras de potenciador** del inventario. **Mientras están equipados, su efecto está siempre activo.** No tienen botón ni se gastan.
- **Inventario:** al seleccionar un potenciador se muestra su función.
- **Persistencia:** nunca se pierden.

| Potenciador | Efecto | Precio | Disponible desde | Aspecto del icono |
| --- | --- | ---: | --- | --- |
| Vigor | +30 de vida máxima. | 200 XP | Antesala del Jefe 1 | Corazón de cristal verde. |
| Filo | +25 % de daño en todos los ataques de Eon. | 250 XP | Antesala del Jefe 1 | Piedra de afilar carmesí con chispas. |
| Codicia | +25 % de XP obtenida. | 150 XP | Antesala del Jefe 1 | Saco con brillo dorado. |
| Coraza | Escudo de 50 SP que se restaura junto con la vida. | 250 XP | Antesala del Jefe 2 | Hexágono azul zafiro. |
| Celeridad | +20 % de velocidad y −40 % de recarga del dash. | 300 XP | Antesala del Jefe 2 | Pluma violeta con descargas. |
| Foco arcano | Tajo ardiente con −50 % de recarga y +50 % de daño (requiere Tajo ardiente equipado). | 350 XP | Antesala del Jefe 3 | Runa naranja incandescente. |

### 3. Habilidades (entregadas por jefes)

- **Tipo:** acciones o mejoras de movimiento permanentes.
- **Obtención:** al vencer a cada jefe (el Jefe 2 entrega dos).
- **Uso:** se equipan en una de las **3 ranuras de habilidad**. Ninguna se descarta: las que no se usan quedan guardadas para elegirlas después.
- **Inventario:** al seleccionar una habilidad se muestran su control y su función.
- **Cambios:** fuera de las arenas de jefe.

| Habilidad | Origen | Tipo | Control | Efecto | Icono |
| --- | --- | --- | --- | --- | --- |
| Doble salto | Jefe 1 | Pasiva | Salto en el aire | Segundo salto en el aire. | Pluma con ráfaga de aire. |
| Tajo ardiente | Jefe 2 | Activa | `J` | La espada lanza un tajo de fuego que atraviesa enemigos: 15 de daño, alcance 8 u, recarga 1,2 s. | Espada envuelta en llamas. |
| Dash cortante | Jefe 2 | Pasiva | Dash | El dash hace 20 de daño a cada enemigo atravesado. | Silueta de dash con filo rojo. |
| Escama pétrea | Jefe 3 | Activa | `K` (mantener) | Se petrifica y reduce el daño un 70 %; el bloqueo perfecto anula el golpe y aturde. Recarga 3 s. | Escama gris con grietas. |

Con 4 habilidades y 3 ranuras, el jugador decide qué combinación llevar a la isla final; las cuatro siguen disponibles en el inventario.


---

## Misiones y Desafíos

El juego tiene una misión principal dividida en cuatro objetivos (uno por jefe) y rutas opcionales de exploración. No hay misiones de rescate ni de aliados.

### Misión principal: La revancha

| Objetivo | Tipo | Zona | Requisito | Éxito | Recompensa |
| --- | --- | --- | --- | --- | --- |
| La marea viva | Principal | Costa | — | Derrotar al Camarón serpiente. | 200 XP, Doble salto. |
| Las ruinas en llamas | Principal | Ruinas Abandonadas | Jefe 1 derrotado | Derrotar al Mago oscuro. | 300 XP, Tajo ardiente, Dash cortante. |
| La serpiente de piedra | Principal | Archipiélago de Tierra | Jefe 2 derrotado | Derrotar a la Serpiente gigante. | 400 XP, Escama pétrea, Puente de la Serpiente. |
| La revancha | Principal | Isla Final | Jefe 3 derrotado | Derrotar a La Entidad. | Final del juego. |

- **Condición de fracaso:** ninguna permanente. Ser derrotado devuelve al punto de control de la antesala.
- **Personaje relacionado:** el mercader, que da pistas sobre cada jefe.

#### Pasos de cada objetivo

1. Recorrer la zona y llegar a la antesala del jefe.
2. Comprar potenciadores al mercader (opcional) y preparar el inventario.
3. Entrar en la arena y vencer al jefe.
4. Recibir la habilidad (queda guardada en el inventario) y decidir si equiparla.

### Rutas opcionales

| Ruta | Zona | Requisito | Recompensa |
| --- | --- | --- | --- |
| Cueva superior | Acantilados de la Costa | Doble salto | Grupo de Aurion (XP). |
| Copa de los árboles | Bosque de Raíces | Doble salto | Atajo hacia las Ruinas. |
| Torre sellada | Ruinas Abandonadas | Tajo ardiente (interruptor lejano) | Atajo y grupo de Vestigios (XP). |
| Islas altas | Archipiélago de Tierra | Doble salto + géiser | Grupo de enemigos (XP). |

### Desafío opcional

| Desafío | Requisito | Recompensa |
| --- | --- | --- |
| Sin rasguños *(si hay tiempo)* | Vencer a un jefe sin recibir daño. | Mensaje de logro al terminar el combate. |


---

## Dirección de Arte

Define la identidad visual del juego y las reglas que deben seguir los recursos gráficos para que el combate sea legible y Kastleland, aun en ruinas, sea coherente.

### Identidad visual

| Elemento | Decisión |
| --- | --- |
| Estilo | Pixel art refinado de alta densidad, sombreado por bloques, inspirado en el anime de acción y fantasía. |
| Referencias | *Blasphemous*, *Gurren Lagann*, *Hollow Knight*, *Terraria* (jefe segmentado). |
| Sensación buscada | Derrota, soledad y urgencia que dan paso a determinación. La Entidad siempre presente en el horizonte. |
| Nivel de realismo | Estilizado: proporciones realistas para Eon, jefes y La Entidad; siluetas icónicas y caricaturescas para enemigos menores. |
| Iluminación | Luz 2D difusa por zona, con puntos de luz propios en núcleos, ojos hostiles, filos y magia. |

### Formas predominantes

- **Entornos y ruinas:** rectángulos sólidos; islas flotantes con base de triángulo invertido.
- **Enemigos comunes:** curvas fluidas con terminaciones afiladas (Aurion); bloques pesados (Earthlem); siluetas lisas y verticales sin rasgos (Vestigio).
- **Jefes:** curvas segmentadas (Camarón serpiente y Serpiente gigante); triángulos y capuchas puntiagudas (Mago oscuro).
- **La Entidad y Vestigios:** silueta angular alargada, sin rostro, superficie lisa.

### Paleta de color

**Colores principales**

- **Azul cobalto y celeste (`#3F6EAE`, `#8CAFD9`):** cielo y niebla atmosférica de los planos de *parallax*.
- **Blanco roto y gris mineral (`#E6E8ED`, `#B0B6C4`):** mármol, rocas celestes, La Entidad y los Vestigios.
- **Ocre terroso y marrón (`#4A3728`, `#7D634C`):** base de las islas, raíces y suelo jugable.

**Colores secundarios**

- **Verde musgo y oliva (`#4E6B3E`, `#2D3E24`):** vegetación del Bosque y enredaderas.
- **Azul marino profundo (`#1B263B`, `#111827`):** siluetas de Aurion y sombras.

**Paleta por zona**

| Zona | Dominante | Acento |
| --- | --- | --- |
| Costa | Turquesa y arena gris | Coral del Camarón serpiente |
| Bosque de Raíces | Verdes profundos | Luciérnagas amarillas |
| Ruinas Abandonadas | Piedra y violeta oscuro | Naranja del fuego y magma del Mago |
| Archipiélago de Tierra | Ocres y cielo pálido | Verde ácido de la baba de la serpiente |
| Isla Final | Gris y blanco | Rojo de los núcleos de La Entidad |

**Colores de información jugable**

| Color | Significado |
| --- | --- |
| Oro `#F4D03F` | XP |
| Rojo carmesí `#E74C3C` | Daño recibido y aviso de ataque |
| Verde esmeralda `#2ECC71` | Vida |
| Cian `#00D2D3` | Escudo y dash |
| Naranja incandescente `#FF7A1A` | Tajo ardiente de Eon |
| Violeta `#8E44AD` | Magia del Mago oscuro (escudo, teletransporte) |
| Blanco intenso con borde rojo | **Aviso de instakill** (exclusivo; no se usa para nada más) |

### Reglas visuales

- **Contraste por planos:** a mayor distancia, menos contraste y más azul atmosférico. El plano jugable siempre tiene la mayor saturación.
- **Claridad de amenaza:** todo enemigo tiene una silueta reconocible y un punto focal iluminado (ojo o núcleo).
- **Suelo jugable resaltado:** las superficies pisables tienen un borde superior claro que las separa del fondo.
- **Instakill inconfundible:** la ráfaga del Jefe 1 y la cabeza del Jefe 3 usan el color de aviso de instakill; la cabeza tiene siempre su brillo encendido.
- **La Entidad en el horizonte:** su silueta aparece en el plano más lejano de cada zona y crece a medida que el juego avanza.

### Referencias

![[Pasted image 20261016112525.png|267]]


---

## Personajes y Animación

Lista de sprites y animaciones necesarios. La identidad de cada personaje está en [[03 - Personajes]] y sus reglas de combate en [[03 - Enemigos y NPC]].

### Requisitos por personaje

| Personaje | Sprite | Animaciones | VFX | Estado |
| --- | --- | --- | --- | --- |
| Eon | 64 × 64 | Idle, correr, saltar, doble salto, caer, aterrizar, dash, ataque ×3, ataque descendente, tajo ardiente, escama pétrea (petrificarse, bloqueo perfecto), recibir daño, muerte, interactuar | Estelas de espada (normal y roja con Filo), polvo de aterrizaje, ráfaga del doble salto, estela de dash (normal y cortante), media luna de fuego del tajo ardiente, piel de piedra y destello de bloqueo | Sprite base hecho (`Default Sprite.png`); animaciones pendientes |
| Mercader | 64 × 64 | Idle, hablar, entregar | — | Pendiente |
| Aurion | 48 × 48 | Flotar, cargar, embestir, aturdido, muerte | Núcleo rojo, estela | Pendiente |
| Earthlem | 96 × 96 | Enterrado, emerger, caminar, barrido, aplastamiento, enterrarse, impacto, muerte | Escombros, onda sísmica | Pendiente |
| Vestigio | 64 × 96 | Caminar, combo, estocada, guardia, impacto, muerte | Brillo del arma, disolución blanca | Pendiente |
| Camaroncito | 24 × 24 | Volar, impacto, muerte | Burbujas | Pendiente |
| Jefe 1 — Camarón serpiente | Cabeza 128 × 128 + segmentos | Nadar, emerger, embestida, varado, mordida, inhalar, ráfaga, agotado, muerte | Ráfaga de agua, plataforma de agua, chapoteos | Pendiente |
| Jefe 2 — Mago oscuro | 96 × 128 | Flotar, conjurar llamaradas, golpear el suelo, escudo, invocar cráneos, desaparecer, aparecer, aturdido, muerte | Llamaradas, picos de magma, esfera violeta, cráneos de fuego, humo | Pendiente |
| Jefe 3 — Serpiente gigante | Cabeza 192 × 192, segmento 96 × 96, cola | Mandíbula, segmento hinchado, petrificación | Gotas y salpicadura de baba, polvo al atravesar islas | Pendiente |
| La Entidad | Escala de fondo y escala de cumbre | Escalar, golpe de mano, barrido, invocar, apertura del rostro, derrota | Ondas, sombras de impacto, núcleo | Diseño hecho (referencia); animación pendiente |

### Animaciones de Eon

| Grupo | Animaciones | Fotogramas orientativos |
| --- | --- | --- |
| Movimiento | Idle, correr, saltar, doble salto, caer, aterrizar | 6 / 8 / 3 / 4 / 2 / 3 |
| Combate | Tajo 1, 2, 3; descendente; dash; tajo ardiente; escama pétrea | 4 / 4 / 6 / 3 / 3 / 5 / 4 |
| Interacción | Interactuar | 4 |
| Daño | Impacto, aturdido | 2 / 4 |
| Derrota | Colapso | 8 |

### Ilustraciones fijas

| Ilustración | Uso |
| --- | --- |
| Cómic del prólogo (5 páginas) | Inicio. La página 5 muestra la derrota de Eon. |
| Entrega de habilidad (×4) | Tras cada jefe. |
| Serpiente petrificada | Tras el Jefe 3: el cuerpo se convierte en piedra y forma el puente a la isla final. |
| Final | Tras La Entidad. |

### Convenciones

- **Nombres de archivo:** `Personaje_Accion` (ej. `Eon_DobleSalto.png`, `MagoOscuro_Teletransporte.png`).
- **Formato:** PNG con transparencia; hojas de sprites por personaje; fuente editable en Clip Studio.
- **Escala:** 32 píxeles por unidad de Unity; filtrado *Point* y sin compresión.
- **Pivote:** en los pies para personajes terrestres; en el centro para voladores.


---

## Entornos

### Zonas

| Zona | Estilo | Elementos | Función | Modularidad |
| --- | --- | --- | --- | --- |
| **Playa del Despertar y Acantilados** | Costa gris y turquesa bajo un cielo nublado; restos de naves y estandartes. | Rocas, faros caídos, cuevas marinas; antesala del Jefe 1 con el mercader. | Tutorial y exploración inicial. | Bloques de roca, arena, restos de barco. |
| **Arena de la Marea** | Playa abierta con el mar a un lado; oleaje animado. | Arena plana, mar con capa de agua animada, plataformas de agua temporales. | Jefe 1. | Reutiliza bloques de la Costa. |
| **Bosque de Raíces** | Árboles altos y vegetación densa. | Raíces colosales entrelazadas, armaduras de caballeros antiguos. | Plataformas verticales; rutas opcionales altas con doble salto. | Segmentos de tronco, raíces, plantas. |
| **Ruinas Abandonadas** | Academia de caballeros arrasada; mármol agrietado y piedra ennegrecida. | Columnas rotas, aulas derrumbadas, estandartes rasgados, torres. | Exploración y combates terrestres. | Columnas, bloques de muro, arcos. |
| **Patio de la Academia** | Suelo de piedra completamente plano entre ruinas. | Restos de estatuas al fondo; sin plataformas; pilares de piedra que emergen en los extremos para cerrar la arena. | Jefe 2. | Reutiliza piezas de las Ruinas como fondo. |
| **Archipiélago de Tierra** | Islas de tierra y roca flotando sobre el vacío; cielo pálido. | Géiseres, raíces colgantes, rocas que caen al vacío. | Exploración aérea con géiseres. | Islas de 3 tamaños, géiser como *prefab*. |
| **Anillo de Islas** | 7 islas de tierra en dos alturas. | Túneles por donde pasa la serpiente. | Jefe 3. | Reutiliza islas del Archipiélago. |
| **Puente e Isla Final** | Cuerpo petrificado de la serpiente; cumbre de mármol bajo un cielo oscuro. | Cañones, islas ascendentes con géiseres, La Entidad a gran escala. | Batalla final. | Reutiliza islas, cañón como *prefab*. |

### Modularidad

- Bloques de suelo con borde superior claro reutilizables en todas las zonas, cambiando solo la paleta.
- *Prefabs* comunes: géiser, punto de control, antesala del mercader, cañón, pilar de las ruinas.
- La silueta de La Entidad es una sola capa de fondo que cambia de escala por zona.

### Iluminación

| Zona | Iluminación |
| --- | --- |
| Costa | Luz diurna nublada y fría. |
| Bosque | Penumbra verde con rayos de luz entre hojas. |
| Ruinas | Atardecer naranja; en la arena del Mago, luz de fuego. |
| Archipiélago | Luz alta y pálida; niebla bajo las islas. |
| Isla Final | Cielo oscuro; La Entidad emite luz propia en sus núcleos. |

### Efectos visuales

- **Agua:** oleaje, salpicaduras, plataforma de agua, ráfaga del Jefe 1.
- **Fuego y magma:** llamaradas, picos de magma, cráneos de fuego.
- **Fuego y magia de Eon:** tajo ardiente (media luna de fuego), piel de piedra de la Escama pétrea.
- **Magia del Mago:** escudo, teletransporte (humo negro).
- **Géiseres:** burbujeo de aviso, columna de vapor y agua.
- **Baba:** gotas verdes y salpicadura al impactar.
- **Petrificación:** grietas grises que recorren el cuerpo de la serpiente.
- **Impactos:** chispas de espada, polvo de aterrizaje, escombros del Earthlem.
- **Clima:** niebla en el Archipiélago; ceniza en las Ruinas.

### Recursos requeridos

- *Tilesets* por zona (Costa, Bosque, Ruinas, Archipiélago, Isla Final).
- 3 capas de *parallax* por zona, más la capa de La Entidad.
- *Prefabs*: géiser, punto de control, antesala del mercader, cañón, plataforma de agua, pilares de las ruinas.
- VFX listados arriba.


---

## Interfaz Visual

### HUD

| Elemento | Posición | Descripción |
| --- | --- | --- |
| Vida | Arriba a la izquierda | Segmentos verdes de 10 HP (10 de base; 13 con Vigor). No se rellena hasta el siguiente punto de control o jefe vencido. |
| Escudo | Sobre la vida | 5 segmentos cian de 10 SP; solo visible con Coraza equipada. |
| XP | Arriba a la izquierda, bajo la vida | Icono dorado y número; se anima al sumar. |
| Habilidades equipadas | Abajo a la izquierda | 3 iconos con su tecla (`J`, `K`) si son activas; las activas muestran su recarga radial. |
| Potenciadores equipados | Abajo a la derecha | 3 iconos pequeños, siempre encendidos (están siempre activos). Sin teclas ni temporizadores. |
| Recarga de dash | Junto a Eon | Pequeño arco que se llena; se oculta si está listo. |
| Barra del jefe | Abajo al centro | Nombre del jefe, barra de vida y marcas de cambio de fase. Solo en arenas. |
| Indicador contextual | Sobre el objeto | Tecla de Interactuar cerca del mercader, un punto de control o un cañón. |
| Indicador fuera de pantalla | Borde de la pantalla | Flecha roja para la embestida de la Serpiente gigante. |

### Jerarquía visual

1. **Avisos de peligro** (instakill y ataques del jefe), siempre por encima de todo.
2. **Vida y escudo.**
3. **Barra del jefe.**
4. **Habilidades y su recarga.**
5. **XP, potenciadores e indicadores contextuales.**

### Estados

| Estado | Representación |
| --- | --- |
| Normal | HUD con opacidad completa. |
| Vida baja (≤ 20 HP) | La barra de vida late en rojo. |
| Daño recibido | Destello rojo de la barra y sacudida leve del HUD. |
| Vida restaurada (punto de control o jefe vencido) | La barra se rellena con un barrido verde. |
| Habilidad en recarga | Icono oscurecido con relleno radial. |
| Ranura vacía | Marco vacío con borde punteado. |
| Acción bloqueada (sin XP en tienda) | Botón en gris y precio en rojo. |

### Inventario

- Dos pestañas: **Habilidades** y **Potenciadores**, cada una con 3 ranuras arriba y la lista de lo obtenido debajo.
- Al seleccionar un elemento, un panel lateral muestra su icono, nombre, **función** y, si la tiene, su **tecla de control** (por ejemplo, *«Tajo ardiente — J: la espada lanza un tajo de fuego…»*; *«Codicia — Pasivo: +25 % de XP obtenida»*).
- Dentro de una arena de jefe se muestra en modo lectura con un candado.

### Convenciones

- **Tipografía:** pixel serif para títulos y nombres de jefe; pixel sans legible para números y texto.
- **Iconografía:** iconos de 32 × 32 con contorno oscuro para leerse sobre cualquier fondo.
- **Tamaños mínimos:** texto de 16 px a 1080p; números del HUD a 20 px.
- **Contraste:** todo elemento del HUD tiene un marco oscuro semitransparente.
- **Animaciones:** entradas y salidas de 0,15 s; los números de XP suben con un pequeño rebote.

### Pantallas

- Menú principal
- Prólogo (cómic)
- Pausa
- Configuración
- **Inventario** (pestañas Habilidades y Potenciadores)
- **Tienda del mercader**
- Entrega de habilidad
- Derrota
- Victoria y créditos


---

## Audio y Música

La música y los efectos acompañan a Eon desde su derrota hasta la revancha: melancolía en la exploración, tensión en los jefes y épica en la isla final.

### Música

**Estilo:** medieval con elementos épicos, melancólicos y de terror cósmico.

**Instrumentación:**

- Violines y violonchelos para momentos emocionales y de tensión.
- Tambores y percusión para combates.
- Flautas y cuerdas suaves para la exploración.
- Coros y sonidos graves para La Entidad.
- Melodías acústicas sencillas para los momentos de esperanza.

**Temas principales:**

| Tema | Uso | Carácter |
| --- | --- | --- |
| Tema de Eon | Menú, prólogo y final (versión triunfal). | Heroico; en el prólogo termina roto. |
| La caída | Página 5 del cómic. | Oscuro y descendente. |
| Costa | Playa y Acantilados. | Melancólico, con sonido de olas. |
| Bosque | Bosque de Raíces. | Misterioso, flautas y cuerdas. |
| Ruinas | Ruinas Abandonadas. | Lento, solitario. |
| Archipiélago | Islas flotantes. | Aéreo, con viento. |
| Jefe 1 | Arena de la Marea. | Percusión rápida con motivos acuáticos. |
| Jefe 2 | Patio de la Academia. | Coros oscuros y órgano. |
| Jefe 3 | Anillo de Islas. | Ritmo pesado y creciente. |
| La revancha | Isla Final. | Tema de Eon reorquestado contra el tema de La Entidad. |
| Antesala | Mercader, antes de cada jefe. | Tranquilo, con tensión creciente. |

**Música dinámica:** sí. Cada jefe tiene una variación más intensa en su segunda fase; la exploración baja de volumen y añade percusión cuando hay enemigos cerca.

### Efectos de sonido

| Evento | Sonido | Propósito |
| --- | --- | --- |
| Caminar | Pasos sobre arena, tierra o piedra | Comunicar el movimiento. |
| Saltar / doble salto | Impulso breve / soplo de aire | Confirmar cada salto. |
| Dash / dash cortante | Corte de aire / tajo metálico | Diferenciar si el dash hace daño. |
| Atacar | Corte de espada y golpe metálico | Comunicar el ataque. |
| Tajo ardiente | Tajo con chisporroteo de fuego | Confirmar el ataque a distancia. |
| Escama pétrea | Crujido de roca; golpe seco en el bloqueo perfecto | Confirmar la defensa y el bloqueo perfecto. |
| Recibir daño | Golpe sordo y quejido | Indicar daño. |
| Recoger XP | Tintineo agudo | Recompensa. |
| Comprar | Campanilla y destello | Confirmar la compra. |
| Equipar potenciador o habilidad | Clic metálico | Confirmar el cambio en el inventario. |
| Punto de control / jefe vencido | Acorde ascendente | Indicar que vida y escudo se restauraron. |
| Géiser | Burbujeo (aviso) y erupción | Anunciar el momento de subir. |
| **Aviso de instakill** | Tono grave exclusivo | Reconocer el peligro sin mirar. |
| Ráfaga de agua | Rugido de agua a presión | Jefe 1. |
| Llamaradas / picos de magma | Silbido y crujido de roca | Jefe 2. |
| Escudo del Mago | Zumbido cristalino | Indicar que no recibe daño. |
| Teletransporte | Soplo de humo | Anunciar dónde reaparece. |
| Gota de baba | Goteo viscoso | Jefe 3. |
| Petrificación | Crujido largo de piedra | Cinemática del Jefe 3. |
| Cañón | Disparo y explosión | Isla Final. |
| Victoria / derrota | Fanfarria breve / música descendente | Resultado. |

### Audio espacial

Se usa paneo estéreo simple (izquierda/derecha) para los avisos de jefe, sobre todo la embestida de la Serpiente gigante que llega desde fuera de pantalla. El resto de los sonidos se reproduce sin atenuación por distancia.

### Voz

- **Narración:** solo texto en esta versión.
- **Diálogos:** texto acompañado de sonidos vocales breves no verbales.
- **Idioma:** español.

### Mezcla

- Prioridad: avisos de instakill > ataques de jefe > daño recibido > ataques del jugador > ambiente > música.
- La música baja durante diálogos e ilustraciones.
- Transiciones suaves entre pistas.


---

## UX y Flujo del Jugador

### Flujo general

```text
Menú principal → Nueva partida → Prólogo (cómic, omitible) → Playa del Despertar
   → Zona → Antesala (mercader + punto de control) → Preparar inventario → Arena de jefe
   → Habilidad guardada en el inventario → Siguiente zona … → Isla Final → Final → Créditos → Menú
   (en cualquier momento tras un jefe: volver a zonas superadas para acumular XP)
```

Continuar lleva directamente al último punto de control guardado.

### Primeros minutos

1. **Prólogo:** el jugador lee o salta el cómic; la última página muestra la derrota de Eon.
2. **Despertar:** control inmediato. Un aviso breve muestra Mover y Saltar.
3. **Primer Aurion:** aparece el aviso de Atacar (`Enter`); al matarlo, los orbes de XP vuelan hacia Eon y el contador del HUD se anima.
4. **Dash:** un hueco que solo se cruza con dash aéreo muestra el aviso de Dash.
5. **Primer punto de control:** un aviso explica que la vida solo se restaura aquí o al vencer a un jefe.
6. **Mercader (antesala del Jefe 1):** el primer diálogo explica que la XP compra potenciadores permanentes y que solo funcionan equipados en el inventario. La primera compra abre el inventario con la pestaña de potenciadores.

Los avisos aparecen una sola vez, en el momento en que se necesitan, y nunca detienen el juego.

### Preparación antes de un jefe

- Cada jefe tiene una antesala con el mercader y un punto de control. Al tocarlo aparece el aviso *«Revisa tu inventario (Tab) antes de entrar»*.
- La entrada a la arena muestra el aviso *«Dentro no podrás cambiar tu equipo»*.
- Si hay ranuras vacías y elementos sin equipar en el inventario, el aviso lo menciona.

### Entrega de una habilidad

1. Muere el jefe; cinemática breve. Vida y escudo se restauran.
2. Ilustración de la habilidad con su nombre, su control y su función.
3. La habilidad **se guarda en el inventario**; no se descarta ninguna. Aviso: *«Abre el inventario (Tab) para equiparla»*.
4. El jugador decide si la equipa y qué deja guardado.

### Inventario

- Al seleccionar una habilidad o un potenciador se muestra siempre su función y, si tiene, su tecla.
- Los potenciadores no se activan: estar equipados basta.
- Se puede cambiar el equipo en cualquier momento fuera de una arena de jefe.

### Derrota y reintento

- Pantalla de derrota con dos opciones: **Reaparecer** (por defecto) y **Salir al menú**.
- Reaparecer lleva al último punto de control con vida y escudo completos. La XP, los potenciadores y las habilidades se conservan.
- Si la derrota fue por instakill, la pantalla muestra una pista breve (*«Sube a la plataforma de agua antes de la ráfaga»*, *«Evita la cabeza: es letal»*), solo las 2 primeras veces.

### Navegación del mundo

- Las rutas opcionales muestran una pista visual de lo que piden (saliente alto, interruptor lejano).
- La Entidad en el horizonte marca la dirección general del avance.
- Las zonas superadas siguen abiertas y sus enemigos reaparecen.


---

## UI y Menús

### Mapa de navegación

```text
Menú principal
├── Nueva partida (confirmación si hay guardado)
├── Continuar
├── Configuración
│   ├── Audio (general, música, efectos)
│   ├── Video (resolución, pantalla completa)
│   └── Controles (vista del mapa de controles)
├── Créditos
└── Salir

En juego
├── Pausa (Escape / Start)
│   ├── Reanudar
│   ├── Volver al último punto de control
│   ├── Configuración
│   └── Salir al menú (confirmación)
├── Inventario (Tab / View)
│   ├── Habilidades
│   └── Potenciadores
└── Tienda (E junto al mercader, en la antesala de cada jefe)
```

### Pantallas

| Pantalla | Propósito | Elementos | Acciones |
| --- | --- | --- | --- |
| Menú principal | Entrar al juego. | Logo, ilustración de fondo con La Entidad, opciones. | Nueva partida, Continuar, Configuración, Créditos, Salir. |
| Prólogo | Contar la caída de Eon. | Viñetas del cómic; indicador de «mantener para omitir». | Avanzar, omitir. |
| Inventario — Habilidades | Elegir qué 3 habilidades usar. | 3 ranuras arriba; lista de todas las habilidades obtenidas; candado en las no obtenidas. Panel con icono, nombre, **control** y **función** de la seleccionada. | Equipar, quitar, intercambiar. En arenas de jefe, solo lectura. |
| Inventario — Potenciadores | Elegir qué 3 potenciadores tener activos. | 3 ranuras arriba; lista de potenciadores comprados. Panel con icono, nombre y **función** (indica «Pasivo: siempre activo mientras esté equipado»). | Equipar, quitar, intercambiar. En arenas de jefe, solo lectura. |
| Tienda | Cambiar XP por potenciadores. | XP actual; catálogo con icono, función y precio; marca «Adquirido» en los ya comprados; retrato y frase del mercader. | Comprar, salir. |
| Entrega de habilidad | Presentar la habilidad nueva. | Ilustración, nombre, control y función; aviso de que se guardó en el inventario. | Continuar, abrir inventario. |
| Pausa | Detener el juego. | Opciones. | Ver mapa de navegación. |
| Derrota | Reintentar. | Mensaje, pista opcional. | Reaparecer, Salir al menú. |
| Victoria | Cerrar la historia. | Ilustración final. | Continuar a créditos. |
| Créditos | Reconocer al equipo. | Nombres del equipo y herramientas. | Omitir. |

### Confirmaciones

| Acción | Confirmación |
| --- | --- |
| Nueva partida con guardado existente | *«Se borrará tu progreso. ¿Continuar?»* |
| Salir al menú desde la pausa | *«Volverás al último punto de control al continuar. ¿Salir?»* |
| Compra en la tienda | *«¿Comprar [potenciador] por [precio] XP?»* (la compra es permanente). |


---

## Accesibilidad

| Área | Medida | Estado |
| --- | --- | --- |
| Visual | Todo aviso de ataque combina color, forma (sombra o círculo) y sonido; no depende solo del color. | Diseño |
| Visual | El aviso de instakill usa un color y un sonido exclusivos. | Diseño |
| Visual | Texto mínimo de 16 px a 1080p con fondo oscuro. | Diseño |
| Auditivo | Volumen separado de música y efectos. | Planeado |
| Auditivo | Avisos sonoros importantes con equivalente visual (flecha en el borde para la embestida de la serpiente). | Diseño |
| Motora | *Buffer* de entrada de 0,1 s y *coyote time*. | Diseño |
| Motora | Dos teclas para Salto (`Espacio`/`W`). | Diseño |
| Motora | Juego completo con teclado o con mando. | Diseño |
| Motora | Los potenciadores no exigen pulsaciones: funcionan siempre equipados. | Diseño |
| Cognitiva | El inventario describe la función y el control de cada habilidad y potenciador. | Diseño |
| Cognitiva | Avisos de tutorial contextuales, una sola vez y sin detener el juego. | Diseño |
| Cognitiva | Pista tras una derrota por instakill (las 2 primeras veces). | Diseño |
| Cognitiva | El prólogo y los diálogos se pueden omitir. | Diseño |

**Fuera de alcance en esta versión:** reasignación libre de teclas, modo de dificultad reducida, lectura de pantalla y desactivar la sacudida de cámara (la sacudida es fija y no configurable).


---

## Guardado y Configuración

### Guardado de partida

- **Tipo:** guardado automático en una sola ranura.
- **Cuándo se guarda:** al tocar un punto de control, al derrotar a un jefe, al comprar en la tienda y al cambiar el inventario.
- **Qué se guarda:**
    - Punto de control actual (zona y posición).
    - XP.
    - Habilidades obtenidas y cuáles están equipadas.
    - Potenciadores comprados y cuáles están equipados.
    - Jefes derrotados.
    - Diálogos y avisos de tutorial ya vistos.
    - Regalo del mercader entregado (sí/no).
- **Qué no se guarda:** vida y escudo actuales (al cargar, Eon empieza en un punto de control con ambos completos) ni la posición de los enemigos (reaparecen).

### Configuración

| Opción | Valores | Se guarda |
| --- | --- | --- |
| Volumen general, música, efectos | 0–100 | Sí |
| Resolución | 1280 × 720, 1920 × 1080, 2560 × 1440 | Sí |
| Pantalla completa | Sí / No | Sí |

La sacudida de cámara no es configurable.

### Casos especiales

- **Nueva partida con guardado existente:** confirmación; al aceptar se borra la ranura.
- **Cerrar durante una arena de jefe:** al continuar se reaparece en el punto de control de la antesala.
- **Cerrar durante la entrega de habilidad:** la habilidad ya cuenta como obtenida.
- **Archivo dañado:** se descarta y se ofrece empezar una partida nueva, avisando al jugador.


---

## Arquitectura Técnica

Arquitectura **propuesta** para Unity. Los nombres de componentes son una guía; se actualizan cuando existan en el proyecto.

### Escenas

| Escena | Contenido |
| --- | --- |
| `MainMenu` | Menú principal y configuración. |
| `Prologue` | Cómic del prólogo. |
| `Zone_Costa` | Playa del Despertar, Acantilados y Arena de la Marea (Jefe 1). |
| `Zone_Bosque` | Bosque de Raíces. |
| `Zone_Ruinas` | Ruinas Abandonadas y Patio de la Academia (Jefe 2). |
| `Zone_Archipielago` | Archipiélago de Tierra y Anillo de Islas (Jefe 3). |
| `Zone_IslaFinal` | Puente de la Serpiente e Isla Final (La Entidad). |
| `Credits` | Final y créditos. |

Una escena persistente (`Bootstrap`) contiene los servicios globales que no se destruyen entre zonas.

### Componentes

| Responsabilidad | Componentes propuestos |
| --- | --- |
| Servicios globales | `GameManager`, `SceneLoader`, `SaveService`, `AudioManager` |
| Jugador | `PlayerInputReader`, `PlayerMotor`, `PlayerCombat`, `PlayerHealth`, `PlayerAbilities` |
| Habilidades | `AbilityDefinition` (ScriptableObject), `DoubleJumpAbility`, `FireSlashAbility`, `DashStrikeAbility`, `StoneScaleAbility` |
| Inventario | `Inventory`, `AbilityLoadout` (3 ranuras), `PowerUpLoadout` (3 ranuras), `ItemDescriptionPanel` |
| Potenciadores | `PowerUpDefinition` (ScriptableObject), `StatModifiers` (aplica los modificadores pasivos de los potenciadores equipados) |
| Economía | `XPWallet`, `XPOrb`, `ShopController`, `ShopCatalog` |
| Combate | `Hitbox`, `Hurtbox`, `DamageInfo` (incluye `isInstakill`), `Health` |
| Enemigos | `EnemyBrain`, `AurionAI`, `EarthlemAI`, `VestigioAI`, `EnemyPool` |
| Jefes | `BossController`, `BossAttack` (ScriptableObject), `ShrimpSerpentBoss`, `DarkMageBoss`, `GiantSerpentBoss`, `EntityBoss` |
| Mundo | `WorldProgress`, `Checkpoint`, `AbilityGate`, `BossArena` (barreras invisibles o pilares), `Geyser`, `Cannon`, `WaterPlatform`, `RuinPillar`, `EnemyRespawner` |
| Cámara | `CameraDirector` (Cinemachine 2D + confinadores) |
| UI | `HUD`, `InventoryView`, `ShopView`, `BossHealthBar`, `PauseMenu`, `DialogueBox`, `ComicPlayer` |

### Principios

- **Datos en ScriptableObjects:** habilidades, potenciadores, ataques de jefe y valores de enemigos se editan sin tocar código.
- **Eventos:** daño, muerte, compra y entrega de habilidad se comunican por eventos (`OnEntityDeath`, `OnAbilityGranted`, `OnXPChanged`).
- **Reservas (*pools*):** tajos ardientes, orbes de XP, gotas de baba, camaroncitos y cráneos se reutilizan.
- **Separación lógica/presentación:** las reglas de combate no dependen de animaciones ni VFX.


---

## Motor y Herramientas

| Área | Herramienta | Uso |
| --- | --- | --- |
| Motor | Unity (Editor y Runtime), 2D | Juego completo. |
| Lenguaje | C# | Lógica de juego. |
| Entrada | Unity Input System | Teclado y mandos con un solo mapa de acciones. |
| Cámara | Cinemachine 2D | Seguimiento, confinadores y sacudida. |
| Físicas | Rigidbody2D / Collider2D | Movimiento y colisiones. |
| Escenarios | Tilemap de Unity | Construcción de zonas. |
| Arte | Clip Studio Paint | Sprites, animaciones e ilustraciones. |
| Audio | *Pendiente de definir* | Música y efectos. |
| Control de versiones | Git + GitHub | Código y GDD (https://github.com/adrielisa/GDD). |
| Documentación | Obsidian | Este GDD. |
| Apoyo | Claude | Productividad, revisión y auditoría de código y documentación. |


---

## Requisitos Técnicos

### Rendimiento

| Métrica | Objetivo |
| --- | --- |
| Tasa de fotogramas | 60 FPS estables a 1920 × 1080. |
| Carga entre zonas | Menos de 5 s. |
| Latencia de entrada | Respuesta en el mismo fotograma o el siguiente. |
| Objetos activos | Hasta 6 camaroncitos, 4 cráneos, 6 gotas de baba y ~20 orbes de XP sin caída de FPS. |

### Equipo mínimo orientativo

| Componente | Mínimo |
| --- | --- |
| Sistema operativo | Windows 10 (64 bits) |
| Procesador | Doble núcleo a 2,0 GHz |
| Memoria | 4 GB de RAM |
| Gráficos | Compatible con DirectX 11 |
| Almacenamiento | 500 MB libres |

*Valores orientativos; se confirman con pruebas de rendimiento.*

### Restricciones

- Sin conexión a internet.
- Guardado local.
- Un solo jugador.


---

## Datos y Persistencia

### Formato

- Archivo JSON en `Application.persistentDataPath/truehero_save.json`.
- Campo `version` para migrar formatos futuros.
- La configuración se guarda aparte en `PlayerPrefs`.

### Estructura del guardado

```json
{
  "version": 1,
  "checkpointId": "costa_antesala_jefe1",
  "xp": 340,
  "abilitiesOwned": ["double_jump"],
  "abilitiesEquipped": ["double_jump", null, null],
  "powerUpsOwned": ["vigor", "codicia"],
  "powerUpsEquipped": ["vigor", "codicia", null],
  "bossesDefeated": ["shrimp_serpent"],
  "tutorialsSeen": ["move", "attack", "dash", "shop"],
  "sellerGiftGiven": false
}
```

### Datos de diseño (ScriptableObjects)

| Asset | Campos principales |
| --- | --- |
| `AbilityDefinition` | id, nombre, función (texto del inventario), tecla de control, icono, tipo (pasiva/activa), recarga, daño. |
| `PowerUpDefinition` | id, nombre, función (texto del inventario), icono, modificadores, precio, antesala de desbloqueo. |
| `EnemyDefinition` | vida, velocidad, daño, detección, XP, probabilidades de orbe. |
| `BossAttack` | aviso, duración, daño, `isInstakill`, recarga, fase mínima, peso. |
| `BossDefinition` | vida, umbrales de fase, ataques, XP, habilidad que entrega. |

### Validación

- Identificadores desconocidos se ignoran.
- XP limitada a 0–9999.
- Nunca más de 3 habilidades ni 3 potenciadores equipados; si el archivo trae más, se conservan los 3 primeros.
- Solo se pueden equipar elementos que figuran como obtenidos o comprados.


---

## Seguridad y Riesgos Técnicos

| Riesgo | Probabilidad | Impacto | Mitigación |
| --- | --- | --- | --- |
| La Serpiente gigante (cuerpo segmentado que atraviesa plataformas) es compleja de programar. | Alta | Alto | Prototipar primero con segmentos que siguen un camino (*path following*); limitar a ~18 segmentos. |
| Ataques instakill percibidos como injustos. | Media | Alto | Aviso mínimo de 1,5 s, color y sonido exclusivos; pruebas con jugadores nuevos. |
| Que un jefe o la ruta principal exijan sin querer una habilidad concreta. | Media | Alto | La ruta principal y cada jefe se prueban sin habilidades equipadas; las `AbilityGate` solo se usan en rutas opcionales. |
| Modificadores de potenciadores aplicados dos veces al reequipar. | Media | Medio | `StatModifiers` recalcula los valores desde la base cada vez que cambia el equipo. |
| Alcance: 4 jefes y 5 zonas para un equipo de 5. | Alta | Alto | Vertical slice primero (Costa + Jefe 1); zonas con módulos reutilizables. |
| Ola de picos de magma imposible de esquivar si Eon está ralentizado. | Baja | Medio | La zona segura del extremo siempre existe; la ola nunca se lanza si Eon está pegado al muro del mago. |
| Daño registrado dos veces en un fotograma. | Media | Medio | Lista de objetivos ya golpeados por *hitbox* activa. |
| Guardado corrupto. | Baja | Alto | Escribir en archivo temporal y reemplazar; validación al cargar. |
| Rendimiento con muchos proyectiles y tajos. | Baja | Medio | *Pools* y límites de objetos simultáneos. |


---

## Alcance

### Dentro del alcance

- Prólogo en cómic de 5 páginas con la derrota de Eon.
- 5 zonas explorables (Playa, Acantilados, Bosque, Ruinas, Archipiélago) y la Isla Final, con rutas opcionales.
- 3 jefes normales (Camarón serpiente, Mago oscuro, Serpiente gigante) y La Entidad.
- 3 enemigos comunes (Aurion, Earthlem, Vestigio), con reaparición, y los camaroncitos del Jefe 1.
- 4 habilidades con 3 ranuras; 6 potenciadores permanentes con 3 ranuras.
- XP como recurso de intercambio y tienda del mercader en la antesala de cada jefe.
- Inventario con descripción de función y control de cada elemento.
- Géiseres, puntos de control, cañones y pilares de las ruinas.
- Ilustración de la serpiente petrificada.
- Guardado local de una ranura.
- Teclado y mando.

### Fuera del alcance

- Aliados, acompañantes o rescate de personajes.
- Objetos de curación o de escudo.
- Objetos que recoger aparte de la XP.
- Compra de armas o cambio de espada.
- Subida de nivel del personaje.
- Multijugador.
- Reasignación libre de controles.
- Voces habladas.
- Otros continentes como zonas jugables.

### Entregables por prioridad

| Prioridad | Entregable |
| --- | --- |
| **P0 — Vertical slice** | Playa + Acantilados + antesala con mercader + Jefe 1 + inventario + Doble salto. |
| **P1** | Bosque + Ruinas + Jefe 2 + Vestigio + Tajo ardiente y Dash cortante. |
| **P2** | Archipiélago + géiseres + Jefe 3 + Escama pétrea + cinemática de petrificación. |
| **P3** | Isla Final + La Entidad + final y créditos. |
| **P4 (si hay tiempo)** | Desafío «Sin rasguños», pulido de VFX, música dinámica por fases. |


---

## Roles y Responsabilidades

| Integrante | Rol | Responsabilidades |
| --- | --- | --- |
| González Cruz Celeste | Responsable del proyecto | Coordinación, prioridades y aprobación de cambios en el GDD. |
| García Velázquez Marco Damián | *Por asignar* | — |
| Rodríguez Pacheco Adriel Isaí | *Por asignar* | — |
| Trujillo Torres Sergio Joel | *Por asignar* | — |
| Vargas Pérez Joel | *Por asignar* | — |

### Áreas que necesitan responsable

| Área | Incluye |
| --- | --- |
| Programación de jugador y combate | Controlador, habilidades, daño. |
| Programación de enemigos y jefes | IA de enemigos comunes y de los 4 jefes. |
| Sistemas y UI | Inventario, tienda, HUD, menús, guardado. |
| Arte de personajes | Eon, jefes, enemigos, animaciones. |
| Arte de entornos e ilustraciones | Tilesets, fondos, cómic, cinemáticas. |
| Audio | Música y efectos. |
| Diseño y documentación | GDD, balance, pruebas. |


---

## Roadmap

Hitos en orden. No se fijan fechas que el equipo no haya acordado; cada hito se marca al cumplirse.

| Hito | Contenido | Criterio para darlo por cumplido |
| --- | --- | --- |
| 0. Documentación | GDD 0.2.0 con la estructura de jefes, XP, habilidades y potenciadores. | Aprobado por el equipo. (Redactado el 07/11/2026; pendiente de aprobación.) |
| 1. Prototipo de control | Movimiento, salto, dash, combo, ataque descendente. | Se siente bien en una sala gris. |
| 2. Prototipo de sistemas | Daño, XP, tienda, inventario con 3 ranuras de habilidad y 3 de potenciador. | Se compra y se equipa un potenciador, y su efecto se aplica. |
| 3. Vertical slice | Playa + Acantilados + Jefe 1 + Doble salto. | Se juega de principio a fin sin errores bloqueantes. |
| 4. Bloque 2 | Bosque, Ruinas, Vestigio, Jefe 2. | Jefe 2 derrotable y entrega 2 habilidades. |
| 5. Bloque 3 | Archipiélago, géiseres, Jefe 3, petrificación. | Puente a la Isla Final funcional. |
| 6. Final | La Entidad, final, créditos. | Juego completo jugable. |
| 7. Pulido y pruebas | Balance, VFX, audio, accesibilidad. | Criterios de [[04 - Criterios de Aceptación]] cumplidos. |


---

## Backlog del Proyecto

| ID | Tarea | Área | Prioridad | Hito | Estado |
| --- | --- | --- | --- | --- | --- |
| B-01 | Controlador de Eon (mover, salto variable, *coyote*, *buffer*) | Programación | P0 | 1 | Pendiente |
| B-02 | Dash con invulnerabilidad y recarga | Programación | P0 | 1 | Pendiente |
| B-03 | Combo de espada (`Enter`) y ataque descendente con rebote | Programación | P0 | 1 | Pendiente |
| B-04 | Sistema de daño con escudo e instakill; restauración solo en puntos de control y jefes | Programación | P0 | 2 | Pendiente |
| B-05 | XP: orbes, contador y atracción | Programación | P0 | 2 | Pendiente |
| B-06 | Tienda del mercader (compra única, «Adquirido») | Programación / UI | P0 | 2 | Pendiente |
| B-07 | Inventario: 3 ranuras de habilidad + 3 de potenciador, con panel de función y control | Programación / UI | P0 | 2 | Pendiente |
| B-08 | 6 potenciadores pasivos como ScriptableObjects y `StatModifiers` | Programación | P0 | 2 | Pendiente |
| B-09 | IA de Aurion y reaparición de enemigos | Programación | P0 | 3 | Pendiente |
| B-10 | Jefe 1: ataques, camaroncitos, plataforma de agua y ráfaga; límites invisibles | Programación | P0 | 3 | Pendiente |
| B-11 | Habilidad Doble salto | Programación | P0 | 3 | Pendiente |
| B-12 | Tilesets y fondos de la Costa | Arte | P0 | 3 | Pendiente |
| B-13 | Sprites y animaciones de Eon | Arte | P0 | 3 | Pendiente |
| B-14 | Sprites del Jefe 1 y camaroncitos | Arte | P0 | 3 | Pendiente |
| B-15 | Cómic del prólogo (5 páginas) | Arte | P0 | 3 | Pendiente |
| B-16 | Puntos de control y guardado | Programación | P0 | 3 | Pendiente |
| B-17 | IA de Earthlem y Vestigio | Programación | P1 | 4 | Pendiente |
| B-18 | Jefe 2: llamaradas, picos, escudo, cráneos, teletransporte; pilares de las ruinas | Programación | P1 | 4 | Pendiente |
| B-19 | Tajo ardiente (`J`) y Dash cortante | Programación | P1 | 4 | Pendiente |
| B-20 | Géiseres | Programación | P2 | 5 | Pendiente |
| B-21 | Jefe 3: cuerpo segmentado, baba, cabeza instakill | Programación | P2 | 5 | Pendiente |
| B-22 | Escama pétrea (`K`): reducción, bloqueo perfecto y aturdimiento | Programación | P2 | 5 | Pendiente |
| B-23 | Ilustración de la serpiente petrificada | Arte | P2 | 5 | Pendiente |
| B-24 | La Entidad: fases, cañones, Vestigios | Programación | P3 | 6 | Pendiente |
| B-25 | **Cerrar el diseño de la fase 3 de La Entidad** | Diseño | P2 | 5 | Pendiente |
| B-26 | Nombres de los jefes, camaroncitos y Vestigio | Diseño | P2 | 5 | Pendiente |
| B-27 | Música por zona y jefe | Audio | P1 | 4–6 | Pendiente |
| B-28 | Menús, pausa y configuración | UI | P1 | 7 | Pendiente |


---

## Gestión de Cambios

### Proceso

1. **Propuesta:** quien quiera cambiar algo del diseño lo describe en una línea: qué cambia, por qué y qué secciones del GDD afecta.
2. **Revisión:** se comprueba contra los [[04 - Pilares de Diseño]] y el [[01 - Alcance]].
3. **Decisión:** la responsable del proyecto aprueba o rechaza.
4. **Registro:** se anota en [[03 - Registro de Decisiones]] y se actualizan las páginas afectadas.
5. **Versión:** se sube la versión del GDD en [[04 - Historial de Versiones]].

### Cambios aplicados en la versión 0.2.0

| Cambio | Antes | Ahora | Secciones afectadas |
| --- | --- | --- | --- |
| Inicio del juego | Prólogo jugable con la derrota frente a La Entidad. | El juego empieza tras la derrota; se cuenta en el cómic. La batalla original pasa a ser la fase 1 de la isla final. | Visión, Trama, Niveles, Diálogos |
| Objetivo de Eon | Reunir sobrevivientes y aliados. | Derrotar 3 jefes para recuperar habilidades y vencer a La Entidad. | Visión, Trama, Personajes, Misiones |
| Economía | — | XP para cambiar por potenciadores con el mercader. | Economía, Objetos, Enemigos, UI |
| Habilidades | No existían. | Habilidades de jefes con 3 ranuras. | Mecánicas, Sistemas, Progresión |
| Cruce entre islas | Trampolines. | Géiseres. | Mecánicas, Entornos, Niveles |
| Enemigos | Aurion, Driller, Earthlem. | Aurion, Earthlem, Vestigio. Driller descartado. | Enemigos, Arte |
| Mundo | Niveles lineales. | Zonas explorables. | Estructura, Niveles |

### Cambios aplicados en la versión 0.2.1

| Cambio | Antes (0.2.0) | Ahora | Secciones afectadas |
| --- | --- | --- | --- |
| Potenciadores | Consumibles con ranuras rápidas y botones. | Permanentes y pasivos: activos siempre mientras están equipados (3 ranuras). Sin controles. | Mecánicas, Economía, Objetos, Controles, UI |
| Curación y escudo | Orbes y potenciadores de curación y escudo. | No existen: vida y escudo se restauran solo en puntos de control y al vencer a un jefe. | Mecánicas, Economía, Reglas, Objetos |
| Objetos del mapa | Había objetos que recoger en las zonas. | Eliminados por completo. Solo se obtiene XP. | Objetos, Niveles, Misiones, Economía |
| Ataque arcano | Orbe mágico. | **Tajo ardiente**: tajo de fuego lanzado por la espada. | Mecánicas, Objetos, Arte, Audio |
| Habilidad del Jefe 3 | Pendiente. | **Escama pétrea**. | Mecánicas, Objetos, Enemigos |
| Habilidades nuevas | Al llenar ranuras había que elegir cuál dejar fuera. | Ninguna se descarta: todas se guardan y el jugador elige cuáles equipar. Ninguna es obligatoria. | Mecánicas, Sistemas, UX |
| Controles | Ataque `J`, dash `Shift`/`K`, potenciadores `1`/`2`/`3`. | Ataque `Enter`, Tajo ardiente `J`, Escama pétrea `K`, dash `Shift`. Sin teclas de potenciador. | Controles, Mecánicas |
| Inventario | — | Muestra la función y el control de cada habilidad y potenciador. | Sistemas, UI |
| Sacudida de cámara | Configurable. | Fija; no se puede desactivar. | Sistemas, Accesibilidad, Configuración |
| Mercader | Varias ubicaciones desde la Playa. | Aparece por primera vez antes del Jefe 1 y después antes de cada jefe. | NPC, Niveles, UX |
| Reaparición | — | Los enemigos comunes reaparecen; se puede volver a zonas superadas para acumular XP. | Economía, Niveles, Sistemas |
| Límites de arena | Barreras genéricas. | Invisibles, salvo en el Jefe 2 (pilares de las ruinas). | Sistemas, Niveles, Enemigos |


---

## Criterios de Calidad

| Área | Criterio |
| --- | --- |
| Control | Toda entrada responde en el mismo fotograma o el siguiente; el dash cancela la recuperación del ataque. |
| Legibilidad | Todo ataque hostil tiene un aviso visible de al menos 0,4 s; los instakill, de al menos 1,5 s con color y sonido exclusivos. |
| Justicia | Cada ataque de jefe se puede evitar sin ninguna habilidad concreta equipada. |
| Vida | La distancia entre puntos de control es razonable, porque no hay curación en el campo. |
| Progresión | La ruta principal se completa sin habilidades concretas; cada habilidad abre al menos una ruta opcional o cambia la forma de pelear. |
| Economía | Un jugador que pelea con normalidad puede comprar al menos un potenciador en cada antesala. |
| Inventario | Cada habilidad y potenciador muestra su función y, si lo tiene, su control. |
| Rendimiento | 60 FPS estables en el equipo mínimo. |
| Estabilidad | Sin errores que bloqueen el avance ni pérdidas de guardado. |
| Arte | Siluetas legibles sobre todos los fondos; suelo pisable siempre distinguible. |
| Audio | Los avisos de peligro se oyen por encima de la música. |
| Coherencia | Lo implementado coincide con este GDD o el cambio está registrado. |


---

## Pruebas

### Tipos de prueba

| Tipo | Qué se prueba | Cuándo |
| --- | --- | --- |
| Funcional | Cada mecánica y sistema según [[02 - Mecánicas]] y [[03 - Sistemas]]. | Al terminar cada tarea del backlog. |
| Jefes | Que cada ataque se pueda esquivar sin habilidades concretas y que las fases cambien en su umbral. | Al terminar cada jefe. |
| Progresión | Que la ruta principal se complete sin ninguna habilidad equipada. | Al terminar cada bloque. |
| Economía | XP obtenida por zona frente a precios; reaparición de enemigos. | Hitos 3 a 6. |
| Guardado | Cerrar y reabrir en cada situación de [[04 - Guardado y Configuración]]. | Hitos 3 y 7. |
| Jugadores nuevos | Personas que no conocen el juego juegan sin ayuda. | Vertical slice y versión final. |
| Rendimiento | FPS con el máximo de objetos activos. | Hito 7. |

### Casos de prueba clave

| ID | Caso | Resultado esperado |
| --- | --- | --- |
| T-01 | Comprar un potenciador con XP justa. | XP en 0; el potenciador aparece en el inventario y como «Adquirido» en la tienda. |
| T-02 | Equipar un potenciador. | Su efecto se aplica de inmediato y permanece activo sin pulsar nada. |
| T-03 | Quitar y volver a equipar Vigor varias veces. | La vida máxima vuelve a 130, nunca más. |
| T-04 | Obtener la cuarta habilidad con 3 equipadas. | Se guarda en el inventario; ninguna se descarta. |
| T-05 | Abrir el inventario dentro de una arena. | Se muestra en modo lectura. |
| T-06 | Seleccionar cada habilidad y potenciador en el inventario. | Se muestra su función y, si la tiene, su tecla. |
| T-07 | Recibir daño y seguir explorando. | La vida no se recupera hasta tocar un punto de control. |
| T-08 | Vencer a un jefe con poca vida. | Vida y escudo se restauran al terminar el combate. |
| T-09 | Recibir la ráfaga del Jefe 1 con escudo. | Derrota (instakill). |
| T-10 | Subir a la plataforma de agua antes de la ráfaga. | Sin daño. |
| T-11 | Escapar de la ola de picos corriendo hacia el extremo. | Sin daño al llegar a la zona segura junto al pilar. |
| T-12 | Tocar la cabeza de la serpiente durante un dash o con Escama pétrea. | Derrota (instakill). |
| T-13 | Bloqueo perfecto con Escama pétrea contra el barrido del Earthlem. | Sin daño; Earthlem aturdido 1 s. |
| T-14 | Volver a una zona superada tras vencer a su jefe. | Los enemigos han reaparecido y dan XP. |
| T-15 | Entrar a cada arena de jefe e intentar salir. | Límite invisible en los Jefes 1 y 3 y La Entidad; pilares visibles en el Jefe 2. |
| T-16 | Ser derrotado con 500 XP. | Reaparece en el punto de control con 500 XP, vida y escudo completos. |


---

## Bugs y Seguimiento

### Clasificación

| Severidad | Definición | Ejemplo |
| --- | --- | --- |
| Crítica | Bloquea el avance o pierde el guardado. | Una arena no se abre al morir el jefe. |
| Alta | Rompe una mecánica principal. | El doble salto no funciona equipado. |
| Media | Afecta la experiencia, con solución alternativa. | Un potenciador no muestra su descripción en el inventario. |
| Baja | Visual o de texto. | Un icono desalineado. |

### Formato de registro

| ID | Fecha | Severidad | Descripción | Pasos para reproducir | Responsable | Estado |
| --- | --- | --- | --- | --- | --- | --- |
| — | — | — | *Sin bugs registrados aún.* | — | — | — |

### Pendientes de diseño (no son bugs)

| Tema | Detalle |
| --- | --- |
| Fase 3 de La Entidad | Cerrar ataques y valores. |
| Nombres | Jefes, camaroncitos y Vestigio. |
| Valores de La Entidad | Ajustar con el encuentro ya diseñado. |


---

## Criterios de Aceptación

| Parte | Comportamiento esperado |
| --- | --- |
| Inicio | Prólogo omitible que termina con la derrota de Eon; control inmediato en la Playa. |
| Movimiento | Salto variable, *coyote time*, *buffer*, dash de 0,20 s con invulnerabilidad (excepto instakill) y 1 dash aéreo. |
| Combate | Combo de 3 tajos con `Enter`, ataque descendente con rebote, retroceso e *hitstop*. |
| Daño | Escudo antes que vida; instakill ignora escudo, dash y Escama pétrea. |
| Vida y escudo | Solo se restauran en puntos de control, al vencer a un jefe y al reaparecer. |
| XP | Orbes atraídos a 3 u; contador del HUD exacto; tope 9999; se conserva al morir. |
| Tienda | Mercader en cada antesala desde el Jefe 1; compra única; catálogo que crece por antesala; regalo antes de la Isla Final. |
| Inventario | 3 ranuras de habilidad y 3 de potenciador; descripción de función y control; cambios bloqueados dentro de arenas. |
| Potenciadores | 6 tipos, permanentes, siempre activos mientras están equipados; sin controles. |
| Habilidades | Doble salto, Tajo ardiente (`J`), Dash cortante y Escama pétrea (`K`) funcionan solo equipados; ninguna se descarta. |
| Enemigos | Aurion, Earthlem y Vestigio con sus ataques, defensas, avisos y XP; reaparecen. |
| Jefe 1 | Camaroncitos, embestida, mordida y ráfaga instakill siempre precedida de una plataforma de agua; límites invisibles; entrega Doble salto. |
| Jefe 2 | Arena plana cerrada por pilares; llamaradas, ola de picos con zona segura, escudo, cráneos y teletransporte al extremo opuesto; entrega Tajo ardiente y Dash cortante. |
| Jefe 3 | Cuerpo dañable, cola débil, lluvia de baba, cabeza instakill; límites invisibles; entrega Escama pétrea; petrificación y puente al morir. |
| La Entidad | Fases según [[03 - Enemigos y NPC]]; cañones funcionales; límites invisibles; victoria lleva a créditos. |
| Géiseres | Ciclo de reposo, aviso y erupción; lanzamiento al destino correcto. |
| Guardado | Todo lo listado en [[04 - Guardado y Configuración]] se conserva. |
| Progresión | La ruta principal y todos los jefes se completan sin ninguna habilidad concreta. |


---

## Glosario

| Término | Definición |
| --- | --- |
| **Eon** | Protagonista; el héroe profetizado que perdió contra La Entidad. |
| **La Entidad** | Titán cósmico, jefe final. |
| **Vestigio** | Enemigo común sin rostro, blanco, con forma parecida a La Entidad (nombre provisional). |
| **Camaroncitos** | Esbirros voladores del Jefe 1 (sin nombre definitivo). |
| **XP (puntos de experiencia)** | Recurso que sueltan los enemigos; se cambia por potenciadores. No sube niveles. |
| **Potenciador** | Mejora pasiva permanente que se compra con XP. Está siempre activa mientras ocupa una de las 3 ranuras de potenciador. |
| **Habilidad** | Acción o mejora permanente que entrega un jefe; solo funciona equipada (3 ranuras). Ninguna se descarta. |
| **Pasiva / activa** | Una habilidad pasiva modifica una acción existente; una activa tiene tecla propia (`J`, `K`). |
| **Tajo ardiente** | Ataque arcano: la espada lanza un tajo de fuego a distancia. |
| **Escama pétrea** | Petrificación defensiva con bloqueo perfecto. |
| **Instakill** | Ataque que derrota a Eon al instante sin importar escudo, dash o Escama pétrea. |
| **Géiser** | Elemento que lanza a Eon de una isla a otra; sustituye a los trampolines. |
| **Punto de control** | Lugar donde se guarda, se restauran vida y escudo, y se reaparece. |
| **Antesala** | Zona segura antes de cada jefe, con el mercader y un punto de control. |
| **Arena de jefe** | Espacio cerrado (con límites invisibles o pilares) donde se combate a un jefe; el equipo queda fijo. |
| **Ventana de castigo** | Momento tras un ataque en que el jefe queda expuesto. |
| **Fragmento** | Parte del poder de Eon absorbida por un jefe; al vencerlo vuelve como habilidad. |
| ***Coyote time*** | Margen breve para saltar después de salir de un borde. |
| ***Buffer* de entrada** | Margen breve en que una pulsación se guarda y se ejecuta al quedar libre. |
| ***Hitbox* / *hurtbox*** | Zona que hace daño / zona que recibe daño. |
| ***Hitstop*** | Pausa mínima al conectar un golpe para dar impacto. |
| ***I-frames*** | Fotogramas de invulnerabilidad. |
| **Kastleland** | Continente donde transcurre el juego. |
| **Eretz** | Planeta del juego. |


---

## Referencias e Inspiración

| Referencia | Tipo | Qué nos interesa | Qué NO queremos copiar |
| --- | --- | --- | --- |
| *Hollow Knight* | Videojuego | Habilidades de movimiento que abren zonas; amuletos con ranuras limitadas; legibilidad de jefes. | Su escala de mapa y su dificultad de plataformas. |
| *Terraria* — Devorador de mundos | Videojuego (jefe) | Jefe segmentado que atraviesa el escenario; cuerpo dañable por partes. | Su división en gusanos más pequeños. |
| *Blasphemous* | Videojuego | Pixel art detallado, tono de mundo caído. | Su violencia gráfica. |
| *Gurren Lagann* | Anime | Escala colosal y energía de revancha. | Su estética mecánica. |
| *Celeste* | Videojuego | Respuesta del control, *coyote time* y *buffer*. | — |
| *Cuphead* | Videojuego | Jefes con patrones claros y fases. | La dificultad extrema. |

### Referencias visuales

![[Pasted image 20261016112525.png|267]]

> [!warning] Propiedad intelectual
> Una referencia sirve para analizar y comunicar una idea. No implica que el proyecto pueda copiar recursos protegidos.


---

## Registro de Decisiones

Decisiones vigentes a partir de la versión 0.2.1 (07/11/2026).

| # | Área | Decisión | Motivo |
| --- | --- | --- | --- |
| D-01 | Historia | El juego empieza después de la derrota de Eon; la derrota se cuenta en el cómic. | Eon ya perdió y va por su revancha. |
| D-02 | Historia | No hay aliados, sobrevivientes que rescatar ni acompañantes. Eon viaja solo. | Simplificar la narrativa y el alcance. |
| D-03 | Historia | Los jefes absorbieron fragmentos del poder de Eon; vencerlos devuelve habilidades. | Justifica que los jefes entreguen habilidades. |
| D-04 | Economía | La XP es el recurso de intercambio: se cambia por potenciadores con el mercader. | Petición del equipo. |
| D-05 | Economía | No hay compra de armas. | La tienda vende potenciadores. |
| D-06 | Economía | La XP no sube niveles. | Evitar un segundo sistema de progresión. |
| D-07 | Economía | La XP se conserva al morir. | Evitar frustración en los reintentos contra jefes. |
| D-08 | Economía | Los enemigos comunes reaparecen; se puede volver a zonas superadas para acumular XP. | Petición del equipo. |
| D-09 | Inventario | 3 ranuras de habilidad y 3 de potenciador. | Petición del equipo; obliga a elegir. |
| D-10 | Inventario | Ninguna habilidad se descarta: todas se guardan y el jugador elige cuáles equipar. | Petición del equipo. |
| D-11 | Inventario | El inventario muestra la función y, si existe, el control de cada habilidad y potenciador. | Petición del equipo. |
| D-12 | Inventario | El equipo se puede cambiar en cualquier momento fuera de las arenas de jefe. | Permitir probar combinaciones. |
| D-13 | Potenciadores | Son permanentes y pasivos: compra única, siempre activos mientras están equipados, sin botones. | Petición del equipo. |
| D-14 | Recursos | No hay objetos de curación ni de escudo. Vida y escudo se restauran solo en puntos de control, al vencer a un jefe y al reaparecer. | Petición del equipo. |
| D-15 | Contenido | No hay objetos que recoger en el mapa aparte de la XP. | Petición del equipo. |
| D-16 | Mecánicas | Doble salto es habilidad del Jefe 1 y el jugador decide si la equipa; la ruta principal no lo exige. | Petición del equipo. |
| D-17 | Mecánicas | El ataque arcano es el **Tajo ardiente**: un tajo de fuego lanzado por la espada. | Petición del equipo. |
| D-18 | Mecánicas | La habilidad del Jefe 3 es la **Escama pétrea**. | Petición del equipo. |
| D-19 | Controles | Ataque `Enter`; Tajo ardiente `J`; Escama pétrea `K`; Dash `Shift izquierdo`. | Petición del equipo. |
| D-20 | Mecánicas | Dash unificado: 0,20 s, 4 u, recarga 1,2 s. | Unificar valores que eran distintos entre páginas. |
| D-21 | Mecánicas | Los instakill ignoran escudo, dash y Escama pétrea. | Mantener la amenaza de la ráfaga y de la cabeza de la serpiente. |
| D-22 | Mecánicas | Caer al vacío resta 25 HP y devuelve al último suelo seguro. | En un mundo por zonas, reiniciar la zona sería demasiado castigo. |
| D-23 | Mecánicas | Los trampolines se sustituyen por géiseres. | Petición del equipo. |
| D-24 | Cámara | La sacudida de cámara es fija y no se puede desactivar. | Petición del equipo. |
| D-25 | Enemigos | Enemigos comunes: Aurion, Earthlem y Vestigio. Driller descartado. | Petición del equipo. |
| D-26 | Jefes | 3 jefes normales y La Entidad como jefe final. | Petición del equipo. |
| D-27 | Jefes | La batalla original contra La Entidad (islas, cañones) pasa a ser la fase 1 del combate final. | Reutilizar lo ya diseñado. |
| D-28 | Jefes | Límites de arena invisibles, salvo en el Jefe 2: pilares de las ruinas que bloquean el paso. | Petición del equipo. |
| D-29 | NPC | El mercader aparece por primera vez antes del Jefe 1 y después antes de cada jefe. | Petición del equipo. |
| D-30 | Reglas | Si Eon y el jefe mueren en el mismo fotograma, gana Eon. | No castigar un golpe final ajustado. |
| D-31 | Mundo | El continente se llama Kastleland en todo el documento. | Coherencia. |

### Decisiones pendientes

| # | Tema | Opciones |
| --- | --- | --- |
| P-01 | Fase 3 de La Entidad | Por definir. |
| P-02 | Nombres | Jefes 1–3, camaroncitos y Vestigio. |
| P-03 | Herramienta de audio | Por definir. |
| P-04 | Roles del equipo | Por asignar. |


---

## Historial de Versiones

| Versión | Fecha      | Cambios principales | Responsable |
| ------- | ---------- | ------------------- | ----------- |
| 0.1.0   | 05/10/2026 | Creación del documento a partir de la plantilla. Visión, mecánicas iniciales, sistemas, economía, historia, mundo, personajes, enemigos (Aurion, Driller, Earthlem), objetos, dirección de arte y audio. | Equipo True Hero |
| 0.1.1   | 16/10/2026 | Actualización de la ficha, la perspectiva, la tecnología y el audio. | Equipo True Hero |
| 0.2.0   | 07/11/2026 | Reestructuración completa: el juego empieza tras la derrota de Eon; 3 jefes (Camarón serpiente, Mago oscuro, Serpiente gigante) y La Entidad; XP como recurso de intercambio; potenciadores con 3 ranuras; habilidades con 3 ranuras; géiseres; zonas explorables; Vestigio como nuevo enemigo; Driller y aliados eliminados. Secciones 06 a 10 completadas. Página de resumen añadida. | Vargas Pérez Joel (con apoyo de Adriel) |
| 0.2.1   | 07/11/2026 | Potenciadores permanentes y pasivos sin controles; sin curación ni escudo en el campo (restauración en puntos de control y jefes); eliminados los objetos del mapa; Eon viaja solo; Tajo ardiente como ataque arcano; Escama pétrea como habilidad del Jefe 3; ninguna habilidad se descarta; nuevos controles (`Enter`, `J`, `K`); inventario con descripciones; sacudida fija; mercader antes de cada jefe; reaparición de enemigos; límites de arena invisibles salvo los pilares del Jefe 2. | Vargas Pérez Joel (con apoyo de Adriel) |

### Convención

- **MAJOR:** cambios estructurales importantes.
- **MINOR:** nuevas secciones o características relevantes.
- **PATCH:** correcciones, aclaraciones y pequeños ajustes.

