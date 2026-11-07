# Datos y Persistencia

## Formato

- Archivo JSON en `Application.persistentDataPath/truehero_save.json`.
- Campo `version` para migrar formatos futuros.
- La configuración se guarda aparte en `PlayerPrefs`.

## Estructura del guardado

```json
{
  "version": 1,
  "checkpointId": "costa_antesala_jefe1",
  "xp": 340,
  "abilitiesOwned": ["double_jump"],
  "abilitiesEquipped": ["double_jump", null, null],
  "powerUpsOwned": ["vigor", "codicia"],
  "powerUpsEquipped": ["vigor", "codicia", null],
  "bossesDefeated": ["shrimp_serpent"],
  "tutorialsSeen": ["move", "attack", "dash", "shop"],
  "sellerGiftGiven": false
}
```

## Datos de diseño (ScriptableObjects)

| Asset | Campos principales |
| --- | --- |
| `AbilityDefinition` | id, nombre, función (texto del inventario), tecla de control, icono, tipo (pasiva/activa), recarga, daño. |
| `PowerUpDefinition` | id, nombre, función (texto del inventario), icono, modificadores, precio, antesala de desbloqueo. |
| `EnemyDefinition` | vida, velocidad, daño, detección, XP, probabilidades de orbe. |
| `BossAttack` | aviso, duración, daño, `isInstakill`, recarga, fase mínima, peso. |
| `BossDefinition` | vida, umbrales de fase, ataques, XP, habilidad que entrega. |

## Validación

- Identificadores desconocidos se ignoran.
- XP limitada a 0–9999.
- Nunca más de 3 habilidades ni 3 potenciadores equipados; si el archivo trae más, se conservan los 3 primeros.
- Solo se pueden equipar elementos que figuran como obtenidos o comprados.

> **Navegación:** [[00 - Índice]] · ← [[03 - Requisitos Técnicos]] · [[05 - Seguridad y Riesgos Técnicos]] →
