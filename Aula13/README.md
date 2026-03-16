<h1>Aula 13</h1>

Esta clase consiste en simular el robot SCARA T3 EPSON en el software EPSON RC+ 7 a través del robot manager y de comandos.

<h2>EPSON RC+ 7</h2>

El software EPSON RC+ 7 permite simular el robot SCARA T3-401S, utilizando la ventana del robot manager y de comandos en lenguaje SPEL+. Es un entorno integrado con el controlador de visión por cámara.

<h3>Comandos SPEL+</h3>

SPEL+ de Epson es un lenguaje de programación para aplicaciones de automatización de robots. Con más de 500 comandos y declaraciones, que incluyen funciones de movimiento, control de E/S, variables y tipos de datos, control de programas, etc.

reset %Resetea el robot
?Motor %Pregunta el estado del robot
motor On/Off %Encender/Apagar robot
on/off 4 %Encender/Apagar la salida digital No. 4
?sw(8) %Pregunta el estado de la entrada digital No. 8
SFree %Libera las articulaciones
SLock %Bloquea las articulaciones
print erroron %Imprime el estado de error del robot
JTran 1,90 %Mueve la articulación 1, 90 grados
Home
SavePoints "robot1.pts"
here p1 %Guarda la coordenadas actuales X, Y y Z en el P1
go here :z(-50)
Pulse 0,0,0,0 %Coloca las articulaciones en la posición de calibración de fábrica (0 grados y 0 mm)

Power High/Low %Low es el 20% de la potencia del robot


<h3>Ejemplo 1</h3>

```SPEL+
Go JA(-90,90,0,0,0,0)
Go JA(-90,90,-50,0,0,0)
Jump JA(0,90,-50,0,0,0)
Jump JA(90,90,0,0,0,0)
```

```SPEL+
Function main 
	Go P1 
	Go P2 
	Go P0 
Fend 
```

```SPEL+
Function main 
	Print "This is my first program." 
	Power High 
	Speed 20 
	Accel 20, 20 
	Go P1 
	Go P2 
	Go P0 
Fend 
```

```SPEL+
Function main
	Motor On
	Jump P1
	On 4
	Jump P2
	Off 4
	Wait 1
	On 4
	Jump P3
	Off 4
	Motor Off
Fend
```


```SPEL+
Function main
	Print "THIS IS MY FIRST PROGRAM"
	Print "MOTOR STATE:", Motor
    Motor On
	Jump P0
	Jump P1
	Jump P2
    Motor Off
Fend
```

<h3>Ejemplo 2</h3>

```SPEL+
Function main
	Print "THIS IS MY SECOND PROGRAM"
	Print "MOTOR STATE:", Motor
	Call ENABLE_ARMS
	If ENABLE_ARMS = True Then
		Print "Enable complete"
	Else
		Print "Incomplete enable"
	EndIf
	Jump P0
	Jump P1
	Jump P2
Fend
Function ENABLE_ARMS As Boolean
	If ErrorOn Then Reset
	If Not Motor Then Motor On
	'Speed ProdVelocity
	'Print Speed
	ENABLE_ARMS = True
Fend
```

<h3>Ejemplo 3</h3>
