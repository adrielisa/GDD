# Bugs y Seguimiento

## Clasificación

| Severidad | Definición | Ejemplo |
| --- | --- | --- |
| Crítica | Bloquea el avance o pierde el guardado. | Una arena no se abre al morir el jefe. |
| Alta | Rompe una mecánica principal. | El doble salto no funciona equipado. |
| Media | Afecta la experiencia, con solución alternativa. | Un potenciador no muestra su descripción en el inventario. |
| Baja | Visual o de texto. | Un icono desalineado. |

## Formato de registro

| ID | Fecha | Severidad | Descripción | Pasos para reproducir | Responsable | Estado |
| --- | --- | --- | --- | --- | --- | --- |
| BUG-01 | 09/11/2026 | Crítica | Durante el combate contra el Mago se podía salir de la arena por las puertas del templo. | Entrar a Ruina_Mago, pasar x ±15 para empezar la pelea y caminar hasta una puerta. | Vargas Pérez Joel | Resuelto: las puertas se sellan mientras la arena está cerrada (`PuertaEscena`). |
| BUG-02 | 09/11/2026 | Alta | Al entrar a Ruina_Mago emergía un muro y unos pilares en medio de la sala que estorbaban el combate. | Entrar a Ruina_Mago desde Eretz y avanzar hacia el centro. | Vargas Pérez Joel | Resuelto: se quitaron los pilares; la sala la cierran los muros del templo. |
| BUG-03 | 09/11/2026 | Media | La cámara mostraba lo que hay más allá del último muro del templo. | Ir a cualquier extremo de Ruina_Mago y mirar el borde de la pantalla. | Vargas Pérez Joel | Resuelto: la cámara se limita a x ±28 (`CameraFollow`). |
| BUG-04 | 09/11/2026 | Media | El fondo del templo no aparecía en Ruina_Mago. | Abrir la escena: el fondo seguía siendo el anterior. Causa: el asset estaba en la referencia del script y sus capas tenían alfa 0. | Vargas Pérez Joel | Resuelto: asignado al objeto `Fondo_Ruina` y capas corregidas. |
| BUG-05 | 09/11/2026 | Baja | Bloques sin textura (morados) en las paredes de Ruina_Mago. | Recorrer la sala del templo. | Vargas Pérez Joel | Resuelto: muros y puertas con el arte gris del templo. |
| BUG-06 | 09/11/2026 | Baja | Un pilar de piedra gigante y caído flotaba a la izquierda del checkpoint `Despues_Mago` en Eretz. | Llegar al checkpoint posterior a la arena del Mago. | Vargas Pérez Joel | Resuelto: tiles y bloques del pilar quitados. |
| BUG-07 | 10/11/2026 | Media | Con el escudo arcano del Mago activo, un Tajo ardiente lanzado desde lejos empujaba a Eon. | Esperar el escudo del Mago y lanzar un Tajo ardiente a más de 2,5 u. | Vargas Pérez Joel | Resuelto: el rebote solo empuja cuerpo a cuerpo (prueba T-34). |
| BUG-08 | 10/11/2026 | Media | El escudo de Eon no sigue las reglas del GDD: empieza en 100 SP sin la Coraza, solo lo recargan los orbes y queda en 0 al reaparecer. | Recibir daño hasta gastar el escudo, morir y reaparecer en un punto de control. | Vargas Pérez Joel | Abierto: falta decidir la regla (ver B-04). |

- **ID:** `BUG-NN`, en orden de aparición. **Estado:** Abierto, En curso o Resuelto (con lo que se hizo).
- Cada bug resuelto debería tener una prueba en [[02 - Pruebas]] para que no vuelva.

## Pendientes de diseño (no son bugs)

| Tema | Detalle |
| --- | --- |
| Fase 3 de La Entidad | Cerrar ataques y valores. |
| Nombres | Jefe 2. |
| Valores de La Entidad | Ajustar con el encuentro ya diseñado. |
| Escudo de Eon | Aplicar las reglas del GDD (restaurar en puntos de control, al vencer a un jefe y al reaparecer) u ocultarlo hasta la Coraza (B-04). |
| Mapa de controles | Unificar el del GDD con el del prototipo (P-06). |
| Espinas punzantes | Confirmar en pruebas el 30 % de probabilidad y el 50 % de daño devuelto. |

> **Navegación:** [[00 - Índice]] · ← [[02 - Pruebas]] · [[04 - Criterios de Aceptación]] →
