# Entornos

## Zonas

| Zona | Estilo | Elementos | Función | Modularidad |
| --- | --- | --- | --- | --- |
| **Playa del Despertar y Acantilados** | Costa gris y turquesa bajo un cielo nublado; restos de naves y estandartes. | Rocas, faros caídos, cuevas marinas; antesala del Jefe 1 con el mercader. | Tutorial y exploración inicial. | Bloques de roca, arena, restos de barco. |
| **Arena de la Marea** | Playa abierta con el mar a un lado; oleaje animado. | Arena plana, mar con capa de agua animada; muros de roca que emergen y se rompen. | Jefe 1. | Reutiliza bloques de la Costa. |
| **Bosque de Raíces** | Árboles altos y vegetación densa. | Raíces colosales entrelazadas, armaduras de caballeros antiguos. | Plataformas verticales; rutas opcionales altas con doble salto. | Segmentos de tronco, raíces, plantas. |
| **Ruinas Abandonadas** | Academia de caballeros arrasada; mármol agrietado y piedra ennegrecida. | Columnas rotas, aulas derrumbadas, estandartes rasgados, torres. | Exploración y combates terrestres. | Columnas, bloques de muro, arcos. |
| **Patio de la Academia** | Suelo de piedra completamente plano entre ruinas. | Restos de estatuas al fondo; sin plataformas; pilares de piedra que emergen en los extremos para cerrar la arena. | Jefe 2. | Reutiliza piezas de las Ruinas como fondo. |
| **Archipiélago de Tierra** | Islas de tierra y roca flotando sobre el vacío; cielo pálido. | Géiseres, raíces colgantes, rocas que caen al vacío. | Exploración aérea con géiseres. | Islas de 3 tamaños, géiser como *prefab*. |
| **Anillo de Islas** | 7 islas de tierra en dos alturas. | Túneles por donde pasa la serpiente. | Jefe 3. | Reutiliza islas del Archipiélago. |
| **Puente e Isla Final** | Cuerpo petrificado de la serpiente; cumbre de mármol bajo un cielo oscuro. | Cañones, islas ascendentes con géiseres, La Entidad a gran escala. | Batalla final. | Reutiliza islas, cañón como *prefab*. |

## Estado en Unity (prototipo)

Arte ya usado en el mapa jugable ([[02 - Niveles]]). Las imágenes están en [[06 - Galería de Assets]].

| Elemento | Cómo está hecho | Carpeta en Unity |
| --- | --- | --- |
| **Estilo general** | Set de pixel art SSW_SET3 (tierra, roca, pasto y decoración) a 21,5 PPU, filtro *Point*, sin contornos negros. | `Assets/Art/Sprites/Environment/SSW_Set3/` |
| **Costa: suelo** | Arena hecha con la textura de tierra SSW recoloreada a tonos de arena, con conchas; rocas de la playa con borde de roca SSW, sin pasto. | `Costa_Dia/Tiles/` |
| **Costa: fondo** | Cielo y nubes (compartidos por todo el mapa), acantilados con textura de roca y bruma, mar con olas, destellos y reflejo, animado en 3 cuadros (≈3 cuadros/s). | `Costa_Dia/Fondo/` |
| **Zona 3: suelo** | Roca SSW en el sendero, la torre y la meseta; árboles y lianas animados del set. | `SSW_Set3/` |
| **Zona 3: fondo** | Templo en ruinas por capas con parallax (bosque lejano, árboles, templo, primer plano y arbustos); el templo aparece una sola vez, centrado en la base de la torre. | `Templo_Ruinas/Fondo/` |
| **Columnas de ruinas** | Columna entera (92 px), rota alta, rota baja, caída, capitel y arco, con musgo y lianas. Solo decoración. | `Ruinas/` |
| **Islas** | Superficie de pasto y tierra SSW; debajo, rocas colgantes en forma de pirámide invertida (de Decoratives) que nunca bajan tanto como para estorbar al saltar en la isla de abajo; encima, árboles, tocones, hongos y rocas. | `SSW_Set3/Tiles/isla_*`, `Islas_Deco/` |
| **Géiser** | 64×128 px: montículo de roca con pasto; *reposo* (8 cuadros, burbujeo y vapor) y *erupción* (10 cuadros, se reproduce al lanzar a Eon). | `Geiser/` |
| **Muros de la arena de Chasko** | Pilar de roca SSW (32 px de ancho); la cabeza y la base son fijas y el centro se repite según la altura. Se rompe en 5 tipos de escombro. | `Assets/Resources/Arena/` |
| **Fondos por zona** | Cada zona tiene un asset con sus capas; al cruzar de una zona a otra el fondo se funde. Cada capa se ajusta en el Inspector (parallax, altura del suelo, ancla, animación). | `Assets/Art/Fondos_Eretz/` |

## Modularidad

- Bloques de suelo con borde superior claro reutilizables en todas las zonas, cambiando solo la paleta.
- *Prefabs* comunes: géiser, punto de control, antesala del mercader, cañón, pilar de las ruinas, muro de roca de arena.
- La silueta de La Entidad es una sola capa de fondo que cambia de escala por zona.

## Iluminación

| Zona | Iluminación |
| --- | --- |
| Costa | Luz diurna nublada y fría. |
| Bosque | Penumbra verde con rayos de luz entre hojas. |
| Ruinas | Atardecer naranja; en la arena del Mago, luz de fuego. |
| Archipiélago | Luz alta y pálida; niebla bajo las islas. |
| Isla Final | Cielo oscuro; La Entidad emite luz propia en sus núcleos. |

## Efectos visuales

- **Agua:** oleaje, salpicaduras y burbujas del Jefe 1.
- **Fuego y magma:** llamaradas, picos de magma, cráneos de fuego.
- **Fuego y magia de Eon:** tajo ardiente (media luna de fuego), piel de piedra de la Escama pétrea.
- **Magia del Mago:** escudo, teletransporte (humo negro).
- **Géiseres:** burbujeo de aviso, columna de vapor y agua.
- **Baba:** gotas verdes y salpicadura al impactar.
- **Petrificación:** grietas grises que recorren el cuerpo de la serpiente.
- **Impactos:** chispas de espada, polvo de aterrizaje, escombros del Earthlem.
- **Clima:** niebla en el Archipiélago; ceniza en las Ruinas.

## Recursos requeridos

- *Tilesets* por zona (Costa, Bosque, Ruinas, Archipiélago, Isla Final).
- 3 capas de *parallax* por zona, más la capa de La Entidad.
- *Prefabs*: géiser, punto de control, antesala del mercader, cañón, pilares de las ruinas.
- VFX listados arriba.

> **Navegación:** [[00 - Índice]] · ← [[02 - Personajes y Animación]] · [[04 - Interfaz Visual]] →
