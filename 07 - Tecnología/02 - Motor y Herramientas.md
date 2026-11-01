# Motor y Herramientas

## Descripción de la sección

Documenta las herramientas utilizadas para crear el videojuego y por qué fueron seleccionadas.

## Motor

**Motor:** Unity

**Versión:** Unity 6 6000.6.3f1

**Renderizado:** 2D con perspectiva isométrica. Se contempla el uso de sprites, Tilemaps y efectos de iluminación 2D. El pipeline de renderizado deberá confirmarse en la configuración del proyecto.

**Física:** Física 2D de Unity, mediante Rigidbody2D y Collider2D para gestionar movimiento colisiones y detección de zonas de interacción.

**Sistema de entrada:**
Teclado y ratón. WASD o flechas para el desplazamiento, clic izquierdo para inspeccionar objetos y tecla E para activar interacciones. La implementación concreta mediante Input System Package o el sistema de entrada clásico deberá verificarse en el proyecto.
## Lenguajes

| Lenguaje        | Uso                                                                                                     |
| --------------- | ------------------------------------------------------------------------------------------------------- |
| C#              | Programación de las mecánicas, sistemas, controladores, eventos narrativos e interfaces del videojuego. |
| Shaderlab/ HLSL | Creación de efectos personalizados.                                                                     |

## Herramientas

| Herramienta                        | Propósito                                                                                                        | Versión                         |
| ---------------------------------- | ---------------------------------------------------------------------------------------------------------------- | ------------------------------- |
| Unity Editor                       | Desarrollo del videojuego, construcción de escenarios, configuración de físicas, animaciones, escenas y pruebas. | Unity 6 versión: 6000.6.3f1     |
| Visual Studio Code / Visual Studio | Escritura, edición y depuración de scripts en C#                                                                 | ==🟣Por verificar.==            |
| Git                                | Control de versiones y registro de cambios del código y los recursos                                             | ==🟣Por verificar.==            |
| GitHub                             | Almacenamiento del repositorio, colaboración y seguimiento de cambios del equipo.                                | Servicio web                    |
| Aseprite                           | Creación de sprites, personajes, elementos visuales y animaciones en pixel art.                                  | ==🟣Por verificar.==            |
| Krita                              | Elaboración de bocetos, ilustraciones, diseños de personajes y escenarios.                                       | ==🟣Por verificar.==<br>        |
| CapCut                             | Edición de videos narrativos, transmisiones y secuencias cinematográficas del videojuego.                        | ==🟣Por verificar.==            |
| Audacity                           | Grabación, limpieza de ruido y edición de voces, efectos sonoros y ambientes.                                    | ==🟣Por verificar.==            |
| FL Studio                          | Composición musical y producción de la banda sonora del videojuego.                                              | ==🟣Por verificar.==            |
| Obsidian                           | Redacción de documentación y organización del cronograma mediante documentos y hojas de cálculo.                 | ==🟣Por verificar.==<br>        |
| ClickUp                            | Gestión del proyecto, organización de actividades y asignación de responsables.                                  | Servicio web                    |
| Claude Pro                         | Apoyo en documentación, análisis y revisión de código.                                                           | Servicio web / Aplicación local |
| ChatGPT Plus                       | Apoyo en documentación, análisis y revisión de código.                                                           | Servicio web / Aplicación local |

## Dependencias

Lista librerías, paquetes, plugins o servicios externos.

Unity 2D Physics
Unity Tilemap
Unity Animator
Unity Video Player
Unity Audio
Unity Input System
Universal Render Pipeline (URP)
Cinemachine

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
    │   └── Voces/
    ├── Materials/
    ├── Prefabs/
    ├── Scenes/
    │   ├── Menu/
    │   ├── Prologo/
    │   ├── Nivel01/
    │   ├── Nivel02/
    │   ├── Nivel03/
    │   └── Desenlace/
    ├── Scripts/
    │   ├── Core/
    │   ├── Player/
    │   ├── Interaction/
    │   ├── Camera/
    │   ├── Enemies/
    │   ├── Narrative/
    │   ├── Audio/
    │   ├── UI/
    │   └── Progress/
    ├── Sprites/
    ├── Tilemaps/
    ├── UI/
    └── Videos/
```


- **Nomenclatura**
Scripts y clases: PascalCase. Ejemplo: MovimientoJugador.cs.

Métodos y propiedades públicas: PascalCase. Ejemplo: IniciarPersecucion().

Variables privadas: camelCase, preferentemente con prefijo _. Ejemplo: _velocidadMovimiento.

Escenas: nombres descriptivos según su contenido. Ejemplo: Nivel02.

Prefabs: nombres que identifiquen su función. Ejemplo: EnemigoHermana.

Sprites: nombres que identifiquen el personaje, objeto o escenario. Ejemplo: Margarita_Idle.

Archivos de audio: nombres asociados con su función. Ejemplo: Ambiente_Nivel01.

Archivos de video: nombres que identifiquen su contenido. Ejemplo: Noticia_Final.

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
|Efectos sonoros y voces|WAV|
|Música y ambientes|WAV u OGG|
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
