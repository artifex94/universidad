# Algoritmos y tiempos de ejecución

## Algoritmos

### *Definición*

> LLamamos algoritmo al conjunto finito y ordenado de acciones con las que podemos resolver un determinado problema. LLamamos problema a una situación que se nos presenta y que, mediante la aplicación de un algoritmo, pretendemos resolver 
> 
> \- Sznajdleder, 2012

Cuando se tienen algoritmosdistintos que resuelven un mismo problema de maneras diferentes, se dice qie dichos algoritmos son equivalentes.

En realidad, se aplican alforitmos todos los días, al realizar las distintas actividades.

En el ambito informático cuando se habla de algoritmos, se está haciendo referencia al conjunto de acciones que debe seguir una computadora para resolver un problema. Se tienen distintos problemas comunes que sirgen para ser resueltos con distintos algortimos, tales como el de la recursión, el del ordenamiento dentro de una estructura. Existe una infinidad de problemas que pueden ser resueltos algorítmicamente.

## Diseño de algoritmos

Para poder diseñar correctamente un algoritmo, es necesario conocer su contexto, de manera que se tenga claro su *alcance*, sus *datos*, sus datos de *entrada* y sus *salidas*.

Para diseñar los algoritmos, también, se cuenta con tres recursos, que son: 
1. la *memoria*, 
2. las *operaciones aritméticas* y 
3. las *operaciones lógicas*

## Análisis de algoritmos
A la hora de elegir un algoritmo para programar la funcionalidad de una aplicación, se tendrán que tener en cuenta los parámetros, como el hardware sobre el que se ejecutará dicha aplicación, la cantidad de datos que procesará y los tiempos de ejecución esperados por el tipo de usuario al que está destinada.

* *Lineal:*
  
  El tiempo de ejecución se incrementa a la misma velocidad en que se aumenta la cantidad de datos de entrada. O sea, son directamente proporcionales a la cantidad de datos de entrada a los qie se someten. Es por esto que es el tipo de algoritmo más eficiente.

* *$N*\log _{(N)}$:*
  
  El logaritmo es una función que crece lentamente. Aunque crece más rápido que la función lineal, es más lenta que la cuadrática y la cúbica. El tiempo de ejecución, en estos algoritmos, es $N$ veces el logaritmo de $N$, siendo $N$ el tamaño de la entrada.

* *Cuadrática:*
  
  El tiempo de ejecución está definido por una función cuadrática siendo $N$ el tamaño de la entrada. Los algoritmos de este tipo son menos eficientes que los del tipo $N*\log _{(N)}$.

* *Cúbica:*
  
  El tiempo de ejecución está definido por una función cúbica siendo $N$ el tamaño de la entrada. Están entre los menos eficientes, ya que, ante pequeños inctrementos en el tamaño de los datos, el tiempo de ejecución del algoritmo crece rápidamente.

Pueden darse casos en que, por las constantes implicadas, una función $N*\log _{(N)}$ sea más eficiente que una lineal. Sin embargo, ante una misma complejidad, las lineales son más eficientes.

## Ejemplos de tiempos de ejecución de los algoritmos

Se examinarán tres problemas para resolver, con el fin de ejemplificar los tipos de funciones que se aplican a algunos algoritmos utilizados normalmente:

* hallar el elemento mínimo de una matriz;
* hallar los puntos más proximos en un plano $(x;y); y$
* hallar todos los grupos de tres puntos colineales en un plano $(x;y)$

### *Hallar el elemento mínimo de una matriz*

el objetivo de este algoritmo es encontrar aquel elemento con menor valor dentro de una estructura de datos que, en este caso, es una matriz.

Consta de los siguientes pasos:

1. guarda, en una variable, el primer elemento de la matríz;
2. Compara el elemento de la variable con cada elemento de la matriz y, en los casos en que el elemento de la matriz sea menor, guardarlo en la variable

Una vez que se hayan recorrido todos los elementos de la matriz, la variablle contendrá el valor mínimo de esta. Este es el caso de un algoritmo lineal, ya que se deben recorrer los elementos de toda la matriz y se posee un tiempo de ejecución fijo para cada elemento.

### *Hallar los puntos más próximos en un plano*

Se tiene un plano con una cantidad $N$ de puntos y el objetivo es encontrar, entre todos esos puntos, al par donde la distancia entre ellos sea menor, en comparación con la distancia entre cualquier otro par de puntos.

Se puede realizar de la siguiente forma:

1. encontrar todos los pares de puntos existentes en el plano;
2. calcular la distancia entre cada par de puntos;
3. hallar el de menor distancia.

La cantidad de pares de puntos existentes en cualquier plano de $N$ puntos es igual a:

>  $\frac{N(N-1)}{2}$
> 
> *Fórmula para calcular la cantidad de pares de puntos existentes*

Si se expande la expresión anterior, queda una función cuadrática:


$\frac{N^2-N}{2} = \frac{1}{2}N^2- \frac{1}{2}N$

Si se utilizan algunos artilugios, se puede evitar calcular la distancia entre todos los pares de puntos del plano. Dicha técnica responde a una función $N\log(N)$ e, incluso, existe una forma que responde a una función lineal.

## Hallar todos los grupos de tres puntos colineales en un plano

Es un problema que se da mucho en el ámbito del tratamiento de los gráficos. Se puede realizar siguendo estos pasos:

1. encontrar todos los grupos de tres puntos existentes en el plano;
2. verificar cuáles se encuentran alineados.

La cantidad de grupos de tres puntos en un plano de $N$ puntos es igual a

> $\frac{N(N-1)(N-2)}{6}$
>
> *Fórmula para calcular los grupos de tres*

> $\frac{1}{6} N^3 - \frac{1}{2}N^2-\frac{1}{3}N$
>
> *Función cúbica*

Al igual que en el caso anterior, existe una forma de resolver este problema de una manera más eficiente, mediante el uso de un algoritmo cuadrático.


