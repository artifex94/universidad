# El lenguaje SQL

El lenguaje SQL es un lenguaje diseñado para la comunicación entre usuarios y la base de datos. Su finalidad es la de realizar todas las tareas requeridas en función de resolver los requerimientos sobre cómo obtener información almacenada, realizar cálculos, modificar lo existente y agregar nuevas filas que contengan información de clientes, productos, transacciones, puesto que la mayoría de las aplicaciones actuales usan bases de datos relacionales y, por ende, SQL.

> La característica más destacada del lenguaje SQL es que es no procedimental, es decir, no se indica en sus sentencias cómo realizar la tarea, sino que se limita a describir el resultado buscado y queda todo el trabajo de resolver sol solicitado al servidor de bases de datos que, se acuerdo con su optimizador y con los metadatos (se denomina así porque son datos acerca de datos) del diccionario, cumplirá con la sentencia SQL provista.
>
> Por lo antedicho, SQL no tiene sentencias de control de flujo desde su origen, aunque recientemente, se han incluido como partes opcionales aceptadas del estándar de SQL, ISO/IEC 9075-5: 1996 que pueden realizar algún control de ejecución.<br> - Reinosa, Maldonado, Muñoz, Damiano, Abrutsky, (2012).

Es común que las sentencias de control de flujo mencionadas anteriormente (conocidas como módulos persistentes almacenados) se consideren como extensiones procedimentales del lenguaje. Los proveedores de bases de datos tienen estas extensiones (por ejemplo: PL/SQL de Oracle, T-SQL de SQL Server de Microsoft, SQL-PL de DB2 de IBM y PSQL de PostgreSQL). En general, estas extensiones complementan a SQL para construir procedimientos almacenados, paquetes y disparadores.

## Características del lenguaje SQL

SQL es un lengiaje diseñado específicamente para la cominicación con bases de datos. Al contrario de otros lenguajes como el inglés, o de programaciones como Java o Visual Basic, SQL se basa en muy pocas palabras. Esto es deliberado, ya que SQL está diseñado para hacer una cosa y hacerla bien, proveer un modo simple y eficiente para leer y escribir datos en una base de datos relacional.

## ¿Cuáles son las ventajas de SQL?

A modo de síntesis queremos destacar por qué es bueno este lenguaje:

+ SQL no es un lenguaje propiedad de un proveedor de base de datos.
+ La mayoría de los sistemas de administración de base de datos usa SQL, por lo que aprender este lenguaje permite interactuar con todas las bases de datos con las que tengamos contacto.
+ SQL es fácil de aprender, está construido con unas pocas palabras habituales del inglés.
+ Aunque su apariencia es simple, SQL es un lenguaje poderoso, e inteligentemente usado puede ejecutar operaciones de base de datos sofisticadas y complejas.

Las fortalezas de SQL ofrecen beneficios a todo tipo de usuarios como los programadores de aplicación, administradores de bases de datos, gerentes y usuarios finales. Técnicamente hablando, SQL es un sublenguaje de datos. Su propósito es ser una interfazcon una base de datos, y todas sus sentencias son instrucciones para la base de datos. Difiere, entonces, de los lenguajes de programación de propósito general como COBOL, C, Basic.

Entre otras características del SQL encontramos las siguientes:

+ Procesa los datos como grupos y no como unidades individuales.
+ Provee navegación automática a los datos.
+ Sus sentencias son complejas y poderosas individualmente.
+ SQL no tiene sentencias de control de flujo desde su origen, aunque recientemente se han visto incluidas como partes opcionales aceptadas del estándar de SQL.

Para profundizar en el uso de SQL, es importante mencionar que es necesario ocuparse de los detalles de implementación cuando se pretende manipular los datos. Por ejemplo para recuperar un conjunto limitado de filas de una tabla, se define una condición usada para filtrar las filas, y todas las filas qque la cumplan serán recuperadas en un solo paso como una unidad para el usuario a otra sentencia SQL o a una aplicación. No es necesario tratar a las filas una a una ni nos tenemos que ocupar de cómo están almacenados físicamente o como son recuperadas.

Todas las sentencias SQL usan el optimizador, que es el componente de programación que determina los medios más eficientes de acceso a los datos especificados. En general, los motores tienen técnicas quue se pueden aplicar para que este optimizador realice la tarea mejor, es decir, en el menor tiempo de ejecución posible.

SQL provee sentencias para una variedad de tareas, incluye:

+ Consultas de datos;
+ inserción, actualización y borrado de filas en una tabla;
+ creación, reemplazo, alteración y eliminación de objetos;
+ control de acceso a la base de datos y a sus objetos;
+ garantizar la consistencia e integridad de la base de datos.

En SQL se unen todas las tareas anteriores en un lenguaje consistente por ser un lenguaje común para todas las bases de datos relacionales.

Tpdps los sistemas de administración de bases de datos relacionales soportan SQL, así se puede transferir todas las habilidades adquiridas en SQL de una base de datos a otra. Además, las consultas escritas en SQL son portables en su gran mayoría y a veces movidas de una base a otra con muy pequeñaz modificaciones.

## SQL empotrado o embebido

SQL empotrado está referido al uso de las sentencias estándares SQL insertadas en un lenguaje de programación procedimental. Las sentencias posibles de incorporar las sentencias SQL son todas las sentencias SQL incluidas SELECT e INSERT y las sentencias dinámicas SQL, tales como PREPARE y OPEN, que integran al lenguaje estándar de SQL dentro de un lenguaje de programación procedimental.

Una vez incluidas las sentencias SQL, un programa llamado precompilador las traduce en sentencias del lenguaje anfintrión, el cual permite ser compilado normalmente por el compilador del lenguaje elegido.

## SQL sublenguaje de manejo de datos o DML

Para estudiar SQL es necesaria esa división del lenguaje en los sublenguajes; es momento de analizar el DML o *Data Management Language*, es decir, el lenguaje de manejo de datos en donde se encuentra clasificada la sentencia más usada del lenguaje, el SELECT.

## Sentencias de DML

El lenguaje DML (*Data Manipulation Language*) contiene sentencias para la administración de los datos. Este "sublenguaje" abarca a SELECTINSERT, DELETE y UPDATE, que sirven respectivamente para realizar consultas, insertar filas o borrarlas, para cambiar el contenido de las columnas en las filas existentes y que cumplan con las condiciones de la cláusula WHERE.

### SELECT

SELECT es la sentencia que permite la obtención de los valores almacenados en las columnas de las filas recuperadas, como resultado del acceso a las tablas o a las vistas de la base de datos. A esta sentencia también se la denomina "Consulta", porque es, justamente, lo que hace el motor: busca las filas de las tablas incluidas en su cláusula FROM y realiza las operaciones definidas en el álgebra relacional para seleccionar aquellas filas que cumplan las condiciones expresadas.

Esta sentencia se estructura en distintas cláusulas. Su funcionamiento que se describirá a continuación.

~~~~ SQL
SELECT      <lista de columnas, valoresconstantes, funciones, subconsultas, etc.>
FROM        <lista de tablas, vistas, subconsultas>
WHERE       <condicion> [AND, OR, NOT]  <condicion>
GROUP BY    <lista de columnas>
HAVING      <condicion> [AND, OR, NOT]  <condicion>
ORDER BY    <lista de columnas, numero de orden o alias de columna> [DESC, ASC]
~~~~

Las cláusulas obligatorias en el SQL de Oracle son SELECT y FROM, pero en otras bases como MySQL solo es obligatoria la cláusula SELECT. En esta cláusula, se puede realizar la operación Proyección del álgebra relacional cuando se enumeran solo algunas columnas de la tabla que se consultará. Como alternativa a esta operación, es decir, incluir a varias, se las escribe una por una, o si requerimos todas las columnas, se usará el operador *asterisco* (*) para la recuperación de todas las columnas de la o las tabla/s del FROM.

En la primera cláusula ("SELECT"), se nombran las columnas, funciones o literales que se pueden combinar, las columnas corresponderán a las tablas, las vistas o las subsonsultas de la clausula FROM, además, podremos incluir funciones, y también podemos escribir en la lista que sigue a la cláusula SELECT subconsultas que deben llevar un sinónimo de columna luego de la palabra "AS". Las subconsultas que se usan en el SELECT deben devolver un solo valor por fila, por lo que se las denomina "escalares". También se puede incluir en esta cláusula SELECT valores literales que se repetirán por cada fila mostrada. Por ejemplo: la siguiente sentencia muestra datos constantes, una columna con el nombre de los empleados, luego el sueldo y, en la columna aumento, el cálculo de sueldo con un 20% de aumento. Es para destacar que en los dos últimos se adoptó un "Alias de Columna" para titular las columnas con un nombre distinto al de las columnas de la tabla.

~~~ SQL
SELECT "El nombre es:",
    ename,
    salario AS salarioAnterior,
    salario*1.20 AS aumento
FROM    empleados;
~~~

La ejecución de la consulta vista resulta en una tabla temporaria con los siguientes nombres de columnas y sus valores:

"El nombre es" | ename | salarioAnterior | aumento
---------     |---------|-------|---------
 El nombre es | Pérez   | 1100  | 1200
 El nombre es | López   | 900   | 1080
 El nombre es | Suárez  | 1100  | 1320
 El nombre es | Gianni  | 700   | 840
 El nombre es | Vinci   | 1500  | 1800

## Funciones de fila simple

En el ejemplo anterior se vio el uso de la función numéroca de fila simple, el símbolo asterisco "*". En este caso, "*" representa a la operación multiplicación que, en otro contexto, significa "todas las columnas de las tablas que figuran en el FROM". Las funciones de fila simple retornan un solo valor por cada fila de una tabla o de una vista consultada. Estas funciones pueden esarse en la lista de columnas del SELECT, en las cláusulas WHERE y HAVING, que forman parte de las condiciones y demás.

## Funciones numéricas

La mayoría de las funciones numéricas, que reciben y devuelven valores numéricos, retornan valores NUMBER con exactitud en 38 dígitos decimales.

Las más simples son los operadores matemáticos *por* (*), *dividido* (/), *mas* (+), *menos* (-).

## Funciones caracter

Las funciones de caracter son aquellas que reciben argumentos numéricos, de fecha o de caracteres y devuelven valores en formato caracter. Estos son:

+ **CHR**       Devuelve un caracter de acuerdo con un argumento numérico, normalmente el valor ASCII.
+ **CONCAT**    Concatena valores.
+ **INITCAP**   Pone mayúscula a las primeras letras de cada palabra.
+ **LOWER**     Transforma en minúsculas.
+ **LPAD**      Completa a la izquierda con un caracter hasta una cantidad de caracteres.
+ **LTRIM**     Recorta una cantidad de caracteres a la izquierda.
+ **REPLACE**   Reemplaza un caracter por otro.
+ **RPAD**      Completa a la derecha con un caracter hasta una cantidad de caracteres.
+ **RTRIM**     Recorta una cantidad de caracteres a la derecha.
+ **SUBSTR**    Toma una subcadena de una cantidad de caracteres desde una posición determinada.
+ **UPPER**     Transforma en maypusculas.

## Funciones generales de comparación

Las funciones generales de comparacipon determinan los valores mayores o mejores de un conjunto de datos:

+ **GRATEST**   Mayor
+ **LEAST**     Menor

## Funciones de grupo

Las funciones de grupo devuelven una fila con el resultado de sumar, contar, etc., de todas las filas resultantes de la consulta. En la cláusula WHERE de la consulta, no se pueden usar las funciones de grupo para filtrar filas porque el resultado de una función de grupo se conoce luego de reunir todas las filas, es decir, luego de ejecutar el WHERE. Por eso las funciones de grupo se usan en la cláusula HAVING.

Las funciones de grupo son usadas comúnmente en combinación con la cláusula GROUP BY con la que se divide a las filas seleccionadas, poruqe complen con las condiciones de filtro del WHERE, en grupos basados en los distintos valores de las columnas incluidas en el GROUP BY.

Vemos las filas de la tabla Estudiantes para entender cómo usar las funciones de grupos:

Legajo | Apellido | Carrera
-------|----------|---------
 7898 | Messi   | SIS
 6677 | García  | SIS
 6644 | Bremen  | SOF
 3566 | Pérez   | ABO
 5522 | Palermo | SOF
 2123 | López   | ABO
 5221 | Vianni  | ABO
 4512 | Suárez  | SOF

GROUP BY "columna" separa las filas del conjunto en grupos de filas que tienen el mismo valor en la columna elegida.

Ahora vemos las filas de la tabla Estudiantes para entender cómo ordena el GROUP BY por la columna que se agrega en la sentencia, en este caso "Carrera".

Legajo | Apellido | Carrera
-------|----------|---------
 7898 | Messi   | SIS
 6677 | García  | SIS
 6644 | Bremen  | SOF
 4512 | Suárez  | SOF
 5522 | Palermo | SOF
 2123 | López   | ABO
 5221 | Vianni  | ABO
 3566 | Pérez   | ABO

La consulta:

~~~ SQL
SELECT carrera, count(*)
FROM estudiantes
GROUP BY carrera
~~~

nos dá como resultado:

Carrera | COUNT(*)
--------|---------
 ABO    | 3
 SIS    | 2
 SOF    | 3

En el ejemplo, se aplicó la función COUNT(*) que cuenta las filas seleccionadas y filtradas por la consulta y muestra el resultado del conteo.

Si se usa una función de grupo sin la cláusula GROUP BY, éstas se aplicarán a todo el conjunto de filas seleccionadas. Se usan las funciones de grupo también en la cláusula HAVING para filtrar los grupos que no cimplen con las condiciones.

La cláusula WHERE filtra grupos antes de que se armen los grupos, y HAVING filtra filas una vez que los grupos están armados.

Todas las funciones de grupo ignoran los valores nulls; esto es, si en una columna "Apellido" se va a contar con COUNT(Apellido) y tiene en todas las filas valores null, esta función devolverá 0 (cero), si solo en algunas tuviera nulls, contará todas las filas con valores distintos de null.

El asterisco en COUNT(*) le indica a la función que cuente todas las filas de la/s tabla/s que están en el FROM. Según la definición de una tabla relacional, esta no puede tener una fila con todos valores null o fila nula.

Algunas de las funciones de grupo más usadas son:

+ **AVG**   Average o promedio
+ **COUNT** Conteo
+ **MAX**   Máximo
+ **MIN**   Mínimo
+ **SUM**   Suma

Se agregan otras funciones de grupo no menos importantes y menos usadas:

+ **STDDEV**    Desviación estándar
+ **VARIANCE**  Varianza

## La cláusula FROM

En la cláusila FROM, se enumeran las tablas, las vistas y las subconsultas que se harán para buscar las columnas que se enumeran en el SELECT. Cuando hay más de una referencia a tablas, se dice que la consulta es MULTITABLA. En este caso, se está frente a la aplicación de la operación reunión (JOIN) del álgebra relacional, y si no se escriben las condiciones de reunión en el WHERE, el optimizador de consultas realizará un producto cartesiano que relacionará todas las filas de las tablas reunidas, lo que generará resultados falsos: si se tuvieran cinco alumnos y tres examenes rendidos, la reunión sin "condiciones de reunión" daría quince filas (5x3 filas). Esto produce un gran volumen de filas reunidas que habitualmente no se utilizarán.

Para algunos casos, esta operación será necesaria, por ejemplo, cuando se requiera relacionar todos los jugadores de un torneo de tenis para armar los partidos posibles, teniendo en cuenta que se eliminarán los pares en los que se repiten los mismos jugadores. ¿Cómo sería esto? Supongamos que hay catorce empleados y se quiere tener previstos todos los partidos posibles (los imposibles serían que un empleado jugara contra si mismo), para esto se puede hacer el producto cartesiano de la tabla "Empleados" consigo mismo con distinto alias de tablas, para identificar a qué rol corresponde.

En el primer intento, dejará un producto cartesiano de la tabla "Empleados" consigo mismo. Esta forma de reunión se denomia también *Auto Join*.

~~~ SQL
SELECT l.ename Local,
    "juega con",
    v.ename Visita
FROM empleados l, empleados v
~~~

Si esta tabla tiene 14 filas, da un resultado de 196 filas.

El producto cartesiano ha combinado todas las filas de la primera tabla con la segunda, con un resultado que tiene algunos inconvenientes como el número de filas resiltantes y que algunas son imposibles de aplicar o que no son de información útil.

En la siguiente consulta, se resolverá el requerimiento que armará los partidos de tenis en el campeonato interno de la empresa.

~~~ SQL
SELECT l.ename Local,
    "juega con",
    v.ename Visita
FROM    EMPLEADOS l,
    empleados v
WHERE l.ename <> v.ename;
~~~

El ejemplo anterior muestra un uso muy común de Auto Join al agregar la cláusula WHERE con una condición que evita el producto cartesiano y también evita una fila que diga "ALLEN juega con ALLEN", es decir, un partido imposible.

Es importante destacar que hemos usado alias de tablas para identificar las columnas "ename", que, al venir de la misma tabla pero repetida en el FROM, hemos tenido que calificarla con la letra que escribimos a continuación de la tabla en esta 