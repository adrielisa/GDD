# Pruebas

## Tipos de prueba

| Tipo | Qué se prueba | Cuándo |
| --- | --- | --- |
| Funcional | Cada mecánica y sistema según [[02 - Mecánicas]] y [[03 - Sistemas]]. | Al terminar cada tarea del backlog. |
| Jefes | Que cada ataque se pueda esquivar sin habilidades concretas y que las fases cambien en su umbral. | Al terminar cada jefe. |
| Progresión | Que la ruta principal se complete sin ninguna habilidad equipada. | Al terminar cada bloque. |
| Economía | XP obtenida por zona frente a precios; reaparición de enemigos. | Hitos 3 a 6. |
| Guardado | Cerrar y reabrir en cada situación de [[04 - Guardado y Configuración]]. | Hitos 3 y 7. |
| Jugadores nuevos | Personas que no conocen el juego juegan sin ayuda. | Vertical slice y versión final. |
| Rendimiento | FPS con el máximo de objetos activos. | Hito 7. |

## Casos de prueba clave

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
| T-09 | Hacer que Chasko choque contra la pared con la embestida. | Queda aturdido 1,6 s y recibe ×1,5 de daño. |
| T-10 | Atravesar con dash la burbuja del chasquido. | Sin daño. |
| T-11 | Escapar de la ola de picos corriendo hacia el extremo. | Sin daño al llegar a la zona segura junto al pilar. |
| T-12 | Tocar la cabeza de la serpiente durante un dash o con Escama pétrea. | Derrota (instakill). |
| T-13 | Bloqueo perfecto con Escama pétrea contra el barrido del Earthlem. | Sin daño; Earthlem aturdido 1 s. |
| T-14 | Volver a una zona superada tras vencer a su jefe. | Los enemigos han reaparecido y dan XP. |
| T-15 | Entrar a cada arena de jefe e intentar salir. | Límite invisible en los Jefes 1 y 3 y La Entidad; pilares visibles en el Jefe 2. |
| T-16 | Ser derrotado con 500 XP. | Reaparece en el punto de control con 500 XP, vida y escudo completos. |

> **Navegación:** [[00 - Índice]] · ← [[01 - Criterios de Calidad]] · [[03 - Bugs y Seguimiento]] →
