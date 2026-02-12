<h1>Aula 4</h1>

Esta clase consiste en aprender a utilizar el simulador para los robots UR5 y UR10 (UR sim).

<h2>UR Sim</h2>

El sistema operativo para el simulador de UR está basado en Ubuntu, por tanto, se debe instalar una máquina virtual (ej: wmware, virtualbox, etc.). El link para descargar virtualbox se encuentra <a href="https://www.virtualbox.org/wiki/Downloads">aquí</a>. El link para descargar UR Sim se encuentra <a href="https://www.universal-robots.com/download/software-cb-series/simulator-non-linux/offline-simulator-cb-series-non-linux-ursim-3158/">aquí</a>

<div align="center">
<img src="Imagenes/image.png" alt="UR Sim"/>
<br>
<figcaption>Fuente: https://academy.universal-robots.com/es/formacion-en-linea-gratuita/</figcaption>
</div>

<h3>Comandos</h3>

<h4>Mover</h4>

El comando Mover controla el movimiento del robot a través de los puntos de paso subyacentes. Los puntos de paso tienen que obedecer a un comando Mover. El comando Mover define la aceleración y velocidad a la que se moverá el brazo robótico entre esos puntos de paso. Existen diferentes movimientos (MoveL, MoveJ y MoveP).

<div align="center">
<img src="Imagenes/image-1.png" alt="Mover"/>
<br>
<figcaption>Fuente: Autor</figcaption>
</div>

<h4>Punto de paso</h4>

Se trata de un punto en la trayectoria del robot. Los puntos de paso son la parte más importante del programa de un robot, ya que le dicen al brazo robótico dónde tiene que ir. Para enseñar un punto de paso fijo, hay que mover físicamente el brazo robótico hasta la posición en cuestión.

<div align="center">
<img src="Imagenes/image-2.png" alt="Punto de paso"/>
<br>
<figcaption>Fuente: Autor</figcaption>
</div>

<h4>Esperar</h4>

Esperar pausa la señal E/S, o la expresión, durante un tiempo definido. Si se selecciona No esperar, no se hace nada.

<div align="center">
<img src="Imagenes/image-3.png" alt="Esperar"/>
<br>
<figcaption>Fuente: Autor</figcaption>
</div>

<h4>Ajustar</h4>

Sirve para ajustar salidas digitales o analógicas para un valor dado. También se pueden configurar las salidas digitales para enviar un pulso individual.

<div align="center">
<img src="Imagenes/image-4.png" alt="Ajustar"/>
<br>
<figcaption>Fuente: Autor</figcaption>
</div>

<h4>Aviso</h4>

El aviso es un mensaje emergente que aparece en la pantalla cuando el programa llega a este comando. Puede seleccionarse el estilo del mensaje y también indicarse el texto con el teclado en pantalla. El robot espera a que el usuario/operador pulse el botón “OK” del aviso emergente antes de continuar con el programa. Si se selecciona la opción “Detener ejecución del programa”, el programa del robot se detendrá al aparecer este aviso emergente.

<div align="center">
<img src="Imagenes/image-5.png" alt="Aviso"/>
<br>
<figcaption>Fuente: Autor</figcaption>
</div>

<h4>Detener</h4>

La ejecución del programa se detiene en ese punto.

<div align="center">
<img src="Imagenes/image-6.png" alt="Detener"/>
<br>
<figcaption>Fuente: Autor</figcaption>
</div>

<h4>Comentario</h4>

Da al programador la opción de añadir una línea de texto al programa. Esta línea de texto no hace nada mientras se ejecuta el programa.

<div align="center">
<img src="Imagenes/image-7.png" alt="Comentario"/>
<br>
<figcaption>Fuente: Autor</figcaption>
</div>

<h4>Bucle</h4>

Repite los comandos del programa subyacente. Dependiendo de lo que se seleccione, los comandos del programa subyacente se repiten hasta el infinito, un número determinado de veces o siempre que la condición dada sea verdadera. Al repetir en bucle un número determinado de veces, se crea una variable (bucle_1) de repetición dedicada, que se puede usar en expresiones dentro del bucle. La variable de bucle cuenta desde 0 hasta N-1.

<div align="center">
<img src="Imagenes/image-8.png" alt="Bucle"/>
<br>
<figcaption>Fuente: Autor</figcaption>
</div>

<h4>Asignación</h4>

Sirve para asignar valores a variables. Una asignación pone el valor computado de la derecha dentro de la variable de la izquierda. Esto puede resultar útil en programas complejos.

<div align="center">
<img src="Imagenes/image-9.png" alt="Asignación"/>
<br>
<figcaption>Fuente: Autor</figcaption>
</div>

<h4>If</h4>

Una estructura de comando si... entonces cambia el comportamiento del robot basándose en valores variables y entradas de sensores. Use el editor de expresiones para describir la condición bajo la cual el robot sigue los argumentos de este comando If. Si la condición se evalúa como True (verdadera), se ejecutan las líneas incluidas en este comando If.

<div align="center">
<img src="Imagenes/image-10.png" alt="If"/>
<br>
<figcaption>Fuente: Autor</figcaption>
</div>

<h4>Evento</h4>

Un evento puede servir para supervisar una señal de entrada, realizar alguna acción o ajustar una variable cuando dicha señal de entrada se vuelva alta. Por ejemplo, si una señal se vuelve alta, el programa de eventos puede esperar 200 ms y luego volver a bajarla. Esto puede simplificar mucho el código del programa principal en el caso de que una máquina externa se active en un flanco ascendente en vez de en un nivel de entrada alto. Los eventos se comprueban cada ciclo de control (8 ms).

<div align="center">
<img src="Imagenes/image-11.png" alt="Evento"/>
<br>
<figcaption>Fuente: Autor</figcaption>
</div>

<h4>Temporizador</h4>

Un temporizador mide el tiempo que necesitan piezas concretas de un programa para funcionar. Una variable de programa

<div align="center">
<img src="Imagenes/image-12.png" alt="Temporizador"/>
<br>
<figcaption>Fuente: Autor</figcaption>
</div>

<h3>Ejemplo</h3>

<div align="center">
<img src="Imagenes/URSim_Cuadrado.png" alt="Ejemplo UR Sim"/>
<br>
<figcaption>Fuente: Autor</figcaption>
</div>