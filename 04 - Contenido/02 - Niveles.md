# Niveles

## Descripción de la sección

Cada nivel debe documentar su propósito jugable, estructura, dificultad, contenido y condiciones de entrada/salida.

## Niveles

### Prólogo — La negación

**Escena:** `PRO_Casa`.

**Objetivo principal:** Revisar el baño real, abrir y cerrar el gabinete del espejo y cruzar el primer portal.

**Objetivos secundarios:**

- Reconocer los elementos del baño para identificar sus alteraciones en niveles posteriores.
- Inspeccionar el lavabo, las toallas y la cortina, y conocer los pensamientos de Elaki.
- Revisar el periódico del padre y el interior del refrigerador.
- Familiarizarse con el movimiento y la interacción.

**Duración estimada:** Aproximadamente 4 minutos.

**Dificultad:** Baja. Introducción a los controles y a la exploración.

**Mecánicas introducidas:**
- Movimiento con WASD o flechas.
- Interacción con objetos mediante E o clic.
- Sentarse a la mesa durante el desayuno.
- Vistas fijas en primera persona del gabinete y del refrigerador, con selección de objetos con el ratón.
- Pensamientos y diálogos.
- Cruce del portal del espejo.

**Mecánicas utilizadas:** Exploración, observación, inspección de objetos e interacción con el entorno.

**Enemigos / obstáculos:** No existen enemigos. El principal obstáculo es descubrir que el gabinete abre el camino.

**Recompensas:** Primeras pistas sobre Margarita y acceso al otro lado.

**Puntos de guardado:** Inicio de la partida y al levantarse de la cama.

**Condición de entrada:** Iniciar una nueva partida.

**Condición de salida:** Abrir y cerrar el gabinete y cruzar el espejo con E.

**Eventos narrativos:**

1. Elaki despierta en su cuarto y mamá lo llama a comer.
2. Al acercarse al comedor, Elaki se sienta. Puede revisar el periódico del padre y debe revisar el lugar vacío.
3. Pregunta por Margarita, cuyo nombre se corrompe, y sus padres niegan su existencia.
4. Sufre un mareo y aparece en el baño real. Después del desayuno, el perro de la familia lo acompaña por la casa.
5. El espejo no refleja a Elaki hasta que abre y cierra el gabinete. El gabinete se abre con E en el espejo o solo, si Elaki se queda quieto 10 segundos frente a él.
6. Al cerrarlo, el espejo se deforma, se abre el portal y una silueta femenina lo cruza.
7. Elaki cruza el espejo.

**Mapa / diagrama:**

```text
CUARTO DE ELAKI
          ↓
COMEDOR: PRIMER DESAYUNO
    ├── Periódico del padre (opcional)
    └── Lugar vacío (obligatorio)
          ↓
MAREO
          ↓
BAÑO REAL
    ├── Lavabo
    ├── Cuatro toallas
    ├── Cortina cerrada
    └── Gabinete (obligatorio)
          ↓
PORTAL EN EL ESPEJO
          ↓
NIVEL 1
```

### Nivel 1 — La primera ruptura

**Escenas:** `N1_Laberinto`, `N1_Pasillo` y `R1_Casa` (segundo despertar).

**Objetivo principal:** Recorrer la primera versión alterada de la casa y seguir la voz de Margarita hasta el fondo del pasillo.

**Objetivos secundarios:**

- Comparar el baño con su versión original.
- Abrir la cortina de la tina y descubrir el pasaje con el calendario del 31 de octubre.
- Revisar los objetos regados por los espacios del otro lado.
- Seguir la voz femenina por el pasillo largo.

**Duración estimada:** ==🟣Pendiente de validar mediante pruebas de recorrido.==

**Dificultad:** Baja. El desafío se concentra en la exploración y la identificación de cambios.

**Mecánicas introducidas:**

- Comparación visual entre versiones de un mismo escenario.
- Exploración de espacios distorsionados.
- Seguimiento de pistas auditivas.
- Activación de eventos ambientales por zona y por número de visitas.

**Mecánicas utilizadas:** Movimiento, interacción, inspección, exploración y uso de portales.

**Enemigos / obstáculos:** No existen persecuciones ni daño. Los obstáculos son una puerta del baño que no abre, espacios conectados de forma inconsistente, un pasillo anormalmente largo cuya salida se cierra detrás de Elaki y una visión que se oscurece con cada paso.

**Recompensas:** Nuevas pistas sobre las dimensiones y la confirmación de que la voz pertenece a alguien que pide ayuda.

**Puntos de guardado:** Entrada a `N1_Laberinto`, entrada a `N1_Pasillo`, inicio del segundo despertar y al levantarse de la cama.

**Condición de entrada:** Atravesar el portal del espejo durante el prólogo.

**Condición de salida:** Llegar a la puerta del fondo del pasillo, desmayarse y completar el segundo desayuno.

**Eventos narrativos:**

1. El protagonista aparece en un baño en blanco, similar al anterior: toallas, gabinete con símbolos ilegibles y una puerta que no abre.
2. Al hacer clic en la cortina, esta se abre y deja ver un pasaje con el calendario del 31 de octubre.
3. El pasaje lleva a una versión liminal del cuarto de Elaki, con su cama y cuadros.
4. Elaki recorre la sala (con el sillón pegado a la pared), la cocina, el comedor (cuatro sillas sin mesa), una pared de frente y el cuarto de lavado. A la tercera vuelta por el cuarto de lavado, Elaki lo nota.
5. Al salir, entra a un pasillo blanco y largo; la salida se cierra detrás. Elaki pregunta «¿M-M-A-A-R?».
6. Una voz femenina se escucha cada vez más cerca y la visión se oscurece con cada paso hacia la puerta del fondo.
7. Frente a la puerta se escucha un golpe y «Ayuda.»; Elaki se desmaya.
8. Despierta en su cuarto real. En el segundo desayuno, la madre le pregunta cómo se siente y Elaki decide no contar lo que vivió.

**Mapa / diagrama:**

```text
BAÑO DEL OTRO LADO (EN BLANCO)
    ├── Toallas
    ├── Gabinete con símbolos
    ├── Puerta que no abre
    └── Cortina (se abre con clic)
          ↓
PASAJE Y CALENDARIO DEL 31
          ↓
CUARTO LIMINAL
          ↓
SALA → COCINA → COMEDOR → PARED DE FRENTE → CUARTO DE LAVADO
          ↓
PASILLO BLANCO Y LARGO
    └── Voz femenina
          ↓
DESMAYO
          ↓
SEGUNDO DESPERTAR Y SEGUNDO DESAYUNO
          ↓
NIVEL 2
```

### Nivel 2 — La deformación

**Escenas:** `R1_Casa` (baño real), `N2_Casa` y `R2_Casa` (tercer despertar).

**Objetivo principal:** Investigar la casa abandonada, escapar de la criatura canina y enfrentar el encuentro con la Manifestación de Margarita.

**Objetivos secundarios:**

- Examinar la fotografía familiar de los cuatro.
- Observar la barda desde la ventana.
- Investigar los cuatro platos y la televisión con estática.
- Interactuar con la computadora.
- Descubrir nuevas pistas después del tercer despertar.

**Duración estimada:** ==🟣Pendiente de validar mediante pruebas, especialmente por la duración de las persecuciones.==

**Dificultad:** Media-alta. Es el primer nivel que incorpora amenazas directas y condiciones de derrota.

**Mecánicas introducidas:**

- Persecuciones y evasión de enemigos.
- Sistema de daño y efectos visuales al recibir ataques.
- Derrota y reinicio desde un punto de control.
- Activación de amenazas mediante eventos narrativos.

**Mecánicas utilizadas:** Movimiento, carrera, exploración, interacción, inspección, activación de eventos, evasión y transición entre escenarios.

**Enemigos / obstáculos:**

- Criatura canina deformada: persigue al protagonista después del evento de la computadora. Elaki puede escaparle corriendo.
- Manifestación de Margarita: aparece al fondo del pasillo y siempre alcanza a Elaki.
- Pasillos y espacios que limitan las rutas de escape.
- Penumbra que dificulta reconocer el entorno.

Las amenazas deben evitarse. No se contempla un sistema de combate.

**Recompensas:** Avance narrativo, la confirmación de que Margarita existió y nuevas pistas sobre la familia.

**Puntos de guardado:** Entrada a `N2_Casa`, al sentarse frente a la computadora, al iniciar el encuentro con la Manifestación y, en el tercer despertar, al levantarse de la cama y en el comedor.

**Condición de entrada:** Completar el segundo desayuno.

**Condición de salida:** Escapar de la criatura canina, recibir el tercer golpe de la Manifestación, revisar los cuatro elementos obligatorios del tercer desayuno y cruzar el espejo.

**Eventos narrativos:**

1. Elaki decide volver al baño real: ahora hay tres toallas, la cortina está en su primer estado y el portal ya está abierto.
2. Cruza a un baño abandonado, con la bañera, las toallas tiesas y el calendario sucios.
3. En el pasillo encuentra la fotografía de los cuatro: «Ahí está ella. Yo no estaba loco.». Por la ventana ve mujeres de pie frente a una barda; después, la ventana queda tapiada.
4. La sala y la cocina están en penumbra, con cuatro platos, la televisión con estática y el refrigerador podrido.
5. Al sentarse frente a la computadora, el juego guarda. El video dura 50 segundos; la penumbra cede poco a poco y el perro de la familia, erguido, se acerca.
6. Al terminar el video, la criatura canina persigue a Elaki. Si lo alcanza tres veces, el juego vuelve casi al final del video.
7. En el pasillo, la Manifestación de Margarita espera al fondo. La criatura canina revienta, la figura gira («¿Eres tú?») y persigue a Elaki.
8. Al tercer golpe, la vista se cierra en espiral y Elaki despierta por tercera vez en su cuarto real.
9. En el tercer desayuno, la madre luce gris y ojerosa. Elaki revisa el lugar vacío, a la madre, la comida y el periódico, que habla de las familias que buscan a sus desaparecidos.
10. En el pasillo real aparece el altar del perro, con un sollozo, y una alacena en el lugar del cuarto de Margarita. Si intenta ir a la cocina, Elaki se detiene.
11. Regresa al baño: cuatro toallas, la cortina en su segundo estado y el gabinete sin los parches.
12. Atraviesa el portal del espejo.

**Mapa / diagrama:**

```text
BAÑO REAL (TRES TOALLAS, CORTINA EN ESTADO 1)
          ↓
BAÑO ABANDONADO Y CALENDARIO
          ↓
PASILLO
    ├── Fotografía de los cuatro
    └── Ventana con la barda
          ↓
SALA Y COCINA EN PENUMBRA
    ├── Cuatro platos
    ├── Televisión con estática
    └── Refrigerador podrido
          ↓
COMPUTADORA Y VIDEO (PUNTO DE CONTROL)
          ↓
PERSECUCIÓN: CRIATURA CANINA
          ↓
ENCUENTRO CON LA MANIFESTACIÓN DE MARGARITA
          ↓
TERCER GOLPE: ESPIRAL Y NEGRO
          ↓
TERCER DESPERTAR Y TERCER DESAYUNO
    ├── Lugar vacío, madre, comida y periódico
    ├── Altar del perro
    └── Alacena
          ↓
BAÑO REAL (CUATRO TOALLAS, CORTINA EN ESTADO 2)
          ↓
NIVEL 3
```

### Nivel 3 — La realidad se rompe

**Escena:** `N3_Casa`.

**Objetivo principal:** Recorrer la casa de carne, regresar al baño y encontrar a Margarita en la tina.

**Objetivos secundarios:**

- Explorar las alteraciones orgánicas del entorno.
- Aprender el ritmo de los apéndices para pasar sin daño.
- Escuchar el anuncio de la televisión desde el sillón (opcional).
- Identificar el calendario del 31 de octubre.
- Reconocer la transformación definitiva del baño.

**Duración estimada:** ==🟣Pendiente de validar mediante pruebas de recorrido.==

**Dificultad:** Media. El nivel se centra en la tensión ambiental, la oscuridad y los peligros del entorno.

**Mecánicas introducidas:**

- Oscuridad con una luz pequeña alrededor de Elaki, que camina lento y no puede correr.
- Evasión de peligros del entorno: apéndices de carne con ritmo fijo.
- Recuperación del daño cuando Elaki pasa unos segundos sin recibir golpes.
- Secuencia narrativa final vinculada con la bañera.

**Mecánicas utilizadas:** Movimiento, exploración, interacción, observación, activación de eventos y transición final.

**Enemigos / obstáculos:** Apéndices que salen de las paredes de la cocina y del pasillo. Antes de salir, una sombra roja en el piso marca por dónde pasarán. Si tocan a Elaki, lo lastiman y lo empujan; tres golpes seguidos lo regresan al último punto de control.

**Recompensas:** Revelación narrativa sobre Margarita y conclusión del demo.

**Puntos de guardado:** Entrada al nivel, cocina, cuarto y pasillo.

**Condición de entrada:** Completar el tercer desayuno y atravesar el portal del baño real.

**Condición de salida:** Llegar a la tina y hacer clic en ella.

**Eventos narrativos:**

1. El protagonista aparece en el baño de carne, con toallas tibias y frascos llenos de dientes.
2. Al salir del baño, la luz parpadea, se apaga y Elaki aparece en la cocina, sellada con carne.
3. De las paredes salen apéndices; la puerta de la cocina está cubierta de carne.
4. De forma opcional, antes de abrir el refrigerador, puede sentarse en el sillón; la televisión transmite un anuncio y se apaga.
5. Al abrir el refrigerador, Elaki ve la carne que late y la membrana de la puerta se abre.
6. Cruza su cuarto deforme: «Mi cuarto. Ya no es mi cuarto.».
7. En el pasillo, tres apéndices cierran el paso; Elaki debe esperar a que se escondan.
8. En el baño, la cortina está abierta por completo y Margarita aparece en el remolino de la tina.
9. Elaki piensa «Te encontré». Al hacer clic en la tina, la imagen se funde a negro y comienza el desenlace.

**Mapa / diagrama:**

```text
BAÑO DE CARNE
    ├── Toallas tibias
    └── Gabinete con dientes
          ↓
PARPADEO DE LA LUZ
          ↓
COCINA SELLADA
    ├── Apéndices en las paredes
    ├── Sillón y anuncio de la televisión (opcional)
    └── Refrigerador: se abre la membrana
          ↓
CUARTO DEFORME
          ↓
PASILLO CON TRES APÉNDICES
          ↓
BAÑO FINAL
    ├── Cortina completamente abierta
    └── Margarita en la tina
          ↓
DESENLACE
```

### Desenlace

**Escena:** `DES_Final`.

**Eventos:** imágenes alternadas de Elaki entrando a la tina del otro lado y de Elaki solo en su baño real; carteles de búsqueda de Margarita; transmisión del noticiero del 25 de diciembre; pantalla de texto sobre el joven ahogado; edificio de la familia de noche, en Navidad; texto de cierre; regreso al menú principal.

## Flujo del nivel

```text
Inicio → Zona A → Desafío → Zona B → Recompensa → Final
```

```text
INICIO
   ↓
PRÓLOGO
Despertar y primer desayuno
   ↓
Exploración e inspección del baño
   ↓
Portal del espejo
   ↓
NIVEL 1
Primera dimensión alterada
   ↓
Pasillo y voz femenina
   ↓
Desmayo, segundo despertar y segundo desayuno
   ↓
NIVEL 2
Baño real y portal
   ↓
Exploración de la casa abandonada
   ↓
Evento de la computadora
   ↓
Persecución de la criatura canina
   ↓
Encuentro con la Manifestación de Margarita
   ↓
Tercer despertar y tercer desayuno
   ↓
NIVEL 3
Baño real y portal
   ↓
Casa de carne
   ↓
Encuentro en la bañera
   ↓
DESENLACE
Carteles, noticiero, texto y edificio
   ↓
MENÚ PRINCIPAL
```
## Criterios de calidad

- El objetivo es comprensible.
- Las reglas se pueden aprender.
- El desafío corresponde al nivel de progresión.
- Existe retroalimentación suficiente.
- El jugador entiende por qué tuvo éxito o fracaso.


> **Navegación:** [[00 - Índice]] · ← [[01 - Estructura del Contenido]] · [[03 - Enemigos y NPC]] →
