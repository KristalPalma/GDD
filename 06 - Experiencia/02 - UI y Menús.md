# UI y Menús

## Descripción de la sección

Define la estructura funcional de las interfaces y menús.

## Mapa de navegación

```text
MENÚ PRINCIPAL
├── Jugar
│   └── Iniciar desde el prólogo
│  
├── Continuar
│   └── Cargar último punto guardado
├── Ajustes
│   ├── Audio
│   ├── Video
│   └── Controles
└── Salir

DURANTE EL JUEGO
└── Menú de pausa (Esc)
    ├── Reanudar
    ├── Ajustes
    └── Volver al menú principal

DERROTA
└── Reiniciar desde el punto de control

FINAL DEL DEMO
└── Volver al menú principal
```
## Pantallas

### Pantalla 01: Menú principal

**Propósito:** Permitir al jugador iniciar una partida, continuar su progreso, modificar los ajustes o salir del videojuego.

**Elementos:**

- Nombre o logotipo.
- Fondo visual relacionado con la atmósfera del juego.
- Botones: **Jugar, Continuar, Ajustes y Salir**.
- Indicador visual de la opción seleccionada.

**Acciones disponibles:**

| Botón     | Acción                                            |
| --------- | ------------------------------------------------- |
| Jugar     | Inicia una partida desde el prólogo.              |
| Continuar | Retoma la partida desde el último punto guardado. |
| Ajustes   | Abre la hoja de Ajustes.                          |
| Salir     | Cierra el videojuego.                             |
**Estados:**
- **Inicial:** Se muestra al abrir el videojuego.
- **Sin partida guardada:** Continuar permanece deshabilitado.
- **Con partida guardada:** Continuar está disponible.
- **Confirmación:** Se solicita autorización antes de reemplazar el progreso existente.

**Transiciones:**
Menú principal → Juego / Ajustes / Salir.

### Pantalla 02: Ajustes

**Propósito:** Permitir al jugador ajustar las configuraciones del videojuego según sus preferencias.

**Elementos:**

| Pestaña   | Configuraciones                                                                              |
| --------- | -------------------------------------------------------------------------------------------- |
| Audio     | Volumen general, música, efectos de sonido y voces (de 0 a 100 %, en pasos de 10).           |
| Video     | Brillo (de 0 a 100 %, en pasos de 10).                                                       |
| Controles | Consulta de las teclas: moverse, correr, interactuar, inspeccionar y pausa. Solo lectura. |

- A la izquierda se muestra el nombre y la descripción de la opción enfocada.
- Resolución, modo de pantalla y calidad gráfica no se eligen en el menú: los fija la configuración del proyecto.
- La reasignación de teclas queda para una versión futura.

**Acciones disponibles:**

| Tecla | Acción                                                  |
| ----- | ------------------------------------------------------- |
| Q / E | Cambiar de pestaña.                                     |
| ↑ / ↓ | Elegir una opción.                                      |
| ← / → | Ajustar el valor de la opción enfocada.                 |
| G     | Guardar los cambios.                                    |
| R     | Restablecer los valores de la pestaña actual (Audio o Video). |
| Esc   | Volver al menú de origen.                               |

**Estados:**

- **Configuración actual:** los valores guardados.
- **Configuración modificada:** los cambios se prueban al momento y aparece el sello **SIN GUARDAR**.
- **Configuración guardada:** aparece el aviso «Guardado».

**Transiciones:** Menú principal o pausa → Ajustes → Menú de origen.

### Pantalla 03 — Menú de pausa

**Propósito:** Permitir al jugador detener temporalmente la experiencia sin perder el progreso.

**Elementos:**

- Título «Pausa».
- Botón **Reanudar**.
- Botón **Ajustes**.
- Botón **Volver al menú principal**.

**Acciones disponibles:** Reanudar la partida, modificar configuraciones o regresar al menú principal.

**Estados:**

- **Pausado:** Se detienen las acciones del juego.
- **Ajustes abiertos:** El jugador puede modificar configuraciones.
- **Confirmación:** Se solicita autorización para salir de la partida cuando corresponda.

**Transiciones:** Juego → Pausa → Juego / Ajustes / Menú principal.

El menú debe poder abrirse con **Esc**, incluso durante las persecuciones y cinemáticas.

### Pantalla 04 — Derrota

**Propósito:** Informar al jugador que ha perdido durante una persecución y permitirle intentarlo nuevamente.

**Elementos:**

- Mensaje breve de derrota.
- Botón Reintentar.
- Presentación visual acorde con la atmósfera del videojuego.

**Acciones disponibles:** Reiniciar desde el último punto de control.

**Estados:**

- Derrota activada.
- Esperando la selección del jugador.
- Reiniciando el punto de control.

**Transiciones:** Persecución → Derrota → Último punto de control.

### Pantalla 05 — Final del demo

**Propósito:** Comunicar que el jugador ha completado el contenido disponible.

**Elementos:**

- Pantalla de cierre con el nombre del videojuego.
- Mensaje «Fin del demo».
- Botón **Volver al menú principal**.

**Acciones disponibles:** Regresar al menú principal.

**Estados:**

- Secuencia final completada.
- Pantalla de cierre visible.

**Transiciones:** Desenlace → Fin del demo → Menú principal.
## Confirmaciones

Documenta acciones destructivas o irreversibles y cómo se confirman.

| Acción                       | ¿Requiere confirmación? | Comportamiento                                                                                   |
| ---------------------------- | ----------------------- | ------------------------------------------------------------------------------------------------ |
| Jugar con progreso existente | Sí                      | Advierte que comenzar desde cero reemplazará la partida guardada, si se utiliza una sola ranura. |
| Salir del videojuego<br>     | sÍ<br>                  | Puede solicitar confirmación para evitar cierres accidentales.                                   |
| Salir de Ajustes sin guardar | Sí                      | Advierte que los cambios que no se guardaron se perderán; con G se guardan.                      |
| Restablecer valores predeterminados | Sí               | Solo cambia la pestaña actual; la partida guardada no se ve afectada.                            |
| Volver al menú principal desde la pausa | Sí           | Advierte que se perderá lo jugado desde el último guardado.                                      |

> **Navegación:** [[00 - Índice]] · ← [[01 - UX y Flujo del Jugador]] · [[03 - Accesibilidad]] →
