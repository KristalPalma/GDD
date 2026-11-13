# Mecánicas

## Descripción de la sección

Una mecánica es una regla o interacción mediante la cual el jugador puede actuar dentro del sistema del juego.

Documenta cada mecánica con suficiente detalle para que otro integrante pueda implementarla.

## Plantilla de mecánica

Cada mecánica principal se documenta con los campos **Propósito**, **Activación**, **Reglas**, **Entrada**, **Estado inicial**, **Estado final**, **Recursos utilizados**, **Recompensa**, **Penalización**, **Interacciones con otras mecánicas** y **Casos límite**.

## Mecánicas principales

### Mecánica 01

**Propósito:**  
Permitir que el jugador explore las habitaciones, se acerque a objetos y alcance los lugares donde ocurren los acontecimientos de la historia.

**Activación:**  
El jugador mantiene presionada una tecla de dirección mientras tiene el control del protagonista.

**Reglas:**

- El personaje puede desplazarse por las áreas transitables.
    
- Las paredes, muebles y puertas cerradas impiden el paso.
    
- El movimiento diagonal debe mantener la misma velocidad que el movimiento en una sola dirección.
    
- El desplazamiento se bloquea durante cinemáticas, transiciones y vistas de inspección.
    
- Entrar en una zona de evento puede activar una secuencia si se cumplen sus condiciones.
    
- Los eventos de una sola ejecución no se repiten al volver a pasar por el mismo lugar.
    

**Entrada:**  
Teclas **W, A, S y D** o **flechas direccionales**, con movimiento correspondiente a las direcciones visibles en pantalla. Elaki camina a 1.5 unidades por segundo.

**Estado inicial:**  
Personaje detenido en una posición válida y con el control habilitado.

**Estado final:**  
Personaje en una nueva posición. Al soltar las teclas, vuelve al estado de reposo.

**Recursos utilizados:**  
Caminar no consume recursos. Correr se documentará como una mecánica independiente.

**Recompensa:**  
Acceso a nuevas zonas, objetos y acontecimientos.

**Penalización:**  
Caminar no tiene una penalización directa. Entrar en una zona peligrosa puede exponer al protagonista a una amenaza.

**Interacciones con otras mecánicas:**  
Inspección, interacción con objetos, activación de eventos, carrera y evasión de enemigos.

**Casos límite:**

- Si el jugador intenta atravesar un obstáculo, el personaje se detiene ante él.
    
- Si presiona direcciones opuestas, el movimiento en ese eje se cancela.
    
- Si comienza una cinemática mientras se desplaza, el movimiento se interrumpe.
    
- Al cambiar de habitación, el personaje aparece en un punto de entrada libre de obstáculos.
### Mecánica 02
**Propósito:**  
Permitir que el jugador descubra información, observe detalles y reconozca cambios entre los escenarios cotidianos y sus versiones distorsionadas.

**Activación:**  
El jugador hace clic sobre un elemento inspeccionable. En la vista del escenario, debe encontrarse dentro de la distancia de interacción establecida.

**Reglas:**

- Solo pueden inspeccionarse los objetos configurados para esta acción.
    
- La inspección puede mostrar una descripción, un pensamiento del protagonista o una ilustración de detalle.
    
- Solo puede existir una inspección abierta a la vez.
    
- Examinar un objeto no implica recogerlo ni añadirlo a un inventario.
    
- Las pistas opcionales aportan contexto sin bloquear el progreso.
    
- Un mismo objeto puede mostrar información diferente según el estado del escenario.
    
- En el prototipo del prólogo y nivel 1, una vista de detalle bloquea el desplazamiento hasta que se cierre.
    

**Entrada:**  
**Clic izquierdo** sobre un objeto que se ilumina al pasar el cursor, con Elaki cerca, o **E** frente al objeto más cercano. **E** o **Esc** cierran la vista de inspección.

**Estado inicial:**  
Objeto disponible para inspección y ninguna otra vista de detalle abierta.

**Estado final:**  
Información presentada al jugador. Al cerrar la inspección, se recupera la vista anterior y el control del personaje.

Si la historia necesita reconocer que el objeto fue examinado, se registra ese estado.

**Recursos utilizados:**  
No consume salud ni energía.

**Recompensa:**  
Información sobre la hermana, el protagonista o las alteraciones del entorno.

**Penalización:**  
Ninguna penalización directa en el prólogo y nivel 1.

**Interacciones con otras mecánicas:**  
Movimiento, vistas de detalle y progresión narrativa. Una inspección puede habilitar otra interacción cuando así lo requiera la secuencia.

**Casos límite:**

- Si el objeto está fuera de alcance, se muestra una indicación breve para acercarse.
    
- Los clics repetidos no abren ventanas duplicadas.
    
- Cerrar una descripción antes de terminar de leerla permite volver a consultarla.
    
- Examinar nuevamente un objeto no repite eventos narrativos de una sola ejecución.
    
- Los objetos decorativos sin interacción no deben mostrar indicadores de inspección.
    
- Si se permite inspeccionar durante encuentros con enemigos, deberá definirse previamente si el peligro continúa o se pausa.
### Mecánica 03
**Propósito:**  
Permitir que las acciones del jugador modifiquen elementos del escenario y habiliten el siguiente momento de la historia.

**Activación:**  
El jugador interactúa con un elemento disponible o entra en una zona que activa un acontecimiento.

**Reglas:**

- Cada interacción tiene condiciones previas y un resultado definido.
- Un objeto bloqueado no ejecuta su acción hasta que se cumplan sus condiciones.
- La acción produce una respuesta visual o sonora que confirma su ejecución.
- Las interacciones narrativas de una sola ejecución quedan registradas.
- Durante una animación o transición no se aceptan nuevas activaciones del mismo elemento.
- Las interacciones obligatorias deben contar con señales que ayuden a identificarlas.
- Las pistas opcionales no se convierten en requisitos de avance.

**Entrada:**  
Tecla **E** para accionar puertas, el espejo y los objetos cercanos. Los eventos por proximidad se activan al entrar en su zona o, en casos como el gabinete del prólogo, al quedarse quieto en ella.

**Estado inicial:**  
Elemento en su estado correspondiente: bloqueado, disponible o ya utilizado.

**Estado final:**  
Elemento actualizado y, cuando corresponda, una nueva interacción o etapa de la secuencia habilitada.

**Recursos utilizados:**  
No consume recursos directamente.

**Recompensa:**  
Acceso a otra zona, activación de un acontecimiento o avance de la historia.

**Penalización:**  
Intentar utilizar un elemento bloqueado no provoca daño ni pérdida de progreso; comunica que todavía no está disponible.

**Interacciones con otras mecánicas:**  
Inspección, movimiento, cambios de vista, portales y transiciones narrativas.
## Mecánicas secundarias

Lista las mecánicas que complementan la experiencia pero no constituyen el núcleo.

|Mecánica|Descripción|Función|
|---|---|---|
|**Correr**|Mantener **Shift** mientras Elaki se mueve aumenta su velocidad de 1.5 a 2.6 unidades por segundo. No consume energía. En el Nivel 3 Elaki camina lento y no puede correr.|Facilitar la evasión durante la persecución de la criatura canina, que avanza a 2.0 unidades por segundo.|
|**Evasión de enemigos**|Consiste en evitar el contacto con las criaturas mediante el desplazamiento y el aprovechamiento de los espacios disponibles.|Permitir que el protagonista sobreviva a los encuentros y continúe la historia.|
|**Evasión de peligros del entorno**|En el Nivel 3, los apéndices de carne salen de las paredes con un ritmo fijo. Una sombra roja en el piso marca por dónde pasarán; el jugador debe esperar a que se escondan para cruzar.|Mantener la tensión del Nivel 3 sin una persecución.|
|**Sentarse**|En los desayunos, Elaki se sienta a la mesa: no camina, pero puede revisar lo que tiene cerca.|Presentar las conversaciones familiares desde el lugar de Elaki.|
> **Navegación:** [[00 - Índice]] · ← [[01 - Jugabilidad]] · [[03 - Sistemas]] →
