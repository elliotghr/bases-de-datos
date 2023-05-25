# Sistema de Peliculas y Series

## Entidades

### peliculas **(ED)**

- pelicula_id **(PK)**
- titulo
- año
- duracion
- sinopsis
- estudio_id
- director
- elenco
- poster
- trailer
- pais **(FK)**

### series **(ED)**

- serie_id **(PK)**
- titulo
- año
- final
- sinopsis
- estudio_id
- creador
- elenco
- poster
- trailer
- pais **(FK)**

### temporadas **(ED)**

- temporada_id **(PK)**
- serie_id **(FK)**
- numero
- estreno
- titulo
- sinopsis
- poster
- trailer

### episodios **(ED)**

- episodios_id **(PK)**
- temporada_id **(KF)**
- numero
- estreno
- titulo
- sinopsis
- director
- duracion

### generos **(ED)**

- genero_id **(PK)**
- nombre

### generos_x_peliculas **(EP)**

- generos_peliculas_id **(PK)**
- pelicula_id **(FK)**
- genero_id **(FK)**

### generos_x_series **(EP)**

- generos_series_id **(PK)**
- serie_id **(FK)**
- genero_id **(FK)**

### paises

- pais_id
- nombre

## Relaciones

Una pelicula tiene paises (1,M)
Una serie tiene paises (1,M)
Las peliculas tiene generos (M,M)
Las series tiene generos (M,M)
Una serie tiene temporadas (1,M)
Una temporada tiene capitulos (1,M)

## Reglas de negocio
