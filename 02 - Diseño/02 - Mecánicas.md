# Mecánicas

Los valores de esta página son la referencia de diseño para implementar y balancear. Si cambian en Unity, se actualizan aquí y en [[03 - Registro de Decisiones]].

## Valores base de Eon

| Parámetro | Valor |
| --- | ---: |
| Vida máxima | 100 HP (130 con el potenciador Vigor) |
| Escudo máximo | 0 SP (50 con el potenciador Coraza) |
| Velocidad de carrera | 7 u/s |
| Altura de salto | 3 u |
| Daño por tajo | 10 / 10 / 15 (combo de 3) |
| Invulnerabilidad tras recibir daño | 0,7 s |

**Vida y escudo no se recuperan durante la exploración ni el combate.** No hay objetos de curación ni de escudo. Ambos se restauran por completo solo al **tocar un punto de control** o al **vencer a un jefe** (también al reaparecer tras una derrota).

## Mecánicas principales

### Movimiento lateral

- Aceleración inmediata y frenado al soltar la dirección; no hay inercia de deslizamiento.
- En el aire se conserva el control horizontal completo.

### Salto

- **Activación:** pulsar Salto en contacto con el suelo.
- **Reglas:**
    - Impulso vertical inmediato; soltar el botón antes corta el ascenso (salto variable).
    - *Jump buffer* de 0,1 s: si se pulsa justo antes de aterrizar, el salto sale al tocar el suelo.
    - *Coyote time* de 0,1 s tras salir de un borde.
    - Sin la habilidad **Doble salto** equipada no hay segundo salto en el aire.
- **Estados:** `Idle`/`Run` → `InAir_Ascending` → `InAir_Falling` → `Landing` → `Idle`/`Run`.
- **Caso límite:** al chocar con un techo, la velocidad vertical se anula y empieza la caída.

### Dash

- **Propósito:** esquivar en el último momento y reposicionarse sin bloqueos pasivos.
- **Activación:** pulsar Dash en tierra o en el aire.
- **Reglas:**
    - Desplazamiento horizontal de 4 u durante 0,20 s.
    - Invulnerabilidad durante todo el recorrido frente a ataques y proyectiles, **excepto los instakill**.
    - Atraviesa enemigos comunes sin daño por contacto.
    - Recarga de 1,2 s desde que termina.
    - 1 dash aéreo por salto; se restablece al tocar suelo o al conectar un ataque descendente.
- **Interacciones:** cancela la recuperación del combo de espada. Con **Dash cortante** equipado, daña a cada enemigo atravesado.
- **Casos límite:** contra un muro la velocidad pasa a cero en el punto de contacto. La invulnerabilidad no evita la caída al vacío.

### Ataque básico (espada)

- **Activación:** pulsar Ataque (`Enter`) en tierra o en el aire.
- **Reglas:**
    - En tierra encadena hasta 3 tajos (10, 10 y 15 de daño).
    - Cada tajo activa una *hitbox* frontal durante 0,10 s.
    - Al conectar se aplica *hitstop* de 0,05 s y retroceso leve a enemigos comunes.
    - Recuperación de 0,1 s al final del combo; se puede cancelar con dash.
    - No se puede atacar durante el aturdimiento por daño recibido.
- **Caso límite:** si el arco toca a varios enemigos, todos reciben daño.

### Ataque descendente

- **Activación:** Abajo + Ataque (`S` + `Enter`) en el aire.
- **Reglas:** golpe vertical de 12 de daño. Si impacta a un enemigo, Eon rebota hacia arriba y recupera su dash aéreo.

## Habilidades (obtenidas de jefes)

- Cada jefe entrega su habilidad (el Jefe 2 entrega dos). **Ninguna se descarta:** todas se guardan en el inventario.
- Hay **3 ranuras de habilidad**. El jugador decide cuáles equipar; solo las equipadas funcionan. Ninguna es obligatoria, ni siquiera el Doble salto.
- Al ver una habilidad en el inventario se muestra siempre su **control y su función**.

| Habilidad | Origen | Tipo | Control | Efecto |
| --- | --- | --- | --- | --- |
| **Doble salto** | Jefe 1 | Pasiva | Salto en el aire | Segundo salto en el aire (80 % de la altura del primero). Se restablece al tocar suelo. |
| **Tajo ardiente** (ataque arcano) | Jefe 2 | Activa | `J` | La espada lanza un tajo ardiente en forma de media luna que viaja en horizontal: 15 de daño, 14 u/s, alcance 8 u, recarga 1,2 s. Atraviesa a los enemigos comunes. |
| **Dash cortante** | Jefe 2 | Pasiva | Dash | El dash inflige 20 de daño a cada enemigo que atraviesa (una vez por enemigo y por dash). |
| **Escama pétrea** | Jefe 3 | Activa | `K` (mantener) | Eon petrifica su cuerpo y se cubre (detalle abajo). |

### Escama pétrea (detalle)

- Mantener `K`: Eon se petrifica y se cubre hasta 1 s; recibe un 70 % menos de daño y no puede moverse.
- **Bloqueo perfecto:** si el golpe llega en los primeros 0,25 s, el daño se anula y el atacante queda aturdido 1 s.
- Recarga de 3 s desde que se suelta.
- **No bloquea ataques instakill** ni evita la caída al vacío.
- Sinergias: el bloqueo perfecto aturde al Earthlem y rompe la guardia del Vestigio.

## Potenciadores

- Se compran con XP al mercader, una sola vez cada uno, y son **permanentes**.
- **No se activan con ningún botón:** mientras están equipados en el inventario, su efecto está siempre activo.
- Hay **3 ranuras de potenciador** en el inventario. Los demás quedan guardados, sin efecto, hasta que se equipen.
- Al ver un potenciador en el inventario se muestra siempre su función.
- Catálogo y precios en [[06 - Economía y Recursos]].

## Mecánicas secundarias

- **Interacción:** `E` / Botón `Y` frente al mercader y los puntos de control.
- **Experiencia:** los enemigos sueltan su XP en forma de orbes dorados que se atraen hacia Eon cuando está a 3 u o menos.
- **Géiseres:** Eon se coloca sobre un géiser y, durante la erupción, sale lanzado en un arco fijo hacia la isla destino.
    - Ciclo: reposo 1,5 s → aviso (burbujeo y vapor) 0,5 s → erupción 1,0 s.
    - Durante el vuelo se conserva un control horizontal leve (±1 u) para corregir el aterrizaje.
    - Sustituyen por completo a los trampolines.
- **Cañones (isla final):** al interactuar, disparan contra La Entidad. Recarga de 6 s por cañón.
- **Reaparición de enemigos:** los enemigos comunes reaparecen al descansar en un punto de control o al volver a entrar a una zona. Se puede regresar a zonas ya superadas para acumular más XP.

> **Navegación:** [[00 - Índice]] · ← [[01 - Jugabilidad]] · [[03 - Sistemas]] →
