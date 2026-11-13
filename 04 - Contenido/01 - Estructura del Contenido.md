# Estructura del Contenido

## Descripción de la sección

Organiza el contenido del videojuego en unidades manejables: mundos, capítulos, zonas, niveles, misiones y desafíos.

## Estructura

```text
Juego
├── Mundo / Capítulo 1
│   ├── Nivel
│   ├── Nivel
│   └── Jefe / Evento
├── Mundo / Capítulo 2
│   └── ...
└── Final
```

```text
Juego
PRÓLOGO — LA NEGACIÓN
│   ├── Despertar en la habitación
│   ├── Primer desayuno con los padres
│   ├── Mareo y llegada al baño real
│   ├── Inspección obligatoria del gabinete
│   └── Portal en el espejo
│
├── NIVEL 1 — LA PRIMERA RUPTURA
│   ├── Baño del otro lado
│   ├── Pasaje detrás de la cortina y calendario
│   ├── Versión liminal del cuarto de Elaki
│   ├── Sala, cocina, comedor y cuarto de lavado del otro lado
│   ├── Pasillo con la voz de Margarita
│   ├── Desmayo
│   ├── Segundo despertar
│   └── Segundo desayuno
│
├── NIVEL 2 — LA DEFORMACIÓN
│   ├── Baño real (segunda visita) y portal
│   ├── Baño abandonado y calendario
│   ├── Pasillo con la fotografía familiar
│   ├── Ventana con la barda
│   ├── Sala y cocina en penumbra
│   ├── Video de la computadora
│   ├── Persecución del perro de la familia
│   ├── Encuentro con la Manifestación de Margarita
│   ├── Tercer despertar
│   ├── Tercer desayuno
│   └── Altar del perro y alacena
│
├── NIVEL 3 — LA REALIDAD SE ROMPE
│   ├── Baño real (tercera visita) y portal
│   ├── Baño de carne
│   ├── Parpadeo de la luz y cocina sellada con apéndices
│   ├── Sillón y anuncio en la televisión (opcional)
│   ├── Refrigerador y membrana de la puerta
│   ├── Cuarto deforme
│   ├── Pasillo con apéndices
│   └── Margarita en la tina
│
└── DESENLACE
    ├── Imágenes alternadas de la tina
    ├── Carteles de búsqueda
    ├── Transmisión sobre el cuerpo de Margarita
    ├── Pantalla de texto sobre el joven ahogado
    ├── Escena del edificio
    └── Texto de cierre
```
## Cantidad estimada

| Tipo     |                                                                                                                                        Cantidad |
| -------- | ----------------------------------------------------------------------------------------------------------------------------------------------: |
| Mundos   |                                                                                 1 entorno principal: la casa familiar y sus distintas versiones |
| Niveles  |                                                                                                                  3 niveles jugables + 1 prólogo |
| Misiones |                                                                                           4 objetivos principales, uno por cada sección jugable |
| Enemigos |                                                               2 amenazas de persecución (criatura canina y Manifestación de Margarita) y 1 peligro del entorno (apéndices de carne del Nivel 3) |
| Jefes    |                                                                                                          no se contemplan combates contra jefes |
| NPC      |                                                     0 NPC con diálogo interactivo; el perro de la familia acompaña a Elaki en la casa real |
| Objetos  | Al menos 9 objetos principales: gabinete, medicamentos y productos personales, toallas, espejo, computadora, periódico, calendario, televisión y refrigerador |

## Dependencias

¿Qué contenido debe existir antes de otro?

| Contenido                 | Dependencia                                                                                    |
| ------------------------- | ---------------------------------------------------------------------------------------------- |
| Prólogo                   | Es el inicio del videojuego. No requiere contenido previo.                                     |
| Nivel 1                   | Completar la exploración del baño real, inspeccionar el gabinete y atravesar el primer portal. |
| Nivel 2                   | Llegar al fondo del pasillo del Nivel 1, completar el segundo desayuno y cruzar el espejo.     |
| Persecuciones del Nivel 2 | Activar el evento de la computadora y escapar de la criatura canina. El encuentro con la Manifestación termina siempre en el tercer despertar. |
| Nivel 3                   | Completar el tercer desayuno y atravesar el portal del baño real.                              |
| Desenlace                 | Llegar a la bañera del Nivel 3 y completar el encuentro con "Margarita".                       |
> **Navegación:** [[00 - Índice]] · ← [[04 - Diálogos y Narrativa]] · [[02 - Niveles]] →
