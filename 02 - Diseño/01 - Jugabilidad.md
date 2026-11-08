# Jugabilidad

## Bucle principal de juego

```text
Explorar la zona → Derrotar enemigos comunes (XP) → Llegar a la antesala del jefe
      → Intercambiar XP por potenciadores con el mercader → Preparar inventario (3 habilidades, 3 potenciadores)
      → Vencer al jefe → Guardar su habilidad en el inventario → Siguiente zona
      (opcional: volver a zonas superadas para acumular más XP)
```

Tras el tercer jefe el bucle se cierra: la serpiente petrificada abre el paso a la isla final y el jugador enfrenta a La Entidad con todo lo reunido.

## Bucles por escala

| Escala | Qué hace el jugador | Qué obtiene |
| --- | --- | --- |
| Segundo a segundo | Corre, salta, hace dash y encadena tajos; lee avisos de ataque. | Esquivar daño y conectar golpes. |
| Minuto a minuto | Despeja tramos con enemigos, cruza géiseres, administra su vida hasta el siguiente punto de control. | XP. |
| Por zona | Explora la zona, compra potenciadores y vence a su jefe. | Una habilidad nueva y acceso a la zona siguiente. |
| Partida completa | Reúne habilidades y potenciadores y vuelve a la isla final. | La revancha contra La Entidad. |

## Acciones principales del jugador

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

## Experiencia de los primeros minutos

El cómic inicial termina con la derrota de Eon. El control empieza cuando despierta solo en la playa. En el primer minuto el jugador camina, salta y se cruza con los primeros Aurion; aprende el combo y el dash mientras recoge su primera XP. Al final de los Acantilados, justo antes del primer jefe, encuentra al mercader y descubre que esa XP compra potenciadores. La silueta de La Entidad se ve en el horizonte del mar.

## Experiencia a largo plazo

Cada jefe entrega una habilidad que cambia la forma de pelear y de moverse, y la batalla final promete la revancha que el cómic dejó pendiente. Las ranuras limitadas obligan a probar combinaciones distintas, y volver a zonas anteriores permite reunir XP para completar el catálogo del mercader.

## Condición de victoria

- **Por zona:** derrotar al jefe de la zona.
- **Del juego:** derrotar a La Entidad en la isla final.

## Condición de derrota

- La salud de Eon llega a 0 (el escudo, si lo tiene, se gasta primero).
- Un ataque instakill conecta: contacto con la cabeza de la serpiente del Jefe 3.
- Caer al vacío resta 25 HP y devuelve a Eon al último suelo seguro. Si eso deja la salud en 0, cuenta como derrota.

Al ser derrotado, Eon reaparece en el último punto de control con la vida y el escudo completos y conserva su XP. Ver [[07 - Reglas y Estados del Juego]].

## Ritmo

- **Exploración:** tramos de plataformas con rutas opcionales que se abren con habilidades.
- **Acción:** encuentros de 10 a 20 segundos con grupos pequeños de enemigos.
- **Tensión:** sin curación en el campo, cada golpe recibido cuenta hasta el siguiente punto de control.
- **Descanso:** puntos de control y la antesala de cada jefe, donde está el mercader.
- **Desafío:** combates contra jefes de 2 a 4 minutos con fases.
- **Recompensa:** la habilidad de cada jefe y la restauración completa de vida al vencerlo.
- **Historia:** ambiental (ruinas, estandartes caídos, la silueta del titán) y diálogos breves con el mercader.

## Principios de interacción

- **Legibilidad de bordes:** los límites transitables y los precipicios tienen siluetas y colisiones alineadas.
- **Un botón de contexto:** mercader, puntos de control y cañones usan `E` y muestran un aviso al entrar en su zona.
- **Avisos antes del daño:** ningún ataque hostil hace daño sin una preparación visible de al menos 0,4 s; los instakill, de al menos 1,5 s.

> **Navegación:** [[00 - Índice]] · ← [[04 - Pilares de Diseño]] · [[02 - Mecánicas]] →
