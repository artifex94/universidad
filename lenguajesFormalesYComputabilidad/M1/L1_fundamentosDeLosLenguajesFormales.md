# Fundamentos de los lenguajes formales

## *Lenguajes formales* 
Toda comunicación implica la utilización de un lenguaje. Es posible distinguir dos tipos de lenguajes:

* **Naturales:** Se generan de manera espontánea, evolucionan y las reglas que rigen su estructura se establecen cuando el lenguaje ya existe.
  
* **Formales:** obedecen reglas estrictas, no evolucionan y se crean con un fin específico.

La definición de los *lenguajes formales* se basa en la teoría de conjuntos

---
## *Conjuntos* 
Un conjunto es una colección finita o infinita de elementos. Si $A$ es un conjunto, la notación $a\in A$ indica que $a$ es un elemento de $A$ mientras que la notación $b\notin A$ indica que $b$ no es un elemento de $A$.
#### *Definiciones*
<!--Completar: 
    Conj vacio, subconj, igualdad de conj y cardibalidad.
    Operaciones con conjuntos: 
    Unión, intersección, diferencia, complemento, producto cartesiano y relación
-->

> * ***Conjunto vacío:***
> es un conjunto sin elementos, se denota con $\empty$.
> * ***Subconjunto:***
> $B$ es un subconjunto de $A$, $B\subseteq A$, si todo elemento de $B$ es también elemento de $A$. El conjunto de partes de $A$, $\varphi(A)$, es el conjunto de todos los subconjuntos de $A$.
> * ***Igualdad de conjuntos:***
> dos conjuntos $A$ y $B$ se dicen iguales si están formados por los mismos elementos.
> * ***Cardinalidad:***
> Si $A$ es un conjunto finito, la cardinalidad de $A$, $|A|$, es un número natural igual a la cantidad de elementos que pertenecen a $A$
---
## *Alfabetos y cadenas* 
Un alfabeto es un conjunto finito y no vacío de elementos denominados símbolos. Los alfabetos se expresan por 
* **extensión:** al enumerar un símbolo que los componen.

* **comprensión:** al eninciar las propiedades que todos los símbolos cumplen.

Por convención, para denotar un alfabeto, ae utiliza la letra griega $\Sigma$.

> * **Alfabeto binario:** $\Sigma=\{0,1\}$ 
> * $\Sigma=\{ x\in\N | x>0^\wedge x<50\}$

El primer alfabeto se ha definido por *extensión* y el segundo por *conprensión*.

Una palabra o cadena sobre un alfabeto $\Sigma$ es una sucesión finita de elementos del alfabeto $\Sigma$. La longitud de una cadena w (|w|) es el número de símbolos que la componen. La cadena cacia de cualquier alfabeto tiene longitud cero y se denota con $\lambda,|\lambda|=0$.

El conjunto de todas las cadenas que pueden formarse sobre el alfabeto $\Sigma$ se denomina universo del alfabeto u se denota como $W(\Sigma)$. La cadena vacía pertenece a todos los universos.

## *Operaciones con cadenas*

* *Concatenación:*
Si $x$ e $y$ son palabras sobre un alfabeto $\Sigma$, la concatenación de $x$ e $y$ $(x.y)$ es una nueva palabra formada por los símbolos de $x$ seguidos de los símbolos de $y$.
* *Potencia:*
La potencia $n$-esima de una palabra se obtiene concatenando dicha palabra $n$ veces con sí misma.

* *Reflección:*
Si una palabra $x$ está formada por símbolos $a_1,a_2,...,$ $a_{n-1},a_n$ la reflexión de x se obtiene invirtiendo el orden de los símbolos $a_n, a_{n-1}, ..., a_2, a_1$ 

---
## *Lenguajes*
Se dice que $L$ es un lenguaje sobre un alfabeto $\Sigma$, si $L$ es un subconjunto del universo de $\Sigma$, $W(\Sigma)$. Los lenguajes, por lo general, se definen por comprensión, es decir, expresan las propiedades que cumplen las palabras que los forman. Raramente pueden definirse por enumeración de las cadenas que los forman, debido a que, por lo general, los lenguajes contienen infinitas cadenas.

## *Operaciones con lenguajes*

* *Unión*:
Si $L_1$ y $L_2$ son lenguajes, su unión es el lenguaje formado por todas las palabras que pertenecen a $L_1$ o a $L_2$.
$$L_1\cup L_2=\{x/x\in L_1\vee x\in L_2\}$$

* *Intersección*:
Si $L_1$ y $L_2$ son lenguajes, su intersección es el lenguaje formado por todas las palabras que pertenecen a $L_1$ y a $L_2$.
$$L_1\cap L_2=\{x/x\in L_1\wedge x\in L_2\}$$

* *Diferencia*: 
Si $L_1$ y $L_2$ son lenguajes, $L_1-L_2$ es el lenguaje formado por todas las palabras que pertenecen a $L_1$ y no pertenecen a $L_2$.
$$L_1-L_2=\{x/x\in L_1\wedge x\notin L_2\}$$

* *Concatenación*
Si $L_1$ y $L_2$ son lenguajes, su concatenación $L_1.L_2$ se obtiene concatenando $n$ veces el lenguaje con sí mismo.

* *Potencia*
La potencia n-esima de un lenguaje $L$ se obtiene concatenando $n$ veces el lenguaje con sí mismo.

* *Reflexión*
La reflexión de un lenguaje $L$ se obtiene aplicando la reflexión a cada una de las palabras que lo conforman.