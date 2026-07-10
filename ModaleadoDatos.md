# Modelado de Datos

## Pasos a seguir

1. Identificar las entidades del sistema. ✅
2. Identificar los atributos de las entidades. ✅
3. Identificar las llaves primarias y foráneas. ✅
4. Asignar una nomenclatura adeacuada a las entidades y sus atributos. ✅
5. Identificar las entidades pivote del sistema. ✅
6. Identificar los catálogos del sistema. ✅
7. Identificar los tipos de relaciones del sistema. ✅
8. Crear el Modelo Entidad-Relación del sistema. ✅
9. Crear el Modelo Relacional de la base de datos del sistema. ✅
10. Identificar los tipos de dato de los atributos de las entidades del sistema. ✅
11. Identificar los atributos que puedan ser únicos en el sistema. ✅
12. Identificar las reglas de negocio (Operaciones CRUD) del sistema.

## Glosario

- **PK**: _Primary Key_
- **FK**: _Foreign Key_
- **UQ**: _Unique Attribute_
- **ED**: Entiedad de Datos
- **EC**: Entiedad Catalogo
- **EP**: Entiedad Pivote

## Estándares de nomenclatura

La nomenclatura estándar recomendada para bases de datos en MySQL prioriza la consistencia y el uso de snake_case (minúsculas con guiones bajos) para evitar problemas de sensibilidad a mayúsculas en sistemas operativos Unix/Linux.

#### Convenciones de Nombres

- Tablas: Se utilizan sustantivos en plural y minúsculas (ej. employees, users).
- Columnas: Se utilizan sustantivos en singular y minúsculas (ej. name, email).
- Llaves primarias: Se nombran con el formato "id" seguido del nombre de la tabla (ej. id_employee, id_user).
- Claves Primarias (PK): Se nombran generalmente como id, de tipo BIGINT UNSIGNED con AUTO_INCREMENT (ej. id_employee, id_user).
- Claves Foráneas (FK): Se forman combinando el nombre de la tabla de referencia en singular con el sufijo \_id (ej. user_id, branch_id).
