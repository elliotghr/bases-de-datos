# MirchaGram

## Entidades

### usuarios **(ED)**

- usuario_id **(PK)**
- username **(UQ)**
- user_date
- email
- password
- phone **(UQ)**
- bio
- web
- avatar
- birthdate
- genre
- pais_id **(FK)**

### posts **(ED)**

- post_id **(PK)**
- post_date
- plot
- url
- usuario_id **(FK)**

### comentarios **(ED|EP)**

- comentario_id **(PK)**
- comentario_date
- comentario
- post_id **(FK)**
- usuario_id **(FK)**

### corazones **(ED|EP)**

- corazon_id **(PK)**
- corazon_date
- post_id **(FK)**
- usuario_id **(FK)**

### followers **(ED|EP)**

- follow_id **(PK)**
- follow_date
- follow_user **(FK)**
- following_user **(FK)**

### paises **(EC)**

- pais_id **(PK)**
- nombre

### relaciones

Un **usuario** _genera_ posts (1,M)
Un **usuario** _tiene_ followers (1,M)
Un **usuario** _genera_ follows (1,M)
Un **usuario** _tiene_ pais (1,1)
Un **usuario** _genera_ comentarios (1,M)
Un **usuario** _genera_ corazones (1,1)
Un **post** _tiene_ comentarios (1,M)
Un **post** _tiene_ corazones (1,M)

## Reglas de negocio

### usuarios

1. Crear un usuario
2. Editar un usuario
3. Leer un usuario
4. Leer todos los usuarios
5. Eliminar un usuario
6. Verificar un usuario

### posts

1. Crear un post
2. Editar el plot del post
3. Leer un post
4. Leer todos los posts
5. Leer todos los posts de un usuario
6. Eliminar un post

### comentarios

1. Crear un comentario
2. Leer un comentario
3. Leer todos los comentarios
4. Contar los comentarios
5. Eliminar un comentario

### corazones

1. Crear un corazon
2. Contar todos los corazones
3. Eliminar un corazon

### followers

1. Crear un follow
2. Leer todos los follows
3. Contar todos los follows de un usuario
4. Contar todos los followings de un usuario
5. Eliminar un follow

### paises

1. Crear un pais
2. Editar el plot del pais
3. Leer un pais
4. Leer todos los paises
5. Eliminar un pais
