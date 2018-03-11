# Fundamentos de BD #

### Propósito general de las Bases de Datos ###
***

- Las **Bases de Datos** surgen de la idea de tener un espacio dónde poder almacenar de una forma mucho más eficiente toda la información de nuestros proyectos. Anteriormente este almacenamiento era en papel, y aunque a la fecha algunas empresas por temas de regulación lo siguen haciendo en parte así, el tener una **Base de Datos** ha permitido tener mucho más control de la información.

- Los **datos no son información.** Solo en el momento que creamos un reporte que contenga ciertos datos, éstos se convierten en información.

- **DBMS** = Data Base Management System o **SGBD** = Sistemas de Gestión de Bases de Datos.


<br>

### Tipos de Bases de Datos y sus aplicaciones en la industria ###
***

Las **Bases de Datos** se pueden dividir en:

- **Bases de Datos Relacionales**
- **Bases de Datos no Relacionales**


**Bases de Datos Relacionales** empresariales (más importantes):

- **DB2**
- **SQL Server**
- **Oracle**


Algunas **Bases de Datos Relacionales** comunes:

- **MariaDB:** Es una distribución de Bases de Datos que deriva de MySQL.
- **PostrgreSQL:** Esta es una Base de Datos comunitaria pero tiene una versión entreprise que tiene soporte.


Algunas **Bases de Datos No Relacionales** comunes:

- **Redis:** Una Base de Datos que en la actualidad se trabaja mucho.
- **neo4j:** Es una Base de Datos basada en nodos. Está centrada en grafos que nos va a permitir encontrar relaciones entre objetos. Muy común en eCommerce.
- **Cassandra:** Es una Base de Datos muy importante del proyecto Apache. Trabaja con grandes volúmenes de datos.
- **MongoDB:** Es una Base de Datos en NoSQL que se basa en trabajar en varias instancias.


<br>

### Visión general de los datos ###
***

**¿Qué es un dato?**

Un dato es algo que nos va a permitir describir un objeto. Ese objeto global lo vamos a poder llamar “Entidad”. Una entidad puede estar llena de datos.

Existen **3 niveles de Abstracción** en las **Bases de Datos:**

- **Conceptual:** Se tiene que empezar a modelar una Base de Datos dependiendo de lo que se quiere hacer basado en los conceptos de “entidad” y “relación”.
- **Lógico:** El diagrama lógico nos va a resolver ciertas dudas de consistencia, para evitar crear loops o evitar que tenga cosas que no tengan sentido en nuestro proyecto.
- **Físico:** Es finalmente cómo lo va a ver la Base de Datos.


<br>

### Tipos de Datos ###
***

Igual que en cualquier lenguaje de programación, existen **variables** en las **Bases de Datos:**

- **Caracteres:** Pueden ser desde letras hasta caracteres especiales.
- **Numérico:** Del 0 al 9 pero con una longitud especial.
- **Varchar:** Caracteres con un formato más variable.
- **Imagen**
- **Fecha:** Generalmente van acompañadas de una hora.
- **Moneda:** esto facilita todo si se trabaja con diferentes denominaciones.
- **Texto:** Variables que tienen mayor tamaño que un char o que un varchar.
- **Bit:** Se puede trabajar con 1 y 0 o también con verdadero y falso.
- **Decimal**

**Esquema =** Es la estructura lógica que va a tener una Base de Datos. <br>
**Instancia =** Contenido de partículas que tiene una Base de Datos en un instante de tiempo.

¿Qué debemos esperar para modelar una **Base de Datos**?

- Los datos.
- La relación que existe entre los datos.
- Restricciones de los datos.

Existen 3 cosas para poder hacer la descripción de una **Base de Datos:**

- **DML =** Data Manipulation Language o Lenguaje de Manipulación de Datos.
- **DDL =** Data Definition Language o Lenguaje de Definición de Datos.
- **SQL =** Structured Query Language o Lenguaje de Consulta Estructurada.

**Otros tipos de Bases de Datos:**

- Bases de Datos Relacionales
- Basadas en Objetos Relacionales
- XML
- NoSQL
- In-Memory


<br>

### Diferentes tipos de Bases de Datos ###
***

**Características de Bases de Datos SQL:**

- Es un lenguaje estructurado.
- Tiene un esquema de tablas.
- Tiene integración con otros tipos de archivos.
- Tiene indexación por medio de árboles.

**Características de Bases de Datos NoSQL:**

- Se puede trabajar con un lenguaje estructurado o con uno no estructurado.
- Tiene diferente tipo de indexación. Se utiliza normalmente Json.
- Tiene un crecimiento horizontal.

**Características de Bases de Datos Analíticas y de Bigdata:**

- Son de lenguaje no estructurado.
- Tiene integración de muchos sistemas.
- Tiene integración también a sistemas tradicionales y sistemas de engagement.
- Principio “divide y vencerás”
- Se basa en esquemas Scale Out.
- Crecimiento horizontal.

**Características de Bases de Datos basadas en aceleración:**

- Normalmente basadas in Memory.
- Uso de aceleradores como GPU, flash cards, FPGAs.
- Tienen estructuras diferentes, por ejemplo, basadas en nodos.
- Uso frecuente de ambientes empresariales productivos y de datawarehouse.


<br>

### ¿Qué es una Entidad? ###
***

**Entidad =** Es una abstracción del mundo real.

**Barker =** Aquí una entidad se representa como una caja, es una caja que va a tener atributos. Estos atributos van a poder ser obligatorios u opcionales.

**Recomendación:**<br>
El formato para trabajar con los ID debe ser “number”. No siempre va a poder ser así, pero es lo más recomendable.


<br>

### ¿Qué es una Relación? ###
***

Para definir una **Relación** tenemos que tener en cuenta los siguientes puntos:

**La obligatoriedad:** Ésta se denota con una línea continua.

**Opcional:** Se representa con una línea punteada.

**Datos importantes:** <br>
El símbolo con el que representamos la característica “de uno a muchos” es con la llamada pata de gallo, que gráficamente es una línea continua con dos líneas en 45 grados en cada lado.

<br>

### Tener en cuenta ###
***

- Las llaves primarias obligatoriamente van a ser índices.
- Las Bases de Datos indexan con un algoritmo llamado: **Árboles B+**
- Los **Árboles B+** son una estructura que va a tener un tronco, tres raíces, de las cuales se van a ir derivando tres raíces más por cada una, hasta donde sea necesario.
- Por defecto todas las Bases de Datos están indexadas, así no le pongamos índices. Lo que sucede es que la Base de Datos siempre obliga a indexar porque siempre tienen un atributo que está oculto, este atributo es RowID.

<br>

### Constrains o Restricciones ###
***

- Las restricciones se pueden trabajar desde la Base de Datos. Normalmente las validaciones con restricciones se hacen desde la aplicación, pero es importante tener en cuenta que podemos hacerlo de igual forma desde la Base de Datos.
- Las llaves primarias y las llaves foraneas no solamente tienen la restricción **_Not null_**, sino que además tienen la restricción **_unique_**, no puede haber otra igual.
- Con **_check_**, las validaciones que podemos hacer son: Igual, mayor o igual, menor o igual, mayor qué o menor qué.

<br>


### Notas ###
***

**Entidad Fuerte:** La constituyen las tablas principales de la BD, que contienen los registros principales del sistema de información y que requieren de entidades o tablasauxiliares para completar su descripción o información.

**Entidad Debil:** Tablas auxiliares de una tabla principal a la que completan o complementan con la información de sus registros relacionados.


<br><br><br>
### Enlaces de interes ###

[SQL-92](https://es.wikipedia.org/wiki/SQL-92) <br>
[Barkers Notation](http://www.vertabelo.com/blog/technical-articles/barkers-erd-notation)