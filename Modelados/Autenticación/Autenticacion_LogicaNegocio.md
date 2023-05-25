# Sistema de Autenticación

## Listado de entidades

### usuarios **(ED)**

- usuario_id **(PK)**
- username **(UQ)**
- password
- email **(UQ)**
- nombre
- apellido
- avatar
- activo
- fecha_creación
- fecha_actualización

### roles **(EC)**

- rol_id **(PK)**
- nombre
- descripcion

### permisos **(EC)**

- permiso_id **(PK)**
- nombre
- descripcion

### roles_x_usuario **(EP)**

- rol_usuario_id **(PK)**
- usuario_id **(FK)**
- rol_id **(FK)**

### permisos_x_roles **(EP)**

- permiso_rol_id **(PK)**
- rol_usuario_id **(FK)**
- permiso_id **(FK)**

## Relaciones

Los **usuarios** _tiene_ roles (M,M)
Los **roles** _tiene_ permisos (M,M)

## Reglas de negocio

### usuarios

- Crear usuarios
- Leer un usuario
- Leer todos los usuarios
- Actualizar usuarios
- Eliminar usuarios
- Habilitar o inhabilitar usuario
- Verificar usuario existente

### roles

- Crear roles
- Leer un rol
- Leer todos los roles
- Actualizar roles
- Eliminar roles

### permisos

- Crear permisos
- Leer un permiso
- Leer todos los permisos
- Actualizar permisos
- Eliminar permisos

### roles_x_usuario

- Crear rol x usuario
- Leer un rol x usuario
- Leer todos los rol x usuario
- Leer todos los rol x usuario de un usuario
- Eliminar rol x usuario

### permisos_x_roles

- Crear permiso x rol
- Leer un permiso x rol
- Leer todos los permiso x rol
- Leer todos los permiso x rol de un usuario
- Eliminar permiso x rol
