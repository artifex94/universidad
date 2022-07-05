# Estadística descriptiva - Parte 1

La estadística descriptiva es la compilación de un conjunto de técnicas y procedimientos que resumen y describen características importantes de los conjuntos de datos. Normalmente tales datos provienen de un proceso de muestreo y estamos interesados en la clasificación de variables, medidas de tendencia central o de localización y las medidas de variabilidad o dispersión.

- - -

## Estadística descriptiva

### Presentación del caso

La empresa HardSofttly tiene 5 empleados en el área de producción algoritmios en Python. Según los registros se tiene la siguiente información:

**Variable/Personal**   | Juliana   | Juan  | Tomas | Luisa | Diego
----                    |----       |----   |----   |----   |----
 **Edad(años)**         | 21        | 23    | 25    | 20    | 18
 **Estatura(metros)**   | 1.65      | 1.75  | 1.60  | 1.75  | 1.63
 **Talla remera**       | S         | L     | S     | M     | S

### Definición 1

Una variable estadística es una propiedad que puede fluctuar y se puede medir, contar o clasificar.

#### Ejemplo 1

En el caso podemos notar que estamos midiendo tres variables estadísticas. Tales variables las podemos fijar mediante:

X:= Edad en años de cada persona del área de torno.<br>
Y:= Estatura de cada persona medida en metros.<br>
Z:= Talle de remera de cada persona medida en letras.<br>

- - -

### Definición 2

La observación es el acto de mirar un fenómeno para extraer información.

#### Ejemplo 2

En el caso podemos notar que estamos observando la edad (X), la estatura (Y) y la talla de remeras (Z). En otras palabras estamos realizando tres observaciones sobre un mismo conjunto: los empleados de la empresa HardSoftly.

- - -

### Definición 3

Un dato es el resultado de una observación. el conjunto de datos
$$\{x_1, x_2, ..., x_n\}$$
se puede escribir en forma simplificada como
$$\{x_i\}_{i=1}^{n}$$

### Ejemplo 3

En el caso para la variable edad (X) podemos denotar por medio de $x_i$, para la estatura (Y) podemos denotar los datos mediante $y_i$ y para la talla de remeras (Z) podemos denotar los datos mediante $z_i$. En cualquier caso, como tenemos cinco observaciones entonces $i = 1,2,3,4,5$.

A continuación el resumen de la primer tabla del caso en función de la notación de datos

| Variable/dato | 1     | 2     | 3     | 4     | 5
| :--:          | --    | --    | --    | --    | --
| $x_i$         | 21    | 23    | 25    | 20    | 18
| $y_i$         | 1.65  | 1.75  | 1.60  | 1.75  | 1.63
| $z_i$         | S     | L     | S     | M     | S

Como podemos notar este permite traducir todo a un lenguaje ordenado por el contador $i$ y simplificado por medio de los nombramientos $x_i$, $y_i$ y $z_i$. Podemos deducir, por ejemplo

$$x_2=23, y_3=1.60, z_1=S$$

También nos permite decir que:

$$\{21, 23, 25, 20, 18\}$$

En un conjunto de datos asociado a cinco observaciones de la variable X (edad) en la empresa HardSofttly

- - -

### Definición 4

Una población es el conjunto de todos los elementos que estamos observando.

### Elemplo 4

En el caso podemos notar que estamos midiendo tres variables estadísticas, esto se traduce que, estamos realizando 3 tipos de observaciones. De este modo podemos concluir que estamos definiendo tres poblaciones distintas.

+ La población uno consiste de la observación de la edad en los empleados de la empresa HardSofttly
+ La población dos consiste de la observación de la estatura en los empleados de la empresa HardSofttly.
+ La población tres consiste de la observación del talle de remera en los empleados de la empresa HardSofttly.

Es muy importante que notemos que el concepto de población liga de forma inherente a las variables estadísticas, los conjuntos observados y los conjuntos de datos.

- - -

### Definición 5

Una muestra es un subconjunto de algunos elementos de la población. Si la muestra posee $n$ elemenentos entonces $n$ es llamado tamaño de la muestra.

### Ejemplo 5

Si observamos la edad en la empresa HardSofttly que tiene cinco empleados en el área de producción de algoritmos en Python, entonces podemos extraer todas las muestras de longitud 4 de esta población. Introducimos formalmente el siguiente concepto que nos permite darle un entorno teórico a nuestro discurso.

- - -

### Definición 6

Supongamos que en una población tenemos una variable estadística X. Definimos el conjunto

$$S=\{m=(x_1, x_2, ..., x_n):m \text{ es una muestra de tamaño }n\}$$

Sea $R$ el conjunto de los números reales. Un estadístico es una función $f:S\to R$. Es decir un estadístico asocia a cada muestra un numero real.

Naturalmente de todas las funciones $f$ que definen estadísticos, estamos interesados en aquellas que arrojen algún tipo de información sobre la muestra.

- - -

### Definición 7

El estadístico del mínimo $X_{min}$ devuelve el valor mínimo de la muestra  
$$(x_1, x_2, ..., x_n)$$

### Ejemplo 6

El estadístico $X_{min}$ toma la muestra $(21, 23, 25, 18)$ y devuelve el valor mínimo. Esto es  
$$X_{min}= 18$$

- - -

### Definición 8

El estadístico del máximo $X_{max}$ devuelve el valor mínimo de la muesrtra $(x_1, x_2, ..., x_n)$

### Ejemplo 7

El estadístico $X_{min}$ toma la muestra $(21, 23, 25, 18)$ y devuelve el valor mínimo. Esto es  
$$X_{min}= 25$$

- - -

### Definición 9

Al estadístico del Recorrido $R$ lo definimos mediante  
$$R= X_{max} - X_{min}$$

### Ejemplo 8

El estadístico $X_{min}$ toma la muestra $(21, 23, 25, 18)$ y devuelve el valor mínimo. Esto es  
$$R= X_{max} - X_{min}= 25 - 18= 7$$

- - -

### Definición 10

El estadístico de la *media muestral* $\underline{X}$ devuelve el valor promedio de la muestra $(x_1, x_2, ..., x_n)$, es decir  
$$\underline{X}= \frac{x_1, x_2, ..., x_n}{n}= \frac{\sum\nolimits_{n=1}^n x_i}{n}$$

### Ejemplo 9

El estadístico de la media muestral toma la muestra $(21, 23, 25, 18)$ y devuelve el valor  
$$\underline{X}= \frac{21+23+25+18}{4}= 21.75$$

- - -

### Definición 11

El estadístico del desvío medio muestral $d$ envía la muestra $(x_1, x_2, ..., x_n)$  
$$d= \frac{|x_1-\underline{X}|+...+|x_n-\underline{X}|}{n}$$

### Ejemplo 10

El estadístico del desvío medio muestral toma la muestra $(21, 23, 25, 18)$ y devuelve el valor  
$$d=\frac{|21-21.75|+|23-21.75|+|25-21.75|+|18-21.75|}{4}= 2.25$$

- - -

