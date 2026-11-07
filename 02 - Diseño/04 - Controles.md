# Controles

La prioridad es la inmediatez: respuesta sin latencia percibida, una acción por botón y retroalimentación audiovisual instantánea.

## Mapa de controles

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

## Principios de control

- **Consistencia:** salto, aceleración y dash son idénticos en todas las zonas.
- **Tolerancia de entrada:** *buffer* de 0,10 s para Ataque, Salto y Dash al terminar una animación o al aterrizar.
- **Sin combinaciones complejas:** no hay medias lunas ni dobles toques; la única combinación es Abajo + Ataque.
- **Pulsación accidental:** la tecla que cierra la tienda o el inventario no se reutiliza como ataque o salto en el mismo fotograma.

## Reasignación

No se incluye reasignación de teclas en esta versión. Salto tiene dos teclas (`Espacio`/`W`).

## Entrada y retroalimentación

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

> **Navegación:** [[00 - Índice]] · ← [[03 - Sistemas]] · [[05 - Progresión]] →
