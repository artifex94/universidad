# Calculo de probabilidad 1

Usamos el término probabilidad para referirnos al estudio del azar y la incertidumbre en situaciones donde varios posibles sucesos pueden ocurrir. La probabilidad nos proporciona métodos para cuantificar, en algún sentido las oportunidades y posibilidades asociadas con sucesos donde interviene el azar o la incertidumbre. Usamos de forma informal el lenguaje de la probabilidad tanto en el contexto escrito como en el hablado. Así pues, en esta lectura daremos un marco teórico para los conceptos más básicos del diccionario de la probabilidad.

## Noción de probabilidad, cálculo de probabilidades

### Presentación del caso

En un grupo de 60 trabajadores, 11 trabajadores hicieron el curso SQL, 7 trabajadores hicieron el curso de Python y 3 hicieron ambos cursos.

1. ¿Cuál es la probabilidad de seleccionar un trabajador que hizo el curso de SQL?
2. ¿Cuál es la probabilidad de seleccionar un trabajador que hizo el curso de Python?
3. ¿Cuál es la probabilidad de seleccionar un trabajador que hizo ambos curos?
4. ¿Cuál es la probabilidad de seleccionar un trabajador que hizo algún curso?
5. ¿Cuál es la probabilidad de seleccionar un trabajador que no haya realizado el curso de SQL?
6. ¿Cuál es la probabilidad de seleccionar un trabajador que no hizo ningún curso?

Para poder resolver cada uno de los numerales de nuestra situación problemática es necesario que podamos traducirlo al lenguaje matenático de las probabilidades.

- - -

### Definición 1

Un experimento es el proceso de obtener un resultado observado de un fenómeno

### Ejemplo 1

En el caso podemos notar que tenemos un conjunto formado por 60 trabajadores. Nuestro experimento es elegir un empleado al azar y determinar qué cursos realizó

- - -

### Definición 2

El conjunto $S$ de todos los resultados posibles de un experimento es llamado espacio muestral.

### Ejemplo 2

En nuestro caso, debemos comprender cómo organizarr la información cuando del conjunto formado por 60 trabajadores, tomamos uno al azar y determinamos qué cursos realizó. El espacio muestral $S$ viene dado por los 60 trabajadores, que son las 60 posibilidades que hay en nuestra selección.

### Comentario 1

Si todos los elementos de un conjunto $A$ también son elementos de un conjunto $B$ entonces decimos que $A$ está contenido en $B$. Simbólicamente escribimos  
$$A\sub B$$  
Esta notación expresa la idea del evento como sigue.

- - -

### Definición 3

Dado un experimento con espacio muestral $S$, si $E$ es un subconjunto de $S$ entonces $E$ es llamado evento de $S$. Es decir, $E$ es un evento de $S$ si  
$$E\sub S$$  
Convenimos que si un evento es vacío (es decir que no posee elementos) lo denotamos mediante la letra griega $\phi$.

### Ejemplo 3

En nuestro caso consideremos los eventos  
$A=$ El trabajador hizo el curso de SQL  
$B=$ El trabajador hizo el curso de Python

La información del problema se puede estructurar en un diagrama de Veen, donde notamos que  
  
+ Hay 3 trabajadores que cumplen las condiciones de $A$  y de $B$ en simultánea.
+ Completamos a $A$ con 8 trabajadores que faltan.
+ Completamos o $B$ con 4 trabajadores que faltan.
+ Y el resto del espacio muestral se completa con 45 trabajadores.

### Comentario 2

Debido a que los eventos son subconjuntos de un espacio muestral, entonces de forma natural surgen relaciones conjuntas entre los eventos. Las relaciones más importantes de las cuales nos ocuparemos son la *unión*, la intersección y el *complemento de conjuntos*. Antes de recordar tales conceptos recordemos que en la notación conjuntista $\in$ es el símbolo que indica pertenencia. Esto si decimos $x\in A$ estamos diciendo que $x$ es un elemento que pertenece al conjunto $A$ y si decimos $x\notin A$ estamos diciendo que $x$ es un elemento que no pertenece al conjunto $A$.

- - -

### Definición 4

Supongamos que $S$ es un espacio muestral de un experimento. Si $A$ y $B$ son eventos de $S$ entonces definimos el *evento unión A con B* mediante:  
$$A\cup B=\{x\in S:x\in A\quad\text{o}\quad x\in B\}$$  

### Ejemplo 4

En nuestro caso podemos notar que la cantidad de elementos que posee la unión de los eventos $A$ y $B$, es decir el evento $A\cup B$ es  
$$8+3+4=15$$

- - -

### Definición 5

Supongamos que $S$ es un espacio muestral de un experimento. Si $A$ y $B$ son eventos de $S$ entonces definimos el *evento intersección de A con B* mediante:  
$$A\cap B=\{x\in S:x\in A\quad\text{y}\quad x\in B\}$$

### Ejemplo 5

En nuestro caso podemos notar que la cantidad de elementos que posee la intersección de los elementos $A$ y $B$, es decir el evento $A\cap B$ es  
$$3$$

- - -

### Definición 6

Supongamos que $S$ es un espacio muestral de un experimento. Si $A$ es un evento de $S$ entonces definimos el *evento complemento de A* mediante:  
$$A'=\{x\in S:x\notin A\}$$  

### Ejemplo 6

En nuestro caso podemos notar que la cantidad de elementos que posee el evento complemento de $A$, es decir el evento $A'$ es  
$$4+45=49$$

### Comentario 3

En la practicidad a menudo solemos usar los eventos $A\text{o}B$, $A\text{y}B$, $A'$ para indicar la unión, la intersección y el complemento de eventos.

- - -

### Definición 7

Dado un experimento con un espacio muestral $S$ y un evento $A$ de $S$. Se define la probabilidad el evento $A$ como:  
$$P(A)=\frac{\text{cantidad de elementos de }A}{\text{cantidad de elementos de }S}=\frac{\text{casos favorables}}{\text{casos posibles}}$$

En tal caso vale $P(\phi)=0$

### Ejemplo 7

1. ¿Cuál es la probabilidad de seleccionar un trabajador que hizo el curso de SQL?  
$P(A)=\frac{11}{60}$

2. ¿Cuál es la probabilidad de seleccionar un trabajador que hizo el curso de Python?  
$P(B)=\frac{7}{60}=0.35$

3. ¿Cuál es la probabilidad de seleccionar un trabajador que hizo ambos curos?  
$P(A\text{ y }B)=\frac{3}{60}=0.05$

4. ¿Cuál es la probabilidad de seleccionar un trabajador que hizo algún curso?  
$P(A\text{ o }B)=\frac{15}{60}=\frac{1}{4}=0.25$

5. ¿Cuál es la probabilidad de seleccionar un trabajador que no haya realizado el curso de SQL?  
$P(A')=\frac{49}{60}=0.8167$

- - -

### Definición 8

Dado un experimento con un espacio muestral $S$ y dos eventos $A$, $B\subset S$ entonces decimos que $A\text{ y }B$ son eventos complementarios si  
$$B=A'$$

### Teorema 1

Si $A$ es un evento de un espacio muestral $S$ entonces  
$$P(A')=1-P(A)$$

### Ejemplo 8

6. ¿Cuál es la probabilidad de seleccionar un trabajador que no hizo ningún curso?

$$P((A\text{ o }B)')=1-P(A\text{ o }B)=1-\frac{1}{4}=\frac{3}{4}=0.75$$

### Teorema 2

Si $A$ y $B$ son dos eventos entonces  
$$P(A\cup B)=P(A)+P(B)-P(A\cap B)$$