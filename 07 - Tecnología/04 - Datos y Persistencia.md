# Datos y Persistencia

## Descripción de la sección

Define qué información necesita conservar el juego y cómo se estructura.

## Datos persistentes

- **Progreso:** escena, habitación, punto de control, posición y orientación de Elaki, salud y estado de la historia.
- **Configuración:** volúmenes, calidad gráfica, brillo, tamaño de texto y subtítulos.
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
| Versión | Número de versión de la estructura del guardado. |
| Fecha de guardado | Momento en que se guardó la partida. |
| Escena | Nivel en el que se encuentra el jugador. |
| Habitación | Espacio de la casa donde se encuentra Elaki. |
| Punto de control | Último punto de control alcanzado. |
| Posición y orientación | Ubicación de Elaki y dirección hacia la que mira. |
| Salud | Daño acumulado al momento de guardar. |
| Banderas narrativas | Acontecimientos de la historia que ya ocurrieron. |
| Diálogos vistos | Diálogos que ya se mostraron, para no repetirlos. |
| Objetos examinados | Objetos que el jugador ya revisó. |
| Portales cruzados | Portales que el jugador ya atravesó. |
| Estado de la cortina | Estado de la cortina del baño en el momento del guardado. |

**2. Configuración**

Preferencias del jugador: volumen general, de música, de efectos y de voces; calidad gráfica; brillo; tamaño de texto y subtítulos. Se conservan entre partidas y no se borran al comenzar una nueva.

**Relación:** la partida y la configuración se guardan por separado. Restablecer la configuración no modifica la partida, y comenzar una partida nueva no modifica la configuración.

## Formato

**Formato de guardado:** La partida se guarda en un archivo JSON. La configuración se guarda con el sistema de preferencias de Unity (PlayerPrefs).

**Ubicación:** `%USERPROFILE%\AppData\LocalLow\Equipo Carencia\Carencia\`, con el archivo principal `carencia_save.json` y su copia de respaldo `carencia_save.bak`.

**Versionado de datos:** El archivo incluye un número de versión de su estructura.

## Migraciones

¿Qué ocurre si cambia la estructura de los datos entre versiones?

Al cargar una partida, el juego traduce los nombres de escena de la versión anterior del proyecto a los nombres actuales. Si el archivo principal está dañado o no es válido, el juego carga la copia de respaldo. Si ninguno de los dos es válido, "Continuar" no está disponible y el jugador comienza una partida nueva.

Al completar el desenlace se elimina la partida guardada, por lo que "Continuar" deja de estar disponible.


> **Navegación:** [[00 - Índice]] · ← [[03 - Requisitos Técnicos]] · [[05 - Seguridad y Riesgos Técnicos]] →