# Seguridad y Riesgos Técnicos

| Riesgo | Probabilidad | Impacto | Mitigación |
| --- | --- | --- | --- |
| Cienojos (cuerpo segmentado que atraviesa plataformas) es compleja de programar. | Alta | Alto | Prototipar primero con segmentos que siguen un camino (*path following*); limitar a ~18 segmentos. |
| Ataques instakill percibidos como injustos. | Media | Alto | Aviso mínimo de 1,5 s, color y sonido exclusivos; pruebas con jugadores nuevos. |
| Que un jefe o la ruta principal exijan sin querer una habilidad concreta. | Media | Alto | La ruta principal y cada jefe se prueban sin habilidades equipadas; las `AbilityGate` solo se usan en rutas opcionales. |
| Modificadores de potenciadores aplicados dos veces al reequipar. | Media | Medio | `StatModifiers` recalcula los valores desde la base cada vez que cambia el equipo. |
| Alcance: 4 jefes y 5 zonas para un equipo de 5. | Alta | Alto | Vertical slice primero (Costa + Jefe 1); zonas con módulos reutilizables. |
| Ola de picos de magma imposible de esquivar si Eon está ralentizado. | Baja | Medio | La zona segura del extremo siempre existe; la ola nunca se lanza si Eon está pegado al muro del mago. |
| Daño registrado dos veces en un fotograma. | Media | Medio | Lista de objetivos ya golpeados por *hitbox* activa. |
| Guardado corrupto. | Baja | Alto | Escribir en archivo temporal y reemplazar; validación al cargar. |
| Rendimiento con muchos proyectiles y tajos. | Baja | Medio | *Pools* y límites de objetos simultáneos. |

> **Navegación:** [[00 - Índice]] · ← [[04 - Datos y Persistencia]] · [[01 - Alcance]] →
