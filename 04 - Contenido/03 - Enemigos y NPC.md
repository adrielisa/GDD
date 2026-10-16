# Enemigos y NPC

## Descripción de la sección

Documenta las entidades controladas por el juego y su comportamiento. Esta sección detalla los parámetros de combate, patrones de movimiento, máquinas de estados y reglas de interacción tanto para los adversarios que pueblan los niveles como para los personajes no jugables aliados que asisten al protagonista en su travesía.
## Enemigos

### Aurion

- **Rol de combate:** Hostigador aéreo / Proyectil teledirigido.

- **Comportamiento:** Flota en distintas trayectorias a media altura. Al detectar al jugador, cambia de coloración (su núcleo se torna rojo brillante), carga durante 0.5 segundos y se lanza a atacar al jugador . Si falla, queda aturdido 0.8 segundos al nivel del suelo antes de volver a elevarse.

- **Vida:** 20 HP (muere de 1 a 2 golpes de espada básica).

- **Daño:** 15 de daño al impactar en picada; 10 por contacto pasivo.

- **Defensas:** Sin armadura ni escudos.

- **Velocidad:** 2.5 u/s en patrulla; 7.0 u/s en embestida en picada.

- **Rango de detección:** 6 unidades horizontales y 4 verticales con línea de visión despejada. (PENDIENTE REVISAR)

- **Ataques:**

    - _Embestida:_ Carga frontal descendente en línea recta hacia la posición registrada del jugador.

- **Debilidades:** Rebotar sobre un Aurion lo destruye instantáneamente y reinicia el dash aéreo del jugador.

- **Recompensa:** 2 a 3 Monedas; 15% de probabilidad de soltar un orbe menor de vida.

**Estados de IA:**

```text
Patrullar (flotación flotante) → Detectar (cambio de color y carga) → Perseguir/Atacar (embestida en picada)
                                         ↓
                                  Aturdimiento en suelo → Retorno a altura base
```

### Driller

- **Rol de combate:** Rompeformaciones aéreo segmentado / Amenaza omnidireccional.

- **Comportamiento:** Gusano aéreo compuesto por 10 segmentos articulados (1 cabeza guía y 9 eslabones corporales). Aparece emergiendo desde cualquier extremo de la pantalla (laterales, techo o suelo) navegando por el aire en curvas continuas. Cada segmento cuenta con su propia hurtbox; al recibir daño letal, el último segmento de la cola se destruye, reduciendo su longitud y aumentando su velocidad de viraje progresivamente.

- **Vida:** 100 HP total (10 HP por cada uno de los 10 segmentos).

- **Daño:** 25 de daño por colisión con la cabeza; 12 de daño por rozar los segmentos del cuerpo.

- **Defensas:** La cabeza desvía ataques frontales simples (requiere parry o golpe lateral); los segmentos del cuerpo reciben daño directo normal.

- **Velocidad:** 4.0 u/s en estado inicial; escala hasta 6.5 u/s cuando le quedan 3 segmentos o menos.

- **Rango de detección:** Global en la zona de arena asignada (rastrea activamente las coordenadas de Eon mientras serpentea por la pantalla).

- **Ataques:**

    - _Vuelo Serpenteante:_ Trayectoria constante en arcos continuos que corta el espacio aéreo del escenario.

    - _Zambullida Rápida:_ Aceleración súbita vertical cruzando la pantalla si el jugador permanece más de 2 segundos en una misma plataforma.

- **Debilidades:** Encadenar rebotes aéreos sucesivos sobre su lomo permite destruir varios segmentos seguidos sin tocar el suelo.

- **Recompensa:** 15 a 20 Monedas de Resonancia (repartidas al destruir eslabones) y alta probabilidad de soltar un potenciador temporal de daño o escudo.

```text
Aparición perimetral → Navegación sinusoidal → Rastreo angular de Eon → Pérdida de segmento por impacto
                                                        ↓
                                  Furia acelerada (cuando restan ≤ 3 segmentos)
```

#### Earthlem

- **Rol de combate:** Tanque terrestre / Bloqueador de paso.

- **Comportamiento:** Permanece camuflado bajo tierra como una formación rocosa plana. Cuando Eon se aproxima a su perímetro, emerge violentamente levantando escombros y bloqueando el camino. Realiza barridos frontales pesados y golpes contra el suelo que proyectan ondas de choque rasantes. Si el jugador se aleja demasiado, se sumerge de nuevo en la tierra para reaparecer más cerca.

- **Vida:** 80 HP (resiste combos prolongados).

- **Daño:** 20 por golpe de puño directo; 15 por onda sísmica rasante; 10 por contacto al emerger.

- **Defensas:** Coraza de piedra frontal: los ataques frontales directos ven reducido su daño en un 50% a menos que se use un contraataque (_Parry_) contra su puñetazo. La espalda es su punto ciego sin reducción.

- **Velocidad:** 1.2 u/s (movimiento terrestre lento y pesado).

- **Rango de detección:** 3.5 unidades terrestres para emerger.

- **Ataques:**
    
    - _Aplastamiento Sísmico:_ Golpea el suelo con ambos puños, liberando una onda de choque terrestre que avanza 3 unidades y obliga a saltar.

    - _Barrido de Roca:_ Tajo horizontal pesado con su brazo derecho tras 0.4 segundos de preparación.

- **Debilidades:** Su lentitud de giro; esquivar a su espalda con el Dash permite castigarlo sin penalización de armadura. Su barrido de puño puede ser neutralizado con _Parry_ para desestabilizarlo.

- **Recompensa:** 8 a 10 Monedas de Resonancia; 20% de probabilidad de soltar un orbe de Escudo de Resonancia.


```text
Enterrado (inactivo/camuflado) → Detección de proximidad → Emergencia violenta → Barrido frontal / Aplastamiento
                                                                    ↓
                                             Jugador fuera de alcance → Inmersión bajo tierra
```

## NPC
### Seller

- **Función:** Mercader de equipamiento y armero de campo. Permite intercambiar monedas acumuladas por nuevas armas con atributos  únicos (variaciones de velocidad, daño y ventana de contraataque).

- **Ubicación:** Zonas de descanso seguras al inicio de cada nivel y en antesalas inmediatas a las arenas de combate principales.

- **Interacción:** El jugador se sitúa dentro de su área de detección y presiona la tecla de interacción (`E` en teclado / Botón `Y` / `Triángulo` en mando). La acción congela temporalmente las entradas de movimiento del jugador y despliega la interfaz gráfica de la tienda. Presionar el botón de cancelar o salir cierra el menú y devuelve el control activo al jugador.

- **Diálogos:**

    - _Saludo inicial (Nivel 1):_

        _"Vaya, el supuesto héroe de la profecía sigue de pie. Tu destino habrá fracasado, pero mi acero no. Si traes monedas, te daré algo con qué defenderte."_
        
    - _Compra exitosa:_

        _"Trato cerrado. Cuida ese filo; en estas ruinas el metal es más confiable que cualquier leyenda."_

    - _Sin fondos suficientes:_

        _"No regalo nada por lástima, muchacho. Vuelve cuando tus bolsillos pesen lo suficiente."_

    - _Previo a zona de peligro (Nivel 2 / Nivel 3):_

        _"Más adelante el aire se vuelve pesado y esas aberraciones se mueven más rápido. Si vas a lanzarte al abismo, asegúrate de llevar un arma que responda a tiempo."_

- **Condiciones:**
    
    - Solo interactuable si no hay enemigos activos en un radio de 8 unidades (zonas libres de combate).

    - Su catálogo se expande de forma progresiva conforme el jugador desbloquea y accede a nuevos niveles.

    - Cada arma solo puede adquirirse una única vez; tras la compra, el artículo queda marcado como adquirido en su menú.

- **Recompensas / información:**

    - Acceso al catálogo de compra de armas: _Espada liviana_ (50 monedas), _Espada real_ (120 monedas) y Espada elemental (200 monedas).

    - Pistas ambientales sobre las debilidades de los enemigos y jefes de la zona en su diálogo introductorio.



> **Navegación:** [[00 - Índice]] · ← [[02 - Niveles]] · [[04 - Objetos y Coleccionables]] →

> **Navegación:** [[00 - Índice]] · ← [[02 - Niveles]] · [[04 - Objetos y Coleccionables]] →
