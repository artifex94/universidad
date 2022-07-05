# Tipos de datos básicos y operadores

## Consideraciones generales sobre los lenguajes de programación

Los lenguajes de programación son formas de comunicación universal que mantienen, en general, criterios modelo y que son empleados por aquellas personas que desarrollan e interpretan productos informáticos.

> Los lenguajes naturales son los que hablamos y escribimos los seres humanos. Son dinámicos, ya que, constantemente, incorporan nuevas variaciones, palabras y significados. Por el contrario, los lenguajes formales son rígidos y se construyen a partir de un conjunto de símbolos (alfabeto) unidos por un conjunto de reglas (gramática). Los lenguajes de programación son lenguajes formales. *Sznajdleder (2012)*

Los lenguajes de programación responden a escenarios en los cuales se genera una serie de códigos e instrucciones que pueden ser leídos e interpretados en la medida en la que cumplen una serie de requisitos y estilos, previamente establecidos por sus desarrolladores.

> El lenguaje de programación debe ser universal. Es decir, cualquier problema debe tener una solución que puerda ser programada en el lenguaje y dicha solución ser implementada en cualquier computador. Este requisito es uno de los más fuertes y pocos lenguajes lo poseen. Se dice que cualquier lenguaje en el cual pueden definirse funciones recursivas se considera universal. Del otro lado, un lenguaje sin recursión ni iteración no puede ser universal. Existen cientos de lenguajes de aplicación que no son universales, pero sí podrían ser razonablemente descritos así mismos como lenguajes de programación. El lenguaje de programación debe ser implementable en una computadora, es decir, debe ser posible ejecutar un programa en términos del lenguaje en cualquier máquina. La notación matemática generalmente no es implementable porque en su notación es posible formular problemas que no pueden ser resueltos por cualquier computador. Los lenguajes naturales tampoco son implementables por razones totalmente diferentes: ellos son imprecisos y tienden a ser muy ambiguos. *Ruiz, 2001, https://bit.ly/3dgU5lH*

### Tabla 1: Sintaxis y semántica

**Sintaxis** | **Semántica**
:------------|:-------------
|  La sintaxis de un lenguaje de<br> programación está relacionada con la<br> forma de los programas; por ejemplo,<br> cómo es que las expresiones, comandos,<br> declaraciones, etc. son puestos juntos en<br> un programa  |  La semántica de un lenguaje de<br> programación está relacionada con el<br> significado de los programas; por ejemplo, <br> cómo ellos se comportarán cuando se<br> ejecuten en una computadora.

La sintaxis de un lenguaje influye en cómo los programas son escritos por el programador, leídos por otro programador y traducidos por el computador. La semántica de un lenguaje determina cómo los programas son compuestos por el programador, entendidos por otros programadores e interpretados por el computador. La sintaxis es importante; pero la semántica es más importante aún.

Respecto a Java, Ditel y Deitel (2012) refieren: " Un objetivo clave de Java es poder escribir programas que se ejecuten en una gran variedad de sistemas computacionales y dispositivos controlados por computadora. A esto se le conoce algunas veces como *escribir una vez, ejecutar en cualquier parte* "

- - -

## Tipos de datos básicos o primitivos

Los tipos de datos también son denominados tipos y están categorizados, según sus particularidades, en básicos o primitivos, y en estructurados o complejos. En el caso de los primeros, estos están referidos a aquellos que, por su carácter fundamental, sirven de base para la composición de nuevas estructuras. A su vez, cada uno es identificado con un nombre clave (completamente en minúsculas) y son capaces de almacenar determinado tipo de información en un rango de valores concreto. En este sentido, existen ocho tipos de datos primitivos.

Tipo        | bits      | Valor
---------   |---------- |---------
 byte       | 8         | –128 a +127 (–27 a 27 –1)
 short      | 16        | –32,768 a +32,767 (–215 a 215 – 1)
 int        | 32        | –2,147,483,648 a +2,147,483,647 (–231 a 231 – 1)
 long       | 64        | –9,223,372,036,854,775,808 a +9,223,372,036,854,775,807 (–263 a 263 – 1)
 float      | 32        | Rango negativo: –3.4028234663852886E+38 a –1.40129846432481707e–45<br> Rango positivo: 1.40129846432481707e–45 a  3.4028234663852886E+38
 double     | 64        | Rango negativo: –1.7976931348623157E+308 a –4.94065645841246544e–324<br> Rango positivo: 4.94065645841246544e–324 a 1.7976931348623157E+308
 boolean    |           | *true* o *false*
 char       | 16        | ‘\u0000’ a ‘\uFFFF’ (0 a 65535)

Existen ciertas palabras que ya han sido reservadas dentro de Java y que, por lo tanto, no pueden ser utilizadas como identificadores.

Palabras    | Clave     | en        |  Java     |           |
:-----:     |:-----:    |:-----:    |:-----:    |:-----:    |
 abstract   | assert    | boolean   | break     | byte      |
 case       | catch     | char      | class     | continue  |
 default    | do        | double    | else      | enum      |
 extends    | final     | finally   | float     | for       |
 interface  | implement | import    | instanceof | int      |
 private    | long      | native    | new       | package   |
 static     | protected | public    | return    | short     |
 this       | strictfp  | super     | switch    | synchronized |
 void       | throw     | throws    | transient | try       |
 |          | volatile  |           | while     |           |

Algunas palabras clave que no se utilizan actualmente son: *const* y *goto*

- - -

## Tipos de operadores

Existen diversos tipos de operadores, los cuales permiten formar experesiones en Java

### Operadores de asignación

El operador de asignación básico es el signo igual. Estos operadores se pueden encadenar como por ejemplo

~~~ Java
x = y = 0
~~~

Java proporciona otros operadores de asignación como, por ejemplo, -=, *= y /=, que modifican la variable indicada en el lado izquierdo del operador mediante la operación resta, multiplicación y división, respectivamente.

### Operadores aritméticos binarios

Son típicos de todos los lenguajes de programación. Los típicamente utilizados en Java son: +, -, * y %, que se corresponden a suma, resta, multiplicación, la división y la operación de cálculo del resto. La división solo devuelve la parte entera y descarta el resto.

**Reglas de presedencia de operadores**, que casi siempre son las mismas que las que se utilizan el álgebra:

1. Las operaciones de multiplicación, división y residuo se aplican primero. Si una expresión contiene varias de esas operaciones, los operadores se aplican de izquierda a derecha. Los operadores de multiplicación, división y residuo tienen el mismo nivel de precedencia.

2. Las operaciones de suma y resta se aplican a continuación. Si una expresión contiene varias de esas operaciones, los operadores se aplican de izquierda a derecha. Los operadores se aplican de izquierda a derecha. Los operadores de suma y resta tienen el mismo nivel de precedencia. Estas reglas permiten a Java aplicar los operadores en el orden correcto. Cuando decimos que los operadores se aplican de izquierda a derecha, nos referimos a su asociatividad. Algunos se asocian de derecha a izquierda.

### Operadores unarios

Java proporciona operadores unarios que solo requieren un único operando; el más utilizado es el menos unario (-x) que devuelve el negado de x. El operador autoincremento (++) y el autodecremento (--) suman uno y restan uno respectivamente. Hay dos formas de incrementar y decrementar, prefija y posfija.

### Operadores de tipo

Se utiliza para generar una entidad temporal de un tipo nuevo.

- - -

## Nombres de clases e identificadores

Ahora bien, es importante saber que, para que el lenguaje se ejecute y se interprete correctamente, debes conocer y suscribirte a las reglas y delimitaciones del lenguaje, y algunas de ellas están asociadas a los nombres de las clases e identificadores.

> Por convención, todos los nombres de clases comienzan con una letra mayúscula, y la primera letra de cada palabra en el nombre de la clase debe ir en mayúscula (EjemploDeNombreDeClase). El nombre de una clase es un identificador: una serie de caracteres que pueden ser letras, dígitos, guiones bajos y signos de moneda ($), que no comience con un dígito ni tenga espacios. *Deitel y Deitel (2012) (p.40).*

> Por lo general, un identificador que no empieza con una letra mayúscula no es el nombre de una clase. Java es sensible a mayúsculas y minúsculas. *Deitel y Deitel (2012) (p.30).*
