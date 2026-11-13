# Gestión de Cambios

## Descripción de la sección

El diseño de un videojuego cambia. Esta sección evita que las modificaciones importantes se pierdan o aparezcan sin evaluar sus consecuencias.

## Solicitud de cambio
### SC-01 — Guion unificado

**Fecha:** 3 de noviembre de 2026

**Cambio propuesto:** Unificar la historia de Carencia en un solo guion que define el orden definitivo del prólogo, los tres niveles y el desenlace.

**Motivo:** El equipo trabajaba con versiones distintas de la historia, con diferencias en el cierre de cada nivel y en el desenlace.

**Beneficio esperado:** Una sola referencia para el diseño, el arte, el audio y la programación, y una progresión narrativa coherente entre los niveles.

**Costo estimado:** Ajustar las secuencias narrativas, los textos de diálogos y pensamientos, y los recursos visuales y sonoros de las escenas afectadas.

**Impacto en otros sistemas:** Secuencias narrativas, diálogos y textos, arte de escenarios y audio.

**Decisión:** Aprobado.

**Responsable:** Wendy Kristal Palma Góngora

### SC-02 — Inicio de cada nivel en el baño real

**Fecha:** 3 de noviembre de 2026

**Cambio propuesto:** Cada nivel inicia en el baño de la casa real y se accede a la versión alterada cruzando el espejo.

**Motivo:** Mantener la comparación constante entre el baño real y sus versiones alteradas a lo largo de toda la historia.

**Beneficio esperado:** El jugador reconoce en cada visita los cambios del baño real, como el número de toallas, el estado de la cortina y el agua de la tina, que preparan la revelación final.

**Costo estimado:** Ajustar el inicio de cada nivel, los estados del baño real en cada visita y los portales del espejo.

**Impacto en otros sistemas:** Secuencias narrativas, portales, arte del baño y progreso.

**Decisión:** Aprobado.

**Responsable:** Ideny López Rodríguez

### SC-03 — Muerte limitada a las persecuciones del Nivel 2

**Fecha:** 3 de noviembre de 2026

**Cambio propuesto:** La muerte solo es posible durante la persecución de la criatura canina y el encuentro con la Manifestación de Margarita. El encuentro con la Manifestación de Margarita no tiene escapatoria y funciona como transición hacia el siguiente despertar.

**Motivo:** Concentrar el peligro en los momentos clave del Nivel 2 y presentar el encuentro con la Manifestación de Margarita como un momento narrativo inevitable.

**Beneficio esperado:** El Nivel 3 se centra en la exploración y la atmósfera, y el encuentro con la Manifestación de Margarita refuerza la contradicción de huir de la persona que se busca.

**Costo estimado:** Retirar el daño de los elementos del Nivel 3 y ajustar el comportamiento y la conclusión del encuentro con la Manifestación de Margarita.

**Impacto en otros sistemas:** Persecuciones, daño visual, derrota y reintento, secuencias narrativas.

**Decisión:** Aprobado.

**Responsable:** Melchor Emmanuel Ojeda Cauich e Ideny López Rodríguez

### SC-04 — Guardado al sentarse frente a la computadora

**Fecha:** 3 de noviembre de 2026

**Cambio propuesto:** El juego guarda cuando Elaki se sienta frente a la computadora del Nivel 2. Si la criatura canina lo alcanza, el reintento comienza cerca del final del video.

**Motivo:** Evitar que el jugador repita el video completo después de cada derrota.

**Beneficio esperado:** Reintentos más ágiles que conservan la tensión de la persecución.

**Costo estimado:** Ajustar el punto de control del Nivel 2 y el reinicio de la secuencia del video.

**Impacto en otros sistemas:** Progreso, puntos de control, persecuciones y secuencia del monitor.

**Decisión:** Aprobado.

**Responsable:** Ideny López Rodríguez

### SC-05 — Nuevo desenlace

**Fecha:** 3 de noviembre de 2026

**Cambio propuesto:** El desenlace se presenta como una secuencia sin control del jugador, con imágenes alternadas de la tina, carteles de búsqueda, una transmisión televisiva, una pantalla de texto y la escena final del edificio.

**Motivo:** Conectar las pistas presentadas durante los niveles con la revelación sobre Margarita y Elaki.

**Beneficio esperado:** Un cierre que permite al jugador reinterpretar la historia desde el inicio y que vincula la experiencia de Elaki con la realidad de las personas desaparecidas.

**Costo estimado:** Construir la secuencia final, sus textos, recursos visuales y sonoros, y la transmisión televisiva.

**Impacto en otros sistemas:** Secuencias narrativas, textos, arte, audio y video.

**Decisión:** Aprobado.

**Responsable:** Ideny López Rodríguez, bajo la coordinación narrativa de Wendy Kristal Palma Góngora

### SC-06 — Cámara que sigue a Elaki

**Fecha:** 3 de noviembre de 2026

**Cambio propuesto:** En exploración, la cámara deja de tener un encuadre fijo por habitación y sigue a Elaki de cerca, sin salirse de los límites del espacio en el que se encuentra. Al cambiar de espacio, la cámara salta a su nueva posición.

**Motivo:** Con el encuadre fijo, los pasillos largos se veían completos y el pixel art perdía nitidez al ajustar el encuadre a cada habitación.

**Beneficio esperado:** El pasillo del Nivel 1 solo muestra la puerta de la que salió Elaki y un poco más, lo que refuerza la sensación de un espacio interminable. El pixel art se mantiene nítido.

**Costo estimado:** Definir los límites de cada espacio y ajustar los acercamientos de las secuencias.

**Impacto en otros sistemas:** Cámara, secuencias y escenarios.

**Decisión:** Implementado.

**Responsable:** Melchor Emmanuel Ojeda Cauich

### SC-07 — Pausa solo con el control de Elaki

**Fecha:** 9 de noviembre de 2026

**Cambio propuesto:** La pausa se abre con Esc únicamente cuando Elaki puede moverse, ya sea explorando o durante una persecución. Durante secuencias, vistas de inspección, diálogos y cargas, Esc conserva su función de avanzar o cerrar.

**Motivo:** El mismo Esc que cerraba un diálogo o una vista abría también la pausa, y una pausa a mitad de una secuencia podía dejarla en un estado incompleto.

**Beneficio esperado:** Esc tiene un solo efecto por pulsación y las secuencias no se interrumpen.

**Costo estimado:** Revisar el estado del jugador antes de abrir la pausa.

**Impacto en otros sistemas:** Pausa, diálogos, vistas de inspección y secuencias.

**Decisión:** Implementado.

**Responsable:** Zurisarai Delgado Rodríguez

### SC-08 — Ajustes sin pestaña de Accesibilidad

**Fecha:** 12 de noviembre de 2026

**Cambio propuesto:** La hoja de Ajustes queda con tres pestañas: Audio, Video (solo brillo) y Controles. Se retiran la pestaña de Accesibilidad (tamaño de texto, subtítulos e indicadores de sonido) y las opciones de resolución, modo de pantalla y calidad.

**Motivo:** El demo no tiene voces con palabras que requieran subtítulos, y las opciones de video adicionales no se iban a probar en todos los equipos antes de la entrega.

**Beneficio esperado:** Una hoja de Ajustes más corta, con opciones que funcionan en el demo.

**Costo estimado:** Actualizar la interfaz de Ajustes, las capturas del GDD y los casos de prueba.

**Impacto en otros sistemas:** Interfaz, configuración y pruebas.

**Decisión:** Aprobado.

**Responsable:** Zurisarai Delgado Rodríguez

### SC-09 — Peligros del entorno en el Nivel 3

**Fecha:** 13 de noviembre de 2026

**Cambio propuesto:** El Nivel 3 incorpora apéndices de carne que salen de las paredes de la cocina y del pasillo con un ritmo fijo. Si tocan a Elaki, lo lastiman y lo empujan; tres golpes seguidos lo regresan al último punto de control, y el daño se recupera si pasa un rato sin recibir golpes. En este nivel Elaki camina lento y no puede correr. Se retiraron las bocas del piso, las carnes que salían del refrigerador, las manos bajo la cama y los ojos del pasillo.

**Motivo:** Sin ningún peligro, la casa de carne perdía tensión frente al Nivel 2. Un solo tipo de peligro, con un ritmo que se puede aprender, mantiene la tensión sin convertir el nivel en otra persecución.

**Beneficio esperado:** Un clímax con tensión ambiental que el jugador supera observando, coherente con el pilar de vulnerabilidad sin combate.

**Costo estimado:** Programar y dibujar los apéndices, ajustar el daño con recuperación y los puntos de control del Nivel 3.

**Impacto en otros sistemas:** Daño visual, puntos de control, diseño del Nivel 3. Modifica parcialmente SC-03: la muerte ya no se limita al Nivel 2.

**Decisión:** Implementado.

**Responsable:** Melchor Emmanuel Ojeda Cauich

## Registro

| Fecha                  | Cambio                                                                                                                                                           | Motivo                                                                                             | Impacto                                             | Estado       |
| ---------------------- | ---------------------------------------------------------------------------------------------------------------------------------------------------------------- | -------------------------------------------------------------------------------------------------- | --------------------------------------------------- | ------------ |
| 3 de noviembre de 2026 | La sala y el pasillo comparten el mismo espacio y se cruzan caminando, sin fundido ni corte de cámara.                                                           | Dar continuidad al recorrido dentro de la casa.                                                    | Habitaciones, puertas y cámara.                     | Implementado |
| 3 de noviembre de 2026 | El gabinete del baño se revisa en una vista frontal con el arte del equipo y cada medicamento se resalta al pasar el cursor.                                     | Presentar la inspección con los recursos visuales definitivos.                                     | Vistas de inspección, interfaz y prólogo.           | Implementado |
| 3 de noviembre de 2026 | El texto de los diálogos avanza a la siguiente línea en cuanto termina de mostrarse.                                                                             | Evitar esperas innecesarias durante la lectura.                                                    | Diálogos e interfaz.                                | Implementado |
| 3 de noviembre de 2026 | La sala de los niveles 2 y 3 y el baño de los niveles 1 y 3 conservan la distribución de la casa real, con el arte alterado de cada dimensión.                   | Reforzar la sensación de un lugar familiar que se deforma y reutilizar la distribución de la casa. | Arte de escenarios, habitaciones e iluminación.     | Implementado |
| 3 de noviembre de 2026 | La Manifestación de Margarita siempre alcanza a Elaki y el encuentro termina sin pantalla de derrota.                                                            | Presentar el encuentro como un momento narrativo inevitable y no como un desafío que se supera.    | Persecuciones, daño, secuencias y progreso.         | Implementado |
| 3 de noviembre de 2026 | Se adopta el guion unificado como referencia de la historia, con el orden prólogo, Nivel 1, Nivel 2, Nivel 3 y desenlace. (SC-01)                                | Contar con una sola versión de la historia para todo el equipo.                                    | Secuencias narrativas, diálogos, arte y audio.      | Aprobado     |
| 3 de noviembre de 2026 | Cada nivel inicia en el baño real y se cruza por el espejo. (SC-02)                                                                                              | Mantener la comparación entre el baño real y sus versiones alteradas a lo largo del juego.         | Secuencias narrativas, portales y arte del baño.    | Aprobado     |
| 3 de noviembre de 2026 | La muerte solo es posible durante la persecución de la criatura canina y el encuentro con la Manifestación de Margarita. (SC-03)                                 | Concentrar el peligro en los momentos clave del Nivel 2.                                           | Persecuciones, daño y diseño de niveles.            | Aprobado     |
| 3 de noviembre de 2026 | El juego guarda al sentarse frente a la computadora del Nivel 2. Si la criatura canina alcanza a Elaki, el reintento comienza cerca del final del video. (SC-04) | Evitar repetir el video completo después de cada derrota.                                          | Progreso, puntos de control y persecuciones.        | Aprobado     |
| 3 de noviembre de 2026 | El desenlace se presenta con imágenes alternadas de la tina, una transmisión televisiva, una pantalla de texto y la escena final del edificio.                   | Conectar las pistas de los niveles con la revelación sobre Margarita y Elaki.                      | Secuencias narrativas, textos, arte, audio y video. | Aprobado     |
| 3 de noviembre de 2026 | La cámara sigue a Elaki dentro de los límites de cada espacio. (SC-06)                                                                                           | Reforzar el pasillo interminable y mantener nítido el pixel art.                                   | Cámara, secuencias y escenarios.                    | Implementado |
| 9 de noviembre de 2026 | La pausa se abre solo cuando Elaki tiene el control. (SC-07)                                                                                                     | Evitar que un mismo Esc cierre un diálogo y abra la pausa.                                         | Pausa, diálogos y secuencias.                       | Implementado |
| 12 de noviembre de 2026 | Ajustes queda con Audio, Video (brillo) y Controles. (SC-08)                                                                                                    | Conservar solo las opciones que funcionan en el demo.                                              | Interfaz, configuración y pruebas.                  | Implementado |
| 13 de noviembre de 2026 | Apéndices de carne como peligro del Nivel 3, con daño que se recupera. (SC-09)                                                                                  | Mantener la tensión del clímax sin otra persecución.                                               | Daño, puntos de control y Nivel 3.                  | Implementado |

> **Navegación:** [[00 - Índice]] · ← [[04 - Backlog del Proyecto]] · [[01 - Criterios de Calidad]] →
