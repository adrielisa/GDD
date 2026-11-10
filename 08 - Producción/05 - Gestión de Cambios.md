# Gestión de Cambios

## Proceso

1. **Propuesta:** quien quiera cambiar algo del diseño lo describe en una línea: qué cambia, por qué y qué secciones del GDD afecta.
2. **Revisión:** se comprueba contra los [[04 - Pilares de Diseño]] y el [[01 - Alcance]].
3. **Decisión:** la responsable del proyecto aprueba o rechaza.
4. **Registro:** se anota en [[03 - Registro de Decisiones]] y se actualizan las páginas afectadas.
5. **Versión:** se sube la versión del GDD en [[04 - Historial de Versiones]].

## Cambios aplicados en la versión 0.2.0

| Cambio | Antes | Ahora | Secciones afectadas |
| --- | --- | --- | --- |
| Inicio del juego | Prólogo jugable con la derrota frente a La Entidad. | El juego empieza tras la derrota; se cuenta en el cómic. La batalla original pasa a ser la fase 1 de la isla final. | Visión, Trama, Niveles, Diálogos |
| Objetivo de Eon | Reunir sobrevivientes y aliados. | Derrotar 3 jefes para recuperar habilidades y vencer a La Entidad. | Visión, Trama, Personajes, Misiones |
| Economía | — | XP para cambiar por potenciadores con el mercader. | Economía, Objetos, Enemigos, UI |
| Habilidades | No existían. | Habilidades de jefes con 3 ranuras. | Mecánicas, Sistemas, Progresión |
| Cruce entre islas | Trampolines. | Géiseres. | Mecánicas, Entornos, Niveles |
| Enemigos | Aurion, Driller, Earthlem. | Aurion, Earthlem, Vestigio. Driller descartado. | Enemigos, Arte |
| Mundo | Niveles lineales. | Zonas explorables. | Estructura, Niveles |

## Cambios aplicados en la versión 0.2.1

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

## Cambios aplicados en la versión 0.3.0

| Cambio | Antes (0.2.1) | Ahora | Secciones afectadas |
| --- | --- | --- | --- |
| Mapa jugable | Zonas solo en papel. | Prototipo Eretz_Mapa con todo el recorrido hasta la isla final, 60 % más largo y con los saltos verificados. | Niveles, Pruebas, Backlog |
| Earthlem | En el Bosque, las Ruinas y el Archipiélago. | Solo en la zona 3 (Bosque y Ruinas). | Enemigos, Niveles |
| Arena de Chasko | Límites invisibles. | Muros de roca que emergen y se rompen al vencerlo. | Enemigos, Niveles, Entornos, Pruebas |
| Driller | Descartado. | Descartado como enemigo común; provisional como jefe del gusano en el prototipo. | Enemigos, Niveles |
| Valores de Eon | Carrera 7 u/s, salto 3 u, dash 4 u en 0,20 s, combo 10/10/15. | Carrera 7,6 u/s, salto 3,6 u, dash 5 u en 0,15 s, combo 12/12/16, ataque un 12 % más pausado. | Mecánicas, Galería |
| Arte de entornos | Por definir. | Set SSW_SET3 en costa, zona 3 e islas; fondos por zona con parallax; géiser, columnas y muros animados. | Entornos, Galería, Personajes y Animación |
| Doble salto | Habilidad sin implementar; efecto de ráfaga de aire. | Chasko suelta el Camarón de Chasko; Doble salto equipable con burbuja bajo los pies. | Mecánicas, Controles, Enemigos, Objetos, Galería, Pruebas |
| Inventario | Pantalla propia (`Tab`). | En el prototipo, sección Habilidades en la pestaña Objetos del menú de pausa. | Sistemas, Controles, UI, UX |

## Cambios aplicados en la versión 0.4.0

| Cambio | Antes (0.3.0) | Ahora | Secciones afectadas |
| --- | --- | --- | --- |
| Jefe 2 | Diseñado, sin implementar; obligatorio. | Mago oscuro implementado y **opcional**; se entra a su templo con Interactuar. | Enemigos, Niveles, Progresión, Misiones, Estructura, Pruebas |
| Arena del Jefe 2 | Patio plano de 36 u con pilares que emergen. | Interior del templo en otra escena (`Ruina_Mago`): sala de 44 u cerrada por muros, puertas selladas durante la pelea, cámara limitada. | Niveles, Sistemas, Reglas, Entornos, Arquitectura |
| Tajo ardiente y Dash cortante | Sin implementar. | Hechos; los entregan la Brasa del Mago y el Filo de sombra. Tajo ardiente en `K` en el prototipo. | Mecánicas, Controles, Objetos, Galería |
| Arte del Mago y del templo | Sin arte. | Mago a escala de Eon con 10 animaciones y 8 efectos; templo gótico de noche por capas; fachada con ruinas detrás. | Personajes y Animación, Entornos, Galería |
| Estado entre escenas | — | `EstadoPartida` conserva jefes, habilidades y materiales durante la partida. | Arquitectura, Datos y Persistencia |

> **Navegación:** [[00 - Índice]] · ← [[04 - Backlog del Proyecto]] · [[01 - Criterios de Calidad]] →
