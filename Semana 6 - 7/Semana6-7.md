# Semana 6 - 7: Base de datos - MySQL

Para estas dos semanas emplearemos MySQL como lenguaje para conocer e interactuar con bases de datos. En este módulo asumimos que ya tienes instalado MySQL y Workbench (IDE por defecto de MySQL).

- [Instalación MAC](./mac.md)
- [Instalación Linux](https://www.youtube.com/watch?v=KM2y_BeDxGg)
- [Instalación Windows](https://youtu.be/hUZKNsnHe_A)


### Conceptos teóricos
- ¿Qué es una base de datos?: Una base de datos es una recopilación organizada de información o datos estructurados, que normalmente se almacena de forma electrónica en un sistema informático. Normalmente, una base de datos está controlada por un sistema de gestión de bases de datos (DBMS). [Mas Info](https://www.oracle.com/mx/database/what-is-database/)

![Server Photo](https://images.pexels.com/photos/1148820/pexels-photo-1148820.jpeg?auto=compress&cs=tinysrgb&dpr=3&h=750&w=1260)

- ¿Qué es SQL?: SQL es un lenguaje de programación que utilizan casi todas las bases de datos relacionales para consultar, manipular y definir los datos, además de para proporcionar control de acceso. El SQL se desarrolló por primera vez en IBM en la década de 1970 con Oracle como uno de los principales contribuyentes, lo que dio lugar a la implementación del estándar ANSI SQL. El SQL ha propiciado muchas ampliaciones de empresas como IBM, Oracle y Microsoft. Aunque el SQL se sigue utilizando mucho hoy en día, están empezando a aparecer nuevos lenguajes de programación. [Mas Info](https://www.oracle.com/mx/database/what-is-database/)

### Manual Básico SQL:
Para trabajar con SQL tenemos dos opciones. La primera con un IDE ya sea WorkBench el que viene por defecto en MySQL hasta los más usados como Visual Studio Code. La segunda es la terminal con MySQL. Ambas maneras son válidas, pero en nuestro caso combinaremos Workbench y la terminal.

1. Creamos la base de datos:
``` 
CREATE DATABASE Ejercicio;
``` 
2. Indicarle que base de datos vamos a usar:
``` 
USE Ejercicio;
``` 
3. Creamos la tabla e indicamos los [tipos de datos](https://disenowebakus.net/tipos-de-datos-mysql.php):
``` 
CREATE TABLE Escala (
    id_escala INT NOT NULL,
    nombre varchar(1) NOT NULL,
    costo INT NOT NULL,
    beca varchar(2) NOT NULL
);
``` 
4. Insertamos datos a la tabla:
``` 
INSERT INTO Escala (id_escala, nombre, costo, beca)
VALUES
    (1, 'A', 2000, 'NO'),
    (2, 'B', 1500, 'NO'),
    (3, 'C', 1000, 'NO'),
    (4,  'D', 500, 'SI');
```
5. Consultar TODOS los datos en una tabla:
``` 
select*from Escala;
``` 
![Tabla Escala](https://i.ibb.co/7v0V8FK/Screen-Shot-2022-05-12-at-2-24-54-PM.png)

6. Ahora es turno y crea tres tablas: Alumnos, CursoMat y Cursos
7. Cómo consultar datos de varias tablas:
``` 
select*from Alumnos, CursosMat, Cursos;
``` 
![Tabla Escala](https://i.ibb.co/gdZLzfh/Screen-Shot-2022-05-12-at-2-27-21-PM.png)
8. Consultar datos específicos:
```
select nombre, costo from Escala;
```