# Economía y Recursos

## Descripción de la sección

Documenta cualquier recurso cuantificable: dinero, vida, energía, munición, experiencia, materiales, tiempo, puntos, etc.

Esta sección documenta los recursos cuantificables del sistema de juego: la salud del protagonista y las monedas de intercambio. Define las fuentes de obtención, los sumideros de gasto, las reglas de acumulación y el balance económico orientado a incentivar el combate activo y la progresión mediante la compra de nuevo armamento con comerciantes aliados.
## Recursos

| **Recurso**                            | **Obtención**                                                                             | **Uso**                                                                                         | **Límite**                                                               | **Pérdida**                                                                            |
| -------------------------------------- | ----------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------------------- | ------------------------------------------------------------------------ | -------------------------------------------------------------------------------------- |
| **Puntos de Salud (HP)**               | Orbes de curación soltados por enemigos (5% de probabilidad), cofres y puntos de control. | Mantener al jugador con vida ante el daño de enemigos.                                          | 100 HP base (10 segmentos de 10 HP c/u).                                 | Al recibir daño directo cuando no hay escudo activo. Llegar a 0 provoca la Derrota.    |
| **Escudo**                             | Orbes azules dejados por enemigos o cofres.                                               | Absorber impactos enemigos antes de que afecten la barra de salud principal.                    | 100 SP puntos (10 segmentos de 10 SP c/u )                               | Se reduce con cada impacto enemigo recibido hasta agotarse por completo.               |
| **Monedas**                            | Eliminación de enemigos (1 a 5 monedas) y apertura de cofres ocultos (15 a 30 monedas).   | Compra de nuevas armas y equipamiento permanente con el comerciante.                            | 999 monedas.                                                             | Al gastarse en la tienda del comerciante. Se conservan al reaparecer tras una derrota. |
| **Potenciadores Temporales (_Buffs_)** | Caída aleatoria y con baja probabilidad (2%–8%) al abatir enemigos en combate.            | Modificar momentáneamente las capacidades del protagonista durante un lapso de 8 a 12 segundos. | 1 potenciador activo a la vez (recoger otro reemplaza el efecto actual). | Se disipan de forma automática al agotarse su temporizador en pantalla.                |

### Catálogo de Potenciadores Temporales (_Buffs_)

- **Filo (Más daño):** Incrementa el daño del arma en un +50% durante 10 segundos; el filo emite un destello rojo.

- **Impulso (Doble salto):** Permite ejecutar un segundo salto en el aire durante 12 segundos.

- **Coraza (Invulnerabilidad total):** Vuelve al protagonista inmune a cualquier tipo de daño o proyectil durante 6 segundos (el personaje parpadea en blanco/dorado).

- **Sobrecarga (Velocidad / Reducción de Cooldown):** Aumenta la velocidad de desplazamiento en un 30% y elimina el tiempo de recarga del _Dash_ durante 8 segundos.


### Fuentes y sumideros

#### Fuentes (Entrada de recursos)

- **Combate continuo:** Los enemigos eliminados son la fuente principal de monedas, orbes de salud parcial, orbes de escudo y potenciadores temporales de combate.

- **Cofres de suministros:** Repartidos en rutas secundarias; garantizan paquetes grandes de monedas y escudos completos.

- **Puntos de control (_Checkpoints_):** Restauran la salud del protagonista al 100%.

#### Sumideros (Salida y consumo)

- **Tienda del Comerciante:** Espacio seguro donde el jugador invierte sus monedas acumuladas en armas definitivas con atributos únicos.

- **Impactos enemigos y trampas:** Consumen primero la barra de escudo y, una vez agotada esta, restan segmentos de la barra de salud regular.

### Reglas

1. **Prioridad de daño (Escudo antes que Salud):** Todo daño entrante impacta primero sobre la barra de escudo. La salud del personaje no se reduce mientras quede al menos 1 punto de escudo disponible.

2. **Exclusividad de Potenciadores:** El personaje solo puede portar un potenciador temporal a la vez. Si recoge un orbe de _Doble salto_ teniendo activo el de _Más daño_, el efecto anterior se cancela y comienza a correr el tiempo del nuevo.

3. **Persistencia económica:** Las monedas obtenidas no se pierden al morir ni al reiniciar desde un punto de control, manteniendo la sensación de avance constante.

4. **Reseteo de combate tras la derrota:** Al reaparecer tras una derrota, el personaje recupera su salud base al 100%, pero pierde los escudos adicionales, monedas y cualquier potenciador temporal activo.

### Balance

#### ¿Qué comportamiento queremos incentivar?

- **Enfrentamientos constantes y encadenados:** Los orbes de escudo y los potenciadores con baja probabilidad motivan al jugador a mantener un ritmo agresivo, ya que derrotar grupos de enemigos puede otorgarle ventajas tácticas inmediatas para arrasar con las siguientes ordas.

- **Aprovechamiento del momento** Al obtener un potenciador como _Invulnerabilidad_ o _Más daño_, el jugador se siente empoderado para lanzarse a la ofensiva directa en lugar de replegarse.

- **Exploración activa:** Buscar cofres para garantizar escudos antes de entrar a zonas de combate densas.

#### ¿Qué comportamiento queremos evitar?

- **Juego ultradefensivo o pasivo:** Evitar que el jugador espere a que la vida se recupere sola (no hay autoregeneración pasiva fuera de combate; la recuperación se gana peleando).

- **Evasión total de enemigos:** Desalentar el simplemente correr hasta el final de la pantalla, ya que el jugador se perdería las monedas necesarias para el comerciante y los potenciadores que facilitan el tramo.

> **Navegación:** [[00 - Índice]] · ← [[05 - Progresión]] · [[07 - Reglas y Estados del Juego]] →
