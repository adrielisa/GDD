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


## Mecánicas secundarias

Lista las mecánicas que complementan la experiencia pero no constituyen el núcleo.


> **Navegación:** [[00 - Índice]] · ← [[01 - Jugabilidad]] · [[03 - Sistemas]] →
