# UI y Menús

## Mapa de navegación

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

## Pantallas

| Pantalla | Propósito | Elementos | Acciones |
| --- | --- | --- | --- |
| Menú principal | Entrar al juego. | Logo, ilustración de fondo con La Entidad, opciones. | Nueva partida, Continuar, Configuración, Créditos, Salir. |
| Prólogo | Contar la caída de Eon. | Viñetas del cómic; indicador de «mantener para omitir». | Avanzar, omitir. |
| Inventario — Habilidades | Elegir qué 3 habilidades usar. | 3 ranuras arriba; lista de todas las habilidades obtenidas; candado en las no obtenidas. Panel con icono, nombre, **control** y **función** de la seleccionada. | Equipar, quitar, intercambiar. En arenas de jefe, solo lectura. |
| Inventario — Potenciadores | Elegir qué 3 potenciadores tener activos. | 3 ranuras arriba; lista de potenciadores comprados. Panel con icono, nombre y **función** (indica «Pasivo: siempre activo mientras esté equipado»). | Equipar, quitar, intercambiar. En arenas de jefe, solo lectura. |
| Tienda | Cambiar XP por potenciadores. | XP actual; catálogo con icono, función y precio; marca «Adquirido» en los ya comprados; retrato y frase del mercader. | Comprar, salir. |
| Entrega de habilidad | Presentar la habilidad nueva. | Ilustración, nombre, control y función; aviso de que se guardó en el inventario. | Continuar, abrir inventario. |
| Pausa | Detener el juego. | Pestañas con icono: Objetos (materiales y ficha del objeto), Configuración de control (esquema del mando) y Ajustes (volúmenes, modo de pantalla, vibración, restablecer, salir). | (A) Confirmar, (B) Volver al juego. |
| Derrota («Has caído») | Reintentar. | Título en rojo, intentos en este nivel, «Pulsa Salto o Ataque para reaparecer en el último punto seguro» y pista opcional. | (A) Reaparecer, (B) Menú principal. |
| Nivel completado | Cerrar un nivel. | Título en dorado, tiempo y reintentos del nivel. | (A) Confirmar, (B) Menú principal. |
| Victoria | Cerrar la historia. | Ilustración final. | Continuar a créditos. |
| Créditos | Reconocer al equipo. | Nombres del equipo y herramientas. | Omitir. |

### Inventario en el prototipo

En Unity, las habilidades se equipan desde el **menú de pausa**, en la pestaña **Objetos**: a la izquierda están los materiales y, a su costado, la sección **Habilidades**.

- Una ranura por habilidad del catálogo (4). Las no obtenidas se ven atenuadas con «?».
- Las equipadas llevan un **rombo dorado**; arriba a la derecha, el contador «Equipadas n/3».
- El panel de detalle muestra nombre, objeto de origen, descripción y estado («Equipada · (A) / Enter para quitar»). Si no se puede cambiar, lo dice en rojo (ranuras llenas o arena de jefe cerrada).
- Al recoger la habilidad aparece un aviso arriba con su icono: *«¡Nueva habilidad: Doble salto! Equípala en Pausa (Esc / Start) ▸ Objetos ▸ Habilidades»*.
- Si se recogen dos habilidades seguidas (las del Mago), los avisos salen uno tras otro.
- **Puertas con Interactuar** (templo del Mago): al acercarse aparece sobre la puerta un aviso flotante «[E] Entrar al templo» que se desvanece al alejarse.

![[05 - Arte y Audio/Galería de Assets/Habilidades/menu_pausa_habilidades_maqueta.png]]

*Maqueta de la distribución (no es una captura de Unity).*

Las pantallas de Sergio (Has caído, Nivel completado y las pestañas del menú de pausa) están en [[06 - Galería de Assets#Interfaz]].

## Confirmaciones

| Acción | Confirmación |
| --- | --- |
| Nueva partida con guardado existente | *«Se borrará tu progreso. ¿Continuar?»* |
| Salir al menú desde la pausa | *«Volverás al último punto de control al continuar. ¿Salir?»* |
| Compra en la tienda | *«¿Comprar [potenciador] por [precio] XP?»* (la compra es permanente). |

> **Navegación:** [[00 - Índice]] · ← [[01 - UX y Flujo del Jugador]] · [[03 - Accesibilidad]] →
