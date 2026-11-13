# Datos y Persistencia

## Descripción de la sección

Define qué información necesita conservar el juego y cómo se estructura.

## Datos persistentes

- **Progreso:** escena del último punto de control, punto de entrada donde reaparece Elaki y banderas narrativas.
- **Configuración:** volúmenes y brillo.
- **Inventario:** no aplica. El juego no tiene inventario.
- **Estadísticas:** no aplica.
- **Desbloqueos:** no aplica. El avance se registra mediante las banderas narrativas del progreso.
- **Otros:** no aplica.

## Modelo de datos

Describe las entidades y relaciones.

El juego maneja dos conjuntos de datos independientes:

**1. Partida guardada**

| Campo | Contenido |
|---|---|
| Escena | Escena del último punto de control, por ejemplo `N2_Casa`. |
| Entrada | Nombre del punto de entrada donde reaparece Elaki, por ejemplo `monitor`. |
| Banderas | Lista de acontecimientos de la historia que ya ocurrieron y objetos ya revisados. |

La fecha que muestra el menú ("hace cuánto se guardó") se toma de la fecha de modificación del archivo. Los golpes recibidos no se guardan: al reiniciar desde un punto de control, Elaki empieza sin daño.

**2. Configuración**

Preferencias del jugador: volumen general, de música, de efectos y de voces, y brillo, de 0 a 100 en pasos de 10. Se conservan entre partidas y no se borran al comenzar una nueva.

**Relación:** la partida y la configuración se guardan por separado. Restablecer la configuración no modifica la partida, y comenzar una partida nueva no modifica la configuración.

## Formato

**Formato de guardado:** Ambos archivos son JSON, escritos con `JsonUtility` de Unity: `partida.json` para la partida y `ajustes.json` para la configuración.

**Ubicación:** `Application.persistentDataPath`. En Windows corresponde a `%USERPROFILE%\AppData\LocalLow\<Compañía>\CARENCIA\`, donde la compañía es la que define *Player Settings* del proyecto.

**Versionado de datos:** Los archivos no incluyen un número de versión. Al leer la configuración, los campos de versiones anteriores (por ejemplo, los de la pestaña de Accesibilidad) se ignoran y desaparecen al volver a guardar.

## Migraciones

¿Qué ocurre si cambia la estructura de los datos entre versiones?

Si `partida.json` falta, está dañado o no tiene escena, el juego lo trata como si no hubiera partida: "Continuar" aparece tachado y el jugador comienza una partida nueva. Si `ajustes.json` falta o está dañado, el juego usa los valores predeterminados y corrige cualquier valor fuera de rango al paso de 10 más cercano.

Elegir "Jugar" con una partida guardada pide confirmación y, si el jugador acepta, borra `partida.json` antes de comenzar.


> **Navegación:** [[00 - Índice]] · ← [[03 - Requisitos Técnicos]] · [[05 - Seguridad y Riesgos Técnicos]] →
