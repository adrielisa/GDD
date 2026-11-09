# Galería de Assets

Catálogo visual de todo el arte que ya está en el proyecto de Unity: Eon, enemigos, jefes y efectos. Cada animación aparece como **GIF a la velocidad real del juego** y como **hoja de cuadros numerada** (de izquierda a derecha y de arriba abajo). Los requisitos de lo que falta están en [[02 - Personajes y Animación]].

> [!info] Cómo leer esta página
> - Los GIF usan los mismos tiempos por cuadro que el juego (clips de Unity, tiempos de Aseprite o constantes del código).
> - Se muestran sobre fondo oscuro y ampliados con escala entera para no deformar el pixel art; el tamaño real está en los datos de cada animación.
> - Las rutas `Assets/...` son las carpetas del proyecto de Unity (`TrueHero/Assets/Art/Sprites/`).
> - Imágenes generadas el 07/11/2026 desde los sprites del proyecto. Si cambia un sprite, hay que volver a generarlas.

## Resumen

| Grupo         | Personaje / efecto                                     | Animaciones               | Estado                                                                                                           |
| ------------- | ------------------------------------------------------ | ------------------------- | ---------------------------------------------------------------------------------------------------------------- |
| Protagonista  | Eon                                                    | 10                        | Movimiento, ataques, daño y muerte hechos; faltan doble salto, dash, tajo ardiente, escama pétrea e interactuar. |
| Enemigo común | Aurion                                                 | 1                         | Vuelo hecho; faltan cargar, embestir, aturdido y muerte.                                                         |
| Enemigo común | Earthlem                                               | 3                         | Emerger, reposo y ataque hechos; faltan caminar, barrido, enterrarse, impacto y muerte.                          |
| Enemigo común | Vestigio                                               | 0                         | Sin arte.                                                                                                        |
| Jefe 1        | Chasko                                                 | 5                         | Completo, con su burbuja.                                                                                        |
| Jefe final    | La Entidad (Titán Blanco)                              | Piezas + mano (3 estados) | Cuerpo por piezas, manos, fondo y 3 ataques con efecto hechos.                                                   |
| Jefes 2 y 3   | Mago oscuro, Serpiente gigante                         | 0                         | Sin arte.                                                                                                        |
| Efectos       | Rayo, tornado, orbe, burbuja                           | 4                         | Hechos.                                                                                                          |
| Entornos      | Costa, zona 3, islas, géiser, columnas, muros de arena | —                         | Hechos para el mapa jugable (ver al final).                                                                      |
| Habilidades | Camarón de Chasko (Doble salto) y burbuja del doble salto | 2 | Hechos. |

## Comparación de escala

Todos los personajes a la misma escala del mundo (cada uno con sus píxeles por unidad), parados sobre el mismo suelo.

![[05 - Arte y Audio/Galería de Assets/General/comparacion_escala.png]]

---

## Eon

| Dato | Valor |
| --- | --- |
| Lienzo | 106 × 80 px por cuadro |
| Píxeles por unidad | 21,5 |
| Pivote | (0,42; 0,10), en los pies |
| Carpeta | `Assets/Art/Sprites/Characters/Player/Eon_Simple/` (una subcarpeta por animación) |
| Clips de Unity | `Assets/Animations/Player/Player_*.anim` y `Player_AnimatorController` |


| Animación | Cuadros | Velocidad | Duración | Bucle |
| --- | --- | --- | --- | --- |
| Reposo | 14 | 100 ms por cuadro | 1,4 s | Sí |
| Reposo de combate | 8 | 100 ms por cuadro | 0,8 s | Sí |
| Correr | 15 | 65 ms por cuadro | 0,97 s | Sí |
| Saltar | 3 | 70–110 ms por cuadro | 0,27 s | No |
| Caer | 3 | 90–110 ms por cuadro | 0,31 s | Sí |
| Ataque | 9 | 51–159 ms por cuadro | 0,72 s | No |
| Ataque en el aire | 6 | 51–114 ms por cuadro | 0,41 s | No |
| Ataque hacia arriba | 8 | 51–136 ms por cuadro | 0,63 s | No |
| Recibir daño | 3 | 70–120 ms por cuadro | 0,3 s | No |
| Muerte | 10 | 70–700 ms por cuadro | 1,6 s | No |


### Reposo

![[05 - Arte y Audio/Galería de Assets/Eon/eon_idle.gif]]

**14 cuadros** · 106×80 px · 100 ms por cuadro · 1,4 s · en bucle

![[05 - Arte y Audio/Galería de Assets/Eon/eon_idle_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Player/Eon_Simple/idle/`

### Reposo de combate

![[05 - Arte y Audio/Galería de Assets/Eon/eon_idle_combate.gif]]

**8 cuadros** · 106×80 px · 100 ms por cuadro · 0,8 s · en bucle

Sin clip propio todavía; se muestra a 100 ms por cuadro.

![[05 - Arte y Audio/Galería de Assets/Eon/eon_idle_combate_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Player/Eon_Simple/idle_combate/`

### Correr

![[05 - Arte y Audio/Galería de Assets/Eon/eon_run.gif]]

**15 cuadros** · 106×80 px · 65 ms por cuadro · 0,97 s · en bucle

![[05 - Arte y Audio/Galería de Assets/Eon/eon_run_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Player/Eon_Simple/run/`

### Saltar

![[05 - Arte y Audio/Galería de Assets/Eon/eon_jump.gif]]

**3 cuadros** · 106×80 px · 70–110 ms por cuadro · 0,27 s · una vez

![[05 - Arte y Audio/Galería de Assets/Eon/eon_jump_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Player/Eon_Simple/jump/`

### Caer

![[05 - Arte y Audio/Galería de Assets/Eon/eon_fall.gif]]

**3 cuadros** · 106×80 px · 90–110 ms por cuadro · 0,31 s · en bucle

![[05 - Arte y Audio/Galería de Assets/Eon/eon_fall_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Player/Eon_Simple/fall/`

### Ataque

![[05 - Arte y Audio/Galería de Assets/Eon/eon_attack.gif]]

**9 cuadros** · 106×80 px · 45–140 ms por cuadro · 0,65 s · una vez

![[05 - Arte y Audio/Galería de Assets/Eon/eon_attack_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Player/Eon_Simple/attack/`

### Ataque en el aire

![[05 - Arte y Audio/Galería de Assets/Eon/eon_attack_air.gif]]

**6 cuadros** · 106×80 px · 45–100 ms por cuadro · 0,38 s · una vez

![[05 - Arte y Audio/Galería de Assets/Eon/eon_attack_air_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Player/Eon_Simple/attack_air/`

### Ataque hacia arriba

![[05 - Arte y Audio/Galería de Assets/Eon/eon_attack_up.gif]]

**8 cuadros** · 106×80 px · 45–120 ms por cuadro · 0,56 s · una vez

![[05 - Arte y Audio/Galería de Assets/Eon/eon_attack_up_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Player/Eon_Simple/attack_up/`

### Recibir daño

![[05 - Arte y Audio/Galería de Assets/Eon/eon_hurt.gif]]

**3 cuadros** · 106×80 px · 70–120 ms por cuadro · 0,3 s · una vez

![[05 - Arte y Audio/Galería de Assets/Eon/eon_hurt_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Player/Eon_Simple/hurt/`

### Muerte

![[05 - Arte y Audio/Galería de Assets/Eon/eon_death.gif]]

**10 cuadros** · 106×80 px · 70–700 ms por cuadro · 1,6 s · una vez

El último cuadro se mantiene 700 ms.

![[05 - Arte y Audio/Galería de Assets/Eon/eon_death_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Player/Eon_Simple/death/`

> [!note] Versión anterior
> Las carpetas `Characters/Player/eon_attack`, `eon_fall`, `eon_idle`, `eon_jump` y `eon_run` son la primera versión de Eon (otro tamaño y otros píxeles por unidad). Los clips actuales ya no las usan.

---

## Enemigos

### Aurion

| Dato | Valor |
| --- | --- |
| Lienzo | 56 × 56 px |
| Píxeles por unidad | 38 |
| Pivote | (0,53; 0,38), cerca del centro (volador) |
| Carpeta | `Assets/Art/Sprites/Characters/Enemies/Aurion/aurion_vuelo/` |


| Animación | Cuadros | Velocidad | Duración | Bucle |
| --- | --- | --- | --- | --- |
| Vuelo | 8 | 85 ms por cuadro | 0,68 s | Sí |


#### Vuelo

![[05 - Arte y Audio/Galería de Assets/Enemigos/aurion_vuelo.gif]]

**8 cuadros** · 56×56 px · 85 ms por cuadro · 0,68 s · en bucle

![[05 - Arte y Audio/Galería de Assets/Enemigos/aurion_vuelo_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Enemies/Aurion/aurion_vuelo/`

### Earthlem

En el proyecto, sus sprites están en la carpeta `Golem`.

| Dato | Valor |
| --- | --- |
| Lienzo | 128 × 112 px |
| Píxeles por unidad | 38 |
| Pivote | (0,48; 0,06), en los pies |
| Carpeta | `Assets/Art/Sprites/Characters/Enemies/Golem/` (`golem_aparicion`, `golem_reposo`, `golem_ataque`) |


| Animación | Cuadros | Velocidad | Duración | Bucle |
| --- | --- | --- | --- | --- |
| Emerger | 15 | 80–100 ms por cuadro | 1,35 s | No |
| Reposo | 8 | 100–170 ms por cuadro | 0,97 s | Sí |
| Ataque (puño) | 12 | 90 ms por cuadro | 1,08 s | No |


#### Emerger

![[05 - Arte y Audio/Galería de Assets/Enemigos/earthlem_aparicion.gif]]

**15 cuadros** · 128×112 px · 80–100 ms por cuadro · 1,35 s · una vez

![[05 - Arte y Audio/Galería de Assets/Enemigos/earthlem_aparicion_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Enemies/Golem/golem_aparicion/`

#### Reposo

![[05 - Arte y Audio/Galería de Assets/Enemigos/earthlem_reposo.gif]]

**8 cuadros** · 128×112 px · 100–170 ms por cuadro · 0,97 s · en bucle

![[05 - Arte y Audio/Galería de Assets/Enemigos/earthlem_reposo_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Enemies/Golem/golem_reposo/`

#### Ataque (puño)

![[05 - Arte y Audio/Galería de Assets/Enemigos/earthlem_ataque.gif]]

**12 cuadros** · 128×112 px · 90 ms por cuadro · 1,08 s · una vez

El golpe empieza en el cuadro 8.

![[05 - Arte y Audio/Galería de Assets/Enemigos/earthlem_ataque_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Enemies/Golem/golem_ataque/`

### Vestigio

Sin arte todavía. Requisitos en [[02 - Personajes y Animación]].

---

## Jefes

### Jefe 1 — Chasko

Camarón de tipo escorpión, rojo y naranja. Reglas de combate en [[03 - Enemigos y NPC]].

| Dato | Valor |
| --- | --- |
| Lienzo | 90 × 90 px |
| Píxeles por unidad | 10 (unas 3 veces la altura de Eon) |
| Pivote | (0,5; 0,27), en los pies |
| Fuente | `Documents/sprites/Jefe_Camaron/Chasko.aseprite` (capas Cuerpo y Efectos) |
| Carpeta | `Assets/Art/Sprites/Characters/Jefe_Camaron/chasko_*` |


| Animación | Cuadros | Velocidad | Duración | Bucle |
| --- | --- | --- | --- | --- |
| Reposo | 9 | 120 ms por cuadro | 1,08 s | Sí |
| Caminar | 9 | 100 ms por cuadro | 0,9 s | Sí |
| Chasquido | 16 | 80–110 ms por cuadro | 1,56 s | No |
| Recibir daño / aturdido | 3 | 100 ms por cuadro | 0,3 s | No |
| Muerte | 8 | 100–400 ms por cuadro | 1,18 s | No |


#### Reposo

![[05 - Arte y Audio/Galería de Assets/Jefes/Chasko/chasko_idle.gif]]

**9 cuadros** · 90×90 px · 120 ms por cuadro · 1,08 s · en bucle

![[05 - Arte y Audio/Galería de Assets/Jefes/Chasko/chasko_idle_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Jefe_Camaron/chasko_idle_*`

#### Caminar

![[05 - Arte y Audio/Galería de Assets/Jefes/Chasko/chasko_walk.gif]]

**9 cuadros** · 90×90 px · 100 ms por cuadro · 0,9 s · en bucle

En fase 2 se reproduce 1,4× más rápido; en la embestida, 2,6×.

![[05 - Arte y Audio/Galería de Assets/Jefes/Chasko/chasko_walk_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Jefe_Camaron/chasko_walk_*`

#### Chasquido

![[05 - Arte y Audio/Galería de Assets/Jefes/Chasko/chasko_attack.gif]]

**16 cuadros** · 90×90 px · 80–110 ms por cuadro · 1,56 s · una vez

Cuadros 1-10 carga, 11 chasquido (sale la burbuja), 12-16 recuperación. También se usa para la onda de choque.

![[05 - Arte y Audio/Galería de Assets/Jefes/Chasko/chasko_attack_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Jefe_Camaron/chasko_attack_*`

#### Recibir daño / aturdido

![[05 - Arte y Audio/Galería de Assets/Jefes/Chasko/chasko_hit.gif]]

**3 cuadros** · 90×90 px · 100 ms por cuadro · 0,3 s · una vez

![[05 - Arte y Audio/Galería de Assets/Jefes/Chasko/chasko_hit_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Jefe_Camaron/chasko_hit_*`

#### Muerte

![[05 - Arte y Audio/Galería de Assets/Jefes/Chasko/chasko_death.gif]]

**8 cuadros** · 90×90 px · 100–400 ms por cuadro · 1,18 s · una vez

![[05 - Arte y Audio/Galería de Assets/Jefes/Chasko/chasko_death_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Jefe_Camaron/chasko_death_*`

La burbuja que dispara está en [[#Burbuja de Chasko]].

### La Entidad (Titán Blanco)

El cuerpo no es una sola animación: el juego lo arma con piezas. La cabeza y el torso suben y bajan juntos; los antebrazos se estiran del codo (dibujado en el torso) a la muñeca de cada mano. Los ojos, el núcleo y el brillo de la palma son blancos y el juego los tiñe del color del ataque.

| Dato | Valor |
| --- | --- |
| Píxeles por unidad | 12,5 |
| Fuente | `Documents/sprites/Jefe_Titan_Blanco/*.aseprite` |
| Carpeta | `Assets/Art/Sprites/Characters/Jefe_Titan/` |
| Escena de prueba | `Sandbox_Jefe` |

#### Cuerpo completo

Armado con las mismas posiciones que usa el juego, con las manos en reposo.

![[05 - Arte y Audio/Galería de Assets/Jefes/La Entidad/titan_cuerpo_reposo.gif]]

#### Piezas

![[05 - Arte y Audio/Galería de Assets/Jefes/La Entidad/titan_piezas.png]]

| Pieza | Archivo | Tamaño | Uso |
| --- | --- | --- | --- |
| Cabeza | `titan_cabeza.png` | 82 × 111 | También `titan_cabeza_expuesta.png` cuando baja la cabeza. |
| Ojos | `titan_ojos.png` | 82 × 111 | Encima de la cabeza; se tiñen. |
| Torso con brazos | `titan_torso.png` | 192 × 371 | Incluye los brazos hasta el codo. |
| Núcleo | `titan_nucleo.png` | 33 × 33 | Brillo del pecho; se tiñe. |
| Antebrazo | `titan_antebrazo.png` | 30 × 94 | Pivote arriba; se estira hasta la muñeca. |
| Mano | `titan_mano_01` … `07.png` | 96 × 160 | Mano derecha; la izquierda se voltea. Se muestra al 85 %. |
| Brillo de palma | `titan_mano_brillo.png` | 96 × 160 | Se tiñe al preparar un ataque. |

#### Manos


| Animación | Cuadros | Velocidad | Duración | Bucle |
| --- | --- | --- | --- | --- |
| Mano en reposo | 4 | 160 ms por cuadro | 0,64 s | Sí |
| Mano cansada | 4 | 160 ms por cuadro | 0,64 s | Sí |
| Mano rota | 1 | 500 ms por cuadro | 0,5 s | Sí |


##### Mano en reposo

![[05 - Arte y Audio/Galería de Assets/Jefes/La Entidad/titan_mano_reposo.gif]]

**4 cuadros** · 96×160 px · 160 ms por cuadro · 0,64 s · en bucle

Cuadros 1-3 de ida y vuelta.

![[05 - Arte y Audio/Galería de Assets/Jefes/La Entidad/titan_mano_reposo_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Jefe_Titan/titan_mano_01-03`

##### Mano cansada

![[05 - Arte y Audio/Galería de Assets/Jefes/La Entidad/titan_mano_cansada.gif]]

**4 cuadros** · 96×160 px · 160 ms por cuadro · 0,64 s · en bucle

Cuadros 4-6 de ida y vuelta.

![[05 - Arte y Audio/Galería de Assets/Jefes/La Entidad/titan_mano_cansada_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Jefe_Titan/titan_mano_04-06`

##### Mano rota

![[05 - Arte y Audio/Galería de Assets/Jefes/La Entidad/titan_mano_rota.gif]]

**1 cuadros** · 96×160 px · 500 ms por cuadro · 0,5 s · en bucle

Cuadro 7, fijo.

![[05 - Arte y Audio/Galería de Assets/Jefes/La Entidad/titan_mano_rota_cuadros.png]]

Origen: `Assets/Art/Sprites/Characters/Jefe_Titan/titan_mano_07`

#### Fondo de la arena

![[05 - Arte y Audio/Galería de Assets/Jefes/La Entidad/titan_fondo.png]]

![[05 - Arte y Audio/Galería de Assets/Jefes/La Entidad/titan_fondo_niebla.png]]

`titan_fondo.png` (silueta del titán al fondo) y `titan_fondo_niebla.png` (niebla del suelo), 340 × 464 px.

Sus ataques usan el [[#Rayo]], el [[#Tornado]] y el [[#Orbe]].

### Jefe 2 — Mago oscuro y Jefe 3 — Serpiente gigante

Sin arte todavía.

---

## Efectos

### Rayo

Lluvia de rayos de La Entidad. 120 × 240 px, 16 píxeles por unidad, pivote abajo al centro (en el suelo). Carpeta `Assets/Art/Sprites/Effects/Titan_Rayo/`.


| Animación | Cuadros | Velocidad | Duración | Bucle |
| --- | --- | --- | --- | --- |
| Secuencia completa | 32 | 60–90 ms por cuadro | 2,14 s | No |
| Aviso (bucle) | 6 | 90 ms por cuadro | 0,54 s | Sí |
| Aviso final, caída e impacto | 19 | 60–70 ms por cuadro | 1,18 s | No |
| Disipación | 7 | 60 ms por cuadro | 0,42 s | No |


#### Secuencia completa

![[05 - Arte y Audio/Galería de Assets/Efectos/rayo_completo.gif|200]]

**32 cuadros** · 120×240 px · 60–90 ms por cuadro · 2,14 s · una vez

Aviso (1-6, en bucle mientras dura), aviso final (7-10), caída (11-21; toca el suelo en el 20), impacto (22-25) y disipación (26-32).

![[05 - Arte y Audio/Galería de Assets/Efectos/rayo_completo_cuadros.png]]

Origen: `Assets/Art/Sprites/Effects/Titan_Rayo/`

#### Aviso (bucle)

![[05 - Arte y Audio/Galería de Assets/Efectos/rayo_aviso.gif|200]]

**6 cuadros** · 120×240 px · 90 ms por cuadro · 0,54 s · en bucle

![[05 - Arte y Audio/Galería de Assets/Efectos/rayo_aviso_cuadros.png]]

Origen: `Assets/Art/Sprites/Effects/Titan_Rayo/rayo_01-06`

#### Aviso final, caída e impacto

![[05 - Arte y Audio/Galería de Assets/Efectos/rayo_caida.gif|200]]

**19 cuadros** · 120×240 px · 60–70 ms por cuadro · 1,18 s · una vez

![[05 - Arte y Audio/Galería de Assets/Efectos/rayo_caida_cuadros.png]]

Origen: `Assets/Art/Sprites/Effects/Titan_Rayo/rayo_07-25`

#### Disipación

![[05 - Arte y Audio/Galería de Assets/Efectos/rayo_disipacion.gif|200]]

**7 cuadros** · 120×240 px · 60 ms por cuadro · 0,42 s · una vez

![[05 - Arte y Audio/Galería de Assets/Efectos/rayo_disipacion_cuadros.png]]

Origen: `Assets/Art/Sprites/Effects/Titan_Rayo/rayo_26-32`

### Tornado

Tornado morado de La Entidad que persigue a Eon; solo se esquiva con dash. 72 × 72 px, 11 píxeles por unidad, pivote abajo. Carpeta `Assets/Art/Sprites/Effects/Titan_Tornado/`.


| Animación | Cuadros | Velocidad | Duración | Bucle |
| --- | --- | --- | --- | --- |
| Secuencia completa | 22 | 80–91 ms por cuadro | 1,87 s | No |
| Movimiento (bucle) | 5 | 91 ms por cuadro | 0,46 s | Sí |


#### Secuencia completa

![[05 - Arte y Audio/Galería de Assets/Efectos/tornado_completo.gif]]

**22 cuadros** · 72×72 px · 80–91 ms por cuadro · 1,87 s · una vez

Aparición (1-7), movimiento en bucle (8-12, aquí 2 vueltas) y desaparición (13-17).

![[05 - Arte y Audio/Galería de Assets/Efectos/tornado_completo_cuadros.png]]

Origen: `Assets/Art/Sprites/Effects/Titan_Tornado/`

#### Movimiento (bucle)

![[05 - Arte y Audio/Galería de Assets/Efectos/tornado_movimiento.gif]]

**5 cuadros** · 72×72 px · 91 ms por cuadro · 0,46 s · en bucle

![[05 - Arte y Audio/Galería de Assets/Efectos/tornado_movimiento_cuadros.png]]

Origen: `Assets/Art/Sprites/Effects/Titan_Tornado/tornado_08-12`

### Orbe

Orbe amarillo que sale de la palma de La Entidad y persigue a Eon; se destruye de un golpe. 52 × 52 px, 40 píxeles por unidad, pivote al centro. Carpeta `Assets/Art/Sprites/Effects/Titan_Orbe/`.


| Animación | Cuadros | Velocidad | Duración | Bucle |
| --- | --- | --- | --- | --- |
| Secuencia completa | 19 | 70–90 ms por cuadro | 1,6 s | No |
| Movimiento (bucle) | 6 | 90 ms por cuadro | 0,54 s | Sí |


#### Secuencia completa

![[05 - Arte y Audio/Galería de Assets/Efectos/orbe_completo.gif]]

**19 cuadros** · 52×52 px · 70–90 ms por cuadro · 1,6 s · una vez

Aparición (1-4), movimiento en bucle (5-10, aquí 2 vueltas) y muerte (11-13).

![[05 - Arte y Audio/Galería de Assets/Efectos/orbe_completo_cuadros.png]]

Origen: `Assets/Art/Sprites/Effects/Titan_Orbe/`

#### Movimiento (bucle)

![[05 - Arte y Audio/Galería de Assets/Efectos/orbe_movimiento.gif]]

**6 cuadros** · 52×52 px · 90 ms por cuadro · 0,54 s · en bucle

![[05 - Arte y Audio/Galería de Assets/Efectos/orbe_movimiento_cuadros.png]]

Origen: `Assets/Art/Sprites/Effects/Titan_Orbe/orbe_05-10`

### Burbuja de Chasko

Burbuja de cavitación del chasquido: avanza a ras de suelo y estalla al chocar o al recibir un golpe. 46 × 46 px, 16 píxeles por unidad. Fuente `Chasko_Burbuja.aseprite`; carpeta `Assets/Art/Sprites/Effects/Chasko_Burbuja/`.


| Animación | Cuadros | Velocidad | Duración | Bucle |
| --- | --- | --- | --- | --- |
| Avanzar (bucle) | 6 | 90 ms por cuadro | 0,54 s | Sí |
| Estallido | 7 | 70 ms por cuadro | 0,49 s | No |


#### Avanzar (bucle)

![[05 - Arte y Audio/Galería de Assets/Efectos/burbuja_mover.gif]]

**6 cuadros** · 46×46 px · 90 ms por cuadro · 0,54 s · en bucle

![[05 - Arte y Audio/Galería de Assets/Efectos/burbuja_mover_cuadros.png]]

Origen: `Assets/Art/Sprites/Effects/Chasko_Burbuja/burbuja_mover_*`

#### Estallido

![[05 - Arte y Audio/Galería de Assets/Efectos/burbuja_explosion.gif]]

**7 cuadros** · 46×46 px · 70 ms por cuadro · 0,49 s · una vez

![[05 - Arte y Audio/Galería de Assets/Efectos/burbuja_explosion_cuadros.png]]

Origen: `Assets/Art/Sprites/Effects/Chasko_Burbuja/burbuja_explosion_*`

---

## Habilidades

### Camarón de Chasko (drop del Doble salto)

Lo suelta Chasko al morir. Versión reducida de la ilustración de referencia: 16 × 16 px con la paleta naranja del jefe y sin contorno negro; en el mundo usa un lienzo de 20 × 20 px para los destellos.

| Animación | Cuadros | Velocidad | Duración | Bucle |
| --- | --- | --- | --- | --- |
| Brillo | 8 | 70–260 ms por cuadro | 0,88 s | Sí |

![[05 - Arte y Audio/Galería de Assets/Habilidades/camaron_chasko_brillo.gif]]

![[05 - Arte y Audio/Galería de Assets/Habilidades/camaron_chasko_cuadros.png]]

Icono del inventario:

![[05 - Arte y Audio/Galería de Assets/Habilidades/camaron_chasko_icono.png]]

Origen: `Assets/Resources/Habilidades/camaron_doble_salto_*` (fuente: `Documents/sprites/Jefe_Camaron/Drop_Doble_Salto/Camaron_Doble_Salto.aseprite`).

### Burbuja del doble salto

Aparece bajo los pies de Eon en el segundo salto, se aplasta con el impulso y estalla en gotitas. Usa los colores de la burbuja de Chasko.

| Animación | Cuadros | Velocidad | Duración | Bucle |
| --- | --- | --- | --- | --- |
| Aparecer | 3 | 40–60 ms por cuadro | 0,15 s | No |
| Estallar | 4 | 50–80 ms por cuadro | 0,26 s | No |
| Burbujita | 1 | — | 0,4–0,6 s (sube y se desvanece) | No |

El GIF va a un tercio de la velocidad real para que se vea.

![[05 - Arte y Audio/Galería de Assets/Habilidades/burbuja_doble_salto.gif]]

![[05 - Arte y Audio/Galería de Assets/Habilidades/burbuja_doble_salto_cuadros.png]]

Origen: `Assets/Resources/Habilidades/burbuja_doble_salto_*` (fuente: `Burbuja_Doble_Salto.aseprite`).

---

## Entornos del mapa jugable

Arte de escenario que ya usa el mapa `Eretz_Mapa` (detalle técnico en [[03 - Entornos]]). Imágenes generadas el 09/11/2026.

### Mapa completo

Vista de todo el recorrido con los enemigos (E = Earthlem, A = Aurion), puntos de control (CP), géiseres (G y su trayectoria) y la meta.

![[05 - Arte y Audio/Galería de Assets/Entornos/mapa_eretz_completo.png]]

### Costa

![[05 - Arte y Audio/Galería de Assets/Entornos/costa.png]]

Mar animado (3 cuadros, unos 300 ms por cuadro):

![[05 - Arte y Audio/Galería de Assets/Entornos/costa_mar_animado.gif]]

Origen: `Assets/Art/Sprites/Environment/Costa_Dia/` (fuente editable: `Documents/sprites/Escenario/Costa_Dia/Estilo_SSW/`).

### Zona 3: templo en ruinas

Vista con la cámara del juego, el cielo de la costa y Eon como referencia de tamaño.

![[05 - Arte y Audio/Galería de Assets/Entornos/zona3_templo.png]]

Origen: `Assets/Art/Sprites/Environment/Templo_Ruinas/Fondo/`.

### Columnas de las ruinas

Columna entera, rota alta, rota baja, caída, capitel caído y arco en ruinas.

![[05 - Arte y Audio/Galería de Assets/Entornos/columnas_ruinas.png]]

Origen: `Assets/Art/Sprites/Environment/Ruinas/`.

### Islas flotantes

![[05 - Arte y Audio/Galería de Assets/Entornos/islas.png]]

Origen: `Assets/Art/Sprites/Environment/SSW_Set3/Tiles/isla_*` y `Assets/Art/Sprites/Environment/Islas_Deco/`.

### Géiser

| Animación | Cuadros | Velocidad | Duración | Bucle |
| --- | --- | --- | --- | --- |
| Reposo | 8 | 110 ms por cuadro | 0,88 s | Sí |
| Erupción | 10 | 70 ms por cuadro | 0,7 s | No (al lanzar a Eon) |

![[05 - Arte y Audio/Galería de Assets/Entornos/geiser.gif]]

![[05 - Arte y Audio/Galería de Assets/Entornos/geiser_cuadros.png]]

Origen: `Assets/Art/Sprites/Environment/Geiser/` (64×128 px, pivote abajo al centro).

### Muro de la arena de Chasko

Muro a su altura real en la arena (14 u) y los escombros en que se rompe.

![[05 - Arte y Audio/Galería de Assets/Entornos/muro_arena_chasko.png]]

Origen: `Assets/Resources/Arena/`.

---

> **Navegación:** [[00 - Índice]] · ← [[05 - Audio y Música]]
