# Mecánicas

## Descripción de la sección

Una mecánica es una regla o interacción mediante la cual el jugador puede actuar dentro del sistema del juego.

Documenta cada mecánica con suficiente detalle para que otro integrante pueda implementarla.

## Plantilla de mecánica

### Nombre de la mecánica

**Propósito:**  
¿Qué aporta a la experiencia?

**Activación:**  
¿Qué debe hacer el jugador?

**Reglas:**  
¿Qué puede y qué no puede ocurrir?

**Entrada:**  
¿Qué botón, gesto o acción la activa?

**Estado inicial:**

**Estado final:**

**Recursos utilizados:**

**Recompensa:**

**Penalización:**

**Interacciones con otras mecánicas:**

**Casos límite:**  
¿Qué ocurre en situaciones poco comunes?

## Mecánicas principales

### Desplazamiento (Dash)

- **Propósito:**

    Otorgar una herramienta de movilidad que permita evadir ataques en el último segundo, reposicionarse rápidamente alrededor de los enemigos y mantener el ritmo ofensivo sin recurrir a bloqueos pasivos.

- **Activación:**
    
    Presionar el botón de dash mientras se avanza o se está de pie (en tierra o en el aire).
    
- **Reglas:**
 
    - Eon se impulsa horizontalmente una distancia fija a alta velocidad durante **0.50 segundos**.
    
    - Otorga marcos de invulnerabilidad totales durante todo el recorrido, Eon no recibe daño de ataques ni proyectiles.
    
    - Atraviesa la colisión física de enemigos comunes sin recibir daño por contacto.
    
    - Solo se puede ejecutar **1 dash aéreo** por salto; no se restablece hasta tocar tierra firme o conectar un ataque.
    
- **Entrada:**
    
    `Shift Izquierdo` o `RB` / `RT` (Mando).
    
- **Estado inicial:**
    
    `Idle`, `Run`, `Attack`, `InAir`.
    
- **Estado final:**
    
    Retorno a `Idle`/`Run` con fricción restaurada, o transición fluida a un nuevo ataque.
    
- **Recursos utilizados:**
    
    Tiempo de recarga (_cooldown_) global de 5 segundos** en tierra; 1 carga de aire que se consume al usarse en suspensión.
    
- **Recompensa:**
    
    Evasión garantizada de golpes letales y reubicación ventajosa a la espalda o flanco del enemigo.
    
- **Penalización:**
    
    Quedar vulnerable si se calcula mal la distancia.
    
- **Interacciones con otras mecánicas:**
    
    - Cancela la animación de recuperación del combo básico de espada.
    
- **Casos límite:**
    
    - **Colisión con muros:** Si el dash termina contra una pared o límite del nivel, la velocidad se reduce a cero en el punto de contacto para evitar atravesar la geometría del mapa.
    
    - **Caídas al vacío:** La invulnerabilidad del dash evita el daño de proyectiles y enemigos, pero caer al vacío inflige daño al terminar la animación.



### Salto

**Propósito:**  
Permitir la navegación vertical, el esquive de proyectiles a nivel de suelo y el cruce entre plataformas flotantes.

**Activación:**  
Presionar el botón de salto mientras se está en contacto con el suelo.

**Reglas:**  
- Aplica un impulso vertical instantáneo hacia arriba.  
- Cuenta con una tolerancia de pulsación antes de tocar el suelo (*jump buffer*) de 0.1 segundos para que el salto se ejecute de inmediato al aterrizar. 
- No se puede ejecutar un segundo salto en el aire a menos que se tenga activo el potenciador temporal de doble salto.

**Entrada:**  
Barra Espaciadora (Teclado) / Botón `A` (Mando Xbox) / Botón `Cruz` (Mando PS). 

**Estado inicial:**
`Idle`, `Run`.

**Estado final:**
**Estado final:** `InAir_Ascending` -> `InAir_Falling` -> `Landing` -> `Idle/Run`.

**Recursos utilizados:**
Ninguno (uso continuo).

**Recompensa:**
Acceso a plataformas superiores y evasión de ataques aéreos o rasantes.

**Penalización:**
Inercia aérea comprometida frente a proyectiles si no se cuenta con el Dash disponible.

**Interacciones con otras mecánicas:**
- Permite activar el Dash en el aire (1 uso por salto). 
- Permite ejecutar el Ataque aéreo en suspensión.

**Casos límite:**  
- **Techos bajos:** Si el personaje choca su cabeza contra una superficie sólida en pleno ascenso, la velocidad vertical se anula de inmediato y pasa directamente a caída libre.


### Ataque básico

**Propósito:**  
Ser la principal herramienta ofensiva directa para infligir daño a los enemigo y abrir cofres.

**Activación:**  
Presionar el botón de ataque mientras se está en tierra o en el aire.

**Reglas:**  
- En tierra, presionar repetidamente encadena un combo de 2 a 3 cortes consecutivos. 
- Cada tajo proyecta una caja de impacto (*hitbox*) frontal durante 0.10 segundos. 
- Conectar un golpe detiene momentáneamente la animación (*hitstop* de 0.05 segundos) para generar impacto visual. 
- No puede ejecutarse mientras se está en animación de aturdimiento por daño recibido.

**Entrada:**  
`J` / Clic Izquierdo (Teclado/Mouse) o Botón `X` (Mando Xbox) / Botón `Cuadrado` (Mando PS).

**Estado inicial:**
`Idle`, `Run`, `InAir`.

**Estado final:**
Retorno a `Idle` tras la ventana de recuperación del ataque.

**Recursos utilizados:**
Ninguno.

**Recompensa:**
Inflige daño a la vida del enemigo y genera retroceso (*knockback*) leve en enemigos comunes.

**Penalización:**
Breve tiempo de recuperación (0.1 segundos) al final del combo.

**Interacciones con otras mecánicas:**
- La animación de recuperación puede cancelarse inmediatamente ejecutando un Dash. 
- **Casos límite:**

**Casos límite:**  

  - **Múltiples impactos simultáneos:** Si el arco de la espada toca a 2 o más enemigos a la vez, el daño se aplica a todos los objetivos dentro del área de impacto.

## Mecánicas secundarias

- **Interacción con Comerciante y Cofres:** Pulsar el botón de interactuar (`E` / `Botón Y`) frente al mercader o un cofre para desplegar el menú de compra o recolectar botines.

- **Atracción Magnética de Monedas:** Las monedas y orbes soltados por enemigos se desplazan automáticamente hacia el jugador cuando entra en un radio de proximidad de 3 unidades.

- **Consumo de Potenciadores Temporales:** Recoger del suelo un orbe de daño, doble salto o invulnerabilidad aplica el estado alterado por 10 segundos reemplazando el efecto activo anterior.


> **Navegación:** [[00 - Índice]] · ← [[01 - Jugabilidad]] · [[03 - Sistemas]] →
