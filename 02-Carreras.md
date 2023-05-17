# Carreras

## Listado de entidades

### carreras (ED)

- carrera_id **(PK)**
- nombre
- tipo_carrera **(FK)**
- tiempo
- mejor_tiempo
- altitud
- lugar
- fecha
- pais **(FK)**
- foto

### tipos_carreras (EC)

- tipo_carrera_id **(PK)**
- descripcion
- distancia

### paises (EC)

- pais_id **(PK)**
- nombre

## Relaciones

1. Una **carrera** _pertenece_ a un **tipo de carrera** (1,1)
2. Una **carrera** se _corre_ en un **pais** (1,1)

## Reglas de negocio

Por cada entidad estableceremos las reglas de negocio (Operaciones CRUD )

### carreras

1. Crear el registro una carrera
2. Leer el registro de una carrera en particular
3. Leer todos los registros de la entidad carreras
4. Actualizar los datos de una carrera dada una condición en particular
5. Eliminar los datos de una carrera dada una condición en particular

### tipos_carreras

1. Todos los valores del atributo distancia, de la entidad tipos*carreras deben ser expresados en _km_ y no se podrán repetir
1. Crear el registro un tipo de carrera
1. Leer el registro de un tipo de carrera en particular
1. Leer todos los registros de la entidad tipos_carreras
1. Actualizar los datos de un tipo de carrera dada una condición en particular
1. Eliminar los datos de un tipo de carrera dada una condición en particular

### paises

1. Crear el registro un pais
2. Leer el registro de un pais en particular
3. Leer todos los registros de la entidad paises
4. Actualizar los datos de un pais dada una condición en particular
5. Eliminar los datos de un pais dada una condición en particular
