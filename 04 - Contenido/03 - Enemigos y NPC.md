# Enemigos y NPC

El juego tiene tres enemigos comunes (Aurion, Earthlem y Vestigio), los esbirros del Jefe 1, tres jefes normales y La Entidad. El enemigo Driller queda descartado. Las cifras son la referencia de diseño; se ajustan en pruebas y se registran en [[03 - Registro de Decisiones]].

## Resumen de enemigos comunes

| Enemigo | Vida | Velocidad | Daño principal | Zonas | XP |
| --- | ---: | --- | --- | --- | ---: |
| Aurion | 20 HP | 2,5 u/s patrulla; 7 u/s embestida | Embestida 15; contacto 10 | Costa, Bosque, Archipiélago | 10 |
| Earthlem | 80 HP | 1,2 u/s | Puño 20; onda 15; emerger 10 | Bosque, Ruinas, Archipiélago | 30 |
| Vestigio | 50 HP | 3 u/s | Combo 18; estocada 22 | Ruinas, Archipiélago, Isla Final | 25 |
| Camaroncito | 5 HP | 3 u/s en el aire | Contacto 8 | Arena de la Marea | 1 |

## Aurion

- **Rol:** hostigador aéreo.
- **Comportamiento:** flota a media altura. Al detectar a Eon su núcleo se vuelve rojo, carga 0,5 s y embiste en línea recta hacia la posición registrada. Si falla, queda aturdido 0,8 s a ras de suelo y luego vuelve a subir.
- **Detección:** 6 u horizontales y 4 verticales con línea de visión.
- **Defensas:** ninguna.
- **Debilidad:** un ataque descendente sobre él lo destruye y recupera el dash aéreo de Eon.
- **Recompensa:** 10 XP.

```text
Patrullar → Detectar (núcleo rojo, 0,5 s) → Embestir → [falla] Aturdido 0,8 s → Volver a altura
```

## Earthlem

- **Rol:** tanque terrestre que bloquea el paso.
- **Comportamiento:** camuflado como roca plana. Cuando Eon se acerca a 3,5 u, emerge levantando escombros. Si Eon se aleja más de 8 u, se entierra y reaparece más cerca.
- **Ataques:**
    - *Barrido de roca:* tajo horizontal tras 0,4 s de preparación; 20 de daño.
    - *Aplastamiento sísmico:* golpe al suelo con ambos puños; onda rasante de 3 u (hay que saltarla); 15 de daño.
- **Defensas:** coraza frontal; los golpes de frente hacen 50 % del daño. La espalda recibe daño completo.
- **Debilidades:** gira despacio; un dash para quedar a su espalda permite castigarlo. Con Dash cortante, el propio dash le hace daño completo. Con Escama pétrea, un bloqueo perfecto contra el barrido lo aturde 1 s.
- **Recompensa:** 30 XP.

```text
Enterrado → Detecta a 3,5 u → Emerge → Barrido / Aplastamiento → [Eon a más de 8 u] Se entierra
```

## Vestigio *(nombre provisional)*

- **Rol:** guerrero cuerpo a cuerpo.
- **Descripción:** humanoide sin rostro, todo blanco, con una silueta que recuerda a La Entidad. Porta una lanza-espada blanca. Es un eco del titán.
- **Comportamiento:** patrulla su plataforma; al ver a Eon se acerca hasta 3 u y elige un ataque.
- **Ataques:**
    - *Combo de dos tajos:* preparación de 0,5 s (el arma brilla); 18 de daño por tajo.
    - *Estocada:* avanza 3 u tras 0,7 s de preparación; 22 de daño.
- **Guardia:** tras recibir 2 golpes frontales seguidos, levanta el arma 1,2 s y bloquea todo daño frontal.
- **Debilidades:** la guardia no cubre la espalda ni el Dash cortante; el Tajo ardiente y el bloqueo perfecto de la Escama pétrea rompen la guardia y lo aturden 0,5 s.
- **Recompensa:** 25 XP.

```text
Patrullar → Detectar → Acercarse → Combo / Estocada → [2 golpes frontales recibidos] Guardia 1,2 s
```

## Jefe 1 — Camarón serpiente *(nombre provisional)*

- **Arena:** Arena de la Marea, playa plana de 30 u con el mar a la derecha. Límites invisibles.
- **Vida:** 500 HP. **Fases:** 1 (100–50 %) y 2 (menos de 50 %).
- **Descripción:** crustáceo alargado con cuerpo de serpiente marina. Pasa la mayor parte del tiempo en el agua; solo se le puede golpear con la espada cuando su cuerpo está sobre la arena.
- **Recompensa:** 200 XP y **Doble salto**.

| Ataque | Aviso | Regla | Daño |
| --- | --- | --- | --- |
| **Invocar camaroncitos** | Chapoteo y burbujas. | Libera 3 camaroncitos (4 en fase 2) que persiguen a Eon en el aire a 3 u/s. Máximo 6 vivos. Recarga 12 s. | 8 por contacto |
| **Embestida corta** | Ojos brillantes y cuerpo recogido 0,6 s. | Se lanza 5 u sobre la arena hacia Eon. Después queda varado 1,5 s: **ventana de castigo**. | 20 |
| **Mordida** | Mandíbulas abiertas 0,4 s. | Solo si Eon está a 2,5 u de la cabeza. | 25 |
| **Ráfaga de agua** | Se eleva en la orilla e inhala 2 s; agua girando en la boca y sonido exclusivo. | Al empezar el aviso **emerge una plataforma de agua** a 2,5 u de altura (alcanzable con salto simple) en una de tres posiciones. La ráfaga barre toda la arena a ras de suelo hasta 2 u de altura durante 1,5 s. La plataforma se disuelve 1 s después. Tras la ráfaga queda agotado 3 s en la orilla: **ventana de castigo**. Cada 20 s (15 s en fase 2). | **Instakill** |

- **Fase 2:** más esbirros, ráfagas más frecuentes y los camaroncitos siguen persiguiendo a Eon mientras está sobre la plataforma de agua.
- **Regla de diseño:** la ráfaga nunca se lanza si no hay una plataforma de agua visible.

```text
Agua (invoca / se acerca) → Embestida → Varado 1,5 s (castigo) → Agua
                    └── cada 20 s: Aviso + plataforma de agua → Ráfaga (instakill) → Agotado 3 s (castigo)
```

### Camaroncitos *(sin nombre)*

- Esbirros voladores pequeños. 5 HP: mueren con un golpe o un ataque descendente (que además rebota a Eon).
- Persiguen a Eon en el aire; al tocarlo hacen 8 de daño y retroceden 1 s antes de volver a perseguir.
- Desaparecen al morir el jefe.

## Jefe 2 — Mago oscuro *(nombre provisional)*

- **Arena:** Patio de la Academia, suelo de piedra **totalmente plano** de 36 u, sin plataformas, dentro de unas ruinas abandonadas. Al empezar, **pilares de las ruinas** emergen en ambos extremos y bloquean el paso; se hunden al morir el jefe.
- **Vida:** 700 HP. **Fases:** 1 (100–40 %) y 2 (menos de 40 %).
- **Descripción:** hechicero encapuchado que flota a ras de suelo. Se puede golpear con la espada siempre que no tenga el escudo activo.
- **Recompensa:** 300 XP, **Tajo ardiente** y **Dash cortante** (se guardan los dos en el inventario).

| Ataque | Aviso | Regla | Daño |
| --- | --- | --- | --- |
| **Lluvia de llamaradas** | Círculos de luz naranja en el suelo 0,8 s. | 5 llamaradas (7 en fase 2) caen del cielo; 2 apuntan a la posición prevista de Eon. Radio de 1 u. | 20 |
| **Picos de magma** | El suelo se agrieta y brilla 0,5 s antes de cada pico. | Una ola de picos nace junto al mago y avanza hacia el extremo opuesto a 6 u/s (Eon corre a 7 u/s). Cada pico mide 2,5 u y dura 1 s. La ola se detiene a 2 u del pilar del extremo: hay que **correr y alejarse** del mago hasta esa zona segura. Saltar sobre el frente no sirve: los picos de detrás siguen activos. | 18 por pico |
| **Escudo arcano** | Esfera violeta que se forma en 0,5 s. | Cada 15 s, durante 4 s, bloquea todo daño. Los golpes rebotan y empujan levemente a Eon. Mientras dura, el mago lanza cráneos. | — |
| **Cráneos de fuego** | Llamas en sus manos 0,6 s. | 3 cráneos (4 en fase 2) que persiguen a Eon en el aire a 3,5 u/s con giro limitado. Duran 6 s. Se destruyen con un golpe. | 15 |
| **Teletransporte** | Humo negro en el punto de destino 0,5 s antes. | Tras cada 3 ataques (2 en fase 2) desaparece y reaparece en el **extremo opuesto** de la arena. Al reaparecer queda expuesto 1 s. | — |

- **Fase 2:** se teletransporta con más frecuencia y puede combinar llamaradas con la ola de picos.

```text
Ataque 1 → Ataque 2 → Ataque 3 → Teletransporte al extremo opuesto (expuesto 1 s) → …
   └── cada 15 s: Escudo 4 s + Cráneos de fuego
```

## Jefe 3 — Serpiente gigante *(nombre provisional)*

- **Arena:** Anillo de Islas, 7 plataformas de tierra flotantes en dos alturas sobre el vacío. Límites invisibles.
- **Vida:** 1200 HP compartidos por todo el cuerpo. **Fases:** 1 (100–50 %) y 2 (menos de 50 %).
- **Descripción:** serpiente segmentada colosal (cabeza + ~18 segmentos + cola) que da vueltas entre y a través de las plataformas, al estilo del Devorador de mundos de Terraria.
- **Recompensa:** 400 XP, **Escama pétrea** y cinemática de petrificación.

| Elemento / ataque | Aviso | Regla | Daño |
| --- | --- | --- | --- |
| **Cabeza** | Ojos y mandíbula brillantes; silueta siempre visible. | Tocarla es **instakill**. No recibe daño. | **Instakill** |
| **Cuerpo** | — | Cada segmento recibe daño de espada, Tajo ardiente, ataque descendente (con rebote) y Dash cortante. Tocarlo hace daño. | 15 por contacto |
| **Cola** | Punta de color distinto. | Punto débil: recibe el doble de daño. | 15 por contacto |
| **Recorrido** | — | Trayectorias en bucle, en ocho y zambullidas verticales a 6 u/s (8 u/s en fase 2). Puede atravesar las plataformas. | — |
| **Lluvia de baba** | El segmento se hincha y gotea 0,4 s antes. | Cada segmento deja caer gotas de baba en momentos aleatorios (cada 2–4 s; máximo 6 gotas a la vez en pantalla). Caen en vertical. | 10 |
| **Embestida de cabeza** | Rugido y flecha en el borde de la pantalla 1,5 s. | La cabeza sale de pantalla y cruza la arena en línea recta hacia la posición de Eon a 14 u/s. | **Instakill** (cabeza) |

- **Fase 2:** más velocidad, gotas más frecuentes (cada 1,5–3 s) y embestidas dobles.
- **Al morir:** el cuerpo se detiene, se petrifica (ilustración fija) y forma el Puente de la Serpiente hacia la isla final.

## La Entidad (jefe final)

- **Arena:** Isla Final. La fase 1 retoma el encuentro ya diseñado del titán (islas ascendentes, cañones, titán al fondo), con géiseres en lugar de trampolines. Límites invisibles.
- **Vida:** 2000 HP *(valor provisional; ajustar con el encuentro existente)*.
- **Recompensa:** victoria y final.

| Fase | Vida | Desarrollo |
| --- | --- | --- |
| **1. Ascenso** | 100–60 % | Eon sube por 3 islas unidas por géiseres. La Entidad, al fondo, golpea zonas del suelo marcadas con sombra 1,2 s (30 de daño) y envía hasta 3 Vestigios. Cada isla tiene un **cañón**: al interactuar dispara 150 de daño; recarga 6 s. |
| **2. Cumbre** | 60–25 % | Cara a cara. La Entidad apoya las manos en la cumbre; los núcleos del dorso de cada mano son puntos débiles. Barrido de mano (saltar o doble salto; 25), onda de choque rasante (20) e invocación de Vestigios. |
| **3. Revancha** | Menos de 25 % | Su rostro se abre y expone el núcleo. Combina los ataques anteriores a mayor velocidad. *(Detalle pendiente de cerrar con el equipo.)* |

## NPC

### Mercader (Seller)

- **Función:** cambia XP por potenciadores permanentes (compra única de cada uno).
- **Ubicación:** aparece por primera vez en la antesala del Jefe 1 y desde entonces en la antesala de cada jefe: Acantilados, Ruinas, Archipiélago y final del Puente de la Serpiente.
- **Interacción:** `E` / `Y` dentro de su zona; congela el movimiento y abre la tienda. Cancelar cierra el menú.
- **Condiciones:**
    - La antesala no tiene enemigos.
    - El catálogo crece al avanzar (ver [[06 - Economía y Recursos]]).
    - Los potenciadores ya comprados aparecen como «Adquirido».
    - En la antesala de la Isla Final regala uno de los potenciadores que falten (una vez).
- **Información:** pistas sobre el jefe de la zona en su diálogo.

> **Navegación:** [[00 - Índice]] · ← [[02 - Niveles]] · [[04 - Objetos y Coleccionables]] →
