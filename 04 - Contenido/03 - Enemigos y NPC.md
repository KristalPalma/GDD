# Enemigos y NPC

## Descripción de la sección

Documenta las entidades controladas por el juego y su comportamiento.

## Enemigos

### Nombre: Criatura canina deformada

**Rol de combate:** Enemigo de persecución. Representa una amenaza física que obliga al jugador a desplazarse y evitar el contacto.

**Comportamiento:** Su aparición se activa después de que el protagonista interactúa con la computadora y observa un video perturbador.

La criatura comienza a perseguirlo por el escenario. El jugador debe desplazarse por la ruta disponible y evitar recibir suficientes ataques como para provocar su derrota.

**Vida:** No aplica. La criatura no puede ser eliminada mediante combate.

**Daño:** Provoca daño al protagonista al alcanzarlo o atacarlo. Cada impacto debe producir una señal visual, como manchas rojas en la pantalla.

**Defensas:** No aplica. El jugador no dispone de ataques que puedan dañarla.

**Velocidad:** 2.0 unidades por segundo. Elaki camina a 1.5 y corre a 2.6, así que puede escaparle corriendo. Busca a Elaki por las celdas libres del escenario, rodeando los obstáculos.

**Rango de detección:** Su persecución se activa por un evento narrativo, no por un sistema de patrullaje. 

**Ataques:** Contacto o ataque de corto alcance que provoca daño. No se han definido ataques a distancia.

**Debilidades:** No presenta vulnerabilidades de combate. La forma de superar el encuentro es escapar y alcanzar la zona segura o el evento que finaliza la persecución.

**Recompensa:** Superar la primera persecución y continuar con los acontecimientos del Nivel 2.

**Estados de IA:**

```text
Patrullar → Detectar → Perseguir → Atacar
                  ↓
                Perder objetivo → Buscar
```

```text
INACTIVO
   ↓
Evento de la computadora
   ↓
APARICIÓN
   ↓
PERSEGUIR AL JUGADOR
   ├── Jugador al alcance
   │       ↓
   │     ATACAR
   │       ├── Jugador sobrevive → PERSEGUIR
   │       └── Jugador derrotado → REINICIAR
   │
   └── Jugador alcanza la salida
           ↓
     FINALIZAR PERSECUCIÓN
```

### Nombre: Manifestación grotesca de Margarita

**Rol de combate:** Antagonista principal en su versión hostil. Enemigo de persecución que combina horror psicológico y corporal.

**Comportamiento:** Aparece después de la primera persecución, al fondo del pasillo, de espaldas, como una figura femenina que recuerda a Margarita. La criatura canina revienta frente a ella.

La figura gira y revela rasgos grotescos. Después persigue al protagonista y siempre lo alcanza: el encuentro no tiene escapatoria.

**Vida:** No aplica. No puede ser derrotada mediante ataques.

**Daño:** Cada golpe aumenta las manchas rojas en la pantalla. Al tercero, la vista se cierra en espiral y pasa a negro, sin pantalla de derrota.

**Defensas:** No aplica. No existe un sistema de combate contra esta manifestación.

**Velocidad:** Siempre alcanza a Elaki, aunque corra. La evasión no es posible por diseño.

**Rango de detección:** La persecución comienza mediante un evento narrativo. No se contempla patrullaje previo.

**Ataques:** Ataque por contacto. 

**Debilidades:** No presenta vulnerabilidades. El jugador no puede derrotarla ni escapar de ella.

**Recompensa:** El tercer golpe lleva al tercer despertar, que permite continuar con la historia.

**Estados de IA:**

```text
INACTIVA
   ↓
Encuentro con figura femenina
   ↓
REVELACIÓN / TRANSFORMACIÓN
   ↓
PERSEGUIR AL JUGADOR
   └── Jugador al alcance
           ↓
         ATACAR
           ├── Primer o segundo golpe → PERSEGUIR
           └── Tercer golpe
                   ↓
             ESPIRAL Y NEGRO
                   ↓
             TERCER DESPERTAR
```

### Nombre: Apéndices de carne

**Rol de combate:** Peligro del entorno del Nivel 3. No persigue a Elaki.

**Comportamiento:** Salen de las paredes de la cocina y del pasillo con un ritmo fijo, desfasado entre apéndices, para que el jugador pueda aprenderlo. Antes de salir, una sombra roja en el piso marca por dónde pasarán. Asoman, latiguean a lo largo del piso y regresan a la pared.

**Vida:** No aplica.

**Daño:** Si tocan los pies de Elaki, lo lastiman y lo empujan hacia el lado del que venía. Tres golpes seguidos lo regresan al último punto de control. Después de 4 segundos sin daño, las manchas se borran poco a poco.

**Defensas:** No aplica.

**Velocidad:** Ciclo fijo; no reaccionan a la posición de Elaki.

**Rango de detección:** No aplica.

**Ataques:** Latigazo a lo largo del piso.

**Debilidades:** Se esconden en la pared al terminar su ciclo: el jugador debe esperar ese momento para pasar.

**Recompensa:** Avanzar hacia el cuarto, el pasillo y el baño.
## NPC 

**Rol:** Madre

**Función:** Personaje narrativo que participa en las conversaciones familiares y contribuye al misterio sobre Margarita.

**Ubicación:** Comedor de la casa familiar, durante las secuencias de desayuno.

**Interacción:** Participación mediante cinemáticas. No cuenta con un sistema de conversación libre.

**Diálogos:** Niega que el protagonista haya tenido una hermana y mantiene una actitud evasiva.

**Condiciones:** Aparece durante los tres desayunos.

**Recompensas / información:** Introduce contradicciones entre los recuerdos del protagonista y las afirmaciones de su familia.


**Rol:** Padre del protagonista. 

**Función:** Personaje narrativo que refuerza la negación de la existencia de Margarita.

**Ubicación:** Comedor de la casa familiar.

**Interacción:** Participación mediante cinemáticas, sin diálogo interactivo.

**Diálogos:** Respuestas breves y evasivas ante las preguntas del protagonista.

**Condiciones:** Aparece durante las secuencias familiares establecidas por la historia.

**Recompensas / información:** Refuerza el conflicto narrativo y la incertidumbre sobre los recuerdos del protagonista.

**Rol:** Margarita en la tina

**Función:** Entidad narrativa que conduce al desenlace del demo.

**Ubicación:** Bañera del Nivel 3.

**Interacción:** Encuentro dirigido mediante un evento narrativo. No cuenta con un sistema de conversación libre.

**Diálogos:** Margarita no habla. Elaki piensa: «Te encontré».

**Condiciones:** Se presenta cuando el protagonista alcanza el baño final.

**Recompensas / información:** Activa la transición hacia los carteles de desaparición y la noticia sobre el hallazgo del cuerpo de Margarita.

**Rol:** Perro de la familia

**Función:** Mascota que acompaña a Elaki en la casa real y anticipa la criatura canina del Nivel 2.

**Ubicación:** Casa real, después del primer desayuno y durante el segundo despertar, hasta que Elaki cruza al Nivel 2.

**Interacción:** Ninguna. Sigue a Elaki unos pasos detrás, por el mismo camino, sin atravesar paredes ni muebles. Si Elaki aparece lejos, el perro reaparece junto a él.

**Diálogos:** No aplica.

**Condiciones:** Prólogo y segundo despertar.

**Recompensas / información:** Establece el vínculo con la mascota antes de su transformación.

> **Navegación:** [[00 - Índice]] · ← [[02 - Niveles]] · [[04 - Objetos y Coleccionables]] →
