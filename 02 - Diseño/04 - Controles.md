# Controles

## Descripción de la sección

Esta sección define el mapeo físico y la respuesta sensorial de cada comando disponible para controlar a el protagonista. Para un prototipo de acción rápida en 2 meses y orientado a pruebas cortas (1-2 minutos), la prioridad es la inmediatez absoluta: cero latencia percibida, botones universales y retroalimentación audiovisual instantánea para que cualquier evaluador domine el combate sin consultar un manual.

## Mapa de controles

| Acción                      | Teclado                    | Mouse | Control                    | Táctil |
| --------------------------- | -------------------------- | ----- | -------------------------- | ------ |
| Mover (Izquierda / Derecha) | `A` / `D`                  | —     | Stick Izquierdo / D-Pad    | —      |
| Interactuar con cañón       | `E` / `Enter`              | —     | Botón `Y`                  | —      |
| Ataque principal            | J                          | —     | Botón `X` (Cuadrado en PS) | —      |
| Ataque secundario           | `S` + `J` (Abajo + Ataque) | —     | Stick Abajo + Botón `X`    | —      |
| Saltar                      | `W`                        | —     | Botón `A` (Cruz en PS)     | —      |
| Menú                        | Escape                     | —     | Botón `Start` / `Options`  | —      |

## Principios de control

- Los controles deben ser consistentes.
- Las acciones críticas deben ser fáciles de identificar.
- Debe existir retroalimentación visual, sonora o háptica cuando corresponda.
- Evitar combinaciones innecesariamente complejas.

- **Consistencia:** Las reglas de salto y aceleración se mantienen idénticas en todo el juego.
- **Tolerancia de entrada (_Coyote Time_ & _Input Buffering_):**
    
    - _Coyote Time:_ Se permite saltar hasta 0.08 segundos después de haber abandonado el borde de una plataforma sin registrar caída prematura.
        
    - _Input Buffering:_ Si el jugador presiona Ataque o Salto hasta 0.10 segundos antes de tocar el suelo o terminar una animación, la acción se ejecuta automáticamente al quedar libre.
        
- **Cero combinaciones complejas:** No se implementan secuencias tipo media luna ni dobles toques de dirección; cada acción responde a una pulsación limpia.


## Reasignación

- **Alcance en el prólogo (2 meses):** No se incluirá reasignación libre de teclas dentro del juego para no consumir tiempo de desarrollo en interfaces complejas.

## Entrada y retroalimentación

Describe qué ocurre inmediatamente después de cada entrada importante.

| **Entrada**                | **Acción resultante**            | **Retroalimentación visual**                                                                               | **Retroalimentación sonora**                        | **Sensación / Game Feel**                                                   |
| -------------------------- | -------------------------------- | ---------------------------------------------------------------------------------------------------------- | --------------------------------------------------- | --------------------------------------------------------------------------- |
| **Pulsar Ataque (Tierra)** | Espadazo horizontal              | Estela de color saturado (cian/blanco) en forma de media luna. Destello en punta de espada.                | Sonido seco de tajo cortando aire (_whoosh_ agudo). | Inercia frontal de 0.5 unidades                                             |
| **Abajo + Ataque (Aire)**  | Espadazo en caída libre vertical | Estela vertical recta; silueta del protagonista inclinada hacia abajo con la punta de la espada brillante. | Silbido agudo descendente.                          | Caída acelerada inmediata; rebote elástico hacia arriba si impacta enemigo. |
| **Recibir Daño**           | Impacto y retroceso              | Parpadeo intermitente del sprite (rojo/transparente) durante 0.7 segundos de inmunidad.                    | Sonido sordo de impacto contundente y quejido seco. | Empuje hacia atrás en el eje X; pérdida de control durante 0.15 segundos.   |

> **Navegación:** [[00 - Índice]] · ← [[03 - Sistemas]] · [[05 - Progresión]] →
