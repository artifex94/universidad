# Calculo de probabilidad 2

En el análisis de datos es fundamental encontrar siempre la forma de ordenar la información. Diagramas de Venn, tablas de contingencia, diagramas de árbol, entre otros, son de uso habitual al momento de resolver problemas que implican el manejo de probabilidades. En esta lectura nos concentramos en la información que podemos extraer de una tabla de doble entrada.

### Presentación del caso

La empresa System S.A decide sortear un viaje a San Martín de los Andes entre los 20 mejores empleados. De ellos,  

+ 12 son mujeres
+ 11 están casados
+ 5 son mujeres casadas

Para dar un conjunto de regalos personalizados por categorías, el responsable de RRHH desea saber, cuáles son las probabilidades de que al elegir una persona al azar se tenga:  

1. Que sea hombre
2. Que sea hombre casado
3. Que sea hombre dado que es casado

- - -

### Comentario 1

Debemos entender que sucede en un espacio muestral $S$ cuando introducimos información sobre el hecho que un evento $A$ haya sucedido y nos preguntamos por la probabilidad de ocurrencia de un evento $B$. Esto es, ¿Qué pasa con la probabilidad de ocurrencia del evento $B$, sabiendo que el evento $A$ ha ocurrido? Esta idea es la del concepto de probabilidad condicional.

### Definición 1

Sea $S$ un espacio muestral, $A$ y $B$ eventos de $S$. La probabilidad condicional de un evento $A$ dado un evento $B$, está definida por  
$$P(A|B)=\frac{P(A\text{ y }B)}{P(B)}$$  
P(A|B) se lee como Probabilidad de $A$ dado $B$

### Teorema 1: Teorema de la multplicación

Para cualquier par de eventos $A$ y $B$ de un espacio muestral $S$. Entonces  
$$P(A\text{ y }B)=P(B)P(A|B)=P(A)P(B|A)$$

### Ejemplo 1

Seguidamente analizamos la información que tenemos de nuestro caso planteado:  
Como podemos ver acá comparamos dos variables categóricas contra otras dos variables categóricas: Mujer y hombre VS personas casadas y solteras.  
Si hay 20 personas de las cuales 12 son mujeres, 11 están casadas y 5 son mujeres casadas entonces podemos construir una tabla de conttingencia de doble entrada como sigue:  


Hombres | Mujeres | Total ||
:----:|:----:|:----:|:----:
 6 | 5 | 11 | **Casados**
 2 | 7 | 9 | **Solteros**
 8 | 12 | 20 | **Total**

Ahora bien, si tenemos los eventos  
$A:=$ la persona seleccionada es hombre  
$B:=$ la persona seleccionada es casada  

1. La probabilidad que sea hombre es:  
   $P(A)=\frac{8}{20}$.
2. Que sea hombre casado  
   $P(B)=\frac{6}{20}$
3. Que sea hombre dado que es casado  
   $P(A|B)=\frac{\frac{6}{20}}{\frac{11}{20}}=\frac{6}{11}$

En consecuencia, la probabilidad que sea hombre es 0.4, la probabilidad que sea hombre casado es 0.3 y la probabilidad que sea hombre dado que es casado es 0.5454

- - -

### Comentario 2

Dos teoremas muy importantes para trabajar con probabilidades condicionales son los *Teoremas de la probabilidad total* y el *Teorema de Bayes*. Sin embargo, los presentamos para que sean tenidos en cuenta en el desarrollo del contenido del curso.

### Definición 2

Supongamos que $S$ es un espacio muestral. Sea $A_1, A_2, ..., A_k$ una familia de eventos de $S$. Diremos que esta familia de eventos es una partición de $S$ si  

+ $A_1, A_2, ..., A_k$ son mutuamente excluyentes dos a dos. Es decir, para cualquier elección de dos eventos $A_i$ y $A_j$ distintos de la lista ellos son mutuamente excluyentes
+ $A_1, A_2, ..., A_k$ son exhaustivos en el sentido su unión alcanza a todo el espacio muestral, es decir:  
  $$S= A_1\cup A_2\cup ...\cup A_k$$

### Teorema 2: Teorema de la probabilidad total

Sea $S$ un espacio muestral. Sean $A_1, ..., A_k$ eventos mutuamente excluyentes y exhaustivos. Entonces para cualquier otro evento $B$ tenemos que:  
$$P(B)=\sum_{i=1}^k\quad P(A_i)P(B|A_i)$$

### Teorema 3: Teorema de Bayes

Sea $S$ un espacio muestral. Sean $A_1, ..., A_k$ eventos mutuamente excluyentes y exhaustivos. Entonces para cualquier otro evento $B$, si $P(B)>0$ entonces  
$$P(A_j|B)=\frac{P(A_j)P(B|A_j)}{\sum_{i=1}^k\quad P(A_i)P(B|A_i)}$$

