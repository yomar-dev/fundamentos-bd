# Fundamentos de BD #

### Propósito general de las Bases de Datos ###
***

- Las **Bases de Datos** surgen de la idea de tener un espacio dónde poder almacenar de una forma mucho más eficiente toda la información de nuestros proyectos. Anteriormente este almacenamiento era en papel, y aunque a la fecha algunas empresas por temas de regulación lo siguen haciendo en parte así, el tener una **Base de Datos** ha permitido tener mucho más control de la información.

- Los **datos no son información.** Solo en el momento que creamos un reporte que contenga ciertos datos, éstos se convierten en información.

- **DBMS** = Data Base Management System o **SGBD** = Sistemas de Gestión de Bases de Datos.

<br><br>

### Visión general de los datos ###
***

**¿Qué es un dato?**

Un dato es algo que nos va a permitir describir un objeto. Ese objeto global lo vamos a poder llamar “Entidad”. Una entidad puede estar llena de datos.

Existen **3 niveles de Abstracción** en las **Bases de Datos:**

- **Conceptual:** Se tiene que empezar a modelar una Base de Datos dependiendo de lo que se quiere hacer basado en los conceptos de “entidad” y “relación”.
- **Lógico:** El diagrama lógico nos va a resolver ciertas dudas de consistencia, para evitar crear loops o evitar que tenga cosas que no tengan sentido en nuestro proyecto.
- **Físico:** Es finalmente cómo lo va a ver la Base de Datos.