# Guardado y Configuración

## Descripción de la sección

Define cómo se conserva el progreso y qué ajustes puede modificar el jugador.

## Guardado

**Tipo:** Automático

**Cuándo se guarda:**
- Al completar el prólogo y atravesar el primer portal.
- Al finalizar un nivel y acceder al siguiente.
- Antes de iniciar las persecuciones del Nivel 2.
- Al superar las persecuciones y avanzar al siguiente acontecimiento narrativo.
- Al llegar a otros puntos de control definidos durante el desarrollo.

**Qué datos se guardan:**
- Nivel actual
- Punto de control
- Progreso narrativo
- Interacciones importantes
- Estado del escenario

**Cantidad de ranuras:** Una ranura de guardado para el demo.

**Qué ocurre si el guardado falla:**
El videojuego deberá mostrar un mensaje indicando que no fue posible guardar el progreso.

Se conservará el último guardado válido, evitando sobrescribirlo con datos incompletos o dañados. El jugador podrá continuar jugando, pero deberá ser informado de que su progreso reciente podría no recuperarse al cerrar el juego.

## Configuración
Los ajustes están disponibles desde el menú principal y el menú de pausa, en la hoja de **Ajustes** con tres pestañas.

| Pestaña   | Ajustes                                                                                        |
| --------- | ---------------------------------------------------------------------------------------------- |
| Audio     | Volumen general, música, efectos de sonido y voces.                                            |
| Video     | Brillo. Resolución, modo de pantalla y calidad gráfica los fija la configuración del proyecto. |
| Controles | Consulta de teclas. La reasignación de controles queda para una versión futura.               |

El demo no incluye pestañas de Accesibilidad ni de Jugabilidad.

## Restablecimiento

¿Qué ajustes pueden volver a valores predeterminados?

El jugador puede restablecer los ajustes de la pestaña actual (Audio o Video) a sus valores originales con la tecla **R** (Restablecer valores predeterminados). Controles no tiene valores que restablecer.

Esta acción deberá solicitar confirmación antes de aplicarse.

El restablecimiento de la configuración no eliminará la partida guardada ni modificará el progreso de la historia.

> **Navegación:** [[00 - Índice]] · ← [[03 - Accesibilidad]] · [[01 - Arquitectura Técnica]] →
