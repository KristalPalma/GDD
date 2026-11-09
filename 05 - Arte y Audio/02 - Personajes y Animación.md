# Personajes y Animación

## Descripción de la sección

Documenta cómo deben verse y comportarse visualmente los personajes.

## Requisitos por personaje

| Personaje | Modelo/Sprite | Animaciones | VFX | Estado |
|---|---|---|---|---|
| Elaki (protagonista) | Modelo 3D `personaje_modelo.blend` (1.60 m). Sprites isométricos de 192×192, 112 px de alto. | Espera (respiración), caminar, correr y muerte, en 8 direcciones. | Manchas rojas de daño en pantalla (UI). | Animaciones terminadas y subidas al repositorio de assets. Faltan retratos y sprite de diálogo. |
| Manifestación de Margarita (Hermana) | Modelo 3D `Character_hermana.blend` (1.77 m). Sprites de 192×192, 124 px de alto. Falda y pelo con simulación de tela. | Correr herida, gateo y combo de ataque, en 8 direcciones. | Gusanos y sangre en el sprite. | Animaciones terminadas y subidas. Pendiente corregir el giro de 45° de las direcciones y faltan la aparición de espaldas, el giro y la versión en la tina. |
| Criatura canina (perro humanoide) | Modelo 3D `Character_perro.blend` (1.84 m). Sprites de 224×224, 132 px de alto. | 13 animaciones renderizadas (ver tabla siguiente). Subidas: correr, ataque y recoger. | Sangre vino en manos y boca. | Animaciones terminadas. Falta el perro doméstico original. |
| Margarita (versión real) | — | Reflejo en la tina (Nivel 3). | Ondas de agua. | Sprite de 192 x 192 terminado. |
| Madre | — | Escenas de desayuno, con tres estados de deterioro. | — | Pendiente |
| Padre | — | Escenas de desayuno. | — | Pendiente |

### Animaciones disponibles

| Personaje | Animación | Frames por dirección | Tiempo por frame | Bucle |
|---|---|---|---|---|
| Elaki | Espera (respiración) | 4 | 450, 150, 450, 150 ms | Sí |
| Elaki | Caminar | 12 | 120 ms | Sí |
| Elaki | Correr | 8 | 120 ms | Sí |
| Elaki | Muerte (caída hacia delante) | 20 | 120 ms | No, termina tendido |
| Manifestación de Margarita | Correr herida | 8 | 120 ms | Sí |
| Manifestación de Margarita | Gateo | 8 | 40 y 80 ms alternados (ritmo frenético) | Sí |
| Manifestación de Margarita | Combo de ataque | 12 | 120 ms | No |
| Criatura canina | Correr | 8 | 120 ms | Sí |
| Criatura canina | Ataque | 20 | 120 ms | No |
| Criatura canina | Recoger objeto | 9 | 120 ms | No |
| Criatura canina | Espera, caminar, gateo, gateo a cuatro patas, morder (2 variantes), morder el cuello, grito, muerte y agonía | Según la animación | 120 ms | Según la animación |

## Animaciones

### Movimiento

- **Idle:** Elaki respira: en el frame 2 suben los hombros y el torso 1 px; en el 3 sube todo lo que está por encima de la cintura, incluida la cabeza. Las piernas no se mueven. La criatura canina tiene una espera encorvada (*Zombie Idle*).
- **Caminar:** Elaki, 12 frames. La criatura canina tiene caminar y gateo.
- **Correr:** Elaki y la criatura canina, 8 frames. La Manifestación de Margarita corre herida, cojeando, o gatea a cuatro patas.
- **Saltar:** No aplica. El juego no tiene salto.
- **Caer:** No aplica como movimiento; solo existe la caída de la muerte.

### Interacción

- Elaki: inspeccionar e interactuar se comunican con la cámara y la UI.
- Criatura canina: recoger un objeto del suelo.

### Combate

Elaki no ataca. Las criaturas sí:

- **Manifestación de Margarita:** combo cuerpo a cuerpo con las garras. Es donde mejor se ve la espiral del vientre.
- **Criatura canina:** ataque, mordidas, mordida al cuello y grito antes de la persecución.

### Daño

Elaki no tiene animación de daño. El daño se comunica con manchas rojas progresivas en la pantalla (ver [[03 - Sistemas]] y [[04 - Interfaz Visual]]).

### Muerte / derrota

- **Elaki:** cae hacia delante y se queda tendido (20 frames, sin bucle). Da paso a la pantalla de derrota.
- **Criatura canina:** muerte y agonía, disponibles, aunque en el diseño actual no se puede derrotar.

## Diseño de cada personaje

### Elaki

- Adolescente de 1.60 m, unas 6.5 cabezas. Pelo negro con flequillo y largo hasta el cuello. Playera blanca con mangas raglán negras, pantalón oscuro, calcetas y pantuflas moradas.
- El modelo se reconstruyó desde una lámina de referencia, porque la primera versión (4 cabezas) no correspondía a la lámina.
- En caminar y correr, el pelo y la silueta de N, NE, E, SE y S se retocaron a mano; SW, W y NW son el espejo de SE, E y NE.
- **Nota:** [[03 - Personajes]] describe el pelo castaño oscuro y la piel morena; el modelo actual tiene el pelo casi negro (`#161616`) y la piel morena clara. 

### Manifestación de Margarita

- Mujer alta (1.77 m) y demacrada, con piel morena de subtono azul y textura de celdas, como un vertido acrílico.
- Brazos largos con codo huesudo y manos de garra. Cara angosta, ojos hundidos, sonrisa siniestra y cuello oscurecido.
- Agujeros en la piel de los que salen gusanos, y manchas de sangre.
- Espiral tipo amonita en el vientre, a través de un rasgón del vestido.
- Vestido negro, sucio y roto, con la falda por encima de las rodillas. Está descalza.
- La falda y el pelo largo se simulan como tela, para que tengan inercia al moverse.
- El rostro se dibujó a mano (cara oscura, dos ojos `#b8968c` y una sonrisa en U) y se llevó a los demás frames con etiquetas 3D.

### Criatura canina

- Humanoide de 1.84 m con cuerpo demacrado de piel gris: costillas, columna y omóplatos salientes, y joroba.
- Brazos muy largos (2 m de envergadura) y patas digitígradas. Garras oscuras.
- Cráneo ancho tipo pitbull con hocico corto y sonrisa de oreja a oreja, con la boca entreabierta.
- La zona de los ojos es oscura, con un solo punto de luz.
- Greñas beige grisáceas, como las del perro de la familia, a lo largo de la columna y en la cabeza. Cola huesuda.
- Cuerpo sucio, con mugre en manos y pies y sangre vino en las manos y la boca.
- El rostro de la animación de ataque se dibujó a mano y se llevó a las demás animaciones.

## Proceso de producción

```text
REFERENCIAS Y LÁMINA
   ↓
MODELO 3D EN BLENDER (pose en T, una malla, materiales con prefijo)
   ↓
FBX → MIXAMO (auto-rig y animaciones "With Skin")
   ↓
PLANTILLA DE RENDER (cámara isométrica fija, luz fija, materiales cel de 3 tonos)
   ↓
RENDER EN 8 DIRECCIONES (512 px, el personaje gira 45° por dirección)
   ↓
PROCESADO (reducción a pixel art, paleta, contorno, limpieza → .aseprite)
   ↓
RETOQUE A MANO EN ASEPRITE (rostro, pelo, silueta, colores)
   ├── Propagar el retoque a todos los frames (etiquetas 3D)
   └── Espejar direcciones (SW←SE, W←E, NW←NE)
   ↓
EXPORTAR TIRAS POR DIRECCIÓN → REPOSITORIO DE ASSETS → UNITY
```

## Convenciones

Define nombres de archivos, tamaños, esqueletos, rigging, frames o formatos cuando sea necesario.

**Tamaños y escala:**

| Personaje | Lienzo | Línea del suelo | Altura | Pivote en Unity |
|---|---|---|---|---|
| Elaki | 192×192 | y = 160 | 112 px | (96, 160) → normalizado (0.5, 0.167) |
| Manifestación de Margarita | 192×192 | y = 160 | 124 px | (96, 160) → (0.5, 0.167) |
| Criatura canina | 224×224 | y = 176 | 132 px | (112, 176) → (0.5, 0.214) |

Todos los sprites se anclan por los pies. Así quedan alineados aunque el lienzo sea distinto.

**Direcciones:** N, NE, E, SE, S, SW, W, NW en los tags de Aseprite; norte, noreste, este, sureste, sur, suroeste, oeste, noroeste en los archivos exportados. S es de frente a la cámara.

**Nombres de archivos:**

- Fuente: `<personaje>_<accion>.aseprite`, con un tag por dirección: `<accion>_<DIR>`, por ejemplo `caminar_SE`.
- Exportado: `<personaje>_<accion>_<direccion>.png`, por ejemplo `protagonista_caminar_sureste.png`.
- snake_case, sin espacios ni acentos. Personajes: `protagonista`, `hermana_ella`, `perro_humanoide`.

**Formato de exportación:** Una tira horizontal PNG por dirección, RGB con fondo transparente y una sola capa. En Unity: Sprite Mode Multiple, Grid By Cell Size (192 o 224), Filter Mode Point y Compression None.

**Esqueleto y rigging:** Auto-rig de Mixamo (`mixamorig`). El modelo se sube en pose en T, como una sola malla, con normales hacia afuera y texturas horneadas (una textura procedural no viaja en el FBX). Las animaciones se descargan "With Skin". Si no vienen "In Place", se fijan al renderizar.

**Frames:** 8 por ciclo de carrera, 12 para caminar y ataques largos, 20 para la muerte. 120 ms por frame salvo donde se indique.

**Ubicación:** Fuentes y exportados en el repositorio de assets, `99_Compartido/<personaje>/` (`fuente/` y `arte/animaciones/`). Modelos, plantillas y renders en `Sprites_Game/Personajes/<personaje>/`.

**Licencias:** El peinado de Elaki parte del modelo "Cabello blanco" de Joseserio (Sketchfab, CC-BY-4.0): hay que darle crédito en el juego. Las animaciones son de Mixamo. ==🟣Revisar contra el criterio de "sin recursos de terceros" de [[01 - Ficha del Proyecto]].==


> **Navegación:** [[00 - Índice]] · ← [[01 - Dirección de Arte]] · [[03 - Entornos]] →
