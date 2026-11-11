# Reglas y Estados del Juego

## Estados principales

- **Menú principal:** nueva partida, continuar, configuración, créditos y salir.
- **Carga:** transición entre escenas; inicializa assets, reinicia *pools* de objetos y coloca entidades.
- **Prólogo (cómic):** secuencia de viñetas que termina con la derrota de Eon; se puede omitir.
- **Jugando (exploración):** control directo de Eon en una zona.
- **Arena de jefe:** variante de Jugando con límites cerrados, cámara confinada y equipo fijado.
- **Inventario:** simulación pausada; permite ver la descripción de todo lo obtenido y cambiar habilidades y potenciadores equipados (fuera de una arena de jefe).
- **Tienda:** simulación pausada mientras se compra con el mercader.
- **Cinemática:** ilustraciones fijas o breves (habilidad obtenida, serpiente petrificada, final). Control bloqueado.
- **Pausa:** `Time.timeScale = 0`; reanudar, volver al último punto de control, configuración o salir al menú.
- **Derrota:** animación de colapso y opción de reaparecer en el último punto de control o salir al menú.
- **Victoria:** al derrotar a La Entidad; lleva al final y a los créditos.
- **Créditos:** desde el menú o tras la victoria.

## Transiciones

| Estado origen | Evento | Estado destino | Condición |
| --- | --- | --- | --- |
| Menú principal | `OnNewGame` | Prólogo | Nueva partida (con confirmación si existe un guardado). |
| Menú principal | `OnContinue` | Carga | Existe guardado; carga la zona del último punto de control. |
| Menú principal | `OnShowCredits` | Créditos | Selección manual. |
| Prólogo | `OnPrologueEnd` | Carga | Última viñeta o mantener `Escape`/`Start` 1,5 s. |
| Carga | `OnSceneLoaded` | Jugando | Zona lista. |
| Jugando | `OnEnterBossArena` | Arena de jefe | Eon cruza el trigger de entrada; se cierran los límites. |
| Arena de jefe | `OnBossDefeated` | Cinemática | Muere el jefe y Eon sigue vivo. |
| Cinemática | `OnCinematicEnd` | Jugando | Habilidad guardada; vida y escudo restaurados; se abren los límites. |
| Jugando | `OnInventoryPressed` | Inventario | — (dentro de una arena, solo lectura). |
| Inventario | `OnInventoryClosed` | Estado previo | — |
| Jugando | `OnInteractSeller` | Tienda | Antesala de un jefe. |
| Tienda | `OnShopClosed` | Jugando | — |
| Jugando / Arena de jefe | `OnPausePressed` | Pausa | `Escape` / `Start`. |
| Pausa | `OnResumePressed` | Estado previo | — |
| Pausa | `OnRestartCheckpoint` | Carga | Volver al último punto de control. |
| Pausa | `OnExitToMenu` | Carga | Confirmación previa. |
| Jugando / Arena de jefe | `OnPlayerDeath` | Derrota | Vida en 0 o instakill. |
| Derrota | `OnRetryCheckpoint` | Carga | — |
| Derrota | `OnExitToMenu` | Carga | — |
| Arena de jefe (Isla Final) | `OnFinalBossDefeated` | Victoria | Muere La Entidad con Eon vivo. |
| Victoria | `OnVictoryEnd` | Créditos | Termina la secuencia final. |
| Créditos | `OnCreditsEnd` | Menú principal | Fin del desplazamiento u omisión. |

## Reglas globales

- **Sin curación en el campo:** vida y escudo solo se restauran al tocar un punto de control, al vencer a un jefe o al reaparecer tras una derrota.
- **Pausa absoluta:** pausa, inventario y tienda detienen el tiempo de juego, los enemigos y las animaciones; los menús usan `Time.unscaledDeltaTime`.
- **Cinemáticas seguras:** durante introducciones de jefe, cambios de fase y cinemáticas, Eon y los enemigos son invulnerables.
- **Puntos de control:** al descansar o reaparecer, Eon vuelve al último punto visitado con vida y escudo completos, y los enemigos comunes reaparecen.
- **Equipo fijado en arena:** al entrar a una arena de jefe no se pueden cambiar habilidades ni potenciadores.
- **Límites de arena:** invisibles en los combates contra el Jefe 1, el Jefe 3 y La Entidad; en el del Jefe 2, los muros del templo, con las puertas selladas durante el combate.
- **Zonas reabiertas:** tras vencer a un jefe, las zonas anteriores siguen accesibles y sus enemigos reaparecen.
- **Persistencia:** XP, potenciadores, habilidades y jefes derrotados se guardan.

## Casos especiales

- **Derrota dentro de una arena:** el jefe vuelve a su vida completa y Eon reaparece en el punto de control de la antesala.
- **Muerte simultánea:** si Eon y el jefe llegan a 0 en el mismo fotograma, prevalece la **victoria**.
- **Instakill y defensas:** escudo y dash no protegen del instakill, y Espinas punzantes no se activa con él.
- **Caída al vacío:** −25 HP y regreso al último suelo seguro. En la arena del Jefe 3, el «último suelo seguro» es la plataforma central.
- **Habilidad nueva:** se guarda en el inventario sin descartar ninguna. Un aviso invita a abrir el inventario para equiparla.
- **Salir durante una cinemática de entrega:** la habilidad ya cuenta como obtenida y se guarda.

> **Navegación:** [[00 - Índice]] · ← [[06 - Economía y Recursos]] · [[01 - Premisa y Trama]] →
