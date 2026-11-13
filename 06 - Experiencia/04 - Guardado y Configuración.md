# Guardado y Configuración

## Descripción de la sección

Define cómo se conserva el progreso y qué ajustes puede modificar el jugador.

## Guardado

**Tipo:** Automático

**Cuándo se guarda:**
- Al entrar a cada escena jugable (prólogo, Nivel 1, pasillo del Nivel 1, despertares, Nivel 2 y Nivel 3).
- Al levantarse de la cama en cada despertar y en el comedor del tercer despertar.
- Al sentarse frente a la computadora del Nivel 2, antes de la persecución.
- Al iniciar el encuentro con la Manifestación de Margarita.
- En la cocina, el cuarto y el pasillo del Nivel 3.

**Qué datos se guardan:**
- Escena actual
- Punto de entrada donde reaparece Elaki
- Banderas narrativas (acontecimientos y objetos ya revisados)

**Cantidad de ranuras:** Una ranura de guardado para el demo.

**Qué ocurre si el archivo falla:**
Si el archivo de la partida falta, está dañado o quedó a medio escribir, el juego lo trata como si no hubiera partida: *Continuar* aparece tachado y el jugador puede comenzar una partida nueva. El demo no muestra un aviso cuando falla la escritura del archivo.

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
