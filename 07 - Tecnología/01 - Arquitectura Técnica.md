# Arquitectura Técnica

## Descripción de la sección

Explica cómo está construido técnicamente el videojuego y cómo se comunican sus componentes.

## Arquitectura

```text
Entrada
  ↓
Controlador
  ↓
Lógica de juego
  ↓
Sistemas
  ↓
Datos / Persistencia
  ↓
Presentación
```

```text
Entrada del jugador
(WASD, flechas, clic, E y pausa)
             ↓
Controladores
(Movimiento e interacción)
             ↓
Lógica de juego
(Mecánicas, condiciones y estados)
             ↓
Sistemas
(Cámara, secuencias, video, persecución,
 daño visual, iluminación y audio)
             ↕
Datos / Persistencia
(Progreso, eventos y configuración)
             ↓
Presentación
(Escenarios 2D, animaciones, interfaz,
 efectos visuales y sonido)
```

## Componentes principales

| Componente                | Responsabilidad                                                                                  | Dependencias                                    | Implementación en Unity |
| ------------------------- | ------------------------------------------------------------------------------------------------ | ----------------------------------------------- | ----------------------- |
| Gestor del juego          | Administrar el estado general de la partida, las transiciones y la coordinación de los sistemas. | Progreso, secuencias y escenas.                 | `PantallaJuego` (carga de escenas, fundidos, manchas, penumbra y video) |
| Controlador del personaje | Procesar el movimiento, la carrera y las restricciones de desplazamiento.                        | Entrada, físicas 2D, colisiones y animaciones.  | `PlayerController`, `AnimadorJugador` |
| Gestor de interacción     | Detectar objetos cercanos y gestionar inspecciones mediante clic y acciones mediante E.          | Movimiento, interfaz y objetos interactivos.    | `InteractionDetector`, `Interactable`, `ResalteAlMouse`, `VistaDeObjetos` |
| Controlador de cámara     | Seguir a Elaki con perspectiva isométrica y realizar cambios de encuadre durante eventos narrativos. | Personaje, escenarios y secuencias.         | `CameraController` con Pixel Perfect Camera |
| Gestor de secuencias      | Ejecutar en orden los pasos de cada acontecimiento: bloqueo, cámara, diálogos, banderas, enemigos y escenas. | Interacción, cámara, enemigos y progreso. | `Secuencia`, `ZonaEvento`, `EsperaQuieto`, `ContarEntradas` |
| Enemigos y peligros       | Perseguir a Elaki por las celdas libres o golpearlo con un ritmo fijo.                           | Movimiento, colisiones y daño.                  | `EnemigoPerseguidor`, `NavGrid`, `ApendiceCarne` |
| Gestor de daño visual     | Registrar el daño recibido, actualizar los efectos rojizos y activar la condición de muerte.     | Enemigos, interfaz y progreso.                  | `SaludJugador` |
| Gestor de iluminación     | Aplicar las condiciones de visibilidad y los cambios ambientales correspondientes a cada nivel.  | Escenarios, cámara y secuencias.                | `PenumbraNivel` y la penumbra de `PantallaJuego` |
| Gestor de audio           | Administrar ambientes, efectos, diálogos, sonidos de pausa y silencios narrativos.               | Escenarios, secuencias, video y enemigos.       | `VolumenPorCategoria` y AudioMixer con grupos de música, efectos y voces |
| Gestor de progreso        | Registrar los eventos completados y restaurar estados válidos después de una muerte o reinicio.  | Escenas, secuencias y estados del personaje.    | `EstadoJuego` (clase estática) y `PuntoEntrada` |
| Diálogos                  | Mostrar cada línea del guion a partir de su clave.                                               | Secuencias e interfaz.                          | `CajaDialogo` y el ScriptableObject `SO_Dialogo_Guion` |
| Interfaz de usuario       | Mostrar indicadores de interacción, vistas de inspección, menús y retroalimentación visual.      | Interacción, estados del juego y configuración. | `MenuPrincipal`, `MenuPausa`, `PantallaOpciones` |

## Comunicación

¿Cómo intercambian información los sistemas?
Los componentes se comunican mediante referencias controladas, métodos públicos y eventos de C# cuando corresponda, evitando que todos los sistemas dependan directamente entre sí.

Cada escena es autosuficiente: contiene su cámara, a Elaki y los sistemas que necesita, y se puede abrir y probar por separado. No se usa `DontDestroyOnLoad` para el progreso: lo que debe sobrevivir al cambio de escena (banderas, golpes y punto de control) vive en la clase estática `EstadoJuego` y en el archivo de la partida. La pausa (`PF_MenuPausa`) se carga sola desde `Resources` en cualquier escena.
El flujo de comunicación se organiza de la siguiente manera:

1. **Entrada y movimiento:** el controlador recibe las acciones del jugador, verifica las restricciones y actualiza la posición del protagonista.
2. **Movimiento e interacción:** el sistema de interacción utiliza la posición del protagonista para determinar qué objetos se encuentran dentro del alcance permitido.
3. **Interacción y secuencias:** al activar un objeto narrativo, el gestor de interacción comunica el evento correspondiente al sistema de secuencias.
4. **Secuencias y presentación:** el gestor de secuencias coordina la cámara, los videos, las animaciones, la iluminación y el audio, además de bloquear o restaurar controles cuando sea necesario.
5. **Persecución y daño:** los enemigos utilizan la posición del protagonista para perseguirlo. Cuando ocurre un ataque válido, el sistema de daño actualiza el estado del personaje y determina si debe producirse un reinicio.
6. **Progreso y transiciones:** el gestor de progreso registra los acontecimientos completados y proporciona la información necesaria para continuar la historia o restaurar una fase.
7. **Desenlace:** al atravesar el portal de la bañera, el gestor de secuencias bloquea los controles, solicita el corte de audio y coordina la reproducción de las noticias y la cinemática final. Al terminar, comunica la finalización de la experiencia al gestor del juego.

## Principios técnicos

- **Responsabilidades claras:** separar las mecánicas jugables, las reglas narrativas y la presentación audiovisual.
- **Código mantenible:** utilizar scripts organizados, nombres descriptivos y funciones reutilizables.
- **Separación de datos y lógica:** almacenar parámetros configurables y datos narrativos de forma independiente cuando corresponda.
- **Reutilización:** permitir que los mismos sistemas de interacción, cámara y secuencias funcionen en diferentes niveles.
- **Control de estados:** impedir acciones incompatibles, como iniciar una interacción mientras se ejecuta una cinemática que bloquea los controles.
- **Gestión de eventos:** evitar la repetición de acontecimientos narrativos de una sola ejecución.
- **Restauración segura:** garantizar que los sistemas recuperen estados válidos después de una muerte, transición o reinicio.
- **Escalabilidad:** facilitar la incorporación de nuevos escenarios, eventos y recursos sin modificar innecesariamente los componentes existentes.


> **Navegación:** [[00 - Índice]] · ← [[04 - Guardado y Configuración]] · [[02 - Motor y Herramientas]] →
