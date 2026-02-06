# McQueen-Car
Hola, soy Alejandro y estoy en 3º de ESO, con optativa de Robótica, y en esta, estamos haciendo un proyecto con la placa microbit y coches mcqueen. A continuación explicaré como ha funcionado el trabajo y que se ha conseguido con él.
## Introducción
El proyecto se trata de controlar vía radio el robót mcqueen con una placa microbit (El robot mcqueen tiene muchasa cosas, excepto "cerebro", se le tiene que implementar una placa microbit extra; conclusión, necesitamos un robot mcqueen con una microbit para recivir ondas radio y una placa microbit para enviarlas).

La clase se dividió en grupos de dos, o comúnmente llamado "en parejas". Después Se decidió quién iba a programar la placa microibit y quién el mcqueen, ya que son distintos claramente, y aquí digo por qué: La placa microbit es llamada "El maestro", porque envía la señal radio y da la orden a "El esclavo", que es el robot mcqueen, y tiene que recibir la onda de radio e interpretarla para luego hacer lo que concluya.

Otra cosa que aclarar, el maestro de nuestro grupo ma a manejar el esclavo del grupo siguiente, y el esclavo será manejado por el maestro de grupo anterior. Entonces los programas no se cuadran, no son para el mismo robot.

Una vez hecho esto empezamos a programar y trabajar, aprendiendo y concluyemdo lo siguente:
## El maestro
Este maestro controló el esclavo del siguiente equipo, en concreto al esclavo que Ramón programó.

Los códigos están hechos con Make Code, que es utilizado para programar las placas Microbit, en un programa de bloques.

El maestro es lo que me tocó a mí, y el más sencillo, ya que tiene un programa más simple:

![](https://github.com/Alexus8650/McQueen-Car/blob/ba6eccddd01a7093c919eb4f71d0cee8da8efd1d/trr.PNG)

### Este programa tiene 2 partes:
#### 1-Void Setup:
Se le adjudica un grupo de radio, en este caso el 8.
#### 2-Void Loop
Aunque dividido en grupos, está constantemente detectando cambios en los sensores para mandar una señal de radio si detecta algo en alguno programado. Si el botón A es presionado se mandará el número 1, si el botón B es presionado se mandará el número 2, si el botón A y B son presionados a la vez se mandará el número 3, si el logotipo es presionado se mandará el número 4 y si es agitada la placa microbit se mandará el número 5.
### Diagrama de Flujo:
Aquí tenemos una imagen esquemática del programa para que se entienda mejor:

![](https://github.com/Alexus8650/McQueen-Car/blob/5fe8e539345a38c09d8e49b5257d23a63f759cfb/Diagrama%20en%20blanco%20(7).png)

## El esclavo
Este código funciona para el esclavo de mi compañero de equipo Adrián que es controlado por Sixto que es el que programó el maestro en su equipo.

Este programa es un programa un poco más complicado que el del maestro, pero no imposible:

![](https://github.com/Alexus8650/McQueen-Car/blob/4217d42746d74832411bdbd31c21021c0fc0bd27/Esclavo.PNG)

### Este programa tiene dos partes también, como en el anterior:
#### Void Setup:
Este se adjudicará el grupo de radio, en este caso el 69.
#### Void Loop:
Este, en vez de enviar ondas de radio, las recive. Está continuamente mirando si hay una onda de radio para reecivir. Cuando se detecta una, compara lo recivido con "5", si es así, el motor derecho avanzará y el izquierdo parará, para que gire a la izquierda; si no, lo comparará con "6", si es así, el motor izquierdo avanzará y el derecho parará para qué gire a la derecha; si no, lo comparará con "7", si es así los dos motores avanzarán para moverse hacia adelante; si no, lo comparaá con el "8", si es así se pararán los dos motores para que se pare el robot en sí. Si todo esto falla se pondrá a intentar captar ondas de radio para empezar el ciclo.
### Diagrama de Flujo:
Aquí tenemos una imagen esquemática del programa para que se entienda mejor:

![](https://github.com/Alexus8650/McQueen-Car/blob/d1b1821b060638fa94f08446d486de2b41cd5e1f/Diagrama%20en%20blanco%20(8).png)

## Producto Final
Este vídeo que aparece acontinuación soy yo manejando, con mi maestro, el esclavo de Ramón. Podemos ver como en la pantalla de mi maestro
[![](https://img.youtube.com/vi/oegCsJTke2k/0.jpg)](https://www.youtube.com/watch?v=oegCsJTke2k)
