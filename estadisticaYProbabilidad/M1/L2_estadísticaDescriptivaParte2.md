# Estadística descriptiva parte 2

## Frecuencias

### presentación del caso

La empresa Hardsoftly decide extender el estudio sobre las edades de las personas que trabajan en el área de programación de Python. Según los registros se tiene la siguiente información en la tabla:


Edad empleados | Cantidad de personas
---------|----------
 18 | 3
 19 | 6
 20 | 7
 21 | 4
 22 | 2

 Explicaremos por medio de un análisis de frecuencias el estudio de tabla de la empresa Hardsoftly.

### Definición 1.

Dada una muestra de longitud $n$, que posee $k$ datos distintos ordenados como sigue  
$$x_1<x_2<x_3<...<x_k$$  
podemos definir para cuando cada $x_1$ su *frecuencia absoluta* $f_i$, la cual es la cantidad de veces que aparece el dato $x_1$ en la muestra.

### Teorema 1

En una muestra de tamaño $n$, que posee $k$ datos distintos con frecuencias absolutas $f_1, f_2, ..., f_k$ vale que  
$$f_1+f_2+..., f_k=n$$  

### Ejemplo 1

Como podemos ver en el caso, en la población observamos la edad. Los valores que toma esta variable son  
$$x_1= 18, x_2= 19, x_3= 20, x_4= 21, x_5= 22$$  
Los cuales ya están ordenados de forma estrictamente creciente. Luego la Tabla 1 de la situación nos provee en su primera columna estos valores. También la Tabla 1 en su segunda columna dice cuántos trabajadores poseen las edades indicadas en la primera columna. Así pues, en términos de frecuencias absolutas tenemos  
$$f_1= 3, f_2= 6, f_3= 7, f_4= 4, f_5= 2$$  
Y resumimos estos datos en la siguiente tabla:

N° | Variable Edad | Frecuencias absolutas
:----:|:----:|:----:
 $i$ | $x_i$ | $f_i$
 1 | 18 | 3
 2 | 19 | 6
 3 | 20 | 7
 4 | 21 | 4
 5 | 22 | 2

Vale la pena notar que  
$$n= 3+6+7+4+2= 22$$

### Definición 2

Dada una muestra de longitud $n$, que posee $k$ datos distintos ordenados como sigue:  
$$x_1<x_2<X_3<...<x_k$$  
podemos definir para cada dato $x_i$ su *frecuencia absoluta acumulada* $F_i$ la cual es la cantidad de datos acumulados en la muestra hasta el dato $X_i$ para  
$$i= 1, 2, ..., k$$

### Comentario 1

Las frecuencias absolutas acumuladas obedecen la siguiente fórmula  
$$\begin{equation*}
F_i=\sum_{j=1}^i\quad f_j
\end{equation*}$$

O de forma recursiva:

$$F_1= f_1\quad F_{i+1}= F_i+f_i$$

### Ejemplo 2

Podemos calcular las frecuencias absolutas acumuladas $F_i$ como sigue

$F_1=f_1=3$  
$F_2=F_1+f_2=3+6=9$  
$F_3=F_2+f_3=9+7=16$  
$F_4= F_3+f_4=16+4=20$  
$F_5=F_4+f_5=20+2=22$

N° | Variable Edad | Frecuencias absolutas | Frecuencias absolutas acumuladas
:----:|:----:|:----:|:----:
 $i$ | $x_i$ | $f_i$ | $F_i$
 1 | 18 | 3 | 3
 2 | 19 | 6 | 9
 3 | 20 | 7 | 16
 4 | 21 | 4 | 20
 5 | 22 | 2 | 22

### Definición 3

Dado un conjunto de frecuencias absolutas $f_1, f_2, ..., f_k$, definimos la frecuencia relativa i-ésima mediante  
$$f_{ri}=\frac{f_i}{n}$$  
Y la frecuencia relativa acumulada i-ésima mediante  
$$\begin{equation*}
F_{ri}=\sum_{j=1}^i\quad f_{rj}
\end{equation*}$$
donde $i=1, 2, ..., k$

### Ejemplo 3

Ahora procedemos a conocer a las frecuencias relativas las cuales se calculan mediante  
$$f_{ri}=\frac{f_i}{n}$$  
Donde $n=22$, por lo tanto  
$$f_{ri}=\frac{3}{22}=0.1364\quad f_{r2}=\frac{6}{22}= 0.2727\quad f_{r3}=\frac{7}{22}= 0.3182\quad f_{r4}=\frac{4}{22}= 0.1818\quad f_{r5}=\frac{2}{22}= 0.0909$$  
Finalmente realizaremos las frecuencias relativas acumuladas sabiendo que  
$$F_{r1}=f_{r1}\qquad\text{y}\qquad F_{ri+1}= F_{ri}+f_{ri+1}$$  
De esta forma tenemos que  
$F_{r1}=f_{r1}=0.1364$  
$F_{r2}=F_{r1}+f_{r2}=0.1364+0.2727=0.4091$  
$F_{r3}=F_{r2}+f_{r3}=0.4091+0.3182=0.7273$  
$F_{r4}=F_{r3}+f_{r4}=0.7273+0.1818=0.9091$  
$F_{r5}=F_{r4}+f_{r5}=0.9091+0.0909=1$

N° | Variable Edad | Frecuencias absolutas | Frecuencias absolutas acumuladas | Frecuencias relativas | Frecuencias relativas acumuladas
:---------:|:----------:|:---------:|:---------:|:----------:|:---------:
 $i$ | $x_i$ | $f_i$ | $F_i$ | $f_ri$ | $F_{ri}$
 1 | 18 | 3 | 3 | 0.1364 | 0.1364
 2 | 19 | 6 | 9 | 0.2727 | 0.4091
 3 | 20 | 7 | 16 | 0.3182 | 0.7273
 4 | 21 | 4 | 20 | 0.1818 | 0.9091
 5 | 22 | 2 | 22 | 0.0909 | 1

### Comentario 3

Naturalmente podemos preguntarnos por cómo calcular los valores estadísticos. Por ejemplo, para los estadísticos media muestral, desvío muestral y varianza muestral tenemos:  
$$\underline{X}=\frac{\sum\nolimits_{i=1}^k\quad x_if_i}{n}$$

$$d=\frac{\sum\nolimits_{i=1}^k\quad |x_i-\underline{X}|f_i}{n}$$

$$S^2=\frac{\sum\nolimits_{i=1}^k\quad (x_i-\underline{X})^2f_i}{n-1}$$

entonces:

$\underline{X}=\frac{\sum\nolimits_{i=1}^5\quad x_if_i}{22}$  
$\underline{X}=\frac{18*3+19*6+20*7+21*4+22*2}{22}= \frac{436}{22}$  
$\underline{X}=19.82$

$d=\frac{\sum\nolimits_{i=1}^5\quad |x_i-19.82|f_i}{22}$  
$d=\frac{|18-19.82|3+|19-19.82|6+|20-19.82|7+|21+19.82|4+|22-19.82|2}{21}$  
$d=\frac{20.7272}{21}=0.9421$

$S^2=\frac{\sum\nolimits_{i=1}^5\quad (x_i-19.82)^2f_i}{22-1}$  
$S^2=\frac{(18-19.82)^23+(19-19.82)^26+(20-19.82)^27+(21-19.82)^24+(22-19.82)^22}{22-1}$  
$S^2=\frac{27.94}{21}=1.3$

### Comentario 4

Naturalmente presentar una tabla de frecuencias llena de números no suele ser muy vistoso. Así pues, la estadística descriptiva ofrece presentar los mismos resultados en representaciones gráficas.