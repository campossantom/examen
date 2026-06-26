# examen

# Memorias entre las olas 
Campusano, Matias. Espinoz, Adriano.
***Pensamiento computacional***
Mujica, Paulina. Sepulveda, Jannis.

**¿Qué es el proyecto?**

En tiempos donde aparentemente hemos decidido olvidar qui
**¿Qué se ve en pantalla?**  

*    En la primera pantalla hay 4 elementos. Observamos un GIF Animado donde se observa una playa generada por Inteligencia artificial para evitar conflictos de legalidad, además esta imagen fue llevada al software WebGPU GrainRad, donde se altero su imagen para darle esta versión tramada con pixeles y llevarla al rojo y negro, colores que no fueron elegidos de forma asaroza, sino, buscan representar una señal de tensión e inquietud en quién la observa y lee. El mar no es azul, es rojo, es potente y cargado. Además se acompaña de una frase de Raúl Zurita que se encuentra en el memorial de Detenidos Desaparecidos en el Cementerio General de Chile: *Pero mi amor te digo, ha quedado adherido en las rocas, el mar y las montañas.Ellas no conocen los malditos galpones de concreto. Ellas son.*  De fondo suenan las olas golpeando contra la playa de manera repetida y tensa. Un botón nos invita a recorrer esta experiencia con la frase *"Continua viendo las olas"*.
*    En la segunda pantalla hay 4 elementos. Observamos un fondo negro completo donde una lluvia de pixeles que busca representar el rocio de las olas, la caída, nostalgía y aquello que te choca cuando te acercas a ver lo que se esconde en el mar, cambia la velocidad, el tamaño y la opacidad de cada pixel. En la parte central un GIF Animado que incluye imagénes reales de Mujeres Detenidas Desaparecidas, quienes sus cuerpos no fueron encontrados, sus paraderos desconocidos y nos invita a recordar y conmemorar sus rostros, alma y memoria. Una frase de autoría propia en la franja superior la acompaña: *"En las olas que van y que vienen, son gaviotas de acero, son almas que viven, abrazadas por siempre al misterio del mar."* De fondo suena la música de Victor Jara, *Manifiesto*. Un botón gris invita a continuar el recorrido con la frase: *"Continua viendo las olas."*
*    En la tercera pantalla hay 4 elementos. Observamos un fondo negro completo y un recuadro central, levemente hacía arriba que muestra nuestra cámara frontal del dispositivo. Esta tiene un filtro Threshold y un Posterizado, con estos efectos buscamos representar una idea de fotografía análoga de baja calidad, representadas a fotoretratos encontrados para representar a Detenidos Desaparecidos de la época. Es una llamada potente y que quizás puede cruzar ciertos limites, pero hay que arriesgarse para conseguir una llamada fuerte. Además, se acompaña de la frase: *PODRÍAS HABER SIDO TU.* Continua sonando la música de la segunda pantalla con intención de generar una atmosfera nostalgica y cargada de sensibilidad. Finalmente un botón que contrasta por debajo con la frase: *Volvamos a empezar*, nos lleva a la pantalla de inicio.
  
**¿Qué elementos visuales aparecen y cómo se relaciona esta lógica con la problemática de género elegida?**  
La idea del proyecto es generar un golpe emocional a través de una frase potente, los sonidos y los colores. Evocar emocionalidad, resensibilizar y conectar haciendo al usuario parte del mismo proyecto, no con ánimos lúdicos, sino que con un ejercicio sencillo, demostrar que a cualquiera, solo por creer en una realidad diferente, ya no esta hoy con nosotros.

Nuestra regla de oro si logramos entender del todo el requerimiento, se resume al filtro ThresHold al 0.4 y el Posterizado, efecto que le da un peso mucho mayor a nuestra problematica porque hace al usuario parte de la obra, parte de la memoria y lo invita a considerarse privilegiado de no continuar esa triste y trágica historia que afecto a miles de personas, mujeres, hombres y niños.
**¿Qué datos entran? (INPUT)**
En este caso entran imagenes en formato .PNG, .GIF, audios en formato .MP3 y una tipografía en formato .TTF (La elección tipográfica responde a una necesidad de como expresar de manera correcta el mensaje sin caer en banalidades o alteraciones del mensaje, por lo que decidimos investigar y nos pareció pertinente utilizar Noto Sans, tipografía usada por el Museo de la Memoria que es de uso gratuito y se encuentra en Google Fonts).

**¿Cómo se procesan y transforman?**  
Se procesan a través de una instrucción de precarga en nuestro Sketch de P5.

**¿Qué respuesta visual o sonora producen? (OUTPUT)**  
Las imagenes se comienzan a reproducir en el draw gracias a un cambio de estado declardo en Switch(state) que genera 3 pantallas diferentes. Cada una reproduce su sonido o lo comparte dependiendo del caso, además la tipografía se incluye en cada pantalla con su texto y ajuste de responsividad. Es importante aclarar que las configuraciones y posicionamientos fueron acompañados y apoyados por inteligencia artificial y modificados a nuestras necesidad personales del proyecto, sobre todo considerando la dificultad matematica que respondía hacer estos diseños y cada elemento responsivo. Aunque luego de la primera ayuda, logramos entender de buena manera esta lógica y solo tuvimos que copiar y pegar el código y modificarlo nosotros mismos dependiendo de las necesidad que cada elemento considerase.

•⁠  ⁠Pensamiento computacional
Reglas que gobiernan el sistema (inputs, procesos, outputs)
Explicación del sistema de interactividad
•⁠  ⁠Referentes
Listado y breve descripción de referentes visuales, teóricos o históricos.
•⁠  ⁠Diagrama de Flujo (Imagen en PNG ) (Agregada en formato MarkDown)
•⁠  ⁠Código de p5.js (Agregado en formato MarkDown)
•⁠  ⁠Link al sketch en P5.js en formato EDITABLE.
