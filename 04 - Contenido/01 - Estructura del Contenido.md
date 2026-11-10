# Estructura del Contenido

El juego es un recorrido por zonas conectadas en un orden principal, con rutas opcionales que se abren con habilidades. Cada bloque termina en una antesala con el mercader y un jefe que entrega una habilidad. Las zonas superadas siguen abiertas para volver a acumular XP.

## Estructura

```text
True Hero
├── Prólogo: cómic «La caída del elegido» (derrota de Eon)
├── Bloque 1 — La Costa
│   ├── Playa del Despertar (tutorial)
│   ├── Acantilados de la Costa (zona explorable)
│   ├── Antesala: mercader + punto de control
│   └── Arena de la Marea → Jefe 1: Chasko → Doble salto
├── Bloque 2 — Tierra adentro
│   ├── Bosque de Raíces (zona explorable)
│   ├── Ruinas Abandonadas (zona explorable)
│   ├── Antesala: mercader + punto de control
│   └── Patio de la Academia → Jefe 2 (opcional): Mago oscuro → Tajo ardiente + Dash cortante
├── Bloque 3 — El cielo roto
│   ├── Archipiélago de Tierra (zona explorable con géiseres)
│   ├── Antesala: mercader + punto de control
│   └── Anillo de Islas → Jefe 3: Serpiente gigante → Escama pétrea
│       └── Cinemática: la serpiente se petrifica
└── Final
    ├── Puente de la Serpiente
    ├── Antesala: mercader (regalo) + punto de control
    └── Isla Final → La Entidad → Final y créditos
```

## Cantidad estimada

| Tipo | Cantidad |
| --- | ---: |
| Bloques | 3 + final |
| Zonas explorables | 5 |
| Arenas de jefe | 4 |
| Jefes normales | 3 |
| Jefe final | 1 |
| Enemigos comunes | 2 |
| NPC | 1 (mercader) |
| Habilidades | 4 |
| Potenciadores | 6 |
| Puntos de control | ~10 (2 por zona, 1 en cada antesala) |
| Apariciones del mercader | 4 (una antesala por jefe) |

## Dependencias

| Contenido | Requiere antes |
| --- | --- |
| Mercader | Llegar a la antesala del Jefe 1. |
| Jefe 1 | Salto, dash y combo enseñados en la Playa y los Acantilados. |
| Jefe 2 | Earthlem presentado en Bosque y Ruinas. |
| Archipiélago de Tierra | Cruzar las Ruinas (el Jefe 2 es opcional; los géiseres funcionan siempre). |
| Jefe 3 | Géiseres y plataformas pequeñas dominados en el Archipiélago. |
| Isla Final | Jefe 3 derrotado (puente petrificado). |
| Rutas opcionales | Doble salto o Tajo ardiente equipados (nunca obligatorias). |

> **Navegación:** [[00 - Índice]] · ← [[04 - Diálogos y Narrativa]] · [[02 - Niveles]] →
