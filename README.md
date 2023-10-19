# PRIMER PARCIAL DE SPD
![1](https://github.com/Cheis18/Parcial_SPD/assets/113544459/5e8f059c-acbe-4afb-b4a5-8df230a62494)
## INTEGRANTES
- Mauricio Gabriel Harriet Thery
- Belkis Yolanda Guanipa Lopez
- Cheimienst Hernández Gómez
  
## Primera parte: Controlar un contador con botones en un programa que utiliza 2 displays de 7 segmentos en multiplexación
![2](https://github.com/Cheis18/Parcial_SPD/assets/113544459/0bd39175-48af-4b50-907b-c18bd9b27456)
## 1) Descripción
Este proyecto involucra la implementación de un contador utilizando dos visualizadores de siete segmentos. El control del contador se realiza mediante tres botones: uno para incrementar el contador, otro para disminuirlo y un tercero para restablecerlo. La estructura fundamental del código comprende los siguientes elementos:

1. Definición de nombres significativos para diversos valores, lo cual no solo mejora la legibilidad del código, sino también optimiza el uso de memoria.
2. Declaración de las variables necesarias para el desarrollo adecuado del programa.
3. Una función llamada `setup()` que configura los pines de entrada para los botones.
4. Una función llamada `loop()` que contiene la lógica principal del programa y se ejecuta continuamente mientras Arduino esté encendido.
5. Una función llamada `presionarPulsador()` que detecta si los botones se han presionado o no.
6. Una función llamada `apagarDisplay()` que se encarga de apagar todos los segmentos de los visualizadores.
7. Una función llamada `mostrarNumero()` que se encarga de activar los segmentos correspondientes en el visualizador.
8. Una función llamada `prendeDigito()` que permite activar los dígitos de unidades o decenas en los visualizadores.
9. Por último, una función llamada `mostrarContador()` que se encarga de presentar los valores de unidades y decenas en los visualizadores.

Además, en términos de la electrónica utilizada, se emplea la [multiplexación](https://www.uazuay.edu.ec/sistemas/teleprocesos/multiplexacion)  y evita problemas de ruido de señal, como el fenómeno conocido como ["debounce"](https://www.murkyrobot.com/guias/arduino/debounce) o ["efecto rebote"](https://www.murkyrobot.com/guias/arduino/debounce).

## 2) Enlace del proyecto
[SPD - Primer parcial - Parte 1]([https://www.tinkercad.com/things/c6Y9zx44Fnb-copy-of-primera-parte-del-examen-de-spd/editel?sharecode=_g-j-M7_DWu3wRsHQ90MPSgqWQZF7gK58weqZ-hQx6w](https://www.tinkercad.com/things/6Zc6LRO8SDc-copy-of-ejericio1-2/editel?tenant=circuits))

## Segunda Parte: Cambio de estado por medio de un interruptor deslizante +  sensor de flexión
![3](https://github.com/Cheis18/Parcial_SPD/assets/113544459/213f7a1c-6212-4d40-82e8-6625440e4881)

## 1) Descripción

Para la parte 1, agregamos ahora un interruptor, donde su funcionamiento es alternar el estado entre, mostrar los números del contador de la misma manera que la parte 1, y mostrar de manera automática los números primos (números que solo sean divisibles por 1 y por si mismos) que se encuentren entre el rango de 0 a 99. Para esto, declaramos una función llamada `detectarPrimo()`

Además, se agregó un [sensor de flexión](https://rambal.com/presion-peso-nivel-flex/250-sensor-flex.html#:~:text=El%20Sensor%20Flex%20(%20Sensor%20de%20Flexiono%20o%20flex%20sensor)%20produce,distintos%20valores%20de%20resistencia%20electrica.), este dispositivo detecta la flexión o curvatura de un objeto, como un cable o una pieza flexible y entrega el angulo de inclinación. Para esto se declaró una función de nombre `mostrarAngulo()`.

## 2) Enlace del proyecto
[SPD - Primer parcial - Parte 2](h[ttps://www.tinkercad.com/things/hBZ97ZE6uDL-segunda-parte-del-examen-de-spd-parte-1/editel?sharecode=j5J0IRgQ8MvUgFu1s8G4YiuOi-3GZQqMK3ufEMskiOQ](https://www.tinkercad.com/things/gKkeTF3bbIq-copy-of-copy-of-copy-of-ejericio1-3/editel?tenant=circuits))

## 3) Sugerencia como componente adicional
![4](https://github.com/Cheis18/Parcial_SPD/assets/113544459/79ea7d16-fa2e-413b-a405-5fe0fa74f45b)

![5](https://github.com/Cheis18/Parcial_SPD/assets/113544459/4f35e6be-9a50-490d-bfc0-4a5434720360)


Se le puede agregar al proyecto un "motor de aficionado", llamado así porque es un motor de cc (corriente continua) que se le acopló una carcasa para generar movimiento, ya sea para brazos, ruedas, helices, etc. Para tener más control sobre este, podemos incluir al proyecto un ["controlador de motor"](https://cursos.mcielectronics.cl/2022/08/05/que-es-un-puente-h/) o tambien llamado ["Puente H"](https://cursos.mcielectronics.cl/2022/08/05/que-es-un-puente-h/). En el siguiente enlace se enseña como podria usarse dicho motor y controlador en una placa arduino para controlar el sentido de giro del motor.
![6](https://github.com/Cheis18/Parcial_SPD/assets/113544459/9e6787b7-6ee3-491b-98be-a97a5700f24d)


## Enlace del ejemplo
[Motor de "aficionado" con inversión de marcha por medio de un controlador](https://www.tinkercad.com/things/3DWHBq6tPv1-glorious-bombul/editel?sharecode=xVmE-y7X4gkLnzfS4gMHEVI4tN6mgUbmRkFmlm31f5o)

## Tercera Parte: Implementación de un sensor ambiental en el proyecto
(![8](https://github.com/Cheis18/Parcial_SPD/assets/113544459/80c2ecff-7d97-4964-b6cf-ad7b2526145e)
Un sensor de luminosidad es un dispositivo que tiene muchas aplicaciones pero, de entre todas ellas, la más destacable de todas es que nos permite hacer un uso mucho más eficiente de la energía que utilizamos, adaptando la potencia de las luminarias a la luz ambiental existente

## 2) Explicación de su funcionamiento

Desde su salida negativa (Cátodo) la alimentamos con 5V y desde su salida positiva (Ánodo) la conectamos ,a una entrada analogica de la placa de Arduino ,y a una resistencia de 50kOhm que esta conectada a Tierra (Podemos colocarle otro valor a la resistencia, pero en este caso decidimos colocarle ese valor para trabajar con ella, en el caso de querer colocar otra resistencia, tendriamos que regular todo otra vez). Ahora, por medio de una variable, en este caso `lectura_luz`, tomamos un rango de todos los valores que nos va dando el sensor a medida que incrementa o disminuye la intensidad luminica, en este caso, nos entrega un rango de (49 - 1023), por lo que para saber que porcentaje de intensidad luminica es, llamamos a otra variable, en este caso es `luz` utilizando la [función map()](https://arduinofacil.com/como-funciona-la-funcion-map/#:~:text=La%20función%20map()%20de,inicio%20rango%20de%20entrada) para poner esos valores entre un rango del 0% al 100%. De esta manera, sabemos que a menor porcentaje de intensidad luminica, el fotodiodo entrega menor voltaje y a mayor porcentaje de luz liminica, el fotodiodo entrega un mayor voltaje.

Uso del sensor ambiental:

El sensor detecta los niveles de luz ambiental para ajustar el brillo y la temperatura de color de la imagen. Gracias a esta función es posible obtener la mejor calidad de imagen posible en las condiciones de iluminación de la habitación.
   
![9](https://github.com/Cheis18/Parcial_SPD/assets/113544459/dc97fdcd-88ef-42cc-94bc-3404b4774e5f)


## 3) Enlace del proyecto
[SPD - Primer parcial - Parte 3](https://www.tinkercad.com/things/hLbInryp3Hc-copy-of-copy-of-ejericio1-3/editel?tenant=circuits)
