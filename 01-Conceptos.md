# Diseño de bases de datos

## Datos

- Un dato es una unidad singular de conocimiento
- Es la mínima unidad de información
- Por si solo no tiene un valor intrinseco pero tiene un significado en cierto contexto

---

## Información

- Nos permite vincular los datos para darle un significado
- Conjunto de datos que nos genera conocimiento, resuelve necesidades o problemas

---

## SGBD / DBMS (Sistema gestor de bases de datos)

Un Sistema gestor de bases de datos es una coleccion de información cuidadosamente organizada en un sistema
Software que nos permite encapsular datos y proporciona una manera de almacenarlos, recuperarlos, ediartlos, eliminarlos

MySQL, SQLServer, MongoDB son Sistemas gestores de bases de datos, no bases de datos.

Ventajas:

- Están optimizados para almacenar y manipular grandes datos
- Mayor seguridad
- Adminstración eficiente de la información
- Varios usuarios pueden acceder de manera concurrente
- Garantizan la integridad de los datos

---

## Tipos de bases de datos

Estos SGBD se agrupan en 2 grandes grupos:

- Relacionales (SQL)
- No relaciones (No SQL)

### Relacionales

Se caracterizan por ser una colección ordenada de registros organizadas en tablas, las tablas son sus elementos principales, los datos se organizan en filas y columnas, se relacionan entre sí y usan el lenguaje SQL, con este lenguaje se pueden obtener y usar los datos de manera organizado teniendo en cuenta la estructura de la base de datos con diferentes comandos

Las tablas también se organizan con identificadores, siempre tendrán un campo único, de este modo se pueden establecer la relación con otras tablas, con esto es más facil organizar la información en las tablas

Ejemplos: Mysql, MariaDB, PostgreSQL

### No relacionales

Están diseñadas para modelar datos con estructuras más especificas y que no necesite relacionar datos unos con otros, son más sencillas que las relacionales, esta sencillez nos permite acceder a los datos de manera rápida, se mejora el rendimiento y el acceso sobre la seguridad e integridad de datos para pdoer procesar la mayor cantidad de datos en el menor tiempo posible.
Estos datos se guardan en un objeto de tipo llave, valor en documentos.

Ejemplos: MongoDB, Apache Cassandra, FireBase

![Tipos de bases de datos](/assets/Tipo-de-bases-de-datos.png)

Una aplicación de tipo contable, inventario de productos, clientes, es mejor el modelo relacional, habrá multiples tablas que se comuniquen entre si

Si nuestra aplicación necesita de un sistema de datos que no se relacionen entre si y que no tengan la misma estructura entonces deberemos de usar una base de datos no relacional, como una aplicación de estadisticas de un usuario, una galería de fotos en Fb, etc.

Una elección de un SGBD erroneo nos puede traer muchos problemas, primero necesitamos hacer un analisis sobre que tipo de base de datos utilizaremos.

---

## Entidades y Atributos

### Entidad

Objeto del mundo real que pretendemos controlar dentro del sistema de información, una persona, un producto, una cuenta, un producto, una factura, es el objeto del cual vamos a almacenar información, tienen caracterisiticas que las describen, estos son llamados atributos de la entidad
Lo primero que tenemos que hacer al diseñar una Base de datos es hacer un listado de las entidades que se verán involucradas en el sistema y por consiguiente sus atributos

#### Tipos de entidades

De datos

- Las entidades de datos son aquellas que alimentan el sistema de información. En ellas se almacenan y se interactúa con los datos.

Catálogos

- Los catálogos son entidades que sus registros son una lista o relación ordenada con algún criterio y por tal motivo su información debe estar precargada en el sistema, antes de comenzar a introducir información en el. Por ejemplo: una lista de códigos postales, colonias, municipios, cuidades o países son un buen ejemplo de entidades cátalogo.

Pivotes

- Las entidades pivotes son las que relacionan la información de 2 o más entidades. Nos ayudan a mantener consistencia e integridad en el sistema y evitan la duplicidad de datos. También suelen llamarse entidades de enlace o asociación.

  Por ejemplo en el proceso de una venta, una entidad pivote puede almacenar la relación de qué y cuántos productos se adquirieron en dicha venta, además de relacionar dichos productos con la información del cliente que los compró.

### Atributos

Los atributos son las caracteristicas de las entidades. En las bases de datos existen varios tipos de datos que se pueden almacenar y manejar. Algunos de los tipos de datos más comunes incluyen:

- Números enternos y flotantes
- Cadenas y caracteres de texto
- Fechas y horas
- Booleans
- Blobs y archivos
- Datos geográficos

---

## Concepto CRUD

CRUD es un acrónimo que significa Create, Read Update & Delete, es decir: "Crear, Leer, Actualizar y Eliminar".

Se refiere a las 4 operaciones básicas que se pueden realizar en una base de datos, es decir, la capacidad de crear nuevos registros, leer, actualizar y eliminar los registros existentes.

Estas operaciones se consideran la funcionalidad básica que se espera de cualquier sistema de gestión de bases de datos, y suelen estar implementadas de manera nativa en la mayoría de los SGBD.

Estas operaciones se utilizan tanto en la administración de objetos y privilegios de la base de datos como en la gestión de los datos mismos.

---

## Lógica de Negócio

La lógica de negocios es el conjunto de reglas, políticas y procesos que describen cómo se lleva a cabo el negocio.

En el modelado de una base de datos, la lógica de negocios se refiere a la representación de las reglas y procesos de negocios en el modelo de datos.

Estas reglas y procesos incluyen cosas como la validación de los datos, la validación de las restricciones de negocios, la definición de las relaciones entre las entidades, y la definición de cómo se deben calcular ciertos valores.

La incorporación de la lógica de negocios en el modelo de datos es importante porque permite asegurarse de que los datos estén correctamente validados y se respeten las restricciones de negocios antes de ser almacenados en la base de datos.

También permite a los desarrolladores entender mejor cómo los datos se relacionan y se utilizan en un sistema, lo que puede ser útil a la hora de realizar tareas de mantenimiento o mejora.

Además, la lógica de negocios puede ser reutilizada en diferentes partes de la aplicación, lo que reduce el esfuerzo y el tiempo necesarios para implementar la misma lógica en múltiples lugares.

---

## Llaves

Una llave en bases de datos es un identificador que permite hacer único a un registro de información tenemos 2 tipos: primarias y foráneas.

### Llave Primaria

Identifica un registro como único dentro de la entidad a la que pertenece. En nuestro listado de atributos pondremos las siglas PK de Primary Key delante del atributo que sea llave principal.

### Llave Foránea

Relaciona los datos de un registro de una entidad con los de otra, o con un registro distinto de la misma entidad. En nuestro listado de atributos pondremos las siglas FK de Foreign Key delante del atributo que sea llave foránea.

### Atributos Únicos

En algunas ocasiones vamos a necesitar que algunos atributos de la entidad sean únicos, es decir que no existan datos duplicados en el atributo, sin que necesariamente sea una llave primaria o foránea.

Esta característica se utiliza a menudo para asegurarse de que los datos sean consistentes y no haya duplicados en la entidad. Por ejemplo para que un usuario no pueda crear 2 cuentas diferentes con un mismo correo o número de teléfono.

Datos que suelen definirse como atributos únicos podrían ser el DNI, email, teléfono móvil, nombre de usuario o alias, número de placas de un automóvil, etc.

---

## Relaciones

Las relaciones son asociaciones entre entidades que se crean para recuperar y vincular datos.

Para crear una relación semánticamente utiliza un verbo para relacionar las entidades en cuestión.

### Tipos de Relaciones

1 a 1: Una persona (e) poseé (r) una única clave de estudiante (e) y viceversa.
1 a M: Una factura (e) se emite (r) a una persona (e) y sólo a una, pero una persona (e) puede tener (r) varias facturas (e) emitidas a su nombre.
M a M: Un cliente (e) puede comprar (r) varios productos (e) y un producto (e) puede ser comprado (r) por varios clientes (e).

---

## Modelo Entidad-Relación

Un diagrama modelo entidad-relación es una herramienta para el modelo de datos, la cual facilita la representación de entidades de una base de datos.​

Se caracteriza por utilizar una serie de símbolos y reglas para representar los datos y sus relaciones. Con este modelo conseguimos representar de manera gráfica la estructura lógica de una base de datos.

![Modelo Entidad-Relación](/assets/db-modelo-entidad-relacion-ejemplo.jpg)

- Las entidades se representan con rectángulos.
- Los atributos se representan con óvalos que se conectan a la entidad a la que pertenecen.
- Los atributos que son llaves primarias se subrayan.
- Las relaciones se representan con rombos que conectan a las entidades relacionadas, dentro del rombo se coloca el verbo que hace la relación entre las entidades.

Hay una variante a este diagrama, que se llama Modelo Relacional de la Base de Datos que también ejemplifica gráficamente la relación de las entidades y la descripción de los atributos de estas.

![Modelo Entidad-Relación](/assets/db-modelo-relacional-ejemplo.png)

Personalmente prefiero este tipo de diagrama por sobre el modelo entidad-relación, ya que nos permite describir el tipo de dato de cada atributo y se vuelve más fácil de manejar al tener cada entidad en una tabla con sus respectivos atributos.

---

## Normalización

La normalización de bases de datos es un proceso que se utiliza para organizar y optimizar la estructura de una base de datos para asegurar su integridad, evitar la redundancia y mejorar el rendimiento. La normalización consiste en la división de las entidades en varias entidades más pequeñas y relacionarlas mediante llaves foráneas.

La normalización se realiza a través de varios niveles o formas, cada uno de los cuales representa un grado de descomposición de la entidad original. Los tres niveles más comunes de normalización son la Primera Forma Normal (1FN), la Segunda Forma Normal (2FN) y la Tercera Forma Normal (3FN), aunque existen otros 2 niveles.

El objetivo de la normalización es reducir la redundancia y garantizar la integridad de los datos al asegurar que cada dato solo se almacene en un solo lugar y que los datos sean consistentes y coherentes. La normalización también ayuda a mejorar el rendimiento de la base de datos, ya que reduce el tamaño y la complejidad de las entidades, lo que facilita la indexación y la búsqueda de información.

Es importante tener en cuenta que la normalización puede tener un impacto en el rendimiento de la aplicación, ya que puede requerir una mayor cantidad de consultas y una complejidad adicional para recuperar y manipular datos. Por lo tanto, es importante encontrar un equilibrio entre la normalización y la eficiencia en el diseño de la base de datos.

---

### Formas Normales

Las formas normales son estándares para la organización y modelamiento de datos en una base de datos relacional. En total existen 5 formas normales.

1. Primera Forma Normal (1FN): Cada atributo de una entidad debe contener solo valores atómicos, es decir, valores indivisibles que no pueden ser divididos en atributos más pequeños.
2. Segunda Forma Normal (2FN): Además de cumplir con la 1FN, cada atributo no dependiente funcionalmente de la llave principal debe estar en una entidad separada.
3. Tercera Forma Normal (3FN): Además de cumplir con la 2FN, todas las dependencias funcionales deben ser eliminadas, es decir, no deben existir dependencias funcionales transitorias.
4. Cuarta Forma Normal (4FN): También llamada de Forma Normal de Boyce-Codd (FNBC), es una forma más restrictiva que la 3FN, donde se garantiza que no existan dependencias funcionales parciales o transitivas en la entidad.
5. Quinta Forma Normal (5FN): También conocida como Forma Normal de Domino-Clave (FNDC), en ella se debe garantizar que no haya dependencias múltiples de conjuntos en las entidades.
   Al aplicar las formas normales a un modelo de base de datos, se puede asegurar que los datos sean consistentes, que no haya redundancia y que sea fácil de mantener y escalar.

Sin embargo, también es importante tener en cuenta que la aplicación de formas normales más rigurosas puede resultar en una estructura de base de datos más compleja y menos eficiente en términos de rendimiento. Por lo tanto, es importante encontrar un equilibrio entre la integridad de los datos y la eficiencia en el diseño de un modelo de base de datos.

---

- Primera Forma Normal: En la 1FN, cada columna de una tabla debe contener únicamente valores atómicos, es decir, valores simples que no pueden ser divididos en partes más pequeñas.
- Segunda Forma Normal: La 2FN requiere que cada columna no dependiente funcionalmente de la clave primaria de una tabla sea movida a una tabla separada. Esto significa que cada tabla debe representar un solo hecho o concepto.
- Tercera Forma Normal: La 3FN requiere que todas las dependencias funcionales sean removidas de la tabla, es decir, que no haya redundancia de información.
- Forma Normal de Boyce-Codd: La FNBC es una forma normal más rigurosa que la anteriores y requiere que cada dependencia funcional sea una clave candidata única.
- Forma Normal de Dominio-Clave: Esta forma normal (FNDC) es una extensiones de la FNBC y se utiliza para asegurar la integridad de los datos en modelos de datos más complejos. No debe haber dependencias funcionales múltiples, es decir, una dependencia funcional en la que varios atributos dependen de una clave externa.

---

### Modelado de Datos

12 pasos para modelado desde 0

1. Identificar las entidades del sistema.
2. Identificar los atributos de las entidades.
3. Identificar las llaves primarias y foráneas.
4. Asignar una nomenclatura adeacuada a las entidades y sus atributos.
5. Identificar las entidades pivote del sistema.
6. Identificar los catálogos del sistema.
7. Identificar los tipos de relaciones del sistema.
8. Crear el Modelo Entidad-Relación del sistema.
9. Crear el Modelo Relacional de la base de datos del sistema.
10. Identificar los tipos de dato de los atributos de las entidades del sistema.
11. Identificar los atributos que puedan ser únicos en el sistema.
12. Identificar las reglas de negocio (Operaciones CRUD) del sistema.
