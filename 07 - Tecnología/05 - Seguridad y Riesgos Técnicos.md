# Seguridad y Riesgos Técnicos

## Descripción de la sección

Documenta riesgos técnicos y medidas para reducir fallos, pérdida de datos o abuso de sistemas.

## Riesgos

| Riesgo                                                         | Probabilidad | Impacto | Mitigación                                                                                                                                                 |
| -------------------------------------------------------------- | ------------ | ------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------- |
| Conflictos en el repositorio al editar escenas al mismo tiempo | Media        | Alto    | Gitflow con una rama por funcionalidad y un solo responsable por escena a la vez.                                                                          |
| Diferencias de versión de Unity entre integrantes              | Media        | Alto    | Todo el equipo utiliza la versión 6000.6.3f1.                                                                                                              |
| Controles bloqueados después de una secuencia narrativa        | Media        | Alto    | Los estados del juego restauran los controles al terminar cada secuencia, después de una derrota y al cargar la partida.                                   |
| Enemigos atascados o persecuciones imposibles de superar       | Media        | Alto    | Los enemigos buscan a Elaki por las celdas libres del escenario; la velocidad de la criatura canina se ajustó para que el jugador pueda escapar corriendo. |
| Eventos narrativos que se repiten                              | Media        | Medio   | Las banderas narrativas registran cada acontecimiento de una sola ejecución.                                                                               |
| Bajo rendimiento en equipos de gama baja                       | Baja         | Medio   | Juego 2D con calidad gráfica ajustable desde las opciones.                                                                                                 |
| Herramientas de prueba disponibles en el ejecutable            | Baja         | Medio   | Los comandos de prueba solo funcionan dentro del editor de Unity y no pueden activarse en el juego compilado.                                              |
| Recursos de audio o video que no se reproducen                 | Baja         | Medio   | Uso de formatos compatibles con Unity (MP4, WAV y MP3) e indicadores escritos para los sonidos necesarios para avanzar.                                    |

## Datos sensibles

El juego no solicita ni almacena información personal, no utiliza cuentas y no envía datos a internet. Solo guarda de forma local el progreso de la partida y las preferencias de configuración.

## Multijugador

No aplica. Carencia es un juego de un jugador y no utiliza conexión en red.

## Recuperación

¿Qué ocurre ante corrupción de datos, pérdida de conexión o fallo del programa?

- **Corrupción de datos:** si el archivo principal está dañado, el juego carga la copia de respaldo. Si ninguno es válido, el jugador puede comenzar una partida nueva.
- **Fallo al guardar:** el juego muestra un aviso y conserva el último guardado válido.
- **Fallo del programa:** al volver a abrir el juego, "Continuar" retoma la partida desde el último punto de control guardado.
- **Pérdida de conexión:** no aplica, porque el juego no requiere conexión.


> **Navegación:** [[00 - Índice]] · ← [[04 - Datos y Persistencia]] · [[01 - Alcance]] →