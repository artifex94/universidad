# Motores de base de datos relacionales

> Una base de datos es un conjunto de datos estructurados y definidos a través de un proceso específico, que busca evitar la redundancia, y que se almacenará en algún medio de almacenamiento masivo, como un disco.
> \-
>Reinosa, Maldonado, Muñoz, & Abrutsky, (2012)

### Tecnologías utilizadas: 
* **Oracle:** ámbito empresarial.
* **MySQL:** ámbito de las aplicaciones web.
* **SQLite:** ámbito de las aplicaciones en celulares.

## 1. Base de datos Oracle

Punto de entrada en la tecnología RBMS para contener la información que requieren los sistemas actuales de gestión empresarial. Al decir que es un punto de entrada decimos que puede configurarse en un equipo de escritorio con los recursos minimos de memoria y espacio de disco, para poder desarrollar aplicaciones que accedan a la base de datos sin necesidad de un servidor empresarial de gran porte. Las bases de datos Oracle soportan aplicaciones de todos los niveles de requerimientos, desde un uso personal hasta instalaciones de empresas de gran porte. La presentación de esta edición puede encontrarse en la página de Oracle y nos dice que

> Oracle Database 18c XS es una edición gratuita y respaldada por la comunidadLos límites de CPU, memoria y disco son: 2 CPU, 2 GB de RAM y hasta 12 GB de datos de usuario. Soporta bases de datos conectables, almacenamiento de columnas en memoria, compresión, soporte espacial y gráfico, cifrado y redacción, particiones, vistas analíticas y más.

## 2. Base de datos MySQL

Tiene su origen en el ámbito del software libre y creció en popularidad como sostén de sitios web cuando estos recién empezaban a necesitar más que texto y gráficos estáticos. Su pequeño tamaño e instalación sencilla lo hizo estándar de facto de la industria, lo adoptaron todos los sitios que buscaban rapidez y economía, ya que su licencia es gratuita -con la condición de que el sitio y la aplicación también lo sean y que la aplicación se publique como abierta con sus fuentes-. Ahora bien, si el uso de la aplicación es comercial debe adoptar una licencia paga para poder usarlo. Esta flexibilidad, de no pafar mientras se inicia el negocio, permitió a los sitios probar y luego -si es exitoso y genera ingresos con el uso de la base- poder aplicar a una licencia con costo, con el agregado extra de un soporte para atender problemas y realizar optimizaciones con el respaldo de los xpertos desarrolladores.

> MySQL es un sistema de festión de bases de datos relacional desarrollado bajo licencia dial: Licencia pública general/Licencia comercial por Oracle Corporacion y estpa considerada como lapbase de datos de código abierto más popular del mundo, y una de las más populares en general junto a Oracle y Micreosoft SQL Server, todo para entornos de desarrollo web.
>
> MySQL fue inicialmente desarrollado por MySQL AB. MySQL AB fue adquirida por Sun Mycrosystems en 2008, y ésta a su vez fue comprada por Oracle Corporation en 2010, la cual ya era dueña desde 2005 de Innobasee Oy, empresa finlandesa desarrolladora del motor InnoDB para MySQL.
>
> Al contrario de prouectos como Apache, donde el software es desarrollado por una comunidad pública y los derechos de autor del código estpan en poder del autor individual, MySQL es patrocidado por una empresa privadaque posee el copyright de la mayor parte del código. Esto es lo que posibilita el esquema de doble licenciamiento anteriormente mencionado. La base de datos se distribuye en varias versiones, una Community, distribuidora bajo la Licencia pública general de GNU, versión 2, y varias cersiones Enterprise, para aquellas empresas qye quieran incorporarlo en productos privativos. Las versiones Enterprise incluyeb productos o servicios adicionales tales como herramientas de monitorización y asistencia técnica oficial.
>
> ... Está desarrollado en su mayor parte en ANSI C y C++. Traducuibaknebte se considera uno de los cuatro componentes de la pila de desarrollo LAMP y WAMP.
>
> MySQL es usado por muchos sitios web grandes y populares, como Wikipedia, Google, Facebook, Twitter, Flickr y Youtube.

## 3. Base de datos con SQLite

SQLite es una opción muy válida para iniciarse rápidamente o para pequeñas aplicaciones con posibilidad de ser corridas en Linux, Windows y Android, por ka sencillez de instalación y funcionamiento. Este *software* tiene la posibilidad real de ffuncionar en un dispositivo Android e intercambiar el archivo de base de datos entre la esta terminal y un servidor central para comunicar las transacciones entre ellos.

> SQLite es un sistema de gestión de bases de datos relacional compatible con ACID, contenida en una relaticamente pequeña (~275 kiB) biblioteca escrita en C. SQLite es un proyecto de dominio público creado por D. Richard Hipp.
>
> A diferencia de los sistemas de gestión de bases de datos cliente-servidor, el motor de SQLite no es un proceso independiente con el que el programa principal se comunica. En ligar de eso, la biblioteca SQLite se enlaza con el programa pasando a ser parte integral del mismo. El programa utiliza la funcionalidad de SQLite a través de llamadas simples a subrutinas y funciones. Esto reduce la latencia en el acceso a la base de datos, debido a que las llamadas a funciones son más eficientes que la comunicación entre procesos. El conjunto de la base de datos (definiciones, tablas, índices, y los proíos datos) son guardados como un solo fichero estándar en la máquina host. Este diseño simple se logra bloqueando todo el fichero de base de datos al principio de cada transacción.
>
> En su versión 3, SQLite permite bases de datos de hasta 2 Terabytes de tamaño, y también permite la inclusión de campos tipo BLOB.