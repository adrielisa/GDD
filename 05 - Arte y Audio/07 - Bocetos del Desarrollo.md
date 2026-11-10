# Bocetos del Desarrollo

Dibujos a mano de la **fase inicial del desarrollo**, antes de pasar a pixel art. Son la base de los diseños de Eon, de los dos primeros jefes, de la magia del Mago oscuro y del interior de su templo. Aquí se guardan como referencia: el arte final está en [[06 - Galería de Assets]] y las reglas de estilo en [[01 - Dirección de Arte]].

> [!info] Cómo leer esta página
> - Cada boceto lleva qué se conservó en el juego y qué cambió.
> - Son fotos de cuaderno (lápiz y rotulador); los colores pueden variar un poco respecto al papel.
> - Los archivos están en `05 - Arte y Audio/Galería de Assets/Bocetos/`.

## Resumen

| Boceto | Tema | Dónde acabó |
| --- | --- | --- |
| [[#Eon — diseño del personaje]] | Armadura, casco y capa de Eon | Sprite de Eon |
| [[#Eon — ciclo de carrera con espada]] | 12 poses de carrera | Animación `run` de Eon |
| [[#Eon — poses de ataque]] | Embestida con espada | Ataque y dash de Eon |
| [[#Chasko y el Doble salto]] | Jefe 1 y su drop | Chasko y el Camarón de Chasko |
| [[#Templo del Mago — interior]] | Composición de la sala del jefe | Escena `Ruina_Mago` |
| [[#Templo del Mago — piezas y paleta]] | Casetas, verja, cornisa y columna | Piezas y fondo del templo |
| [[#Mago oscuro y su magia]] | Jefe 2, sus ataques y su drop | Mago oscuro, efectos v2 y Filo de sombra |

---

## Eon

### Eon — diseño del personaje

![[05 - Arte y Audio/Galería de Assets/Bocetos/eon_boceto_diseno.jpg|420]]

Primer diseño completo de Eon, a lápiz.
- **Casco cúbico** con una rendija de visor y la parte de abajo abierta, que deja ver la barbilla.
- **Hombreras y peto** de placas, cinturón ancho, pantalón holgado y botas con caña.
- **Capa** que cae por un lado y **espada a la espalda** con la empuñadura sobre el hombro.

**En el juego:** se conservan la silueta acorazada, la capa y la espada. Ver [[06 - Galería de Assets#Eon]] y [[02 - Personajes y Animación]].

### Eon — ciclo de carrera con espada

![[05 - Arte y Audio/Galería de Assets/Bocetos/eon_boceto_carrera_espada.jpg]]

Estudio de movimiento de **12 cuadros** (3 filas de 4, de izquierda a derecha) con maniquí: Eon corre inclinado hacia delante con la espada baja y hacia atrás, el brazo libre recogido y los hombros que se mueven al ritmo de las piernas.

**En el juego:** es la base de la animación de correr. Ver [[06 - Galería de Assets#Correr]].

### Eon — poses de ataque

![[05 - Arte y Audio/Galería de Assets/Bocetos/eon_boceto_poses_ataque.jpg]]

Dos poses de embestida con la espada sujeta baja y en diagonal, con todo el peso hacia delante.
- **Izquierda:** variante temprana con la cara descubierta, pelo corto y **gafas**, y vendas cruzadas en la bota.
- **Derecha:** el mismo movimiento con el cuerpo acorazado y sin cabeza definida.

**En el juego:** la pose de embestida se usa en el ataque y el dash. La versión con gafas quedó descartada: Eon lleva el casco cerrado.

---

## Jefe 1 — Chasko

### Chasko y el Doble salto

![[05 - Arte y Audio/Galería de Assets/Bocetos/chasko_boceto.jpg]]

Hoja de exploración del primer jefe, a rotulador y lápiz.
- **Chasko** (izquierda): camarón rojo y naranja de cuerpo acorazado y enroscado, un ojo negro grande, antenas largas y cola en abanico.
- **Variantes a lápiz** (abajo): versiones de tipo escorpión con la cola en segmentos alzada sobre el lomo.
- **Ataque** (derecha): la pinza cierra de golpe y lanza un **chorro de agua**, la idea de partida de las burbujas de cavitación.
- **Habilidad Doble salto** (arriba a la derecha): camarón pequeño con burbujas, el objeto que suelta al ser derrotado.

**En el juego:** el diseño final mezcla las dos ideas: camarón de tipo escorpión con la cola sobre el lomo. El chorro se convirtió en la **burbuja** que dispara la pinza y el camarón pequeño en el **Camarón de Chasko** que da el Doble salto. Ver [[06 - Galería de Assets#Jefe 1 — Chasko]], [[06 - Galería de Assets#Burbuja de Chasko]] y [[06 - Galería de Assets#Camarón de Chasko (drop del Doble salto)]].

---

## Templo del Mago oscuro

### Templo del Mago — interior

![[05 - Arte y Audio/Galería de Assets/Bocetos/templo_boceto_interior.jpg]]

Composición de la sala del jefe.
- **Columnas verdes oscuras** a los dos lados, con muros de ladrillo detrás, que enmarcan la escena.
- **Luz amarilla** que entra desde arriba en rayos.
- En el centro, una **verja con arco** entre dos **casetas** de tejado a dos aguas.

**En el juego:** la sala de `Ruina_Mago` conserva el encuadre de columnas laterales, el ladrillo detrás y la puerta central con arco. Las columnas pasaron a **piedra gris** (ver la paleta del boceto siguiente). Ver [[06 - Galería de Assets#Jefe 2 — Mago oscuro]] y [[03 - Entornos]].

### Templo del Mago — piezas y paleta

![[05 - Arte y Audio/Galería de Assets/Bocetos/templo_boceto_piezas.jpg|520]]

Piezas sueltas del templo a rotulador gris.
- **Caseta** de tejado en punta con dos ventanas.
- **Pilar de la verja** con arco, **muro de ladrillo** curvo y **verja de hierro** con puntas.
- **Bloque de cornisa** y **columna** con base de ladrillo.
- **Paleta de rotuladores:** WG7 (gris cálido, para la base de ladrillo) y CG9, CG7 y CG5 (grises fríos, de más oscuro a más claro).

**En el juego:** esta paleta de grises es la del templo: columnas, ladrillos, arcos, puertas y suelo del interior. Ver la sección del templo en [[06 - Galería de Assets]].

---

## Jefe 2 — Mago oscuro

### Mago oscuro y su magia

![[05 - Arte y Audio/Galería de Assets/Bocetos/mago_boceto_magia.jpg]]

Hoja del segundo jefe con su magia y su drop.
- **Mago** (derecha): espíritu encapuchado **morado** sin cuerpo, con un **ojo cian** en el hueco de la capucha y la parte de abajo que se deshace como humo.
- **Conjuro de fuego** (arriba a la izquierda, a lápiz): el mago con una llama en la mano.
- **Pico magma:** tres tamaños de pico de **piedra negra con vetas de lava**.
- **Explosión:** secuencia de 9 pasos, de una chispa amarilla a una bola de fuego que acaba en humo gris.
- **Desaparición:** 7 pasos en los que el mago se enrosca y se reduce hasta un punto.
- **Habilidad Dash cortante:** una hoja morada con filo rojo.

**En el juego:**
- El mago conserva la capucha morada y el ojo cian, que se vuelve naranja al conjurar ([[03 - Enemigos y NPC]]).
- La desaparición es el **remolino** con el que aparece y desaparece.
- El pico y la explosión son la base de los **efectos v2** (picos de piedra con lava y explosión con humo).
- El Dash cortante lo entrega el **Filo de sombra**.

Ver [[06 - Galería de Assets#Jefe 2 — Mago oscuro]], [[06 - Galería de Assets#Efectos del Mago oscuro]] y [[06 - Galería de Assets#Habilidades]].

> **Navegación:** [[00 - Índice]] · ← [[06 - Galería de Assets]]
