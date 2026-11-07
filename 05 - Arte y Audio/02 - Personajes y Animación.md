# Personajes y Animación

Lista de sprites y animaciones necesarios. La identidad de cada personaje está en [[03 - Personajes]] y sus reglas de combate en [[03 - Enemigos y NPC]].

## Requisitos por personaje

| Personaje | Sprite | Animaciones | VFX | Estado |
| --- | --- | --- | --- | --- |
| Eon | 64 × 64 | Idle, correr, saltar, doble salto, caer, aterrizar, dash, ataque ×3, ataque descendente, tajo ardiente, escama pétrea (petrificarse, bloqueo perfecto), recibir daño, muerte, interactuar | Estelas de espada (normal y roja con Filo), polvo de aterrizaje, ráfaga del doble salto, estela de dash (normal y cortante), media luna de fuego del tajo ardiente, piel de piedra y destello de bloqueo | Sprite base hecho (`Default Sprite.png`); animaciones pendientes |
| Mercader | 64 × 64 | Idle, hablar, entregar | — | Pendiente |
| Aurion | 48 × 48 | Flotar, cargar, embestir, aturdido, muerte | Núcleo rojo, estela | Pendiente |
| Earthlem | 96 × 96 | Enterrado, emerger, caminar, barrido, aplastamiento, enterrarse, impacto, muerte | Escombros, onda sísmica | Pendiente |
| Vestigio | 64 × 96 | Caminar, combo, estocada, guardia, impacto, muerte | Brillo del arma, disolución blanca | Pendiente |
| Camaroncito | 24 × 24 | Volar, impacto, muerte | Burbujas | Pendiente |
| Jefe 1 — Camarón serpiente | Cabeza 128 × 128 + segmentos | Nadar, emerger, embestida, varado, mordida, inhalar, ráfaga, agotado, muerte | Ráfaga de agua, plataforma de agua, chapoteos | Pendiente |
| Jefe 2 — Mago oscuro | 96 × 128 | Flotar, conjurar llamaradas, golpear el suelo, escudo, invocar cráneos, desaparecer, aparecer, aturdido, muerte | Llamaradas, picos de magma, esfera violeta, cráneos de fuego, humo | Pendiente |
| Jefe 3 — Serpiente gigante | Cabeza 192 × 192, segmento 96 × 96, cola | Mandíbula, segmento hinchado, petrificación | Gotas y salpicadura de baba, polvo al atravesar islas | Pendiente |
| La Entidad | Escala de fondo y escala de cumbre | Escalar, golpe de mano, barrido, invocar, apertura del rostro, derrota | Ondas, sombras de impacto, núcleo | Diseño hecho (referencia); animación pendiente |

## Animaciones de Eon

| Grupo | Animaciones | Fotogramas orientativos |
| --- | --- | --- |
| Movimiento | Idle, correr, saltar, doble salto, caer, aterrizar | 6 / 8 / 3 / 4 / 2 / 3 |
| Combate | Tajo 1, 2, 3; descendente; dash; tajo ardiente; escama pétrea | 4 / 4 / 6 / 3 / 3 / 5 / 4 |
| Interacción | Interactuar | 4 |
| Daño | Impacto, aturdido | 2 / 4 |
| Derrota | Colapso | 8 |

## Ilustraciones fijas

| Ilustración | Uso |
| --- | --- |
| Cómic del prólogo (5 páginas) | Inicio. La página 5 muestra la derrota de Eon. |
| Entrega de habilidad (×4) | Tras cada jefe. |
| Serpiente petrificada | Tras el Jefe 3: el cuerpo se convierte en piedra y forma el puente a la isla final. |
| Final | Tras La Entidad. |

## Convenciones

- **Nombres de archivo:** `Personaje_Accion` (ej. `Eon_DobleSalto.png`, `MagoOscuro_Teletransporte.png`).
- **Formato:** PNG con transparencia; hojas de sprites por personaje; fuente editable en Clip Studio.
- **Escala:** 32 píxeles por unidad de Unity; filtrado *Point* y sin compresión.
- **Pivote:** en los pies para personajes terrestres; en el centro para voladores.

> **Navegación:** [[00 - Índice]] · ← [[01 - Dirección de Arte]] · [[03 - Entornos]] →
