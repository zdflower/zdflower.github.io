---
layout: post
title: Mashup CS50 PSet8
---

## Problem set del curso edxCS50.

- [x] Instalar los requirements.
- [x] Obtener la API key de Google.
- [x] Bajar datos postales de Argentina. 
- [x] Cargar la base de datos.

### ¿Cómo cargué la base de datos?

Abrí el archivo de la base de datos.

    sqlite3 mashup.db

Luego, en el shell creé la tabla y a partir de la información de readme.txt le asigné el tipo de datos a cada campo:

    sqlite> create table places (
		country_code char,
	    postal code varchar(20),
		place name varchar(180),
		admin name1 varchar(100),
		admin code1 varchar(20),
		admin name2 varchar(100),
		admin code2 varchar(20),
		admin name3 varchar(100),
		admin code3 varchar(20),
		latitude int,
		longitude int,
		accuracy int
    );

Después importé los datos de AR.txt, que estaban separados por "\t" (tabulador):

    sqlite> .separator "\t"
    sqlite> .import AR.txt places;



