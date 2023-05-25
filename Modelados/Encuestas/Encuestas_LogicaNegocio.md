# Encuesta

## Listado de entidade

### encuestas **(ED)**

- encuesta_id **(PK)**
- nombre
- descripción
- imagen
- fecha
- encuestados

### preguntas **(ED)**

- pregunta_id **(PK)**
- encuesta_id **(FK)**
- pregunta

### respuestas **(ED)**

- respuesta_id **(PK)**
- pregunta_id **(FK)**
- respuesta
- es_correcta

### ecuestados **(ED)**

- encuestado_id **(PK)**
- nombre
- apellido
- edad
- email **(UQ)**

### resultados **(ED|EP)**

- resultado_id **(PK)**
- encuesta_id **(FK)**
- encuestado_id **(FK)**
- preguntas
- correctas

## Relaciones

- Una **encuesta** _tiene_ preguntas (1,M)
- Una **pregunta** _tiene_ respuestas (1,M)
- Una **encuesta** _tiene_ resultados (1,M)
- Una **encuestado** _tiene_ resultados (1,M)

## Reglas de negocio

### encuestas

1. Crear el registro una encuesta
2. Leer el registro de una encuesta en particular
3. Leer todos los registros de la entidad encuestas
4. Actualizar los datos de una encuesta dada una condición en particular
5. Eliminar los datos de una encuesta dada una condición en particular
6. Cada que se conteste una encuesta se aumentará en 1 atributo encuestados

### preguntas

1. Crear el registro una pregunta
2. Leer el registro de una pregunta en particular
3. Leer todos los registros de la entidad preguntas
4. Actualizar los datos de una pregunta dada una condición en particular
5. Eliminar los datos de una pregunta dada una condición en particular

### respuestas

1. Crear el registro una respuesta
2. Leer el registro de una respuesta en particular
3. Leer todos los registros de la entidad respuestas
4. Actualizar los datos de una respuesta dada una condición en particular
5. Eliminar los datos de una respuesta dada una condición en particular

### ecuestados

1. Crear el registro un encuestado
2. Leer el registro de un encuestado en particular
3. Leer todos los registros de la entidad encuestados
4. Actualizar los datos de un encuestado dada una condición en particular
5. Eliminar los datos de un encuestado dada una condición en particular
6. Antes de crear un encuestado en la entidad, verificar mediante su email que no exista

### resultados

1. Crear el registro un resultado
2. Leer el registro de un resultado en particular
3. Leer todos los registros de la entidad resultados
4. Actualizar los datos de un resultado dada una condición en particular
5. Eliminar los datos de un resultado dada una condición en particular
6. Sacar el porcentaje de acertividad que tuvo el encuestado al contestar la encuesta
