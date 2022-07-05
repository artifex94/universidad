# Componentes del motor de bases de datos MySQL

## 1. Elementos de una aplicación en base de datos MySQL

### **Herramientas en el mercado**

Son muy cariadas las posibilidades de eleccipon de herramientas que permiten administrar una base de datos.

> Dentro de los tipos gestores que podemos encontrar están MySQL, que se caracteriza por su rapidez y es usado por sitis webs grandes como Facebook, Google, Wikipedia, Twitter, Youtube y Flickr. Además es uno de los más empleados junto a Microsoft SQL Server. Esta última es muy utilizada para manejar grandes volúmenes de información.
>
> 4 herramientas para administrar MySQL:
>
>   1. **MySQL Workbench:** Esta es una herramienta que ofrece modelado de datos, desarrollo de SQL y diseño, gestión, administración y mantenimiento de bases de datos. Fue fabricada por Oracle y es compatible con Windows, Linux y Mac OS.
>   2. **Navicat For MySQL:** es un administrador gráfico y un software de desarrollo creado por PremiumSoft CyberTech Ltd. Cuenta con una interfaz gráfica intuitiva y con un gran alcance para el desarrollo, mantenimiento y gestión de bases de datos. Ideal para aquellos que empiezan en MySQL. Es compatible con Windows, Linux y Mac OS
>   3. **Sequel Pro:** es una herramienta exclusiva de Mac OS, fabricada por Sequel Pro & CocoaMySQL Team. Dentro de sus características están la exploración de tablas para consultas, un panel para localizar consultas de manera rápida, permite la depuración de la información de manera cómoda y la creación y modificación de la estructura de tablas.
>   4. **Heidi SQL:** es un software libre de código abierto que permite conectarse a servidores MySQL, Microsoft SQL Server y PostgreSQL. Sólo está disponible paea Windows y fue fabricado por el alemán Ansgar Becker. Heidi permite ver y editar datos, puede exprotar estructuras y datos, además de editar triggers, vistas, procedimientos y tablas.

## 2. Herramientas a utilizar

En primer lugar, necesitaremos usar el motor de base de datos MySQL y una aplicación que permita la administración, diseño y construcción de un modelo de datos para luego crear el conjunto de tablas para consolidar lsa habilidades necesarias para construir las competencias a adquirir en esta materia. Así que, junto con el motor de base de datos, adoptaremos a **MySQL Workbench**.

El motor ya trae un conjunto de tablas a los que se denomina genéricamente "esquema" (*schema* en inglés); se llama "sakila" y ya contiene tablas que nos permitirán aplicar las utilidades de **MySQL Workbench**. Si este esquema no estuviera creado, se pueden obtener los scripts y las instrucciones para crearlo [aquí](https://dev.mysql.com/doc/sakila/en/sakila-installation.html).

Con esta herramienta nos conectaremos y crearemos un usuario BD1 con la contraseña "Siglo21!" respetando mayúsculas y signos de puntuación para que la revición de contraseña determine que es de una complejidad aceptable para lograr un grado razonable de seguridad. También puedes elegir el usuario a gusto. Finalmente le agregas el esquema "sakila" al usuario para que puedas consultar las tablas del mismo.