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
| Ruinas Abandonadas | 7 min | Earthlem, Vestigio | Torre sellada (Tajo ardiente: interruptor lejano): atajo y Vestigios | Mitad y antesala del Jefe 2 |
| Patio de la Academia | 3 min | Jefe 2 | — | — |
| Archipiélago de Tierra | 9 min | Aurion, Vestigio, Earthlem | Islas altas (Doble salto + géiser): grupo de enemigos | Mitad y antesala del Jefe 3 |
| Anillo de Islas | 4 min | Jefe 3 | — | — |
| Puente e Isla Final | 6 min | La Entidad, Vestigios | — | Antesala de la Isla Final |

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

- Playa plana de 28 u de ancho con el mar en el lado derecho. Sin plataformas: el combate es a ras de suelo.
- **Límites invisibles** a ambos lados mientras dura el combate.

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
- **Enemigos:** Earthlem, primer Vestigio.
- **Puntos de control:** mitad del recorrido y antesala (mercader).

## Patio de la Academia (Jefe 2)

- Arena **completamente plana**, 36 u de ancho, sin plataformas, dentro de las ruinas.
- Al entrar, **pilares de piedra de las ruinas** emergen del suelo en ambos extremos y bloquean el paso; se hunden al morir el jefe. Es la única arena con límites visibles.
- Al vencer al jefe se activan los géiseres que llevan al Archipiélago.

## Archipiélago de Tierra

- **Objetivo principal:** cruzar las islas hasta el Anillo de Islas.
- **Duración:** 9 minutos. **Dificultad:** alta.
- **Mecánicas introducidas:** géiseres; combate en islas pequeñas sobre el vacío.
- **Enemigos:** Aurion, Vestigio, Earthlem.
- **Puntos de control:** mitad del recorrido y antesala (mercader).

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
