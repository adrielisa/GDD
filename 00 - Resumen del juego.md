# True Hero: resumen del diseño

**GDD 0.2.1 · 7 de noviembre de 2026.**

Eon, el héroe de la profecía, ya perdió contra La Entidad. Despierta solo en la costa de Kastleland sin su equipo legendario y emprende la revancha: recorre zonas explorables, derrota enemigos que le dan XP, cambia esa XP por potenciadores permanentes con un mercader que aparece antes de cada jefe y vence a tres jefes que le devuelven sus habilidades. Al caer el tercero, su cuerpo petrificado forma el puente hacia la isla final, donde Eon vuelve a enfrentar a La Entidad.

## Recorrido

```text
Cómic (derrota de Eon) → Costa → Jefe 1 → Bosque → Ruinas → Jefe 2 → Archipiélago → Jefe 3
   → Puente de la Serpiente → Isla Final → La Entidad → Final
```

## De un vistazo

| Área | Contenido |
| --- | --- |
| Control | Mover, salto, dash (`Shift`), ataque con espada (`Enter`), ataque descendente, Tajo ardiente (`J`), Escama pétrea (`K`). |
| Vida | Sin curación en el campo: vida y escudo se restauran solo en puntos de control y al vencer a un jefe. |
| Economía | XP de los enemigos → potenciadores del mercader. Los enemigos reaparecen; se puede volver a zonas superadas. |
| Potenciadores | 6, permanentes y pasivos; **3 equipados**, siempre activos, sin botones. |
| Habilidades | Doble salto (Jefe 1), Tajo ardiente y Dash cortante (Jefe 2), Escama pétrea (Jefe 3). **3 equipadas**; ninguna se descarta. |
| Inventario | Muestra la función y el control de cada habilidad y potenciador. |
| Enemigos | Aurion, Earthlem y Vestigio. |
| Jefes | Chasko (costa), Mago oscuro (ruinas planas), Serpiente gigante (islas de tierra flotante), La Entidad (isla final). |
| Mundo | 5 zonas explorables con rutas opcionales; géiseres entre islas. |

## Jefes

| Jefe | Lo esencial | Entrega |
| --- | --- | --- |
| Chasko | Camarón tipo escorpión: dispara burbujas con la pinza, embiste contra la pared (queda aturdido) y en fase 2 lanza ondas de choque. Límites invisibles. | Doble salto |
| Mago oscuro | Arena plana sin plataformas, cerrada por pilares de las ruinas. Llamaradas del cielo, ola de picos de magma de la que hay que huir, escudo periódico, cráneos de fuego teledirigidos y teletransporte al otro extremo. | Tajo ardiente + Dash cortante |
| Serpiente gigante | Rodea islas flotantes; su cuerpo deja caer baba; tocar la cabeza es instakill. Al morir se petrifica y forma el puente. Límites invisibles. | Escama pétrea |
| La Entidad | Ascenso por islas con géiseres y cañones; cara a cara en la cumbre; fase final. Límites invisibles. | Victoria |

## Pendiente

- Cerrar la fase 3 de La Entidad.
- Nombres de los jefes 2 y 3 y Vestigio.
- Asignar roles del equipo.

## Dónde consultar cada parte

- [[02 - Mecánicas]] y [[03 - Sistemas]]: reglas y valores.
- [[04 - Controles]]: mapa de teclas.
- [[06 - Economía y Recursos]]: XP y potenciadores.
- [[02 - Niveles]]: zonas.
- [[03 - Enemigos y NPC]]: enemigos, jefes y mercader.
- [[03 - Registro de Decisiones]]: qué se decidió y por qué.

> **Navegación:** [[00 - Índice]] · [[01 - Ficha del Proyecto]] →
