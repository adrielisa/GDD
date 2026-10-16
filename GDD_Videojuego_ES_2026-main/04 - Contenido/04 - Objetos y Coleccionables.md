# Objetos y Coleccionables

## Descripción de la sección

Define objetos que el jugador puede recoger, utilizar, equipar, vender, intercambiar o descubrir. Esta sección documenta las especificaciones técnicas y visuales de las entidades recolectables en el escenario, los consumibles de combate directo, los potenciadores temporales (_buffs_), las armas adquiribles en la tienda.

### 1. Moneda y Consumibles Básicos

#### Moneda del reino

- **Tipo:** Recurso acumulable / Moneda de cambio.

- **Descripción:** Fragmento metálico.

- **Función:** Divisa económica canjeable en la tienda para desbloquear armas.

- **Cómo se obtiene:** Al derrotar enemigos comunes (1 a 5 monedas) y abrir cofres ocultos en rutas secundarias (15 a 30 monedas).

- **Cómo se utiliza:** Se debita automáticamente en la interfaz de la tienda al confirmar la compra de un artículo.

- **Cantidad máxima:** 999 monedas.

- **Valor:** 1 unidad monetaria base.

- **Rareza:** Común.

- **Restricciones:** No consumible en combate directo; se conserva al morir o reiniciar desde un punto de control.

- **Interacciones:** Se atrae magnéticamente hacia el jugador al situarse a menos de 3 unidades de distancia.

- **Representación visual:** Cristal romboidal brillante de color amarillo/dorado que rota sobre su propio eje.

#### Orbe de vitalidad

- **Tipo:** Consumible instantáneo de campo.

- **Descripción:** Esfera de condensación biológica liberada al romper la coraza de los enemigos.

- **Función:** Restaura 10 puntos de salud (1 segmento completo de la barra de vida del personaje).

- **Cómo se obtiene:** Caída directa de enemigos con una probabilidad base del 5% o dentro de cofres de suministros.

- **Cómo se utiliza:** Se activa instantáneamente al contacto físico del jugador con el objeto en el escenario.

- **Cantidad máxima:** Inmediato (no se almacena en inventario).

- **Valor:** No comerciable.

- **Rareza:** Común.

- **Restricciones:** Si la vida del jugador está al 100% (100 HP), el orbe permanece flotando en el suelo durante 10 segundos antes de desaparecer.

- **Interacciones:** Emite un destello verde en el sprite del personaje  y actualiza la barra de interfaz en tiempo real.

- **Representación visual:** Esfera luminosa de color verde esmeralda con partículas ascendentes.


#### Orbe de escudo

- **Tipo:** Consumible defensivo instantáneo.

- **Descripción:** Celda de energía protectora que proyecta una barrera cinética perimetral.

- **Función:** Otorga 20 puntos de escudo (2 segmentos de la barra de SP), absorbiendo daño antes de afectar la salud principal.

- **Cómo se obtiene:** Botín dejado por enemigos pesados (como Earthlem), cofres de exploración o santuarios.

- **Cómo se utiliza:** Se consume automáticamente al tocarlo.

- **Cantidad máxima:** 100 SP acumulables (10 segmentos de escudo).

- **Valor:** No comerciable.

- **Rareza:** Poco común.

- **Restricciones:** Los puntos de escudo se pierden en su totalidad al morir y reaparecer en un punto de control.

- **Interacciones:** Despliega una capa azul translúcida momentánea sobre el protagonista y rellena la barra azul de escudo en el HUD.

- **Representación visual:** Poliedro hexagonal de color azul zafiro rodeado por un anillo luminoso protector.

### 2. Potenciadores Temporales (_Buffs_)

#### Orbe de daño (Daño Potenciado)

- **Tipo:** Potenciador temporal de combate (_Buff_).

- **Descripción:** Esfera incandescente de sobrecarga marcial.

- **Función:** Incrementa el daño base del arma equipada en un +50% durante 10 segundos.

- **Cómo se obtiene:** Caída aleatoria al abatir enemigos (probabilidad entre 2% y 8%).

- **Cómo se utiliza:** Activación instantánea al recogerlo del suelo.

- **Cantidad máxima:** 1 potenciador activo en el personaje (reemplaza cualquier otro potenciador vigente).

- **Valor:** No comerciable.

- **Rareza:** Rara.

- **Restricciones:** Se disipa al agotarse el temporizador de 10 segundos o al morir.

- **Interacciones:** Cambia la estela del corte de la espada a un color rojo intenso y muestra un icono con temporizador circular en la interfaz.

- **Representación visual:** Esfera flameante de color carmesí con pequeñas chispas de impacto.


#### Orbe de impulso (Doble Salto)

- **Tipo:** Potenciador temporal de movilidad (_Buff_).

- **Descripción:** Esfera etérea condensada de viento huracanado.

- **Función:** Permite al jugador ejecutar un segundo salto libre en el aire sin necesidad de rebotar en un enemigo durante 12 segundos.

- **Cómo se obtiene:** Caída aleatoria al derrotar enemigos voladores o en cofres.

- **Cómo se utiliza:** Activación instantánea al contacto.

- **Cantidad máxima:** 1 potenciador activo en el personaje.

- **Valor:** No comerciable.

- **Rareza:** Rara.

- **Restricciones:** Se extingue a los 12 segundos; reemplaza el potenciador actual si ya portaba otro.

- **Interacciones:** Genera una ráfaga de aire blanco bajo los pies del personaje al realizar el segundo impulso aéreo.

- **Representación visual:** Orbe plumoso de color blanco cian brillante.


#### Orbe de coraza (Invulnerabilidad)

- **Tipo:** Potenciador temporal defensivo (_Buff_).

- **Descripción:** Fragmento de barrera temporal que desfasa el cuerpo del portador de la realidad física.

- **Función:** Vuelve al protagonista completamente inmune a cualquier tipo de daño, proyectil o contacto físico durante 6 segundos.

- **Cómo se obtiene:** Caída muy rara de enemigos de élite (probabilidad cercana al 2%) o cofres de desafíos de combate.

- **Cómo se utiliza:** Activación instantánea al contacto.
 
- **Cantidad máxima:** 1 potenciador activo en el personaje.

- **Valor:** No comerciable.

- **Rareza:** Épica.

- **Restricciones:** No evita la muerte instantánea si el personaje cae al vacío fuera de los límites de la pantalla. Dura 6 segundos.

- **Interacciones:** El sprite de Eon parpadea en tonos blancos y dorados continuos; los proyectiles enemigos rebotan o se destruyen al rozarlo.

- **Representación visual:** Diamante dorado flotante que emite pulsos de luz radiante.


#### Orbe de sobrecarga (Velocidad y Dash Continuo)

- **Tipo:** Potenciador temporal de movilidad y agilidad (_Buff_).

- **Descripción:** Chispa de resonancia pura que estimula las articulaciones mecánicas y reflejos.

- **Función:** Aumenta la velocidad de desplazamiento en un 30% y elimina el tiempo de enfriamiento (_cooldown_) del Dash durante 8 segundos.

- **Cómo se obtiene:** Caída aleatoria de enemigos ágiles (probabilidad entre 2% y 8%).

- **Cómo se utiliza:** Activación instantánea por contacto.

- **Cantidad máxima:** 1 potenciador activo en el personaje.

- **Valor:** No comerciable.

- **Rareza:** Rara.

- **Restricciones:** Dura 8 segundos exactos; se anula al expirar el tiempo.

- **Interacciones:** Deja siluetas residuales de sombra tras los movimientos y sprints de Eon; el botón de Dash responde sin retardo de recarga.

- **Representación visual:** Prisma electrizado de color violeta con descargas eléctricas mínimas en su superficie.

### 3. Equipamiento / Armamento Comerciable

#### Espada liviana

- **Tipo:** Arma cuerpo a cuerpo equipable.

- **Descripción:** Espada corta de manufactura estandarizada, ligera y equilibrada, perteneciente a los antiguos reclutas de Eurooppa.

- **Función:** Aumenta el daño de ataque base en un 25%.

- **Cómo se obtiene:** Se compra en el puesto de Seller en el Nivel 1.

- **Cómo se utiliza:** Se equipa en el inventario o menú de pausa.

- **Cantidad máxima:** 1 (desbloqueo permanente).

- **Valor:** 50 monedas.

- **Rareza:** Común.

- **Restricciones:** Sustituye el arma activa al ser seleccionada.

- **Interacciones:** Permite encadenar ataques a los enemigos.

- **Representación visual:** Espada recta plateada de doble filo con cruceta simple y empuñadura de cuero marrón.


#### Espada real

- **Tipo:** Arma cuerpo a cuerpo equipable.

- **Descripción:** Mandoble forjado con acero de la mejor calidad usado por nobles

- **Función:** Aumenta el daño de ataque base en un 50%

- **Cómo se obtiene:** Se compra en el puesto de Seller en el Nivel 2.

- **Cómo se utiliza:** Se equipa desde el menú de pausa o al momento de la compra.

- **Cantidad máxima:** 1 (desbloqueo permanente).

- **Valor:** 120 Monedas.

- **Rareza:** Poco común.

- **Restricciones:**  Sustituye el arma activa al ser seleccionada.

- **Interacciones:** Permite encadenar ataques  a los enemigos.

- **Representación visual:** Espadón pesado con grietas negras y moradas que desprenden vapores oscuros.

#### Espada elemental

- **Tipo:** Arma cuerpo a cuerpo equipable.

- **Descripción:** Sable fabricado con elementos únicos.

- **Función:** Aumenta el daño de ataque base en un 100%

- **Cómo se obtiene:** Se compra en la tienda de Seller en el Nivel 3

- **Cómo se utiliza:** Se equipa como arma principal de combate.

- **Cantidad máxima:** 1 (desbloqueo permanente).

- **Valor:** 200 Monedas.

- **Rareza:** Rara.

- **Restricciones:**  Sustituye el arma activa al ser seleccionada.

- **Interacciones:** Permite encadenar ataques  a los enemigos.

- **Representación visual:** Florete estilizado de hoja translúcida con empuñadura ornamentada en oro y azul.



> **Navegación:** [[00 - Índice]] · ← [[03 - Enemigos y NPC]] · [[05 - Misiones y Desafíos]] →
