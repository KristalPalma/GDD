# Controles

## Descripción de la sección

Define la relación entre las acciones del jugador y las entradas físicas del dispositivo.

## Mapa de controles

| Acción                     | Teclado                      | Mouse                                     | Control | Táctil |
| -------------------------- | ---------------------------- | ----------------------------------------- | ------- | ------ |
| Mover al personaje         | WASD / Flechas direccionales | -                                         | X       | X      |
| Correr                     | Shift (mantener)             | -                                         | X       | X      |
| Interactuar                | E (puertas, espejo y objetos cercanos) | -                               | X       | X      |
| Inspeccionar               | -                            | Clic izquierdo sobre un objeto iluminado, con Elaki cerca | X | X |
| Cerrar inspección          | E o Esc                      | -                                         | X       | X      |
| Avanzar diálogo            | E, Enter o Esc               | Clic izquierdo                            | X       | X      |
| Ataque principal           | X                            | X                                         | X       | X      |
| Pausar/ Abrir Menú         | Esc (cuando Elaki tiene el control) | Clic en opciones del menú          | X       | X      |


## Principios de control

1. **Consistencia:** las mismas teclas deben conservar su función durante los distintos niveles, salvo cuando una secuencia narrativa bloquee temporalmente alguna acción.
2. **Movimiento directo:** el protagonista se desplaza mediante WASD o flechas direccionales. Hacer clic sobre un objeto no provoca que el personaje camine automáticamente hacia él.
3. **Interacción por proximidad:** el jugador debe acercarse a un objeto para que aparezca la opción de inspeccionarlo o activarlo. No es posible interactuar con objetos fuera del rango establecido.
4. **Retroalimentación:** cada acción válida debe producir una respuesta visual, sonora o mediante animación que confirme su ejecución.
5. **Claridad:** las opciones de interacción deben ser visibles y fáciles de comprender, sin saturar la pantalla.
6. **Bloqueo temporal de controles:** durante determinadas secuencias narrativas, como la reproducción del video en el monitor, el movimiento puede deshabilitarse. Al finalizar, los controles correspondientes deben restaurarse.
7. **Respuesta durante las persecuciones:** el movimiento debe mantenerse fluido y preciso para permitir que el jugador reaccione y esquive enemigos.
8. **Simplicidad:** se evitarán combinaciones de teclas innecesarias, priorizando controles fáciles de aprender.

## Reasignación

¿El jugador puede cambiar los controles?
La reasignación de teclas no se contempla inicialmente.

El juego utiliza controles predeterminados, con WASD y flechas direccionales como alternativas de movimiento. Las teclas pueden consultarse en Ajustes → Controles.

La reasignación de teclas queda para una versión futura.

## Entrada y retroalimentación

Describe qué ocurre inmediatamente después de cada entrada importante.

| Entrada del jugador                              | Respuesta del juego                                                                                                                          |
| ------------------------------------------------ | -------------------------------------------------------------------------------------------------------------------------------------------- |
| Presionar WASD o flechas direccionales           | El protagonista se desplaza en la dirección correspondiente y reproduce su animación de movimiento.                                          |
| Acercarse a un objeto interactivo                | Aparece sobre el objeto el indicador de la tecla E.                                                                                          |
| Pasar el cursor sobre un objeto inspeccionable   | El objeto muestra su contorno iluminado.                                                                                                     |
| Presionar la tecla "E"                           | Se ejecuta la acción del objeto, mostrando información o activando un evento narrativo.                                                      |
| Alejarse de un objeto interactivo                | El indicador de interacción desaparece.                                                                                                      |
| Presionar Shift mientras se mueve                | El protagonista corre y reproduce su animación de carrera.                                                                                   |
| Presionar Esc                                    | Si Elaki tiene el control, se abre el menú de pausa y se detiene el tiempo de juego. Durante un diálogo, una vista o una secuencia, Esc conserva su función (cerrar o avanzar). |
| Presionar Esc para reanudar                      | Se cierra el menú y el juego continúa desde el estado en que fue pausado.                                                                    |



> **Navegación:** [[00 - Índice]] · ← [[03 - Sistemas]] · [[05 - Progresión]] →
