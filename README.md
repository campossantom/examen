# Examen Pensamiento Computacional

# Memorias entre las olas 
Campusano, Matias. Espinoz, Adriano.
***Pensamiento computacional***
Mujica, Paulina. Sepulveda, Jannis.

### ¿Qué es el proyecto?

En tiempos donde aparentemente hemos decidido olvidar qui
### ¿Qué se ve en pantalla? 

*    En la primera pantalla hay 4 elementos. Observamos un GIF Animado donde se observa una playa generada por Inteligencia artificial para evitar conflictos de legalidad, además esta imagen fue llevada al software WebGPU GrainRad, donde se altero su imagen para darle esta versión tramada con pixeles y llevarla al rojo y negro, colores que no fueron elegidos de forma asaroza, sino, buscan representar una señal de tensión e inquietud en quién la observa y lee. El mar no es azul, es rojo, es potente y cargado. Además se acompaña de una frase de Raúl Zurita que se encuentra en el memorial de Detenidos Desaparecidos en el Cementerio General de Chile: *Pero mi amor te digo, ha quedado adherido en las rocas, el mar y las montañas.Ellas no conocen los malditos galpones de concreto. Ellas son.*  De fondo suenan las olas golpeando contra la playa de manera repetida y tensa. Un botón nos invita a recorrer esta experiencia con la frase *"Continua viendo las olas"*.
*    En la segunda pantalla hay 4 elementos. Observamos un fondo negro completo donde una lluvia de pixeles que busca representar el rocio de las olas, la caída, nostalgía y aquello que te choca cuando te acercas a ver lo que se esconde en el mar, cambia la velocidad, el tamaño y la opacidad de cada pixel. En la parte central un GIF Animado que incluye imagénes reales de Mujeres Detenidas Desaparecidas, quienes sus cuerpos no fueron encontrados, sus paraderos desconocidos y nos invita a recordar y conmemorar sus rostros, alma y memoria. Una frase de autoría propia en la franja superior la acompaña: *"En las olas que van y que vienen, son gaviotas de acero, son almas que viven, abrazadas por siempre al misterio del mar."* De fondo suena la música de Victor Jara, *Manifiesto*. Un botón gris invita a continuar el recorrido con la frase: *"Continua viendo las olas."*
*    En la tercera pantalla hay 4 elementos. Observamos un fondo negro completo y un recuadro central, levemente hacía arriba que muestra nuestra cámara frontal del dispositivo. Esta tiene un filtro Threshold y un Posterizado, con estos efectos buscamos representar una idea de fotografía análoga de baja calidad, representadas a fotoretratos encontrados para representar a Detenidos Desaparecidos de la época. Es una llamada potente y que quizás puede cruzar ciertos limites, pero hay que arriesgarse para conseguir una llamada fuerte. Además, se acompaña de la frase: *PODRÍAS HABER SIDO TU.* Continua sonando la música de la segunda pantalla con intención de generar una atmosfera nostalgica y cargada de sensibilidad. Finalmente un botón que contrasta por debajo con la frase: *Volvamos a empezar*, nos lleva a la pantalla de inicio.
  
### ¿Qué elementos visuales aparecen y cómo se relaciona esta lógica con la problemática de género elegida?  
La idea del proyecto es generar un golpe emocional a través de una frase potente, los sonidos y los colores. Evocar emocionalidad, resensibilizar y conectar haciendo al usuario parte del mismo proyecto, no con ánimos lúdicos, sino que con un ejercicio sencillo, demostrar que a cualquiera, solo por creer en una realidad diferente, ya no esta hoy con nosotros.

Nuestra regla de oro si logramos entender del todo el requerimiento, se resume al filtro ThresHold al 0.4 y el Posterizado, efecto que le da un peso mucho mayor a nuestra problematica porque hace al usuario parte de la obra, parte de la memoria y lo invita a considerarse privilegiado de no continuar esa triste y trágica historia que afecto a miles de personas, mujeres, hombres y niños.
### ¿Qué datos entran? (INPUT)
En este caso entran imagenes en formato .PNG, .GIF, audios en formato .MP3 y una tipografía en formato .TTF (La elección tipográfica responde a una necesidad de como expresar de manera correcta el mensaje sin caer en banalidades o alteraciones del mensaje, por lo que decidimos investigar y nos pareció pertinente utilizar Noto Sans, tipografía usada por el Museo de la Memoria que es de uso gratuito y se encuentra en Google Fonts).

### ¿Cómo se procesan y transforman? 
Se procesan a través de una instrucción de precarga en nuestro Sketch de P5.

### ¿Qué respuesta visual o sonora producen? (OUTPUT)  
Las imagenes se comienzan a reproducir en el draw gracias a un cambio de estado declardo en Switch(state) que genera 3 pantallas diferentes. Cada una reproduce su sonido o lo comparte dependiendo del caso, además la tipografía se incluye en cada pantalla con su texto y ajuste de responsividad. Es importante aclarar que las configuraciones y posicionamientos fueron acompañados y apoyados por inteligencia artificial y modificados a nuestras necesidad personales del proyecto, sobre todo considerando la dificultad matematica que respondía hacer estos diseños y cada elemento responsivo. Aunque luego de la primera ayuda, logramos entender de buena manera esta lógica y solo tuvimos que copiar y pegar el código y modificarlo nosotros mismos dependiendo de las necesidad que cada elemento considerase.

### Pensamiento computacional, código reescrito y cada elemento dentro de él
Cumplimos con todos los elementos solicitados en el examén a excepción del ***map*** ya que no logramos incluirlo en una aspecto que considerasemos necesario para explicar y representar nuestra propuesta, por lo que voluntariamente decidimos no incluirlo.
Sin embargo en nuestro listado hay:
*    14 variables globales
*    1 Array
*    1 Class
*    6 Funciones propias
*    2 Bucles
*    6 Condicionales
*    2 Switch

### Referentes
Como referencias utilizamos a los siguientes autores y obras:  
*    Raúl Zurita
*    Lotty Rosefeld
*    Alfredo Jaar: Lament of the Images
*    Ay Sudamerica: Grupo CADA
*    Ausencia y Memoria: MMDH
*    Patricio Guzmán: El botón de Nacar

•⁠  ⁠Diagrama de Flujo (Imagen en PNG ) (Agregada en formato MarkDown)

### Código en formato MarkDown

### Código de P5: [Link editable de P5 Examen](https://editor.p5js.org/campossantom/sketches/EiKsR5mmp)

## Código Fuente (`sketch.js`)

```javascript
let noTo;         // fuente tipográfica NotoSans
let cam;          // captura de la cámara web
let first;        // GIF del mar (pantalla inicial)
let sea;          // audio del mar
let jara;         // audio de Jara
let pixels = [];  // array que almacena los objetos Pixel (lluvia de cuadrados)
let state = 0;    // estado actual: 0=inicio, 1=experiencia, 2=final
let miss;         // GIF de la pantalla de experiencia
let press;        // imagen del botón 1
let press2;       // imagen del botón 2
let press3;       // imagen del botón de regreso

class Pixel {
  constructor() {
    this.reset(); // al crear el pixel, lo inicializa con valores aleatorios
  }
  reset() {
    this.x = random(width);        // posición horizontal aleatoria en el canvas
    this.y = random(-height, 0);   // posición vertical aleatoria fuera del canvas (arriba)
    this.size = random(2, 6);      // tamaño aleatorio entre 2 y 6 px
    this.speed = random(2, 4);     // velocidad de caída aleatoria entre 2 y 4
    this.opacity = random(20, 50); // opacidad aleatoria para dar profundidad
  }
  update() {
    this.y += this.speed;          // mueve el pixel hacia abajo cada frame
    if (this.y > height) this.reset(); // si sale por abajo, lo reinicia arriba
  }
  draw() {
    noStroke();                            // sin borde
    fill(255, this.opacity);               // color blanco con opacidad variable
    rect(this.x, this.y, this.size, this.size); // dibuja el cuadradito
  }
}

function preload() {
  first = loadImage("mar.gif");      // carga el GIF del mar antes de iniciar
  sea = loadSound("mar.mp3");        // carga el audio del mar
  noTo = loadFont("NotoSans.ttf");   // carga la fuente tipográfica
  jara = loadSound("Jara.mp3");      // carga el audio de Jara
  miss = loadImage("missed.gif");    // carga el GIF de la pantalla de experiencia
  press = loadImage("boton.png");    // carga la imagen del botón 1
  press2 = loadImage("boton2.png");  // carga la imagen del botón 2
  press3 = loadImage("back.png");    // carga la imagen del botón de regreso
}

function setup() {
  createCanvas(windowWidth, windowHeight); // crea canvas a pantalla completa
  textAlign(CENTER);                       // alinea el texto al centro horizontalmente
  textFont(noTo);                          // aplica la fuente NotoSans al texto
  cam = createCapture(VIDEO);              // activa la cámara web del dispositivo
  cam.hide();                              // oculta el elemento de video del DOM

  for (let i = 0; i < 300; i++) {
    pixels.push(new Pixel()); // crea 300 objetos Pixel y los guarda en el array
  }
}

function draw() {
  switch (state) {           // ejecuta una función según el estado actual
    case 0:
      initialScreen();       // estado 0: muestra la pantalla inicial
      break;
    case 1:
      experienceScreen();    // estado 1: muestra la pantalla de experiencia
      break;
    case 2:
      finalScreen();         // estado 2: muestra la pantalla final con cámara
      break;
  }
}

function windowResized() {
  resizeCanvas(windowWidth, windowHeight); // ajusta el canvas si cambia el tamaño de la ventana
}

function initialScreen() {
  background(0); // fondo negro

  let escalaX = width / first.width;   // escala horizontal para que el GIF quepa en pantalla
  let escalaY = height / first.height; // escala vertical para que el GIF quepa en pantalla
  let escala = min(escalaX, escalaY);  // usa la menor escala para mantener proporciones

  push();                                                    // guarda el estado de transformación actual
  translate(width / 2, height / 2);                          // mueve el origen al centro del canvas
  scale(escala);                                             // aplica la escala calculada
  image(first, -first.width / 2, -first.height / 2, first.width, first.height); // dibuja el GIF centrado
  pop();                                                     // restaura el estado de transformación

  push();                                                    // nuevo contexto de transformación
  fill(255);                                                 // texto en blanco
  textSize(min(windowWidth * 0.025, 25));                    // tamaño de texto responsive (máx 25px)
  textAlign(CENTER, CENTER);                                 // alinea el texto al centro
  text(
    "Todo mi amor esta aquí\ny se ha quedado pegado a las rocas, al mar, a las montañas.\nellas no conocen los malditos galpones de concreto.\nELLAS SON.",
    width / 2,
    height / 2  // dibuja el poema de Zurita en el centro de la pantalla
  );
  textSize(min(windowWidth * 0.015, 15));                    // tamaño más pequeño para la atribución
  text("— Raúl Zurita", width / 1.25, height / 2 + min(windowWidth * 0.1, 100)); // nombre del autor
  pop();                                                     // restaura transformación

  btnW = min(windowWidth * 0.2, 200);    // ancho del botón responsive (máx 200px)
  btnH = min(windowHeight * 0.08, 100);  // alto del botón responsive (máx 100px)
  btnX = width / 2 - btnW / 2;          // posición X centrada
  btnY = height * 0.72;                  // posición Y al 72% de la pantalla

  image(press, btnX, btnY, btnW, btnH); // dibuja el botón de inicio
}

function experienceScreen() {
  background(0);                 // fondo negro
  for (let p of pixels) {
    p.update();                  // actualiza la posición de cada pixel
    p.draw();                    // dibuja cada pixel en su posición actual
  }
  let escalaX = width / miss.width;   // escala horizontal para el GIF de experiencia
  let escalaY = height / miss.height; // escala vertical para el GIF de experiencia
  let escala = min(escalaX, escalaY); // mantiene proporciones usando la menor escala

  push();                                    // guarda transformación
  translate(width / 2, height / 2);         // mueve origen al centro
  scale(escala);                             // aplica escala
  image(
    miss,
    -miss.width / 4.5,   // desplazamiento X para centrar el GIF reducido
    -miss.height / 4.5,  // desplazamiento Y para centrar el GIF reducido
    miss.width / 2.5,    // ancho del GIF al 40% de su tamaño original
    miss.height / 2.5    // alto del GIF al 40% de su tamaño original
  );
  pop();                                     // restaura transformación

  btnW = min(windowWidth * 0.2, 200);    // ancho del botón responsive
  btnH = min(windowHeight * 0.08, 100);  // alto del botón responsive
  btnX = width / 2 - btnW / 2;          // posición X centrada
  btnY = height * 0.72;                  // posición Y al 72% de la pantalla
  image(press2, btnX, btnY, btnW, btnH); // dibuja el botón de avance

  push();                                 // nuevo contexto
  fill(255);                              // texto blanco
  textSize(min(windowWidth * 0.025, 25)); // tamaño responsive (máx 25px)
  textAlign(CENTER, CENTER);              // alineación central
  text(
    "En las olas que van y que vienen,\nSon gaviotas de acero, son almas que viven,\nAbrazadas por siempre al misterio del mar.",
    width / 2,
    height / 5  // dibuja los versos en el tercio superior de la pantalla
  );
  pop(); // restaura contexto
}

function finalScreen() {
  background(0); // fondo negro

  let targetW, targetH;
  if (width / height < 2 / 3) {     // si la pantalla es más vertical que 2:3
    targetW = width * 0.6;           // ancho de la cámara al 60% del canvas
    targetH = targetW * (3 / 2);     // alto calculado para mantener proporción 2:3
  } else {                           // si la pantalla es más horizontal
    targetH = height * 0.5;          // alto de la cámara al 50% del canvas
    targetW = targetH * (2 / 3);     // ancho calculado para mantener proporción 2:3
  }

  push();                                      // guarda contexto
  fill(255);                                   // texto blanco
  textSize(min(windowWidth * 0.025, 25));      // tamaño responsive (máx 25px)
  textAlign(CENTER, CENTER);                   // alineación central
  text("PODRÍAS HABER SIDO TU,\nRECUERDA", width / 2, height / 1.5); // texto en la parte inferior
  pop();                                       // restaura contexto

  push();                                                  // nuevo contexto de transformación
  translate(width / 2, height / 3);                       // mueve origen al tercio superior
  image(cam, -targetW / 2, -targetH / 2, targetW, targetH); // dibuja el feed de la cámara centrado
  filter(THRESHOLD, 0.4); // convierte la imagen a blanco/negro duro según umbral de brillo
  filter(POSTERIZE);      // reduce colores de la imagen para efecto gráfico de posterización
  pop();                                                   // restaura transformación

  btnW = min(windowWidth * 0.2, 200);    // ancho del botón responsive
  btnH = min(windowHeight * 0.08, 100);  // alto del botón responsive
  btnX = width / 2 - btnW / 2;          // posición X centrada
  btnY = height * 0.72;                  // posición Y al 72% de la pantalla
  image(press3, btnX, btnY, btnW, btnH); // dibuja el botón de regreso
}

function mousePressed() {
  if (
    mouseX > btnX &&           // el click está a la derecha del borde izquierdo del botón
    mouseX < btnX + btnW &&    // el click está a la izquierda del borde derecho del botón
    mouseY > btnY &&           // el click está debajo del borde superior del botón
    mouseY < btnY + btnH       // el click está sobre el borde inferior del botón
  ) {
    state++;                        // avanza al siguiente estado
    if (state > 2) state = 0;      // si supera el estado 2, vuelve al 0 (ciclo)

    switch (state) {
      case 0:
        jara.stop();  // detiene el audio de Jara
        sea.loop();   // reactiva el loop del sonido del mar
        break;
      case 1:
        sea.stop();   // detiene el audio del mar
        jara.loop();  // activa el loop del audio de Jara
        break;
      case 2:
        break;        // en el estado final no cambia el audio (Jara sigue sonando)
    }
  }
}


