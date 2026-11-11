# Objetos y Coleccionables

Solo hay tres tipos de elementos que el jugador obtiene: **materiales de monstruos**, **potenciadores** y **habilidades**. No hay objetos de curación ni de escudo: la vida y el escudo se restauran únicamente en puntos de control y al vencer a un jefe.

## 1. Materiales de Monstruos (Moneda de Intercambio)

* **Tipo:** recursos de intercambio y comercio.
* **Obtención:** botín (*drop*) que dejan caer los enemigos específicos al morir.
* **Uso:** comerciar con el mercader en las antesalas de los jefes para adquirir mejoras de atributos.
* **Reglas:** se recogen automáticamente al contacto con Eon; no desaparecen mientras Eon permanezca en la misma zona. Se conservan tras morir.
* **Aspecto en HUD / Inventario:** ranuras dedicadas con contador numérico acumulativo.

| Material         | Enemigo que lo dropea | Tipo de enemigo       | Aspecto del icono                                               |
| :--------------- | :-------------------- | :-------------------- | :-------------------------------------------------------------- |
| **Hueso**  | Earthlem              | Terrestre / Roca      | Hueso desgastado y cubierto de musgo.                           |
| **Ala**    | Aurion                | Volador               | Ala membranosa oscura tipo murciélago.                         |
| **Cabeza** | Driller               | Subterráneo / Gusano | Cabeza cilíndrica serpentina de color verde con ojo brillante. |

## 2. Potenciadores (permanentes y acumulables)

* **Tipo:** mejoras pasivas directas de atributos.
* **Obtención:** intercambio entregando materiales de monstruos al mercader en las antesalas de cada jefe.
* **Uso:** se aplican de forma pasiva y permanente una vez adquiridos. Los atributos de daño, vida y escudo permiten hasta 3 compras acumulativas (+10 % por nivel, hasta un máximo de +30 %). La velocidad se adquiere en un único nivel (+5 %).
* **Inventario:** el menú de estado muestra el nivel adquirido y el porcentaje total activo de cada estadística.
* **Persistencia:** nunca se pierden al morir ni al reiniciar en puntos de control.

| Potenciador                    | Efecto por compra                           | Límite de compras | Bonificación máxima | Material de intercambio asociado |
| :----------------------------- | :------------------------------------------ | :----------------: | :-------------------: | :------------------------------- |
| **Velocidad**            | +5 % de velocidad de movimiento.            |      1 nivel      |         +5 %         | Alas                             |
| **Fuerza (Daño)**       | +10 % de daño en todos los ataques de Eon. |     3 niveles     |         +30 %         | Huesos                           |
| **Vitalidad (Vida)**     | +10 % de vida máxima base.                 |     3 niveles     |         +30 %         | Cabezas                          |
| **Protección (Escudo)** | +10 % de capacidad máxima de escudo.       |     3 niveles     |         +30 %         | Combinación de materiales       |

## 3. Habilidades (entregadas por jefes)

* **Tipo:** acciones o mejoras de movimiento permanentes.
* **Obtención:** al vencer a cada jefe (el Jefe 2 entrega dos).
* **Uso:** se equipan en una de las **3 ranuras de habilidad**. Ninguna se descarta: las que no se usan quedan guardadas para elegirlas después.
* **Inventario:** al seleccionar una habilidad se muestran su control y su función.
* **Cambios:** fuera de las arenas de jefe.
* **Entrega en el mundo:** el jefe suelta un objeto que la representa y que se recoge al tocarlo. El del Jefe 1 es el **Camarón de Chasko**; el Jefe 2 suelta la **Brasa del Mago** (Tajo ardiente) y el **Filo de sombra** (Dash cortante), y el Jefe 3, la **Espina de Cienojos** (Espinas punzantes).

| Habilidad                | Origen | Tipo   | Control                  | Efecto                                                                                            | Icono                                                                      |
| :----------------------- | :----- | :----- | :----------------------- | :------------------------------------------------------------------------------------------------ | :------------------------------------------------------------------------- |
| **Doble salto**    | Jefe 1 | Pasiva | Salto en el aire         | Segundo salto en el aire (80 % de altura), impulsado por una burbuja bajo los pies.               | Camarón de Chasko: camarón pequeñito naranja y enroscado (16 × 16 px). |
| **Tajo ardiente**  | Jefe 2 | Activa | `J` (prototipo: `K`) | La espada lanza un tajo de fuego que atraviesa enemigos: 15 de daño, alcance 8 u, recarga 1,2 s. | Brasa del Mago: brasa naranja con chispas (20 × 20 px).                   |
| **Dash cortante**  | Jefe 2 | Pasiva | Dash                     | El dash hace 20 de daño a cada enemigo atravesado.                                               | Filo de sombra: hoja oscura con filo rojo (20 × 20 px).                   |
| **Espinas punzantes** | Jefe 3 | Pasiva | — | 30 % de probabilidad de que el atacante reciba el 50 % del daño que le hace a Eon; no con instakill ni con daño del entorno. | Espina de Cienojos: espina curva azul noche con una gota de veneno en la punta (32 × 32 px). |

Con 4 habilidades y 3 ranuras, el jugador decide qué combinación llevar a la isla final; las cuatro siguen disponibles en el inventario.

> **Navegación:** [[00 - Índice]] · ← [[03 - Enemigos y NPC]] · [[05 - Misiones y Desafíos]] →
