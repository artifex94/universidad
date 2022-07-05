# Variables aleatorias discretas. Parte 1

## Introducción

Dado un espacio muestral $S$, podemos considerar las funciones $X:S\to R$, donde $R$ es el conjunto de los números reales. $X$ es llamada variable aleatoria. El concepto de variable aleatoria permite pasar de los resultados experimentales a un lenguaje funcional formal de fácil uso teórico.

### Presentación del caso

En un experimento químico, el investigador descubre que su variable X de estudio solo toma cuatro valores. Además, conoce los valores $P[X=x]$ y los consigna en la siguiente tabla:

$X$         | 0     | 1     | 2     | 3
:----:      |:----: |:----: |:----: |:----:
 $P[X=x]$   | 0.1   | 0.2   | 0.3   | 0.4

+ ¿Cuál es la probabilidad de que los valores de $X$ se encuentren entre 1 y 2?
+ ¿Cuál es la función de densidad de probabilidad acumulada de $X$?
+ ¿Cuál es el valor esperado de los resultados de la variabe del experimento?
+ ¿Cuál es la varianza de la variable $X$?

### Definición 1

> Para un espacio muestral dado $S$ de  algún experimento, una **Variable aleatoria** es cualquier regla que asocia un número con cada resultado en $S$. En lenguaje matemático, una variable aleatoria es una función cuyo dominio es el espacio muestral y cuyo rango es el conjunto de los números reales.  
> *Devore, 2012. cap. 3.*

### Comentario 1

Dado un experimento espacio muestral $S$, una variable aleatoria es una función  
$$X:S\to R$$

### Ejemplo 1

En nuestro caso, $X:S\to R$ y toma los valores  
$$X=0, 1, 2, 3$$

### Definición 2

> Cualquier variable aleatoria cuyos únicos valores posibles son 0 y 1 se llama **variable aleatoria de Bernoulli**  
> *Devore, 2012. cap. 3.*

### Ejemplo 2

Lanzar una moneda y ver qué cae genera una variable aleatoria como sigue:  
El espacio muestral es  
$$S=C, S$$  
La variable aleatoria puede contar las caras en el lanzamiento, así:  
$$X:S\to R$$  
Mediante  
$$XC=1,\quad XS=0$$

### Definición 3: Clasificación de las variables aleatorias

> Una variable **discreta** es una variable aleatoria cuyos valores posibles constituyen un conjunto finito o bien pueden ser puestos en lista en una secuencia infinita en la cual existe un primer elemento, un segundo elementom y así sucesivamente("contablemente" infinita).  
> Una variable aleatoria es **continua** si *ambas* de las siguientes condiciones se cumplen:  
>  
> 1. Su conjunto de valores posibles se compone de todos los nimeros que hay en un solo intervalo sobre la línea de numeración (posiblemente de extensión infinita, es decir, desde $-\infin$ hasta $\infin$) o todos los números en una unión disjunta de dichos intervalos (por ejemplo, $[0, 10]\cup[20, 30]$).  
> 2. Ningún valor posible de la variable tiene probabilidad positiva, esto es, $P(X=c)=0$ con cualquier valor posible de $c$.  
> *Devore, 2012, cap. 3.*

### Ejemplo 3

En nuestro caso $X:S\to R$ y toma los valores  
$$x=0, 1, 2, 3$$  
Por lo tanto, $X$ es una variable aleatoria discreta. Además  
$$P[1\leq X\leq 2]=P[X=1\text{ o }X=2]=f_{(1)}+f_{(2)}=0.2+0.3=0.5$$

### Definición 4: Función de masa de probabilidad

> La **distribución de probabilidad** o **función de masa de probabilidad** (fmp) de una variable discreta se define para cada número $x$ como $p(x)=P(X=x)=P$ (todas las $s\in S:X(s)=x$)  
> *Devore, 2012. cap. 3.*

### Comentario 2

También a las funciones de masa de probabilidad las llamamos funciones de densidad de probabilidad. Es muy importante notar que la función $p$ está  definida en todos los números reales, es decir:  
$$p:R\to R$$

### Ejemplo 4

En nuestro casola función de densidad de probabilidad ciene dada mediante la siguiente tabla:  

$X$             | 0     | 1     | 2     | 3     | Otro caso
 ----           | ----  | ----  | ----  | ----  | ----
 $p(x)=P[X=x]$  | 0.1   | 0.2   | 0.3   | 0.4   | 0

### Definición 5: Parámetro de distribución

> Supóngase que $p(x)$ depende de la cantidad que puede ser asignada a cualquiera de un número de valores posibles, y cada valor determina una distribución de probabilidad diferente. Tal cantidad se llama **parámetro** de distribución. El conjunto de todas las distribuciones de probabilidad para diferente valores del parámetro se llama **familia** de distribuciones de probabilidad.  
> Devore, 2012, cap. 3.

### Ejemplo 5

Si la probabilidad de que salga cara en el lanzamiento de la moneda es $p$, entonces tenemos la siguiente tabla:  

$X$             | 0     | 1     | Otro caso
:----:          |:----: |:----: |:----:
 $p(x)=P[X=x]$  | $1-p$ | $p$   | 0

En este caso, tenemos el valor $p$ como un parámetro.

### Definición 5: Función de distribución acumulativa de una variable aleatoria discreta

> La **función de distribución acumulativa** (fda) $F_{(x)}$ de una variable aleatoria discreta $X$ con función de masa de probabilidad $p_{(x)}$ se define para cada número $x$ como  
> $$F_{(x)}=P_{(X\leq x)}=\sum_{y:y\leq x}p_{(y)}$$  
> Para cualquier número $x$, $F_{(x)}$ es la probabilidad de que el valor observado de $X$ será cuando mucho $x$.  
> *Devore, 2012. cap. 3.*

### Ejemplo 6

En nuestro caso la función de densidad de probabilidad viene dada mediante la siguiente tabla:  

$X$ | $x<0$ | $0\leq x<1$ | $1\leq x<2$ | $2\leq x<3$ | $3<x$
:----:|:----:|:----:|:----:|:----:|:----:
 $F_{(x)}=P[X\leq x]$ | 0 | 0.1 | 0.3 | 0.6 | 1

O también la podemos presentar de la siguiente forma:  
$$F_{(x)}=\{0\text{ Si }x<0;\quad0.1\text{ Si }0\leq x<1;\quad0.3\text{ Si }1\leq x<2;\quad0.6\text{ Si }2\leq x<3;\quad1\text{ Si }3<x\}$$

### Definición 6: El valor esperado o valor medio de una variable aleatoria discreta X

> Sea $X$ una variable aleatoria discreta con un conjunto de valores posibles $D$ y una función de masa de probabilidad $p_{(x)}$. El **valor esperado** o **valor medio** de $X$, denotado por $E{(X)}$ o $\mu_x$ o sólo $\mu$, es  
> $$E_{(X)}=\mu_x=\sum_{x\in D}x\cdot p_{(x)}$$  
> *Devore, 2012. cap. 3.*

### Ejemplo 7

En nuestro caso, el valor esperado o valor medio viene dado mediante lo siguiente:  
$$E[X]=0*0.1+1*0.2+2*0.3+3*0.4=2$$  
El valor esperado de cualquier función