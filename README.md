
# API para tienda (Práctica)

API desarrollada en express con Typescript como ejemplo para clase de fundamento de base de datos.

Descargar módulos
* npm install

Iniciar proyecto
* npm run dev

Construir app
* npm run start

# Ejemplo de variables de entorno (.env)
DB_HOST=localhost

DB_PORT=3306

DB_USER= root

DB_PASSWORD=12345

DB_NAME=farmacia_chris

PORT=3000

# Construcción de base de datos

CREATE DATABASE farmacia_chris

USE farmacia_chris

CREATE TABLE employee (
    employee_id int NOT NULL AUTO_INCREMENT,
    full_name varchar(50) NOT NULL,
    password varchar(60) NOT NULL,
    created_at datetime DEFAULT NULL,
    created_by varchar(50) DEFAULT NULL,
    updated_at datetime DEFAULT NULL,
    updated_by varchar(50) DEFAULT NULL,
    deleted tinyint(1) DEFAULT NULL,
    PRIMARY KEY (employee_id)
);

CREATE TABLE products (
    id INT NOT NULL AUTO_INCREMENT PRIMARY KEY,
    stock INT NOT NULL,
    nombre VARCHAR(50) NOT NULL,
    precio DECIMAL(10,2) NOT NULL,
    description TEXT,
    formula TEXT,
    efectos_secundarios TEXT,
    caducidad VARCHAR(10),
    created_at DATETIME,
    created_by VARCHAR(30),
    updated_at DATETIME,
    updated_by VARCHAR(30),
    deleted TINYINT(1)
);

# Crear producto
Campos minimos para crear un producto
{
  "stock": 1,
  "nombre": "",
  "precio": 11.11,
  "created_by": "admin"
}

Campos completos
{
		"id": 19,
		"stock": 100,
		"nombre": "Producto A",
		"precio": 11.11,
		"description": "",
		"formula": "",
		"efectos_secundarios": "",
		"caducidad": "",
		"created_at": "2024-06-29T03:53:01.000Z",
		"created_by": "admin"
	}

# Actualizar producto
{
		"stock": 100,
		"nombre": "Producto A",
		"precio": 11.11,
		"description": "",
		"formula": "",
		"efectos_secundarios": "",
		"caducidad": "",
		"updated_by": "employee"
	}

# login

{
	"full_name": "",
	"password": ""
}

# create employee

{
  "full_name": "",
  "password": "",
  "created_by": "admin"
}
