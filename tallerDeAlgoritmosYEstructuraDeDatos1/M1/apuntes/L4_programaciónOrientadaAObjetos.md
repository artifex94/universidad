# Programación orientada a objetos - Herencia

## Herencia

> La herencia [...] es una forma de reutilización de software en la que se crea una nueva clase, al absorber los miembros de una existente, y se mejoran con nuevas capacidades, o con modificaciones en las capacidades ya existentes.  
> *Deitel y Deitel. (p. 360) (2012)*

Aunado a ello, a la herencia se la conoce algunas veces como especialización.

Supongamos que deseamos trabajar con la clase **Fecha**. Supongamos que no tenemos acceso al código de esta clase. La solución será crear una nueva clase. La solución será crear una nueva clase que herede de **Fecha** y que modifique la manera en que ésta se representa como cadena.  
Esto lo podemos hacer sobreescribiendo el método **toString**. Llamaremos a la nueva clase **FechaDetallada**. La clase **FechaDetallada** hereda de la clase base **Fecha** y sobreescribe el método **toString** para retornar una representación con más nivel de detalle que la que provee la implementación de su padre. Para indicar que una clase hereda de otra, se utiliza la palabra *extends*. Decimos entonces que **FechaDetallada** *extiende* a **Fecha**.  
Otras expresiones validas son:  

+ **FechaDetallada** *hereda* de **Fecha**
+ **FechaDetallada** *es una especie* de **Fecha**.
+ **FechaDetallada** *es hija* de **Fecha**.
+ **FechaDetallada** *es una subclase* de **Fecha**.
+ **FechaDetallada** *subclasea* a **Fecha**.

### Terminología clave para la comprensión de la herencia en POO

#### Superclase

Al crear una clase, en vez de declarar miembros completamente nuevos, el programador puede designar que la nueva clase herede los miembros de una existente, la cual se conoce como superclase.

#### Subclase

Es la clase nueva generada como subclase. Cada subclase puede convertirse en la superclase de futuras subclases. Una subclase puede agregar sus propios campos y métodos. Por lo tanto, una subclase es más específica que su superclase y representa un grupo más especializado de objetos. La subclase exhibe los comportamientos de su superclase y puede modificarlos, de modo que operen de forma apropiada para la sub clase.

#### Superclase directa

La superclase directa es la superclase a partir de la cual la subclase hereda de forma explícita.

#### Superclase indirecta

Una superclase indirecta es cualquier clase arriba de la superclase directa en la jerarquía de clases, que define las relaciones de herencia entre las clases. En Java, la jerarquía de clases empieza con la clase Object (en el paquete java.lang), a partir de la cual se extienden (o *heredan*) **todas** las clases en Java, ya sea de forma directa o indirecta.

#### Herencia simple

Java solo soporta la herencia simple, en la que cada clase se deriva solo de **una** superclase directa. A diferencia de C++, Java **no** soporta la herencia múltiple (que ocurre cuando una clase se deriva de más de una superclase directa).

- - -

## El constructor

El constructor de una clase es un método *especial* a través del cual se pueden crear los onjetos de la clase. Toda clase tiene, al menos, un constructor. Se puede programar explícitamente, o bien aceptar el contructor que, por defecto, Java definirá por nosotros.

El constructor se utiliza para crear los objetos de las clases. Se crea un objeto a través del constructor por default:

~~~ Java
Fecha f= new Fecha();
~~~

En esta línea de código, declaramos y creamos el objeto **f** utilizando el constructor **Fecha()**. Vemos también que el operador **new** recibe como argumento al constructor de la clase. Es decir, que el constructor de una clase es un método que se llama exactamente igual que la clase y solo puede invocarse como argumento del operador **new** al momento de crear objetos de la clase.

### Declarar y "crear" objetos

Para utilizar un objeto, no basta con declarar una variable. Además, hay que *crearlo*. En la siguiente línea, declaramos un objeto Fecha, pero no lo creamos.

~~~~ Java
// declaramos un objeto de tipo fecha

Fecha f;
~~~~

El objeto **f** que declaramos arriba no está listo para ser usado porque no fue *creado* (instanciado). Esto lo haremos a continuación:

~~~ Java
// creamos (instanciamos) el objeto f

f= new Fecha();
~~~

Las dos líneas de código anteriores podrían resumirse en una única línea en la que declaramos e instanciamos al objeto **f**:

~~~ Java
// declaramos e instanciamos el objeto f de la clase Fecha

Fecha f= new Fecha();
~~~

### Miembros protected

> El uso del acceso *protected* ofrece un nivel intermedio de acceso entre *public* y *private*. Los miembros *protected* de una superclase pueden ser utilizados por los miembros de esa superclase, por los de sus subclases y por los de otras clases en el mismo paquete; los miembros *protected* también tienen acceso a nivel de paquete. Todos los miembros *public* y *protected* de una superclase retienen su modificador de acceso original cuando se convierten en miembros de la subclase. Los miembros *private* de una superclase no pueden utilizarse fuera de la propia clase. En cambio, están ocultos en sus subclases y se pueden utilizar solo a través de los métodos *public* o *protected* heredados de la superclase.  
> *Deitel y Deitel p. 363 (2012)*.

### Métodos de Object

+ **clone**  
Este método protected, que no recibe argumentos y devuelve una referencia Object, realiza una copia del objeto en el que se llama.  
La implementación predeterminada de este método de realiza algo que se conoce como copia superficial: los valores de las variables de instancia en un objeto se copian a otro objeto del mismo tipo. Para los tipos por referencia, solo se copian las referencias. Una implementación típica del método *clone* sobrescrito sería realizar una copia en profundidad, que crea un nuevo objeto para cada variable de instancia de tipo por referencia. Es difícil implementar el método *clone* en forma correcta. Por esta razón, no se recomienda su uso. Muchos expertos de la industria sugieren que se utilice mejor la serialización de objetos.

+ **equals**  
Este método compara la igualdad entre dps pbjetos; devuelve *true* si son iguales y *false* en caso contrario. El método recibe cualquier objeto Object como argumento. Cuando debe compararse la igualdad entre objetos de una clase en particular, la clase debe sobrescribir el método *equals* para comparar el **contenido** de los objetos. La implementación *equals* predeterminada utiliza el operador **==** para determinar si dos referencias se refieren al mismo objeto en la memoria.

+ **finalize**  
El recolector de basura llama a este método *protected* para realizar las tareas de preparación para la terminación en un objeto, justo antes de que el recolector de basura reclame la memoria de este. Recuerde: no se garantiza que se ejecute el método finalize del objeto, ni cuando se ejecutará. Por esta razón, la mayoría de los programadores deberán ecitar usar el método *finalize*.

+ **getClass**  
Todo objeto en Java conoce su tipo en tiempo de ejecución. El método *getClass* devuelve un objeto de la clase Class (paquete java.lang), el cual contiene información acerca del tipo del objeto, como el nombre de su clase (devuelto por el método *getName* de Class).

+ **hashCode**  
Los códigos de hash son valores *int* útiles para almacenar y obtener información en alta velocidad y en una extructura que se conoce como tabla de hash. Este método también se llama como parte de la implementación del método toString determinado de la clase Object.

+ **wait, notify, notifyAll**  
Los métodos notify, notifyAll y las tres versiones sobrecargadas de wait están relacionados con la tecnología multihilo.

+ **toString**  
Este método devuelve una representación String de un objeto. La implementación predeterminada de este método devuelve el nombre del paquete y el nombre de la clase del objeto, seguidos por una representación hexadecimal del valor devuelto por el método hashCode del objeto.

- - -

## Definición de términos

### Excepciones

> Las excepciones son errores que pueden ocurrir durante la ejecución de un programa Java.  
> Sznajdleder (2012) p.367.

### Herencia

> La herencia permite definir clases en función de otras clases ya existentes. Diremos que la *clase derivada* o la *subclase* hereda los métodos y los atributos de la *clase base*. Esto posibilita redefinir el comportamiento de los métodos heredados o extender su funcionalidad.  
> Deitel y Deitel (2012) p.380.

### Objetos

> Los objetos son punteros. Al declarar un objeto, estamos declarando un puntero que, inicialmente, apuntará a una dirección de memoria nula (*null*). El objeto no se podrá utilizar mientras que no apunte a una dirección de memoria válida.  
> Sznajdleder (2012) p.367.

