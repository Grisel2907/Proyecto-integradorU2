# 🧑‍🚀 Walk Cycle Animation — Astronauta | Blender Grease Pencil
### Proyecto Integrador Unidad 2 | Graficación por Computadora

> Animación 2D frame a frame de un **astronauta** caminando y dando un salto, realizada con **Blender Grease Pencil**. El ciclo consta de **8 frames** trazados manualmente usando poses de referencia generadas con IA.

---

## 🛠️ Requisitos

- [Blender](https://www.blender.org/download/) 3.x o superior


---

## 🎨 Principios de Animación Aplicados

Antes de explicar el proceso técnico, es importante entender los principios de animación clásicos que se aplicaron en esta animación. Estos principios fueron desarrollados por animadores de Disney y son la base de cualquier animación convincente.

### Anticipación
Antes de que el astronauta salte, primero se **agacha** (Frame 4 — Preparación). Este movimiento previo al contrario de la acción principal se llama anticipación. Sin él, el salto se vería brusco e irreal porque el espectador no tendría tiempo de "prepararse" para verlo. La anticipación también comunica **peso**: un personaje pesado como un astronauta con traje espacial necesita más esfuerzo para despegar.

### Compresión y Estiramiento
Aunque en esta animación el astronauta mantiene su forma rígida por el traje espacial, el principio se aplica sutilmente:
- En el **Frame 4 (Preparación)** el cuerpo se comprime hacia abajo.
- En el **Frame 5 (Salto)** el cuerpo se estira hacia arriba al despegar.
- En el **Frame 7 (Aterriza)** el cuerpo vuelve a comprimirse al impactar el suelo.

### Inercia
Cuando el astronauta aterriza, su cuerpo no se detiene de golpe. Los brazos siguen moviéndose hacia adelante por inercia (Frame 7 y 8). Esto hace que el movimiento se sienta físicamente creíble y con peso real.

### Ritmo
Con solo 8 frames, cada pose debe comunicar claramente su momento en la acción. Los frames de caminata (1–3) tienen un ritmo constante, mientras que el salto (4–8) tiene una aceleración hacia arriba y una desaceleración al aterrizar, imitando la física real del movimiento bajo la gravedad.

### Pose por Pose
La técnica utilizada en esta animación es **Pose to Pose**: se definen primero las poses clave más importantes (contacto, salto, aterrizaje) y luego se rellenan los frames intermedios. Es el método opuesto a "straight ahead" (dibujar frame por frame sin planear), y da mayor control sobre la composición y el ritmo.

---

## 📖 How To — Paso a Paso

---

### 1. Configuración inicial del proyecto

1. Abre Blender y en la pantalla de inicio selecciona **General**.
2. Elimina el cubo predeterminado: selecciónalo, presiona `X` → **Delete**.
3. Ve a **Output Properties** (ícono de impresora en el panel derecho) y configura:
   - **Frame Rate:** `24 fps`
   - **Start Frame:** `1`
   - **End Frame:** `8`
4. En la **Timeline** en la parte inferior, confirma que el rango muestre `1–8`.
5. Guarda el archivo desde el inicio: `Ctrl + S` → nómbralo `protectoBkender.blend`.

---

### 2. Crear el lienzo Grease Pencil

1. Presiona `Shift + A` en el viewport.
2. Selecciona **Grease Pencil → Blank**. Esto crea un objeto de dibujo 2D vacío en la escena.
3. Con el objeto seleccionado, presiona `Tab` para entrar en **Draw Mode**.
4. En la barra lateral (`N`) → pestaña **Tool**, configura tu pincel:
   - **Pincel de línea (Ink):** para los contornos del traje espacial. Grosor recomendado: `5–10px`.
   - **Pincel de relleno (Fill):** para el color interior del traje.
   - Puedes cambiar entre pinceles desde la barra superior izquierda en Draw Mode.
5. En **Stroke Placement** (barra superior), selecciona **Surface** o **View** para que los trazos queden en el plano correcto.

---

### 3. Importar la referencia de poses

1. En el viewport presiona `Shift + A` → **Image → Reference**.
2. Navega y selecciona tu imagen `my_poses_reference.png`.
3. Asegúrate de estar en la vista de frente presionando `Numpad 1`.
4. Escala la imagen con `S` hasta que ocupe bien el viewport.
5. Selecciona la imagen, ve a **Object Properties** (ícono de naranja) → baja la **Opacity** a `0.3–0.5` para que sea una guía sutil.
6. Activa la opción **In Front** en las mismas propiedades para que siempre sea visible detrás del dibujo.
7. Para que la imagen no se mueva accidentalmente, selecciónala y presiona `G` → `Escape` y luego en **Object Properties** activa **Lock** en Location, Rotation y Scale.

> La referencia de poses fue generada con IA con el prompt.

---


### 4. Dibujar la animación frame a frame

La animación sigue exactamente estas 8 poses:

| Frame | Pose | Principio aplicado |
|-------|------|--------------------|
| 1 | **Contacto Inicial** | Pose base — punto de referencia del ciclo |
| 2 | **Paso 1** | Timing — ritmo constante de caminata |
| 3 | **Paso 2** | Timing — continuación del ritmo |
| 4 | **Preparación** | Anticipación — el cuerpo se comprime antes del salto |
| 5 | **Salto** | Squash & Stretch — el cuerpo se estira al despegar |
| 6 | **Aire** | Timing — punto más alto, gravedad desacelera |
| 7 | **Aterriza** | Squash & Stretch + Follow Through — impacto y compresión |
| 8 | **Contacto** | Inercia — el cuerpo se estabiliza gradualmente |

---

####  Proceso de dibujo por frame

**Frame 1 — Contacto Inicial**
1. Ve al frame `1` en la Timeline (haz clic en el número `1` en la barra inferior).
2. Con el objeto Grease Pencil seleccionado, entra en **Draw Mode** (`Tab`).
3. Dibuja al astronauta con el **pie izquierdo al frente** y el **pie derecho atrás**, ambos tocando el suelo.
4. El brazo derecho va al frente y el izquierdo atrás — siempre opuesto a las piernas para simular el balanceo natural.
5. El cuerpo está ligeramente inclinado hacia adelante (unos 5–10°) para comunicar que está en movimiento.
6. Incluye los detalles del traje: casco esférico, mochila de oxígeno en la espalda, guantes redondeados, botas gruesas.


**Frame 2 — Paso 1**
1. Ve al frame `2`.
2. El Onion Skinning mostrará el frame 1 en naranja como guía.
3. Dibuja la primera zancada completa: el pie izquierdo empuja hacia atrás y se despega del suelo, el pie derecho avanza y toca el suelo.
4. El cuerpo sube levemente respecto al frame anterior (es el momento "up" del ciclo de caminata).
5. Los brazos cambian: el izquierdo va al frente, el derecho atrás.


**Frame 3 — Paso 2**
1. Ve al frame `3`.
2. Dibuja la segunda zancada: ahora el **pie derecho** está completamente al frente y el **izquierdo** atrás.
3. El cuerpo baja levemente (momento "down" del ciclo).
4. Los brazos vuelven a su posición del frame 1 (derecho al frente, izquierdo atrás).
5. Este frame es casi un espejo del Frame 1 pero con los pies intercambiados.
6. Presiona `I` → **All**.

**Frame 4 — Preparación**
1. Ve al frame `4`.
2. Dibuja al astronauta con las **rodillas flexionadas** hacia abajo, como si fuera a sentarse a medias.
3. El cuerpo baja considerablemente respecto al frame 3 — este es el punto más bajo antes del salto.
4. Los brazos van **hacia atrás y abajo**, acumulando energía para el impulso.
5. La mochila de oxígeno es visible claramente desde este ángulo.
6. Este es el frame de **anticipación** más importante — sin él el salto se vería falso.
7. Presiona `I` → **All**.

**Frame 5 — Salto**
1. Ve al frame `5`.
2. Dibuja al astronauta completamente **despegado del suelo**, con las piernas recogidas hacia arriba y atrás.
3. El cuerpo está en su punto más elevado del frame (aunque el pico real es el frame 6).
4. Los brazos se abren hacia los lados o arriba para transmitir la sensación de vuelo e impulso.
5. Agrega una **sombra ovalada pequeña** debajo del personaje para reforzar que está en el aire.
6. El casco mira ligeramente hacia arriba, siguiendo la dirección del salto.

**Frame 6 — Aire**
1. Ve al frame `6`.
2. Este es el **punto más alto del salto**. El astronauta comienza a descender.
3. Dibuja el cuerpo con las piernas ligeramente más extendidas que en el frame 5 (empiezan a caer).
4. Los brazos pueden estar más abiertos o comenzar a bajar.
5. La **sombra debajo** crece un poco más respecto al frame 5, indicando que está más alto.
6. La gravedad empieza a actuar — el cuerpo no sube más, solo cae.

**Frame 7 — Aterriza**
1. Ve al frame `7`.
2. Dibuja al astronauta con los **pies tocando el suelo**, rodillas muy dobladas para amortiguar el impacto.
3. El cuerpo baja bruscamente — más comprimido incluso que en el Frame 4 de preparación.
4. Los brazos van **hacia adelante** por inercia del impacto, el cuerpo tiende a seguir moviéndose aunque los pies ya frenaron.
5. La sombra desaparece (el astronauta ya está en el suelo).
6. Este frame aplica **Squash**: el cuerpo se achata por el impacto.


**Frame 8 — Contacto**
1. Ve al frame `8`.
2. Dibuja al astronauta **recuperando la postura**, cuerpo volviendo a erguirse.
3. Las rodillas se extienden de regreso, los brazos bajan a los lados.
4. La postura es muy similar al Frame 1 para que el ciclo pueda repetirse sin saltos bruscos.
5. Este frame aplica **Follow Through**: el movimiento no se detiene de golpe, sino gradualmente.


---

### 6. Revisar la animación

1. Presiona `Spacebar` en el viewport para reproducir la animación.
2. Observa si las transiciones entre poses se ven fluidas y el astronauta no "teletransporta" entre frames.
3. Si un frame se ve brusco:
   - Entra en **Edit Mode** (`Tab`) estando en ese frame.
   - Selecciona los puntos de los trazos que necesitas ajustar (`A` para seleccionar todos).
   - Muévelos con `G` o ajusta individualmente.
4. Usa el Onion Skinning mientras corriges para comparar con el frame anterior.
5. Revisa especialmente la transición **Frame 3 → 4** (inicio de preparación) y **Frame 7 → 8** (recuperación del aterrizaje).

---
### 5. Agregar el fondo de luna/espacio

#### Activar el Add-on "Images as Planes"
1. Ve a **Edit → Preferences** (esquina superior izquierda).
2. En el menú izquierdo selecciona **Add-ons**.
3. En el buscador escribe `Images as Planes`.
4. Activa la casilla ✅ del add-on que aparece.
5. Cierra las preferencias.

#### Importar la imagen de fondo
1. Ve a **File → Import → Images as Planes**.
2. Navega hasta tu imagen de fondo (espacio/luna) y selecciónala.
3. Haz clic en **Import Images as Planes**.
4. Aparecerá un plano en la escena con tu imagen aplicada como textura.

#### Posicionar el fondo
1. Con el plano seleccionado, presiona `Numpad 1` para ir a la vista de frente.
2. Escálalo con `S` hasta que cubra todo el área visible de la escena.
3. Para que quede **detrás** del astronauta:
   - Presiona `G → Y` y muévelo hacia atrás (en el eje Y).
   - O en **Object Properties → Transform**, cambia el valor de **Y** a `-1` o `-2`.
4. Verifica en el viewport que el astronauta aparezca **delante** del fondo.

#### Verificar en el render
1. Presiona `Numpad 0` para ver desde la cámara.
2. Confirma que el fondo cubre todo el encuadre.
3. Si no lo cubre, selecciona el plano y escálalo más con `S`.
---

## Guia de poses

![Guia de poses](https://github.com/user-attachments/assets/7419f043-3f62-478b-a70e-639b811c6743)

---

## Vista Previa
<img width="772" height="433" alt="Imagen de la animacion" src="https://github.com/user-attachments/assets/a26f2470-5fee-47fb-9192-3f9ac225141c" />



---

## 👩‍💻 Autor

**Grisel** — Ingeniería en Sistemas Computacionales  
Instituto Tecnológico de Cuautla  
Materia: Graficación 
