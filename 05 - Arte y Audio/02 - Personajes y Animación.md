# Personajes y Animación

## Descripción de la sección

Documenta cómo deben verse y comportarse visualmente los personajes.

## Requisitos por personaje

| Personaje | Modelo/Sprite | Animaciones | VFX | Estado |
|---|---|---|---|---|
| Elaki | Sprite de 64 × 104 px en 8 direcciones | Espera, caminar, correr y muerte en 8 direcciones; sentarse y espera sentado (comedor); sentado frente a la computadora | Se enrojece un instante al recibir un golpe | Integrado |
| Madre | Sprite de pie y sentada | Parpadeo sutil, de pie y sentada | — | Integrado |
| Padre | Sprite de pie y sentado, siempre con el periódico | Extiende el periódico, de pie y sentado | — | Integrado |
| Perro de la familia | Sprite de frente, de espalda y de lado | Caminar y espera | — | Integrado |
| Criatura canina | Sprite en 8 direcciones | Correr y ataque en 8 direcciones | Revienta frente a la Manifestación de Margarita | Integrado |
| Manifestación de Margarita | Sprite en 8 direcciones | Correr, ataque y gateo en 8 direcciones | Gusanos y llanto | Integrado |
| Margarita | Sprite de frente, de lado y de espalda | Aparición en el remolino de la tina | Agua de la tina | En progreso: falta la cinemática de la tina |

## Animaciones

### Movimiento
ELAKI
- Caminar![[SPR_PJ_Elaki_Caminar_SO_R.png]]
![[SPR_PJ_Elaki_Caminar_E_R.png]]
![[SPR_PJ_Elaki_Caminar_N_R.png]]
![[SPR_PJ_Elaki_Caminar_NE_R.png]]
![[SPR_PJ_Elaki_Caminar_NO_R.png]]
![[SPR_PJ_Elaki_Caminar_O_R.png]]
![[SPR_PJ_Elaki_Caminar_S_R.png]]
![[SPR_PJ_Elaki_Caminar_SE_R.png]]


- Correr
ELAKI
![[SPR_PJ_Elaki_Correr_E_R.png]]

![[SPR_PJ_Elaki_Correr_N_R.png]]
![[SPR_PJ_Elaki_Correr_NE_R.png]]
![[SPR_PJ_Elaki_Correr_NO_R.png]]
![[SPR_PJ_Elaki_Correr_O_R.png]]
![[SPR_PJ_Elaki_Correr_S_R.png]]
![[SPR_PJ_Elaki_Correr_SE_R.png]]
![[SPR_PJ_Elaki_Correr_SO_R.png]]
Criatura canina
![[SPR_ENE_PerroHumanoide_Correr_E_R.png]]

![[SPR_ENE_PerroHumanoide_Correr_N_R.png]]

![[SPR_ENE_PerroHumanoide_Correr_NE_R.png]]

![[SPR_ENE_PerroHumanoide_Correr_NO_R.png]]

![[SPR_ENE_PerroHumanoide_Correr_O_R.png]]

![[SPR_ENE_PerroHumanoide_Correr_S_R.png]]

![[SPR_ENE_PerroHumanoide_Correr_SE_R.png]]

![[SPR_ENE_PerroHumanoide_Correr_SO_R.png]]
Manifestación de margarita
![[SPR_ENE_Hermana_Correr_S_R.png]]

![[SPR_ENE_Hermana_Correr_SE_R.png]]

![[SPR_ENE_Hermana_Correr_SO_R.png]]

![[SPR_ENE_Hermana_Correr_E_R.png]]

![[SPR_ENE_Hermana_Correr_N_R.png]]

![[SPR_ENE_Hermana_Correr_NE_R.png]]

![[SPR_ENE_Hermana_Correr_NO_R.png]]

![[SPR_ENE_Hermana_Correr_O_R.png]]
- Esperar
![[SPR_PJ_Elaki_Espera_E_R.png]]
![[SPR_PJ_Elaki_Espera_N_R.png]]
![[SPR_PJ_Elaki_Espera_NE_R.png]]
![[SPR_PJ_Elaki_Espera_NO_R.png]]
![[SPR_PJ_Elaki_Espera_O_R.png]]
![[SPR_PJ_Elaki_Espera_S_R.png]]
![[SPR_PJ_Elaki_Espera_SE_R.png]]
![[SPR_PJ_Elaki_Espera_SO_R.png]]

### Interacción
ELAKI
- Sentarse y esperar sentado a la mesa durante los desayunos (`SPR_PJ_Elaki_Sentarse`, `SPR_PJ_Elaki_EsperaSentado`).
- Sentado frente a la computadora del Nivel 2.

PADRES
- Madre: parpadeo sutil, de pie y sentada (`SPR_PJ_Madre_Parpadear`, `SPR_PJ_Madre_ParpadearSentada`).
- Padre: extiende el periódico que le cubre la cara, de pie y sentado (`SPR_PJ_Padre_Periodico`, `SPR_PJ_Padre_PeriodicoSentado`).

### Combate
Criatura canina

![[SPR_ENE_PerroHumanoide_Ataque_SO_R.png]]

![[SPR_ENE_PerroHumanoide_Ataque_E_R.png]]

![[SPR_ENE_PerroHumanoide_Ataque_N_R.png]]

![[SPR_ENE_PerroHumanoide_Ataque_NE_R.png]]

![[SPR_ENE_PerroHumanoide_Ataque_NO_R.png]]

![[SPR_ENE_PerroHumanoide_Ataque_O_R.png]]

![[SPR_ENE_PerroHumanoide_Ataque_S_R.png]]

![[SPR_ENE_PerroHumanoide_Ataque_SE_R.png]]

Manifestación de margarita![[SPR_ENE_Hermana_Ataque_N_R.png]]

![[SPR_ENE_Hermana_Ataque_NE_R.png]]

![[SPR_ENE_Hermana_Ataque_NO_R.png]]

![[SPR_ENE_Hermana_Ataque_O_R.png]]

![[SPR_ENE_Hermana_Ataque_S_R.png]]

![[SPR_ENE_Hermana_Ataque_SE_R.png]]![[SPR_ENE_Hermana_Ataque_SO_R.png]]

![[SPR_ENE_Hermana_Ataque_E_R.png]]

### Daño
Elaki no tiene una animación de daño propia. Cada golpe se comunica con un destello rojo oscuro en la pantalla, una sacudida de cámara, el sprite de Elaki enrojecido durante medio segundo y las manchas rojas progresivas (ver [[03 - Sistemas]]).

### Muerte / derrota
![[SPR_PJ_Elaki_Muerte_O_R.png]]

![[SPR_PJ_Elaki_Muerte_S_R.png]]

![[SPR_PJ_Elaki_Muerte_SE_R.png]]

![[SPR_PJ_Elaki_Muerte_SO_R.png]]

![[SPR_PJ_Elaki_Muerte_E_R.png]]

![[SPR_PJ_Elaki_Muerte_N_R.png]]

![[SPR_PJ_Elaki_Muerte_NE_R.png]]

![[SPR_PJ_Elaki_Muerte_NO_R.png]]

## Convenciones

- **Nombres de sprites:** `SPR_<Categoría>_<Personaje>_<Acción>_<Dirección>_R`, con categoría `PJ` para personajes y `ENE` para enemigos. Ejemplo: `SPR_PJ_Elaki_Caminar_SO_R`.
- **Direcciones:** N, NE, E, SE, S, SO, O y NO, con los pies anclados a la misma línea de suelo.
- **Animaciones de Unity:** `ANIM_<Personaje>_<Acción>_<Dirección>` y un Animator Controller por personaje, `AC_<Personaje>`. El gateo de la Manifestación reutiliza su controlador con un Animator Override Controller (`AOC_Hermana_Gateo`).
- **Tamaños:** lienzo de 64 × 104 px para Elaki y de 64 × 96 px para la madre y Margarita, a 48 *Pixels Per Unit* (ver [[01 - Dirección de Arte]]).
- **Importación:** filtro *Point*, sin compresión y pivote en la base del personaje. Los archivos `.aseprite` se importan directamente con el paquete Aseprite Importer.


> **Navegación:** [[00 - Índice]] · ← [[01 - Dirección de Arte]] · [[03 - Entornos]] →
