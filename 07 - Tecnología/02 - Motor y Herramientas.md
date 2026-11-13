# Motor y Herramientas

## Descripción de la sección

Documenta las herramientas utilizadas para crear el videojuego y por qué fueron seleccionadas.

## Motor

**Motor:** Unity

**Versión:** Unity 6 6000.6.3f1

**Renderizado:** 2D con perspectiva isométrica, con Universal Render Pipeline 2D (URP 17.6), sprites, Tilemaps y Pixel Perfect Camera. Los sprites se ordenan según su posición en la vista isométrica.

**Física:** Física 2D de Unity, mediante Rigidbody2D y Collider2D para gestionar movimiento colisiones y detección de zonas de interacción.

**Sistema de entrada:**
Teclado y ratón. WASD o flechas para el desplazamiento, Shift para correr, clic izquierdo para inspeccionar objetos, tecla E para activar interacciones y Esc para pausar. El proyecto utiliza el paquete Input System (versión 1.20) como único sistema de entrada, con el archivo de acciones `Settings/InputSystem_Actions.inputactions`.
## Lenguajes

| Lenguaje        | Uso                                                                                                     |
| --------------- | ------------------------------------------------------------------------------------------------------- |
| C#              | Programación de las mecánicas, sistemas, controladores, eventos narrativos e interfaces del videojuego. |
| Shaderlab/ HLSL | Creación de efectos personalizados, como el shader del video del portal (`PortalVideo.shader`).         |

## Herramientas

| Herramienta                        | Propósito                                                                                                        | Versión                                                  |
| ---------------------------------- | ---------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------- |
| Unity Editor                       | Desarrollo del videojuego, construcción de escenarios, configuración de físicas, animaciones, escenas y pruebas. | Unity 6 versión: 6000.6.3f1                              |
| Visual Studio Code / Visual Studio | Escritura, edición y depuración de scripts en C#                                                                 | Visual studio: 18.10.3<br>Visual Studio Code:<br>1.143.1 |
| Git                                | Control de versiones y registro de cambios del código y los recursos                                             | 2.55.0.windows.5                                         |
| GitHub                             | Almacenamiento del repositorio, colaboración y seguimiento de cambios del equipo.                                | Servicio web                                             |
| Aseprite                           | Creación de sprites, personajes, elementos visuales y animaciones en pixel art.                                  | Aseprite v1.3.18.6                                       |
| Krita                              | Elaboración de bocetos, ilustraciones, diseños de personajes y escenarios.                                       | v5.3.4.1<br>                                             |
| CapCut                             | Edición de videos narrativos, transmisiones y secuencias cinematográficas del videojuego.                        | v20.0.0                                                  |
| FL Studio                          | Composición musical y producción de la banda sonora del videojuego.                                              | v26.1.7                                                  |
| Obsidian                           | Redacción de documentación y organización del cronograma mediante documentos y hojas de cálculo.                 | v1.15.0<br>                                              |
| ClickUp                            | Gestión del proyecto, organización de actividades y asignación de responsables.                                  | Servicio web                                             |
| Claude Pro                         | Apoyo en documentación, análisis y revisión de código.                                                           | Servicio web / Aplicación local v4.23118.0               |
| ChatGPT Plus                       | Apoyo en documentación, análisis y revisión de código.                                                           | Servicio web / Aplicación local                          |

## Dependencias

Lista librerías, paquetes, plugins o servicios externos.

| Paquete | Versión | Uso |
|---|---|---|
| Universal Render Pipeline (URP) | 17.6.0 | Renderizado 2D y Pixel Perfect Camera |
| Input System | 1.20.0 | Entrada de teclado y ratón |
| 2D Animation | 16.0.1 | Animaciones de personajes |
| 2D Aseprite Importer | 6.0.0 | Importación directa de archivos `.aseprite` |
| 2D Tilemap y Tilemap Extras | 1.0.0 y 9.0.1 | Pisos y paredes de la casa |
| uGUI y TextMeshPro | 2.6.0 | Menús, caja de diálogo y textos |
| Timeline | 6.6.0 | Instalado; las secuencias narrativas usan el componente propio `Secuencia` |
| Test Framework | 1.8.0 | Pruebas automáticas en EditMode |
| Módulos de Unity | — | Física 2D, Animator, Video Player y Audio |

No se utiliza Cinemachine: la cámara se controla con un script propio (`CameraController`).

## Convenciones del proyecto

- **Estructura de carpetas**
```text
Assets/
└── _Carencia/
    ├── Animations/
    ├── Audio/
    │   ├── Ambientes/
    │   ├── Efectos/
    │   ├── Musica/
    │   ├── Voces/
    │   └── Mixer/
    ├── Data/
    ├── Materials/
    ├── Prefabs/
    ├── Resources/          (pausa y guion de diálogos)
    ├── Scenes/
    │   ├── Menu/
    │   ├── Prologo/
    │   ├── Nivel01/
    │   ├── Nivel02/
    │   ├── Nivel03/
    │   ├── Desenlace/
    │   └── Pruebas/        (no entran al build)
    ├── Scripts/
    │   ├── Core/           (estado del juego y guardado)
    │   ├── Player/
    │   ├── Interaction/
    │   ├── Camera/
    │   ├── Cuartos/
    │   ├── Enemies/
    │   ├── Narrative/
    │   ├── Dialogue/
    │   ├── Effects/
    │   ├── Audio/
    │   └── UI/
    ├── Settings/           (Input Actions)
    ├── Sprites/
    ├── Tests/
    ├── Tilemaps/
    ├── UI/
    └── Videos/
```


- **Nomenclatura**
Scripts y clases: PascalCase. Ejemplo: MovimientoJugador.cs.

Métodos y propiedades públicas: PascalCase. Ejemplo: IniciarPersecucion().

Variables privadas: camelCase, sin prefijo. Ejemplo: velocidadCarrera.

Escenas: prefijo del tramo y nombre del espacio. Ejemplos: MEN_Principal, PRO_Casa, N1_Laberinto, N1_Pasillo, R1_Casa, N2_Casa, R2_Casa, N3_Casa, DES_Final. Las escenas de prueba usan el prefijo PRB_.

Prefabs: prefijo PF_. Ejemplo: PF_PerroAcompanante.

Sprites: prefijo SPR_, categoría, nombre y variante. Ejemplo: SPR_PJ_Elaki_Caminar_S_R.

Archivos de audio: prefijos AMB_, SFX_, MUS_ y VOZ_, seguidos del nivel y el nombre. Ejemplo: AMB_N1_PasilloLiminal.

Archivos de video: prefijo VID_, nivel y nombre. Ejemplo: VID_N2_Monitor.

Datos: prefijo SO_ para los ScriptableObject. Ejemplo: SO_Dialogo_Guion.

La tabla completa está en `CONTRIBUTING.md` del repositorio del juego.

- **Control de versiones**
- Utilizar Git para registrar los cambios.
- Mantener el repositorio en GitHub.
- Trabajar mediante ramas cuando sea necesario.
- Realizar commits descriptivos.
- Utilizar un archivo .gitignore adecuado para Unity.
- Evitar subir archivos temporales o generados automáticamente.
- Conservar los archivos .meta de Unity.
- Coordinar la integración de cambios para reducir conflictos entre escenas y recursos.

- Formato de assets

|Recurso|Formato recomendado|
|---|---|
|Sprites y pixel art|PNG|
|Archivos editables de Aseprite|`.ase` o `.aseprite`|
|Ilustraciones editables de Krita|`.kra`|
|Imágenes de referencia|PNG o JPG|
|Efectos sonoros y voces|MP3 (WAV para algunos efectos)|
|Música y ambientes|MP3 (WAV para algunas pistas)|
|Videos narrativos|MP4 compatible con Unity|
|Animaciones de Unity|`.anim`|
|Materiales de Unity|`.mat`|
|Prefabs de Unity|`.prefab`|

- Convenciones de código
- Mantener una responsabilidad principal por componente.
- Evitar la duplicación de código.
- Utilizar nombres descriptivos para clases, métodos y variables.
- Separar la lógica del juego de la presentación visual.
- Utilizar `[SerializeField]` para configurar campos privados desde el Inspector.
- Evitar dependencias innecesarias entre sistemas.
- Gestionar los eventos narrativos mediante condiciones y estados.
- Documentar funciones complejas.
- Verificar que las cinemáticas y transiciones restauren correctamente los controles.
- Realizar pruebas después de integrar cambios importantes.

> **Navegación:** [[00 - Índice]] · ← [[01 - Arquitectura Técnica]] · [[03 - Requisitos Técnicos]] →
