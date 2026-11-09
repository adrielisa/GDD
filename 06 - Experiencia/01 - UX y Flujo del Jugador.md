# UX y Flujo del Jugador

## Flujo general

```text
Menú principal → Nueva partida → Prólogo (cómic, omitible) → Playa del Despertar
   → Zona → Antesala (mercader + punto de control) → Preparar inventario → Arena de jefe
   → Habilidad guardada en el inventario → Siguiente zona … → Isla Final → Final → Créditos → Menú
   (en cualquier momento tras un jefe: volver a zonas superadas para acumular XP)
```

Continuar lleva directamente al último punto de control guardado.

## Primeros minutos

1. **Prólogo:** el jugador lee o salta el cómic; la última página muestra la derrota de Eon.
2. **Despertar:** control inmediato. Un aviso breve muestra Mover y Saltar.
3. **Primer Aurion:** aparece el aviso de Atacar (`Enter`); al matarlo, los orbes de XP vuelan hacia Eon y el contador del HUD se anima.
4. **Dash:** un hueco que solo se cruza con dash aéreo muestra el aviso de Dash.
5. **Primer punto de control:** un aviso explica que la vida solo se restaura aquí o al vencer a un jefe.
6. **Mercader (antesala del Jefe 1):** el primer diálogo explica que la XP compra potenciadores permanentes y que solo funcionan equipados en el inventario. La primera compra abre el inventario con la pestaña de potenciadores.

Los avisos aparecen una sola vez, en el momento en que se necesitan, y nunca detienen el juego.

## Preparación antes de un jefe

- Cada jefe tiene una antesala con el mercader y un punto de control. Al tocarlo aparece el aviso *«Revisa tu inventario (Tab) antes de entrar»*.
- La entrada a la arena muestra el aviso *«Dentro no podrás cambiar tu equipo»*.
- Si hay ranuras vacías y elementos sin equipar en el inventario, el aviso lo menciona.

## Entrega de una habilidad

1. Muere el jefe; cinemática breve. Vida y escudo se restauran.
2. Ilustración de la habilidad con su nombre, su control y su función.
3. La habilidad **se guarda en el inventario**; no se descarta ninguna. Aviso: *«Abre el inventario (Tab) para equiparla»*. En el prototipo el jefe suelta un objeto (Chasko: el Camarón de Chasko) que hay que tocar, y el aviso indica Pausa ▸ Objetos ▸ Habilidades.
4. El jugador decide si la equipa y qué deja guardado.

## Inventario

- Al seleccionar una habilidad o un potenciador se muestra siempre su función y, si tiene, su tecla.
- Los potenciadores no se activan: estar equipados basta.
- Se puede cambiar el equipo en cualquier momento fuera de una arena de jefe.

## Derrota y reintento

- Pantalla de derrota con dos opciones: **Reaparecer** (por defecto) y **Salir al menú**.
- Reaparecer lleva al último punto de control con vida y escudo completos. La XP, los potenciadores y las habilidades se conservan.
- Si la derrota fue por instakill, la pantalla muestra una pista breve (*«Evita la cabeza: es letal»*), solo las 2 primeras veces.

## Navegación del mundo

- Las rutas opcionales muestran una pista visual de lo que piden (saliente alto, interruptor lejano).
- La Entidad en el horizonte marca la dirección general del avance.
- Las zonas superadas siguen abiertas y sus enemigos reaparecen.

> **Navegación:** [[00 - Índice]] · ← [[05 - Audio y Música]] · [[02 - UI y Menús]] →
