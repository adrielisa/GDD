# Reglas y Estados del Juego

## Descripción de la sección

Define las reglas globales y los estados que puede atravesar el videojuego.

## Estados principales

- Menú principal: Pantalla inicial del juego; permite iniciar una partida nueva, continuar con una existente, ajustar configuraciones de audio o salir de la aplicación.
- **Carga:** Pantalla de transición entre escenas que inicializa los assets requeridos, restablece los pools de objetos y posiciona las entidades en el mapa.
- **Jugando:** Bucle activo de gameplay; el jugador tiene control directo sobre el protagonista, la física se actualiza en tiempo real y la inteligencia artificial hostil procesa sus rutinas de combate.
- **Pausa:** Estado de suspensión de la simulación (`Time.timeScale = 0`); desactiva la captura de entradas del personaje y despliega el menú contextual con opciones para reanudar, reiniciar desde el último punto de control o volver al menú.
- **Victoria:** Secuencia detonada al derrotar al jefe final o superar el objetivo de la demo; se congelan las entradas de combate, se activa la animación de triunfo y se reproducen los efectos cinemáticos de finalización.
- **Derrota (Muerte y Reintento):** Estado detonado cuando la salud del protagonista llega a 0. Desactiva el control de ataque y movimiento, ejecuta una breve animación de colapso y despliega un mensaje inmediato en pantalla permitiendo presionar un botón para reaparecer de inmediato en el último punto de control guardado o para salir al menú.
- **Créditos:** Pantalla de reconocimiento al equipo de desarrollo, se accede desde el menú principal o automáticamente después de la pantalla de victoria.

## Transiciones

| **Estado origen**  | **Evento**            | **Estado destino** | **Condición**                                                                                                    |
| ------------------ | --------------------- | ------------------ | ---------------------------------------------------------------------------------------------------------------- |
| **Menú principal** | `OnStartGame`         | **Carga**          | El jugador presiona "Nueva partida" (inicia Nivel 1) o selecciona "Continuar".                                   |
| **Menú principal** | `OnShowCredits`       | **Créditos**       | El jugador selecciona manualmente la opción "Créditos" desde el menú.                                            |
| **Carga**          | `OnSceneLoaded`       | **Jugando**        | El nivel en turno completa su carga, pools de objetos y posicionamiento de entidades.                            |
| **Jugando**        | `OnPausePressed`      | **Pausa**          | El jugador presiona la tecla `Escape` o el botón `Start` en el mando.                                            |
| **Pausa**          | `OnResumePressed`     | **Jugando**        | El jugador selecciona "Reanudar" o vuelve a presionar `Escape`/`Start`.                                          |
| **Pausa**          | `OnRestartCheckpoint` | **Carga**          | El jugador elige reiniciar voluntariamente desde el último punto de control del nivel actual.                    |
| **Pausa**          | `OnExitToMenu`        | **Carga**          | El jugador selecciona "Salir al menú".                                                                           |
| **Jugando**        | `OnPlayerDeath`       | **Derrota**        | La barra de salud del protagonista llega a 0 (`Health <= 0`).                                                    |
| **Derrota**        | `OnRetryCheckpoint`   | **Carga**          | El jugador confirma reaparecer en el último punto de control del nivel actual.                                   |
| **Derrota**        | `OnExitToMenu`        | **Carga**          | El jugador presiona la opción para abandonar la sesión y regresar al menú principal.                             |
| **Jugando**        | `OnLevelComplete`     | **Carga**          | El jugador alcanza la meta de los Niveles 1 o 2 (nivel completado < 3); se prepara la carga del siguiente nivel. |
| **Jugando**        | `OnFinalBossDefeated` | **Victoria**       | Se derrota al jefe final o se completa con éxito el Nivel 3.                                                     |
| **Victoria**       | `OnVictoryEnd`        | **Créditos**       | Concluye la secuencia de triunfo y desenlace del Nivel 3.                                                        |
| **Créditos**       | `OnCreditsEnd`        | **Menú principal** | Finaliza el desplazamiento de créditos o el usuario presiona un botón para omitir.                               |

## Reglas globales

1.
2.
3.

## Casos especiales

Documenta excepciones importantes para evitar interpretaciones diferentes durante la implementación.


> **Navegación:** [[00 - Índice]] · ← [[06 - Economía y Recursos]] · [[01 - Premisa y Trama]] →
