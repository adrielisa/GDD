# Arquitectura Técnica

Arquitectura **propuesta** para Unity. Los nombres de componentes son una guía; se actualizan cuando existan en el proyecto.

## Escenas

| Escena | Contenido |
| --- | --- |
| `MainMenu` | Menú principal y configuración. |
| `Prologue` | Cómic del prólogo. |
| `Zone_Costa` | Playa del Despertar, Acantilados y Arena de la Marea (Jefe 1). |
| `Zone_Bosque` | Bosque de Raíces. |
| `Zone_Ruinas` | Ruinas Abandonadas y Patio de la Academia (Jefe 2). |
| `Zone_Archipielago` | Archipiélago de Tierra y Anillo de Islas (Jefe 3). |
| `Zone_IslaFinal` | Puente de la Serpiente e Isla Final (La Entidad). |
| `Credits` | Final y créditos. |

Una escena persistente (`Bootstrap`) contiene los servicios globales que no se destruyen entre zonas.

**En el prototipo** hay dos escenas de juego: `Eretz_Mapa` (todo el recorrido) y `Ruina_Mago` (interior del templo, Jefe 2). Se cambia de una a otra con `PuertaEscena` + `TransicionEscena` (fundido a negro, carga de la escena y Eon colocado en un punto de control por nombre). `EstadoPartida` es un estado estático que sobrevive al cambio de escena: jefes derrotados, habilidades obtenidas y equipadas, y materiales.

## Componentes

| Responsabilidad | Componentes propuestos |
| --- | --- |
| Servicios globales | `GameManager`, `SceneLoader`, `SaveService`, `AudioManager` |
| Jugador | `PlayerInputReader`, `PlayerMotor`, `PlayerCombat`, `PlayerHealth`, `PlayerAbilities` |
| Habilidades | `AbilityDefinition` (ScriptableObject), `DoubleJumpAbility`, `FireSlashAbility`, `DashStrikeAbility`, `StoneScaleAbility` |
| Inventario | `Inventory`, `AbilityLoadout` (3 ranuras), `PowerUpLoadout` (3 ranuras), `ItemDescriptionPanel` |
| Potenciadores | `PowerUpDefinition` (ScriptableObject), `StatModifiers` (aplica los modificadores pasivos de los potenciadores equipados) |
| Economía | `XPWallet`, `XPOrb`, `ShopController`, `ShopCatalog` |
| Combate | `Hitbox`, `Hurtbox`, `DamageInfo` (incluye `isInstakill`), `Health` |
| Enemigos | `EnemyBrain`, `AurionAI`, `EarthlemAI`, `EnemyPool` |
| Jefes | `BossController`, `BossAttack` (ScriptableObject), `ShrimpSerpentBoss`, `DarkMageBoss`, `GiantSerpentBoss`, `EntityBoss` |
| Mundo | `WorldProgress`, `Checkpoint`, `AbilityGate`, `BossArena` (barreras invisibles o pilares), `Geyser`, `Cannon`, `WaterPlatform`, `RuinPillar`, `EnemyRespawner` |
| Cámara | `CameraDirector` (Cinemachine 2D + confinadores) |
| UI | `HUD`, `InventoryView`, `ShopView`, `BossHealthBar`, `PauseMenu`, `DialogueBox`, `ComicPlayer` |

## Principios

- **Datos en ScriptableObjects:** habilidades, potenciadores, ataques de jefe y valores de enemigos se editan sin tocar código.
- **Eventos:** daño, muerte, compra y entrega de habilidad se comunican por eventos (`OnEntityDeath`, `OnAbilityGranted`, `OnXPChanged`).
- **Reservas (*pools*):** tajos ardientes, orbes de XP, lágrimas de Cienojos, burbujas de Chasko y cráneos se reutilizan.
- **Separación lógica/presentación:** las reglas de combate no dependen de animaciones ni VFX.

> **Navegación:** [[00 - Índice]] · ← [[04 - Guardado y Configuración]] · [[02 - Motor y Herramientas]] →
