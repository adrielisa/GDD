# Niveles y zonas

Cada zona tiene una ruta principal que se puede completar sin ninguna habilidad concreta y rutas opcionales que piden Doble salto o Tajo ardiente. Las rutas opcionales ofrecen atajos y grupos de enemigos que dan más XP. No hay objetos que recoger aparte de la XP.

Antes de cada jefe hay una **antesala** con el mercader y un punto de control. Las zonas superadas siguen abiertas: sus enemigos reaparecen y se puede volver a acumular XP.

## Resumen de zonas

| Zona | Duración | Enemigos | Rutas opcionales | Puntos de control |
| --- | --- | --- | --- | --- |
| Playa del Despertar | 3 min | Aurion | — | Inicio |
| Acantilados de la Costa | 6 min | Aurion | Cueva superior (Doble salto): grupo de Aurion | Mitad y antesala del Jefe 1 |
| Arena de la Marea | 3 min | Jefe 1 (Chasko) | — | — |
| Bosque de Raíces | 8 min | Aurion, Earthlem | Copa de los árboles (Doble salto): atajo | Entrada y salida |
| Ruinas Abandonadas | 7 min | Earthlem | Torre sellada (Tajo ardiente: interruptor lejano): atajo y grupo de enemigos | Mitad y antesala del Jefe 2 |
| Patio de la Academia | 3 min | Jefe 2 | — | — |
| Archipiélago de Tierra | 9 min | Aurion | Islas altas (Doble salto + géiser): grupo de enemigos | Mitad y antesala del Jefe 3 |
| Anillo de Islas | 4 min | Jefe 3 | — | — |
| Puente e Isla Final | 6 min | La Entidad | — | Antesala de la Isla Final |

## Mapa jugable actual (Eretz_Mapa)

Prototipo en Unity que reúne en un solo mapa la Costa, el Jefe 1, la zona 3 (Bosque de Raíces y Ruinas Abandonadas), la arena del Jefe 2 y el Archipiélago. Sirve para probar el ritmo del recorrido antes de dividirlo en zonas. Todo el recorrido de abajo es la ruta principal: se completa sin habilidades.

- **Escena:** `Assets/Scenes/Levels/Eretz_Mapa.unity`. La forma del mapa sale de `Assets/Scripts/Levels/Editor/Datos/eretz_mapa.json` y de `EretzMapaGenerator`; la escena se puede editar a mano y no se regenera sola (si el generador cambia la forma del mapa, antes guarda una copia en `Assets/Scenes/Levels/Respaldos/`).
- **Tamaño:** 368 u de ancho (antes 230 u). Se alargó un 60 % para que el recorrido no sea tan rápido: tramo de tutorial de combate antes de Chasko, sendero de transición después de Chasko, meseta antes del Mago y más espacio entre islas.
- **Escala:** 1 u = 21,5 px de arte; tiles de 16 px (0,744 u). La cámara muestra 216 px de alto con los pies de Eon al 18 % de la pantalla.

| # | Tramo | x (u) | Equivale a | Enemigos | Puntos de control y otros |
| --- | --- | --- | --- | --- | --- |
| 1 | Costa | −83 a −51 | Playa del Despertar | — | Inicio sobre una roca. |
| 2 | Primeros enemigos | −51 a 18 | Acantilados de la Costa | 4 Aurion (primero solos, luego en pareja) | `Costa_Tutorial`; escalones de roca para llegar a la arena; `Costa_Antes_Chasko`. |
| 3 | Arena de Chasko | 20 a 46 | Arena de la Marea | Jefe 1 | Muros de roca que emergen al empezar (ver abajo). |
| 4 | Sendero al templo | 46 a 81 | Bosque de Raíces | 1 Earthlem, 1 Aurion | `Despues_Chasko`; columnas de ruinas; fondo del templo. |
| 5 | Torre de los Earthlem | 81 a 119 | Ruinas Abandonadas | 3 Earthlem | Repisas; géiser `Torre_Repisa` a la cima; `Torre_Arriba`; 2 estatuas (NPC). |
| 6 | Meseta | 119 a 158 | Antesala del Jefe 2 | 2 Earthlem, 1 Aurion | `Antes_Mago`. |
| 7 | Templo del Mago | 159 a 177 | Patio de la Academia | Jefe 2 *(opcional, en la escena `Ruina_Mago`)* | Fachada del templo con ruinas detrás; se entra con Interactuar (ver abajo). |
| 8 | Después del Mago | 177 a 207 | Salida de las Ruinas | 2 Aurion | `Despues_Mago`; géiser `Torre_Cima` a la isla A. |
| 9 | Islas A–E | 167 a 266 (alto 31–71) | Archipiélago de Tierra | 5 Aurion | Géiseres A, B, C y E; `Isla_A`, `Isla_D`. |
| 10 | Isla final | 233 a 285 (alto 82) | Anillo de Islas | 1 Aurion; Driller *(provisional, ver [[03 - Enemigos y NPC]])* | `Isla_Final`; arena del gusano y meta. |

- **Earthlem solo en la zona 3** (tramos 4 a 6). En la costa, después del Mago y en las islas solo hay Aurion.
- **Saltos verificados:** se simuló el salto de Eon (carrera 7,6 u/s, salto 3,6 u, salto corto y dash aéreo) desde todas las plataformas. Todo el recorrido se puede completar en orden y no se puede llegar a una sección posterior sin su géiser. Para conseguirlo se separaron las islas B y C (antes se saltaba de una a otra sin el géiser) y se quitó la colisión a los muros de la arena del Mago (cerraban el paso y el mapa no se podía terminar).
- **Orbes de vida:** el prototipo tiene 4 (tutorial, sendero, antes del Mago e isla final). Contradicen la regla de no curar en el campo; queda pendiente decidir si se quitan (P-05 en [[03 - Registro de Decisiones]]).
- **Fondos:** cielo y nubes de la costa en todo el mapa; la costa tiene acantilados y mar animado, y la zona 3 el templo en ruinas (ver [[03 - Entornos]]).

![[05 - Arte y Audio/Galería de Assets/Entornos/mapa_eretz_completo.png]]

### Templo del Mago (entrada y escena `Ruina_Mago`)

- **Entrada en Eretz:** fachada del templo centrada en la arena (x ≈ 168), con una capa de ruinas detrás (torre rota, nave derrumbada y columnata suelta). Al acercarse aparece el aviso «[E] Entrar al templo»; con Interactuar la pantalla se funde a negro y Eon aparece dentro. La puerta solo funciona mientras el Mago siga vivo. Se quitó el pilar de piedra que quedaba de la antigua arena junto a `Despues_Mago`.
- **Escena `Ruina_Mago`:** `Assets/Scenes/Levels/Ruina_Mago.unity`, creada por `RuinaMagoGenerator` (y ajustada sin regenerar por `RuinaMagoTemploAjustes`).
    - Sala de x −22 a +22 (44 u) entre dos muros del templo; techo a 13 u.
    - Entrada en `Checkpoint_Entrada_Ruina` (x −18). Puerta izquierda (x −20,6): vuelve a Eretz, a `Antes_Mago`. Puerta derecha (x 18): solo tras vencer al Mago, lleva a `Despues_Mago`.
    - La pelea empieza al pasar x ±15; el Mago se mueve y se teletransporta entre x −20 y +20.
    - La cámara se detiene en el borde exterior de los muros (x ±28).
- **Estado entre escenas:** jefes derrotados, habilidades y materiales se conservan al cambiar de escena (solo durante la partida; aún no hay guardado en disco).

![[05 - Arte y Audio/Galería de Assets/Entornos/templo_mago_entrada_eretz.png]]

## Playa del Despertar

- **Objetivo principal:** enseñar movimiento, salto, combo y dash con un Eon debilitado.
- **Objetivos secundarios:** presentar la XP y la silueta de La Entidad.
- **Duración:** 3 minutos. **Dificultad:** baja.
- **Mecánicas introducidas:** movimiento, salto, ataque, ataque descendente, dash.
- **Enemigos:** 4 Aurion aislados.
- **Recompensas:** XP.
- **Entrada:** fin del prólogo. **Salida:** borde derecho hacia los Acantilados.
- **Eventos:** despertar de Eon.

```text
Despertar → Primeros Aurion → Punto de control → Acantilados
```

## Acantilados de la Costa

- **Objetivo principal:** llegar a la antesala del Jefe 1.
- **Objetivos secundarios:** explorar cuevas marinas y faros caídos.
- **Duración:** 6 minutos. **Dificultad:** media-baja.
- **Mecánicas utilizadas:** saltos sobre precipicios, dash aéreo, rebote sobre Aurion.
- **Enemigos:** grupos de 2–3 Aurion.
- **Puntos de control:** mitad del recorrido y antesala.
- **Eventos:** en la antesala aparece el mercader por primera vez y abre la tienda.

```text
Entrada → Faro caído → Cuevas marinas → Punto de control → Antesala (mercader) → Arena de la Marea
                         └── Cueva superior (Doble salto, opcional)
```

## Arena de la Marea (Jefe 1)

- Playa plana de unas 26 u de ancho con el mar al fondo. Sin plataformas: el combate es a ras de suelo.
- **Muros de roca:** al empezar el combate, un pilar de roca emerge del suelo en cada extremo (unos 0,6 s) con una sacudida de pantalla y piedritas en la base, y cierra la arena. Al vencer a Chasko, los muros tiemblan, se rompen en escombros y desaparecen. Si Eon cae o es derrotado durante el combate, los muros bajan y la arena se reinicia.

## Bosque de Raíces

- **Objetivo principal:** atravesar el bosque hasta las Ruinas.
- **Duración:** 8 minutos. **Dificultad:** media.
- **Mecánicas:** plataformas verticales sobre raíces (alcanzables con salto y dash).
- **Enemigos:** Aurion, primer Earthlem.
- **Puntos de control:** entrada y salida.
- **Entrada:** salida de la Arena de la Marea. **Salida:** camino hacia las Ruinas.

## Ruinas Abandonadas

- **Objetivo principal:** llegar al Patio de la Academia.
- **Objetivos secundarios:** explorar aulas derrumbadas y torres.
- **Duración:** 7 minutos. **Dificultad:** media-alta.
- **Enemigos:** Earthlem.
- **Puntos de control:** mitad del recorrido y antesala (mercader).

## Patio de la Academia (Jefe 2)

- **Jefe opcional:** la entrada es un templo junto al camino; se puede pasar de largo.
- La arena es el **interior del templo**: sala **completamente plana** de 44 u, sin plataformas, cerrada por los muros del templo.
- Al empezar el combate las puertas quedan selladas hasta que muere el jefe o cae Eon. No hay pilares que emerjan.
- El Archipiélago no depende del jefe: los géiseres funcionan siempre.

## Archipiélago de Tierra

- **Objetivo principal:** cruzar las islas hasta el Anillo de Islas.
- **Duración:** 9 minutos. **Dificultad:** alta.
- **Mecánicas introducidas:** géiseres; combate en islas pequeñas sobre el vacío.
- **Enemigos:** Aurion. Los Earthlem no salen de la zona 3 (Bosque y Ruinas).
- **Puntos de control:** mitad del recorrido y antesala (mercader).
- **Islas:** superficie de pasto y tierra; por debajo cuelgan formaciones de roca en forma de pirámide invertida, con lianas.

```text
Géiser de las Ruinas → Isla 1 → Géiser → Isla 2 (punto de control) → Géiser → Islas 3–4 → Antesala (mercader) → Anillo de Islas
                                                      └── Islas altas (opcional)
```

## Anillo de Islas (Jefe 3)

- 7 plataformas de tierra flotantes en dos alturas, separadas a distancias que se cubren con salto y dash (el Doble salto facilita, pero no es necesario). La serpiente las rodea y las atraviesa.
- **Límites invisibles** a los lados; el vacío inferior aplica la regla de caída.
- Al vencer: ilustración de la serpiente petrificada; su cuerpo forma el Puente de la Serpiente.

## Puente de la Serpiente e Isla Final (La Entidad)

- **Puente:** tramo corto y sin enemigos sobre el cuerpo de piedra; termina en la última antesala, donde el mercader regala un potenciador.
- **Isla Final:** combate en fases con **límites invisibles**. La primera fase recupera la estructura del encuentro original (islas ascendentes, géiseres en lugar de trampolines, cañones y el titán al fondo). Detalle en [[03 - Enemigos y NPC]].

## Criterios de calidad

- El objetivo de cada zona se entiende sin texto.
- La ruta principal nunca exige una habilidad concreta; las rutas opcionales muestran qué falta.
- La distancia entre puntos de control es justa, porque no hay curación en el campo.
- Cada zona enseña lo que su jefe va a exigir.

> **Navegación:** [[00 - Índice]] · ← [[01 - Estructura del Contenido]] · [[03 - Enemigos y NPC]] →
