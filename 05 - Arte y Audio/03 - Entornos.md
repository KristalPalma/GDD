# Entornos

## Descripción de la sección

Define la estética y necesidades visuales de escenarios, fondos, objetos y elementos ambientales.

## Zonas

| Zona | Estilo | Elementos | Función |
|---|---|---|---|
| Casa real (prólogo) | Hogar mexicano cotidiano y limpio. Colores cálidos: azulejo beige y madera café rojiza. | Habitación de Elaki, comedor con mesa cuadrada y mantel, baño con lavabo, cuatro toallas, gabinete, espejo y cortina cerrada. | Punto de partida y referencia para comparar los cambios de cada nivel. |
| Casa liminal (Nivel 1) | La misma casa con colores cambiados y espacios vacíos. Alteraciones sutiles. | Baño alterado (toallas distintas, inodoro amarillento, gabinete distorsionado, cortina en estado 1), pasillo prolongado, ventana cubierta con tablas, puerta bloqueada. | Introducir la ruptura de la realidad y la comparación visual. |
| Casa deformada (Nivel 2) | Casa oscura, sucia y abandonada. | Fotografía familiar alterada, sala con sillón y televisión, computadora, ventana con la barda y las figuras, calendario del 31 de octubre. | Persecuciones de la criatura canina y la Manifestación de Margarita. |
| Casa de carne (Nivel 3) | Horror corporal en la arquitectura: paredes carnosas con ojos y órganos. | Paredes con ojos, pasillo con agua y ojos que lloran, baño con cortina abierta y tina. | Punto máximo de deterioro y encuentro final. |

## Modularidad

¿Qué elementos pueden reutilizarse?

- **Azulejos modulares** (terminados): azulejo de 32×16 px, bloque base de 64×32 px (2×2 azulejos), losa de 10 px y líneas de 2 px. Incluyen variantes según la posición en el piso (esquina trasera, bordes traseros, esquinas laterales, interior, tiras y bloque suelto), paredes izquierda y derecha (base y apilable), columna y esquina de pared. Hay una versión beige (casa real) y una versión lila (casa alterada).
- **Cómo se arman:** desde el vértice superior de cada bloque, el siguiente va a +32, +16 (abajo a la derecha) o −32, +16 (abajo a la izquierda). Las paredes van 32 px por encima del vértice del bloque y −32 px por cada nivel apilado. Se dibuja de atrás hacia delante.
- **El baño** se repite en todos los niveles con la misma distribución; solo cambian los colores, los objetos y el estado de la cortina (0 cerrada → 3 abierta).
- **Muebles:** mesa isométrica de madera (256×256) y mesa redonda con flor (32×32). Se pueden reutilizar entre la casa real y sus versiones, cambiando los colores.
- **Recoloreado por versión:** cada dimensión reutiliza las piezas de la casa real con otra paleta o con manchas encima, en lugar de dibujarlas de nuevo.
- **Plantillas:** `Sprite-Azulejo-Plantilla-64x32.aseprite` y `Plantilla de uso.aseprite` sirven de base para piezas nuevas.

## Iluminación

Describe iluminación global, fuentes de luz y cambios durante el juego.

- **En los sprites:** luz fija desde arriba a la izquierda, sin sombras proyectadas. Los personajes y los objetos usan la misma dirección de luz.
- **En Unity:** iluminación 2D de URP para la atmósfera de cada nivel. Propuesta:
  - **Casa real:** luz tenue y cálida, de mañana en el desayuno.
  - **Nivel 1:** luz plana y fría que hace ver los espacios vacíos.
  - **Nivel 2:** penumbra; la luz se concentra en el camino y en los objetos importantes.
  - **Nivel 3:** luz rojiza y baja, con la tina como punto de atención.
- ==🟣Pendiente definir los valores de cada luz en Unity.==

## Efectos visuales

- **Partículas:** No se contemplan.
- **Clima:** No aplica; el juego ocurre dentro de la casa. La vista por la ventana es de noche.
- **Humo:** No aplica.
- **Fuego:** No aplica.
- **Agua:** Agua de la tina en varios niveles, con ondas y el reflejo de Margarita en el Nivel 3. Pasillo con agua en el Nivel 3.
- **Magia / energía:** Portal del espejo con el símbolo de la espiral y distorsión al cruzarlo.
- **Impactos:** Manchas rojas de daño en pantalla. Efectos de pantalla previstos: desenfoque, ojo de pez, texto con *glitch* y viñeta con latido.

## Recursos requeridos

Lista los modelos, sprites, texturas, materiales y efectos necesarios.

| Recurso | Tipo | Estado |
|---|---|---|
| Azulejos modulares de piso y pared (beige y lila) | Sprites isométricos | Terminado |
| Mesa isométrica de madera | Sprite | Terminado |
| Mesa redonda con flor | Sprite | Terminado |
| Comedor: mesa cuadrada con mantel y elementos de la mesa | Sprites | ==🟣Pendiente== |
| Baño: lavabo, espejo, gabinete, inodoro, toallas y tina | Sprites, con variantes por nivel | ==🟣Pendiente== |
| Cortina del baño en 4 estados (cerrada → abierta) y niveles de agua | Sprites | ==🟣Pendiente== |
| Pasillo modular | Sprites | ==🟣Pendiente== |
| Calendario del 31 de octubre | Sprite | ==🟣Pendiente== |
| Fotografía familiar (normal y alterada) | Ilustración | ==🟣Pendiente== |
| Sala con sillón y televisión, y reproductor de video | Sprites | ==🟣Pendiente== |
| Paredes con ojos y órganos (Nivel 3) | Sprites | ==🟣Pendiente== |
| Vista por la ventana: barda y figuras (Nivel 2) y hombre armado (Nivel 3) | Ilustraciones | ==🟣Pendiente== |
| Portal en espiral | Sprite animado y VFX | ==🟣Pendiente== |
| Efectos de pantalla (daño, desenfoque, ojo de pez, *glitch*, viñeta) | VFX / shaders | ==🟣Pendiente== |

**Formato:** PNG con fondo transparente para Unity (Filter Mode Point, Compression None) y fuente `.aseprite`. Los recursos que se usan en más de un momento van en `99_Compartido/` del repositorio de assets.


> **Navegación:** [[00 - Índice]] · ← [[02 - Personajes y Animación]] · [[04 - Interfaz Visual]] →
