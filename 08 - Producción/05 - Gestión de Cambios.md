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

> **Navegación:** [[00 - Índice]] · ← [[04 - Backlog del Proyecto]] · [[01 - Criterios de Calidad]] →
