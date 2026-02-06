# McQueen-Car
Hola, soy Alejandro y estoy en 3º de ESO, con optativa de Robótica, y en esta, estamos haciendo un proyecto con la placa microbit y coches mcqueen. A continuación explicaré como ha funcionado el trabajo y que se ha conseguido con él.
## Introducción
El proyecto se trata de controlar vía radio el robót mcqueen con una placa microbit (El robot mcqueen tiene muchasa cosas, excepto "cerebro", se le tiene que implementar una placa microbit extra; conclusión, necesitamos un robot mcqueen con una microbit para recivir ondas radio y una placa microbit para enviarlas).

La clase se dividió en grupos de dos, o comúnmente llamado "en parejas". Después Se decidió quién iba a programar la placa microibit y quién el mcqueen, ya que son distintos claramente, y aquí digo por qué: La placa microbit es llamada "El maestro", porque envía la señal radio y da la orden a "El esclavo", que es el robot mcqueen, y tiene que recibir la onda de radio e interpretarla para luego hacer lo que concluya.

Una vez hecho esto empezamos a programar y trabajar, aprendiendo y concluyemdo lo siguente:
## El maestro
El maestro es lo que me tocó a mí, y el más sencillo, ya que tiene un programa más simple:

![](https://github.com/Alexus8650/McQueen-Car/blob/bdd9b5b245801a5e1ed6825f4d27899cc135e634/op.PNG)

### Este programa tiene 2 partes:
#### 1-Void Setup:
Se le adjudica un grupo de radio, en este caso el 8.
#### 2-Void Loop
Aunque dividido en grupos, está constantemente detectando cambios en los sensores para mandar una señal de radio si detecta algo en alguno programado. Si el botón A es presionado se mandará el número 1, si el botón B es presionado se mandará el número 2, si el botón A y B son presionados a la vez se mandará el número 3, si el logotipo es presionado se mandará el número 4 y si es agitada la placa microbit se mandará el número 5.
### Diagrama de Flujo
Aquí tenemos una imagen esquemática del programa para que se entienda mejor:

![](https://github.com/Alexus8650/McQueen-Car/blob/5fe8e539345a38c09d8e49b5257d23a63f759cfb/Diagrama%20en%20blanco%20(7).png)

## El esclavo
Este programa lo hizo mi compañero Adrián, un programa un poco más complicado pero no imposible:

![](*Imagen programa*)

### Este programa tiene dos partes también, como en el anterior:
#### Void Setup:
Este se adjudicará el grupo de radio, en este caso el *Número de radio*
#### Void Loop:
