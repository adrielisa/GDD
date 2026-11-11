# Economía y Recursos

La economía gira en torno a la recolección de tres recursos biológicos de intercambio: **materiales de monstruos (Huesos, Alas y Cabezas)**. Los enemigos comunes los sueltan al morir y el mercader los intercambia por mejoras permanentes de atributos para Eon.

## Recursos

| Recurso                 | Obtención                                                                                                                       | Uso                                                     | Límite                                                             | Pérdida / recarga                                                                                     |
| ----------------------- | -------------------------------------------------------------------------------------------------------------------------------- | ------------------------------------------------------- | ------------------------------------------------------------------- | ------------------------------------------------------------------------------------------------------ |
| **Salud (HP)**    | Se restaura por completo en puntos de control, al vencer a un jefe y al reaparecer.                                              | Mantener a Eon con vida.                                | 100 HP base (hasta 130 HP con Vitalidad máx.).                     | Se pierde al recibir daño una vez agotado el escudo. No hay curación en campo. En 0 HP: derrota.     |
| **Escudo (SP)**   | Valor base de protección. Se restaura por completo junto con la vida en puntos de control, al vencer a un jefe y al reaparecer. | Absorber daño directo antes de comprometer la salud.   | Base definida según diseño (hasta +30 % con Protección máx.).   | Se reduce con impactos enemigos. Funciona con las mismas reglas de daño y restauración que la salud. |
| **Hueso**         | Drop garantizado/probable de **Earthlem**.                                                                                 | Moneda de intercambio (mejoras de ataque/fuerza).       | 999.                                                                | Se gasta con el mercader. **Se conserva al morir.**                                              |
| **Ala**           | Drop garantizado/probable de **Aurion**.                                                                                   | Moneda de intercambio (mejoras de velocidad/movilidad). | 999.                                                                | Se gasta con el mercader. **Se conserva al morir.**                                              |
| **Cabeza**        | Drop garantizado/probable de **Driller**.                                                                                  | Moneda de intercambio (mejoras de vitalidad/salud).     | 999.                                                                | Se gasta con el mercader. **Se conserva al morir.**                                              |
| **Potenciadores** | Intercambio por materiales con el mercader.                                                                                      | Aumentos pasivos permanentes a las estadísticas.       | Niveles fijos (Velocidad: 1 nivel; Daño, Vida, Escudo: 3 niveles). | Permanentes. No ocupan ranuras; se aplican directamente al personaje.                                  |
| **Habilidades**   | Derrotar jefes.                                                                                                                  | Nuevas acciones activas y mejoras de movilidad.         | 3 equipadas a la vez.                                               | Nunca se pierden ni se descartan. Se gestionan desde el inventario.                                    |

---

## Fuentes de Materiales

| Enemigo            | Tipo                  | Material obtenido | Tasa / Cantidad |
| ------------------ | --------------------- | ----------------- | :-------------: |
| **Earthlem** | Terrestre / Roca      | **Hueso**   |  1–2 por baja  |
| **Aurion**   | Volador               | **Ala**     |  1–2 por baja  |
| **Driller**  | Subterráneo / Gusano | **Cabeza**  |   1 por baja   |

- Los enemigos comunes **reaparecen** al descansar en un punto de control o al volver a entrar a una zona.
- El jugador puede regresar a biomas anteriores para farmear materiales específicos según la mejora que desee adquirir antes de entrar a un jefe.

---

## Catálogo de Potenciadores (Mercader)

Todas las mejoras son **pasivas y permanentes**: una vez compradas, su efecto queda integrado de inmediato en los atributos de Eon sin ocupar ranuras de inventario.

| Potenciador                    | Efecto por nivel                            | Niveles disponibles | Efecto máximo total | Coste orientativo de materiales |
| ------------------------------ | ------------------------------------------- | :-----------------: | :------------------: | ------------------------------- |
| **Velocidad**            | +5 % de velocidad de movimiento.            |          1          |    **+5 %**    | Alas                            |
| **Fuerza (Daño)**       | +10 % de daño en todos los ataques de Eon. |          3          |   **+30 %**   | Huesos                          |
| **Vitalidad (Vida)**     | +10 % de vida máxima.                      |          3          |   **+30 %**   | Cabezas                         |
| **Protección (Escudo)** | +10 % de escudo máximo.                    |          3          |   **+30 %**   | Combinación de materiales      |

- Las mejoras no adquiridas en una antesala continúan disponibles en los siguientes encuentros con el mercader.

---

## Fuentes y Sumideros

### Fuentes

- **Combate ordinario:** enemigos comunes reaparecen y entregan materiales (**Huesos**, **Alas**, **Cabezas**).
- **Jefes:** entregan habilidades únicas de combate/movilidad.
- **Puntos de control y jefes vencidos:** restauran por completo la salud y el escudo de Eon.

### Sumideros

- **Tienda del mercader:** consumo directo de materiales para adquirir niveles de potenciadores.
- **Daño recibido:** reduce progresivamente el escudo (SP) y la vida (HP) hasta el próximo punto de control o muerte.

---

## Reglas

1. **Escudo antes que vida:** el escudo absorbe el daño recibido. La salud solo se reduce una vez que el escudo llega a 0 SP.
2. **Restauración idéntica:** el escudo se comporta en reposición igual que la salud: solo se recarga en puntos de control, al abatir un jefe o al reaparecer.
3. **Instakill:** las caídas al vacío o trampas letales ignoran el escudo, la salud y cualquier invulnerabilidad activa, y no activan Espinas punzantes.
4. **Sin curación en campo:** no existen pociones, consumibles ni orbes de curación ni de escudo durante la exploración o combate.
5. **Persistencia total de inventario:** los materiales recolectados, las habilidades y las mejoras adquiridas **se conservan al morir**.
6. **Reaparición selectiva:** los enemigos comunes reaparecen para permitir el farmeo; los jefes abatidos no reaparecen.

---

## Balance

### Comportamientos que queremos incentivar

- **Caza selectiva:** motivar al jugador a buscar y eliminar enemigos concretos según el material que necesite para la mejora deseada.
- **Supervivencia y precisión:** castigar el error, ya que ni el escudo ni la vida se regeneran de forma pasiva en combate.
- **Exploración y *backtracking*:** volver a zonas previas si se desea optimizar las estadísticas al máximo antes de un combate exigente.

### Comportamientos que queremos evitar

- **Dependencia de curaciones infinitas:** forzar la maestría mecánica y el dominio del movimiento sobre el tanqueo por consumibles.
- **Ignorar el combate regular:** el sistema de materiales obliga a interactuar con los distintos arquetipos de enemigos para progresar en estadísticas.

> **Navegación:** [[00 - Índice]] · ← [[05 - Progresión]] · [[07 - Reglas y Estados del Juego]] →
