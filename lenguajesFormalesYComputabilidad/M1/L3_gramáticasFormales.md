# Gramáticas formales

El formalismo conocido como gramática formal tiene su origen en la gramática generativa del lingüista Noam Chomsky. Trata de un conjunto de reglas con las cuales es posible crear secuencias de palabras existentes en un lenguaje al realizar sucesivas sustituciones partiendo de un símbolo inicial.

## Clasificación o jerarquía de las gramáticas formales

> Toda gramática genera un único lenguaje, distintas gramáticas pueden generar el mismo lenguaje. No es posible clasificar las gramáticas según el lenguaje que generan. Las clasificaciones se basab en la forma de la gramática. - *UTN de Rosario, 2014*

Noam Chomsky clasificó las gramáticas y los lenguajes dentro de cuatro familias jerárquicamente ordenadas como modelos potenciales del lenguaje natural.

Esta clasificación se establece aumentando las restricciones sobre las producciones y se las nombra como
* gramática de tipo 0;
* gramática de tipo 1;
* gramática de tipo 2;
* gramática de tipo 3.

cada gramática de un determinado tipo surge de aplicar ciertas restricciones al tipo anterior.

### *Tipo 0 o gramática sin restricciones*
Es el caso menos restrictivo. En ella cada producción es de la forma que se presenta a continuación.

$$\alpha\to\beta\text{ donde: }\alpha\in(\Sigma T\cup\Sigma N)\text{ y }\beta\in(\Sigma T\cup\Sigma N)$$

La única restricción de las gramáticas de tipo 0 es que el miembro izquierdo de las producciones debe contener al menos un símbolo no terminal.

### *Tipo 1 o gramática dependiente del contexto*
En este caso las producciomes tienen la siguiente forma.

$$\alpha A\beta\to\alpha\gamma\beta\text{ donde: }A\in\Sigma N\qquad\alpha,\beta\in(\Sigma N\cup\Sigma T)\quad\gamma\in(\Sigma N\cup\Sigma T)$$

Es decir, $\alpha$ y $\beta$ son cadenas que contienen cualquier símbolo de la gramática, terminal o no terminal 