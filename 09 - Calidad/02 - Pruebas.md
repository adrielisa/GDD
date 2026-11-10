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
| T-11 | Escapar de la ola de picos corriendo hacia el extremo. | Sin daño al llegar a la zona segura junto al muro del templo. |
| T-12 | Tocar la cabeza de la serpiente durante un dash o con Escama pétrea. | Derrota (instakill). |
| T-13 | Bloqueo perfecto con Escama pétrea contra el barrido del Earthlem. | Sin daño; Earthlem aturdido 1 s. |
| T-14 | Volver a una zona superada tras vencer a su jefe. | Los enemigos han reaparecido y dan XP. |
| T-15 | Entrar a cada arena de jefe e intentar salir. | Muros de roca en el Jefe 1; puertas selladas en el Jefe 2; límite invisible en el Jefe 3 y La Entidad. |
| T-16 | Ser derrotado con 500 XP. | Reaparece en el punto de control con 500 XP, vida y escudo completos. |
| T-17 | Empezar el combate contra Chasko. | Los muros emergen con sacudida de pantalla y cierran la arena. |
| T-18 | Vencer a Chasko. | Los muros se rompen en escombros y desaparecen; el paso queda libre. |
| T-19 | Morir durante el combate contra Chasko. | Los muros bajan; al volver a entrar se cierran de nuevo. |
| T-20 | Recorrer el mapa Eretz sin habilidades. | Se llega a la meta; cada sección posterior solo se alcanza con su géiser. |
| T-21 | Vencer a Chasko. | Sale el Camarón de Chasko, cae y flota; al tocarlo aparece el aviso y la habilidad queda en el inventario sin equipar. |
| T-22 | Sin equipar Doble salto, saltar en el aire. | No hay segundo salto. |
| T-23 | Pasar caminando por delante del templo del Mago sin pulsar Interactuar. | No cambia de escena; el recorrido sigue hasta la meta sin enfrentar al Mago. |
| T-24 | Pulsar Interactuar frente al templo. | Fundido a negro, título «Ruinas del Templo» y Eon aparece dentro, en la entrada. |
| T-25 | Empezar la pelea con el Mago e ir a la puerta de la izquierda. | La puerta no funciona hasta vencer o caer. |
| T-26 | Huir de la ola de picos corriendo al extremo opuesto. | La ola se detiene a 2 u del muro; sin daño. |
| T-27 | Golpear al Mago con el escudo activo. | Sin daño; el golpe rebota y empuja a Eon. |
| T-28 | Vencer al Mago. | Suelta la Brasa del Mago y el Filo de sombra; al recogerlos salen dos avisos seguidos y las habilidades quedan en el inventario sin equipar. |
| T-29 | Equipar Tajo ardiente y pulsar `K`. | Sale la media luna de fuego (15 de daño); no se puede volver a lanzar hasta 1,2 s después. |
| T-30 | Volver a Eretz tras vencer al Mago. | La puerta del templo ya no se abre; las habilidades siguen en el inventario. |
| T-23 | Equipar Doble salto (Pausa ▸ Objetos ▸ Habilidades) y saltar en el aire. | Segundo salto al 80 % de altura con burbuja bajo los pies; se recupera al tocar suelo. |
| T-24 | Intentar cambiar habilidades con los muros de una arena cerrados. | No cambia; el menú avisa en rojo. |
| T-25 | Confirmar con `Enter` / `Espacio` en la pausa y volver al juego. | Eon no ataca ni salta solo al cerrar el menú. |

## Herramientas de prueba (solo en el editor y en *builds* de desarrollo)

| Herramienta | Uso |
| --- | --- |
| Salto entre puntos de control | En Play: `.` siguiente, `,` anterior, `L` lista (el juego se pausa). Al llegar, el punto de control se activa. |
| Jugar desde un punto de control | Clic derecho en el componente Checkpoint ▸ *Jugar desde aquí*, o *TrueHero ▸ Pruebas ▸ Jugar desde el checkpoint seleccionado*. |
| Colisiones visibles | Los bloques de colisión ocultos bajo los tiles se dibujan en la vista de escena; se activan o apagan en *TrueHero ▸ Blockout*. |
| Vista previa del fondo | Sin Play, el fondo por zonas sigue a la vista de escena para ver el parallax mientras se edita. |
| Simulación de saltos | Script que simula el salto de Eon sobre el mapa para detectar atajos y zonas inalcanzables (resultado en [[02 - Niveles]]). |
| Dar Doble salto | En Play: clic derecho en el componente PlayerInventory de Eon ▸ *Pruebas/Dar y equipar Doble salto* (o *Quitar todas las habilidades*). |

> **Navegación:** [[00 - Índice]] · ← [[01 - Criterios de Calidad]] · [[03 - Bugs y Seguimiento]] →
