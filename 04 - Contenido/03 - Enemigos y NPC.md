# Enemigos y NPC

El juego tiene dos enemigos comunes (Aurion y Earthlem), tres jefes normales y La Entidad. El Driller queda descartado como enemigo común; en el prototipo ocupa de forma provisional el lugar del Jefe 3 (ver abajo). Las cifras son la referencia de diseño; se ajustan en pruebas y se registran en [[03 - Registro de Decisiones]].

## Resumen de enemigos comunes

| Enemigo | Vida | Velocidad | Daño principal | Zonas | Drop de material |
| --- | ---: | --- | --- | --- | --- |
| Aurion | 20 HP | 2,5 u/s patrulla; 7 u/s embestida | Embestida 15; contacto 10 | Costa, Bosque, Archipiélago, Isla Final | Ala |
| Earthlem | 80 HP | 1,2 u/s | Puño 20; onda 15; emerger 10 | Solo zona 3: Bosque y Ruinas | Hueso |

## Aurion

- **Rol:** hostigador aéreo.
- **Comportamiento:** flota a media altura. Al detectar a Eon su núcleo se vuelve rojo, carga 0,5 s y embiste en línea recta hacia la posición registrada. Si falla, queda aturdido 0,8 s a ras de suelo y luego vuelve a subir.
- **Detección:** 6 u horizontales y 4 verticales con línea de visión.
- **Defensas:** ninguna.
- **Debilidad:** un ataque descendente sobre él lo destruye y recupera el dash aéreo de Eon.
- **Recompensa:** Ala (material de intercambio).

```text
Patrullar → Detectar (núcleo rojo, 0,5 s) → Embestir → [falla] Aturdido 0,8 s → Volver a altura
