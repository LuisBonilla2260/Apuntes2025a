# 05-02-2024
___
## Instrucciones Pedagogicas

### Herramientas

POSTRGRESQL
MONGODB
CASSANDRA


## PONDERACION

### >Parcial 70%

            
* >TALLERES - QUIZ----->25%

* >AUTO COE ------> 5%


### PLATAFORMA DE ENTREGA ES MOODLE

## Correo Electronico Docente
### jmllanosm@corhuila.edu.co

### Lunes Miercoles de 11 a 12 M  B209
---
## Comandos Github 

    git add .
    git commit -m "commit"
    git push
___
___
___


# 06-02-25

### Instalacion de Docker E Imagen de postgress

----
### 12-02
---

### Repaso
Se hace repaso de sql.

- Diferencia entre varchar&char:\

 ***VARCHAR*** is the more commonly used and standardized way to define variable-length strings in SQL, while ***VAR*** or CHARACTER VARYING is less common but functionally equivalent in most databases.
```sql
 \l = Permite listar 
 \c (name db)= Permite ingresar a la db
 \d = Permite listar las tablas de DB
 \d (name-table)
```
13-02
```sql
-- Crear la base de datos
CREATE DATABASE tienda;

-- Conectar a la base de datos
\c tienda;

-- Crear la tabla Ciudad
CREATE TABLE Ciudad (
    id SERIAL PRIMARY KEY,
    nombre VARCHAR(100) NOT NULL
);

-- Crear la tabla Cliente
CREATE TABLE Cliente (
    id SERIAL PRIMARY KEY,
    nombre VARCHAR(100) NOT NULL,
    email VARCHAR(150) UNIQUE NOT NULL,
    id_ciudad INT NOT NULL,
    FOREIGN KEY (id_ciudad) REFERENCES Ciudad(id) ON DELETE CASCADE
);

-- Crear la tabla Compra
CREATE TABLE Compra (
    id SERIAL PRIMARY KEY,
    id_cliente INT NOT NULL,
    fecha DATE NOT NULL,
    total DECIMAL(10,2) NOT NULL,
    FOREIGN KEY (id_cliente) REFERENCES Cliente(id) ON DELETE CASCADE
);




```