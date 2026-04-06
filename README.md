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

