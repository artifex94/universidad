# Arreglos

Un *array* representa un conjunto de variables de un mismo tipo; cada uno de ellos está identificado por un nombre del *array* (identificador) más un subíndice que indica la posición relativa de la variable dentro del conjunto.

> Un arreglo es un grupo de variables (llamadas elementos o componentes) que contienen valores, todos del mismo tipo. Los arreglos son objetos, por lo que se consideran [...] tipos de referencia [...] Lo que consideramos, por lo general, [...] un arreglo es, en realidad, una referencia a un objeto arreglo en memoria. Los elementos de un arreglo pueden ser tipos primitivos o de referencia (incluyendo arreglos). Para hacer referencia a un elemento específico en un arreglo, debemos especificar el nombre de la referencia al arreglo y el número de la posición del elemento en el arreglo. El número de la posición del elemento se conoce formalmente como el índice o subíndice del elemento.
> 
> *Deitel y Deitel (2012) (p. 242)*.

> Cuando trabajamos con conjuntos numéricos, acotados, consecutivos y "razonablemente" pequeños, podemos utilizar a los elementos del conjunto como índice de acceso al *array*, y así establecer una relación unívoca entre estos elementos y las variables del *array*. En estos casos, hablamos de acceso directo sobre el *array*.
> 
> *Sznajdleder (2012) (p. 156)*.

Por su parte, el acceso indirecto sobre *arrays* se da cuando no se puede acceder a estos. Para ello, se usarán dos arrays; los llamaremos aNum y aCont, entre cada una de las posiciones del *array* y cada uno de los valores del conjunto.

## Capacidad versus longitud de un array

Haremos una diferenciación entre los conceptos de **capacidad** y **longitud** de un *array*.  
Sea el *array* **a** de tipo int[50] entonces:

+ La capacidad es: 50.
+ La longitud de **a** en princípio será 0 y aumentará en la medida en que vayamos agregando elementos al *array*. A la longitud del *array* la llamaremos **len** (abreviatura de length).

la longitud indica cuántos elementos están siendo contenidos, por lo que, si agregamos elementos al *array*, debemos incrementar su longitud. En cambio, la capacidad hace referencia al tope físico que, en el caso de a, es de 50 valores de tipo int. Consideremos ahora estas líneas de código:

~~~ java
int a[50];
a[0]=8;
a[1]=4;
a[2]=6;
~~~

### Operaciones sobre array y sus características

1. **Agregar un elemento al array**  
Esta operación permite agregar un elemento en la primera posición libre del *array*. Es decir, al final.<br> Si consideramos que el *array* está vacío, entonces su longitud (len) será cero y este valor coincidirá con la posición en la que el elemento debe ser agregado. Luego de esto, tendremos que incrementar len, ya que la longitud del *array* pasará a ser 1.

    ~~~ java
    int agregar(int a[], int* len, int v)
    ~~~

    En esta función, **a** es el *array* en cuya primera posición libre asignaremos el valor **v**. La función retornará la posición en la que se agregó a **v**, que siempre coincidirá con el valor de **len-1**, e incrementará el valor de **len**, ya que, al agregar un nuevoo elemento al *array*, su longitud debe ser incrementada.

2. **Búsqueda secuencial**  
Esta operación consiste en secuencialmente el *array* para determinar si este contiene o no un determinado valor.  
Desarrollaremos la función buscar que recibirá el *array*, su longitud y el elemento que queremos determinar si está o no contenido dentro del *array*. La función retornará la posición en la cual el *array* contiene al elemento que estamos buscando o un valor negativo si el elemento no está contenido dentro del *array*. El encabezado de la función será el siguiente:

    ~~~ java
    int buscar(int a[], int len, int v).
    ~~~

    En ella, **a** es el *array*, **len** su longitud y **v** el elemento cuyo valor queremos determinar si está o no cpntenido dentro del *array* a.  
    La estrategia para desarrollar la función buscar será la siguiente: recorrer el *array* comenzando por la posición 0 y avanzando hacia la siguiente posición siempre y cuando no estemos excediendo su longitud y no encontremos lo que estamos buscando.

3. **Buscar y agregar**  
Esta operaciónes una combinación de las dos anteriores. La idea es buscar un elemento en un *array* y retornar la posición en la que se encontró o bien agregarlo al final en caso de no haberlo encontrado. La función **buscarYAgregar** tendrá el siguiente encabezado:

    ~~~ java
    int buscarYAgregar(int a[], int* len, int v, int *enc)
    ~~~

    Asignara *true* o *false* en el parámetro **enc** según el elemento **v** se encuentre previamente o no en el *array* **a** y su valor de retorno representara:

   + Si **enc** es *true*: la posición en donde **a** previamente contenía a **v**.
   + Si **enc** es *false*: la posición en donde (ahora) **a** contiene a **v**.

4. **Insertar un elemento**  
A través de esta operación, podremos insertar un elemento en una determinada posición del *array* siempre y cuando esta posición este comprendida entre 0 y **len**. Llamemos **pos** a la posición en la que vamos a insertar el elemento **v**.  
El algoritmo consiste en desplazar hacia abajo a todos aquellos elementos comprendidos entre **pos** y **len-1** para dejar libre la posición **pos** y poder asignar allí a **v**.

5. **Eliminar un elemento**  
Esta es la operación inversa a la de insertar un elemento. La idea es eliminar del *array* al elemento que se encuentre en una posición especificada. El algoritmo consistirá en desplazar hacia arriba a todos los elementos ubicados entre **pos+1** y **len** siendo **len** la longitud del *array* y **pos** la posición del elemento que queremos eliminar. También será necesario decrementar el valor de **len** porque, luego de eliminar un elemento, la longitud del *array* habrá disminuido.

6. **Insertar en orden**  
Esta operación permite insertar un valor **v** en un *array* respetando el criterio de ordenamiento que mantienen sus elementos. Es decir, que el contenido del *array* debe estar ordenado. El algoritmo consiste en recorrer el *array* comenzando desde la posición 0 y avanzando mientras que no excedamos su longitud y mientras que el elemento que encontramos en la i-esima posición sea menor o igual al que buscamos. Luego, lo insertaremos en la posición i.  
La función **insertarEnOrden** tendrá el siguiente encabezado:

    ~~~ java
    int insertarEnOrden(int a[], int* len, int v, int* encontro)
    ~~~

7. **Buscar en orden**  
Esta operación realiza la búsqueda secuencial de un elemento **v** sobre un *array* **a**, considerando que el contenido de **a** está ordenado. Con esta premisa, no será necesario recorrer el *array* hasta el final para determinar si contiene o no a **v**, ya que si durante la recorrida encontramos que **a[i]** es mayor que **v**, será porque a no contiene a **v**.  
Desarrollaremos la función **buscarEnOrden** con el siguiente encabezado:

    ~~~ java
    int buscarEnOrden(int a[], int len, int v, int* enc)
    ~~~

    La función debe buscar a **v** en **a**. Si lo encuentra, retornará la posición en la que **a** contiene a **v** y asignará *true* al parámetro **enc**. Si no, asignará *false* a **enc** y retornará la posición en la que **a** debería contener a **v** para que, si lo fuéramos a insertar, el *array* continúe manteniendo los elementos en orden.

8. **Buscar e insertar en orden**  
Esta operación combina las dos operaciones anteriores y permite insertar (en orden) un valor que no esté contenido en el *array*. Si intentamos insertar un valor repetido, retornará la posición en la cual el *array* contiene dicho valor.

    ~~~ java
    int buscarEInsertarEnOrden(int a[], int* len, int v, int* enc)
    ~~~

    La función asignará en **enc** *true* o *false*, según el valor **v** se encuentre o no en el *array* **a** y retornará un valor entero cuyo significado será:

    + Si **enc** es *true*, la posición en la que **a** contiene a **v**.
    + Si **enc** es *false*, la posición de **a** en la que se insertó a **v**.

    Teniendo resueltas las funciones **buscarEnOrden** e **insertarEnOrden**, el algoritmo que resuelve esta operación será trivial y se limitará a "buscar en orden" a **v** en **a** y luego **a** "insertarlo en orden", en caso de no haberlo encontrado.

9. **Ordenar arrays (algoritmo de la "burbuja")**  
Existen diferentes algoritmos a través de los cuales podemos ordenar los elementos contenidos en un *array*. Estudiaremos el algoritmo más simple (también el menos eficiente), conocido como el "algoritmo de la burbuja". El algoritmo de la "burbuja" consiste en recorrer el *array* analizando la relación de precedencia que existe entre cada elemento y el elemento que le sigue, para determinar si estos se encuentran ordenados entre sí y, en caso de ser necesario, permutarlos para que queden ordenados. Genéricamente hablando, si **a** es el *array* que vamos a ordenar, e **i** es un valor comprendido entre 0 y **len-1**, entonces: si **a[i]** > **a[i+1]**, significa que estos dos elementos se encuentran desordenados entre sí y que habrá que permutarlos.

- - -

## Arrays multidimensionales

> Sabemos que un *array* representa un conjunto de variables del mismo tipo de datos. Cuando el tipo de dato del *array* es, en sí mismo, un *array*, hablamos de *arrays* multidimensionales. En el lenguaje de programación Pascal, esto se observa claramente al momento de declarar una variable de tipo *array*.  
> 
> ~~~ java
> //define un array de enteros
> var a:array[1..3] of intefer;
> 
> //define un array de arrays de enteros
> var b:array[1..3] of array[1..5] of integer;
> 
> // define un array de arrays de arrays de enteros
> var c:array[1..3] of array[1..5] of array[1..4] of integer;
> ~~~
> 
> *Sznajdleder (2012)*.

### Arrays bidimensionales (matrices)

Un *array* bidimensional es aquel cuyo tipo de datos es, en sí mismo, otro *array*. A un *array* con estas características lo llamamos **matriz**, ya que gráficamente lo representamos como un conjunto de filas y columnas. Las celdas que se forman en las intersecciones de estas son los elementos del *array* bidimensional. En C, definimos una matriz de enteros de la siguiente forma:

~~~ C
int m[4][3]
~~~

luego de esto, la variable **m** representa un *array* de cuatro elementos de tipo int[3]. Esto es: un *array* con capacidad para contener cuatro *arrays*, cada uno con capacidad para contener tres enteros. O bien: una matriz de cuatro filas y tres columnas de enteros.  
Ejemplos:

~~~ java
nombreDelArray = new TipoPrimitivoUObjeto [numero]; //Creación del array

private int[] miArrayDeNumeros = {2, -3, 4, 7, -10}; //Sintaxis ejemplo declarar y crear un array en una línea

// uso con tipos primitivos

prrivate int[] autosPorDia; // Declaración: reserva espacio de memoria

autosPorDia = new int[365]; // Creamos un array de enteros con índices entre el 0 y el 364

autosPorDia[9]= 350; // Ejemplo de asignación

autosPorDia [hora] = 350; // Ejemplo de asignación

autosPorDia [30]++; // Ejemplo de asignación que equivale a autosPorDia [30]+1;

private boolean[] superado;

superado = new boolean [1000];

superado [750] = false;

// uso con tipos objeto

private Persona[] Grupo5B;

Grupo3A = new Persona[100]; //array de objetos Persona con índices entre el 0 y el 99

private String[] nombre;

nombre = new String[200];

nombre[48] = "Eduardo";

// Declarar el array y crear el objeto en una misma línea

Tipo[] nombreDelArray = new Tipo[número];

// uso incluyendo en un método main

int[] arrayEnteros = {2, 3, 1, 7, -1}; // El 2 es el elemento don índice 0 y el -1 el elemento con índice 4

String[] misNombres = new String[10];

misNombres[4] = "Eduardo Palacios";

System.out.println(misNombres[4]);

~~~

- - -

## Definición de términos

### Array
Un arreglo es un grupo de variables (llamadas elementos o componentes) que contienen valores, todos del mismo tipo. Los arreglos son objetos, por lo que se consideran tipos de referencia

### Excepción
Una excepción indica un problema que ocurre mientras se ejecuta un programa. El nombre *excepción* sugiere que el problema no ocurre con frecuencia; si la *regla* es que una instrucción, por lo general, se ejecuta de forma correcta, entonces el problema representa la *excepción a la regla*.

### Manejo de excepciones
El manejo de excepciones nos permite crear programas tolerantes a fallas que pueden resolver (o manejar) las excepciones.