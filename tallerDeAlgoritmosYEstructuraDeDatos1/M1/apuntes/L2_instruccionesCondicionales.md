# Instrucciones condicionales

Las instrucciones condicionales son aquellas instrucciones que permiten el flujo de control; las instrucciones condicionales y los bucles, básicamente, permiten la evaluación de una condición o variable.

### Operadores de igualdad y relacionales para la toma de decisiones

Mediante los operadores de igualdad o relacionales, se puede proceder a llevar a cabo comparaciones entre tipos primitivos o básicos.

> Una condición es una exresión que puede ser verdadera (*true*) o falsa (*false*). Esta sección presenta la instrucción *if* de Java, la cual permite que un programa tome una decisión, con base en el valor de una condición [...]. Si la condición en una instrucción *if* es verdadera, el cuerpo de la instrucción *if* se ejecuta. Si la condición es falsa, el cuerpo no se ejecuta. Las condiciones en las instrucciones *if* pueden formarse utilizando los operadores de igualdad (== y !=) y los operadores relacionales (>, <, >= y <=) [...] Ambos operadores de igualdad tienen el mismo nivel de precedencia, que es menor que la precedencia de los operadores relacionales. Los operadores de igualdad se asocian de izquierda a derecha. Todos los operadores relacionales tienen el mismo nivel de precedencia y también se asocian de izquierda a derecha.<br> - *Detiel y Detiel (2012) (p. 56).*

### Operadores lógicos

Java proporciona operadores lógicos que se utilizan para simular los conceptos de AND, OR y NOT propios de 'algebra booleana. Los operadores correspondientes son &&, || y !. De la misma manera, se cumple lo siguiente:

> Las expresiones lógicas pueden conectarse a través de los operadores lógicos y así se obtienen expresiones lógicas compuestas cuyo valor de verdad dependerá de los valores de verdad de las expresiones lógicas y así obtener una nueva expresión lógica con su correspondiente valor de verdad. <br> - *Sznajdler (2012) (p. 29).*

Igualmente, se cumple lo siguiente

> Este tipo de operadores es cortocircuitable precisamente porque las expresiones pueden ser evaluadas de manera independiente y con solo evaluar una de ellas es suficiente.<br> - *Allen Weis (2013) (p. 11).*

### La instrucción *if*

La instrucción *if*, de selección simple, realiza una acción indicada solo cuando la condición es verdadera (true); de no ser así, se evita dicha acción. Su forma básica es:

~~~ Java
if (expresión)

instrucción1;

instruccion2.
~~~

Esto permite que, si la instruccion1 se ejecuta como *true*, entonces la instruccion2 también se ejecuta. En caso de que la instruccion1 se ejecute como *false*, entonces la segunda no se ejecuta.

Por otra parte, una forma más compleja del *if*, la instrucción *if-else* de selección doble, le permite especificar una acción a realizar cuando la condición es verdadera, y otra distinta cuando es falsa. La forma básica del *if-else* es:

~~~ Java
if (expresion)

instruccion1;

else
instrucción2;

instruccion3.
~~~

La instrucción *if* puede ser anidada, es decir, encontrarse inmersa dentro de otra instrucción *if*.

### Instrucciones de repetición *while*, *do* y *for*

Este tipo de instrucciones son también llamadas **bucles**, instrucciones de ciclo o de repetición, y pueden anidarse al igual que las instrucciones *if*.

> Java cuenta con tres instrucciones de repetición (también llamadas instrucciones de ciclo) que permiten a los programas ejecutar instrucciones de forma repetida, siempre y cuando una condición (llamada la condición de continuación del ciclo) siga siendo verdadera. Las instrucciones de repetición son *while*, *do-while* y *for* [...]. Las instrucciones *while* y *for* realizan la acción (o grupo de acciones) en sus cuerpos, cero o más veces; si, en un principio, la condición de continuación del ciclo es falsa, no se ejecutará la acción (o grupo de acciones) en su cuerpo, una o más veces. Las palabras *if*, *else*, *switch*, *while*, *do* y *for* son palabras clave en Java.<br> - Deitel y Deitel (2012).

* En lo que respecta a la instrucción *while*, esta es una de las tres formas de aplicación de bucles o instrucciones de repetición, y es la única que permite hacer todo tipo de repeticiones, aún cuando exista otras dos formas. Su forma básica es:

~~~ Java
while(expresión)

instrucción;

siguiente instrucción.
~~~

Mientras que la expresión es *true*, se ejecuta instrucción, y luego se vuelve a evaluar expresión. Cuando el bucle termine, el bloque se devuelve a la siguiente instrucción.

* La instrucción *for* se utiliza, principalmente, para iteraciones simples. Su sintaxis es:

~~~ Java
for(inicialización; comprobación; actualización)

instrucción;

siguiente instrucción.
~~~

* La instrucción *do* es una estructura de bucle que garantiza que, al menos, se dará una ejecución y es la que se utiliza con menos frecuencia. Su sintaxis es:

~~~ Java
do

instrucción

while(expresión)

siguiente instrucción.
~~~

### Instrucciones break y continue

Las instrucciones *for* y *while* permiten terminar el bucle antes del principio de una instrucción repetida y la instrucción *do* permite que se ejecute al menos una vez, entonces la instrucción *break* se utiliza cuando lo que se desea es interrumpir eventualmente la ejecución de una instrucción repetida. Tiene la sintaxis:

~~~ Java
while(...)
{
    if(algo)

    break;
    ...
}.
~~~

Por su parte, en el caso de que la instrucción *continue*, se utiliza cuando lo que se desea es interrumpir una iteración y pasar a la siguiente. Para ello, se utuliza la siguente sintaxis:

~~~ Java
for(...)
{
    if(...)
    
    continue;

    ...
}.
~~~

### La instrucción *switch*

Se utiliza para seleccionar entre vario valores pequeños de ripo entero o caracter. El bloque contiene una secuencia de instrucciones y una colección de etiquetas que representan los posibles valores de la expresión.

### El operador condicional

El operador condicional: se utiliza para los condicionales *if-else* simples. Su formato general es **ComprobacionExpr ? Expr si : Expr no.**

## Métodos de entrada y salida.

En lo que respecta a los métodos de entrada y salida:

> También es conocido que, para las entradas de Java, los códigos pueden provenir de varios puntos diferentes: El terminal, cuya entrada se denomina entrada estándar. Parámetros adicionales en la invocación de la máquina virtual, argumentos de la línea de comandos. Un componente GUI. Un archivo.
> [...]
> La E/S básica a través del terminal se realiza a través del *nextLine* y *Println*. El flujo estándar es *System.in* y el flujo de salida es *System.out*. El mecanismo básico para la E/S formateada utiliza el "tipo" String.
> [...]
> Por su parte, el método main es quien empieza la ejecución de la aplicación en Java y tiene la forma de
> 
> ~~~ Java
> public static void main(String[]args)
> ~~~
> 
> <br> - Allen Weiss (2013). (p. 4).

Por lo tanto, es de gran importancia saber cómo indicarle al programa las instrucciones correctas, de modo que este pueda entregar los resultados deseados; por ejemplo: si lo que se desea es imprimir un texto.

~~~ Java
// Imprimir1.java El código fuente Java reside en archivos cuyos nombres terminan con el sufijo java.
// Programa para imprimir texto.

public class Imprimir1
{
    // aplicando el método main, empieza la ejecución de la aplicación en Java
    public static void main(String[]args)
    {
        System.out.println("Imprimir1");
    } // fin del método main
} // fin de clase Imprimir1

Imprimir1
~~~

Existen disposiciones que se pueden realizar de modo de facilitar el orden u la lectura en el ordenador, una de ellas es el uso de las lineas o espacios en blanco, las cuales son ignoeadas por el compilador. Asimismo, se encuentra el usp de las sangrías, las cuales tienen algunas caranteristicas especiales.

~~~ java
//Imprimir varias líneas con el mpetodo System.out.printf.

public class Prueba2
{
    public static void main(String[args])
    {
        System.out.printf("%s\n%s\n",
        "Prueba de impresión", "en dos líneas.");
    } // fin del método main
} // fin de la clase Prueba2
~~~

En este caso puede observarse el uso de las secuencias de escape, el cual afecta la manera de mostrar caracteres en la ventana de comandos.

### Algunas secuencias de escape comunes

* **\n**    *Nueva línea:* Coloca el cursor de la pantalla al inicio de la siguiente línea
* **\t**    *Tabulador horizontal:* Desplaza el cursor de la pantalla jasta la siguiente posición de tabulación.
* **\r**    *Retorno de carro:* Coloca el cursor de la pantalla al inicio de la línea actual; no avanza a la siguiente línea. Cualquier caracter que se imprima después del retorno de carro sobreescribe los caracteres previamente impresos en esa línea.
* **\\\\**  *Barra diagonal inversa:* Se usa para imprimir un caracter de barra diagonal inversa.
* **\\"**   *Doble comilla:* Se usa para imprimir un caracter de doble comilla. Por ejemplo:

~~~ java
System.out.println("\"entre comillas\"");
~~~

displays "entre comillas".

- - -

## Definición de términos básicos

* *Condición:* Una condición es una expresión que puede ser verdadera (*true*) o falsa (*false*).
* *Método:* Un método es similar a una función en otros lenguajes. La cabecera del método está compuesta por el nombre, el tipo de retorno y una lista de parámetros. La declaración del método incluye el cuerpo del mismo.
* *Variable:* Una variable es una ubicación en la memoria de la computadora, en la que se puede guardar un valor para utilizarlo después en un programa. Todas las variables deben declararse con un nombre y un tipo antes de poder usarse. El nombre de esta, que puede ser cualquier identificador válido, permite al programa acceder al valor de la variable en memoria. El tipo de una variable especifica la clase de información que se guarda en esa ubicación de memoria. Al igual que las demás instrucciones, las instrucciones de declaración terminan con punto y coma (;).