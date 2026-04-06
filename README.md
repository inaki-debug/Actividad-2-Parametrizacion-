# Actividad-2-Parametrizacion-

En esta actividad se diseñó y se pudo visualizar trayectorias mediante el uso de funciones paramétricas. Estas trayectorias permiten definir el movimiento de un actuador final en un plano cartesiano a través del tiempo. 

**Explicación del código**
1. Se limpian las variables del espacio de trabajo y se cierran las figuras abiertas.

```
clear all
close all
clc
```
2. Se define un vector de tiempo o ángulo que servirá como la variable independiente de la cual dependen x y y.
Para curvas continuas se usa un paso muy corto como de 0.01 para que la curva sea suave mientras que para polígonos se definen puntos discretos según el número de vértices

```
tiempo=[0:0.01:10];
```
3. Dependiendo de la trayectoria, se selecciona un tipo de función. Por ejemplo para el circulo es de la siguiente manera:

```
x=2*cos(t);
y=2*sin(t);
```
4. Para las trayectorias de la actividad 2.2, se utilizó la función `normalize` la cual aseguraba que el movimiento ocurriera en un intervalo de tiempo específico pero que cubra el rango angular necesario.
```
t = normalize(tiempo, "range", [0, 2*pi]);
```
5. Para visualizar los resultados se utilizan las funciones `plot` que muestra la trayectoria completa de forma instantánea y la función `comet` la cual simula el movimiento de un punto a través de la trayectoria. Esta es la ideal para visualizar la dirección y la velocidad del robot.

**Resultados**
Para las trayectorias especiales como la curva de Lissajous o el Epitrocoide, se logró parametrizar su trayectoria mediante su modelo matemático y ajustando las variables correpondientes de cada figura, se logró hacer la medida correcta de cada una de las figuras que lo compone En el caso de las trayectorias poligonales, los puntos se conectan mediante lineas rectas. Para obtener polígonos regulares, el salto entre ángulos debe ser constante y el vector debe cerrarse repitiendo el primer punto. Por último, las curvas que generan "pétalos" se observa que su número de pétalos corresponde a la constante que multiplica t dentro del coseno de las componentes x y y. 

<img width="506" height="338" alt="imagen" src="https://github.com/user-attachments/assets/fd78f429-25eb-489f-8e15-02a77b9493ca" />

<img width="506" height="338" alt="imagen" src="https://github.com/user-attachments/assets/ab81e4c1-6043-4535-a4b8-53009048a232" />

<img width="506" height="338" alt="imagen" src="https://github.com/user-attachments/assets/66082b91-3592-456d-96d6-fd53a60c4e99" />


**Conclusion**
Es importante la parametrización de trayectorias debido a que se pueden descomponer los movimientos en funciones simples que dependen del tiempo. La correcta elección del paso de integración y la normalización del parámetro temporal garantizan que la trayectoria sea ejecutable por un sistema físico manteniendo la suavidad y precisión requeridas.

