# Ventas

## Listado de entidades

### clientes **(ED)**

- cliente_id **(PK)**
- nombre
- apellidos
- telefono **(UQ)**
- email **(UQ)**
- direccion
- cp
- ciudad
- pais_id **(FK)**

### productos **(ED|EC)**

- producto_id **(PK)**
- nombre
- descripción
- foto
- precio
- cantidad

### ventas **(ED)**

- ventas_id **(PK)**
- cliente_id **(FK)**
- fecha
- monto

### articulos_x_venta **(EP)**

- articulo_id **(PK)**
- venta_id **(FK)**
- producto_id **(FK)**
- cantidad

### paises **(EC)**

- pais_id **(PK)**
- nombre
- dominio **(UQ)**

## Relaciones

1. Un **cliente** _tiene_ pais (1,1)
2. Un **cliente** _genera_ ventas (1,M)
3. Un **venta** _contiene_ articulos (1,M)
4. Un **articulo** _es_ un producto (1,1)

## Reglas de negocio

### clientes

1. Crear el registro un cliente
2. Leer el registro de un cliente en particular
3. Leer todos los registros de la entidad clientes
4. Actualizar los datos de un cliente dada una condición en particular
5. Eliminar los datos de un cliente dada una condición en particular

### productos

1. Crear el registro un producto
2. Leer el registro de un producto en particular
3. Leer todos los registros de la entidad productos
4. Actualizar los datos de un producto dada una condición en particular
5. Eliminar los datos de un producto dada una condición en particular
6. Cada que haya una venta se debe restar la cantidad de productos disponibles

### ventas

1. Crear el registro una venta
2. Leer el registro de una venta en particular
3. Leer todos los registros de la entidad ventas
4. Leer todas las ventas de un cliente
5. Leer todas las ventas de un producto
6. Actualizar los datos de una venta dada una condición en particular

### articulos_x_venta

1. Crear el registro un articulo
2. Leer el registro de un articulo en particular
3. Leer todos los registros de la entidad articulos
4. Leer todos los articulos de una venta
5. Leer todos los articulos de una producto
6. Leer todos los articulos de una cliente
7. Actualizar los datos de un articulo dada una condición en particular
8. Eliminar los datos de un articulo dada una condición en particular

### paises

1. Crear el registro un pais
2. Leer el registro de un pais en particular
3. Leer todos los registros de la entidad paiss
4. Actualizar los datos de un pais dada una condición en particular
5. Eliminar los datos de un pais dada una condición en particular
