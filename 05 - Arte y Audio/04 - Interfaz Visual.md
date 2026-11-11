# Interfaz Visual

## HUD

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
| Indicador fuera de pantalla | Borde de la pantalla | Flecha roja para la embestida de Cienojos. |

## Jerarquía visual

1. **Avisos de peligro** (instakill y ataques del jefe), siempre por encima de todo.
2. **Vida y escudo.**
3. **Barra del jefe.**
4. **Habilidades y su recarga.**
5. **XP, potenciadores e indicadores contextuales.**

## Estados

| Estado | Representación |
| --- | --- |
| Normal | HUD con opacidad completa. |
| Vida baja (≤ 20 HP) | La barra de vida late en rojo. |
| Daño recibido | Destello rojo de la barra y sacudida leve del HUD. |
| Vida restaurada (punto de control o jefe vencido) | La barra se rellena con un barrido verde. |
| Habilidad en recarga | Icono oscurecido con relleno radial. |
| Ranura vacía | Marco vacío con borde punteado. |
| Acción bloqueada (sin XP en tienda) | Botón en gris y precio en rojo. |

## Inventario

- Dos pestañas: **Habilidades** y **Potenciadores**, cada una con 3 ranuras arriba y la lista de lo obtenido debajo.
- Al seleccionar un elemento, un panel lateral muestra su icono, nombre, **función** y, si la tiene, su **tecla de control** (por ejemplo, *«Tajo ardiente — J: la espada lanza un tajo de fuego…»*; *«Codicia — Pasivo: +25 % de XP obtenida»*).
- Dentro de una arena de jefe se muestra en modo lectura con un candado.

## Convenciones

- **Tipografía:** pixel serif para títulos y nombres de jefe; pixel sans legible para números y texto.
- **Iconografía:** iconos de 32 × 32 con contorno oscuro para leerse sobre cualquier fondo.
- **Tamaños mínimos:** texto de 16 px a 1080p; números del HUD a 20 px.
- **Contraste:** todo elemento del HUD tiene un marco oscuro semitransparente.
- **Animaciones:** entradas y salidas de 0,15 s; los números de XP suben con un pequeño rebote.

## Pantallas

- Menú principal
- Prólogo (cómic)
- Pausa
- Configuración
- **Inventario** (pestañas Habilidades y Potenciadores)
- **Tienda del mercader**
- Entrega de habilidad
- Derrota
- Victoria y créditos

> **Navegación:** [[00 - Índice]] · ← [[03 - Entornos]] · [[05 - Audio y Música]] →
