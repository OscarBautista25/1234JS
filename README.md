CREATE DATABASE IF NOT EXISTS user_management;

USE user_management;

-- Tabla para almacenar los usuarios registrados
CREATE TABLE IF NOT EXISTS usuarios (
    id INT AUTO_INCREMENT PRIMARY KEY,
    cedula VARCHAR(255) NOT NULL,
    name VARCHAR(255) NOT NULL,
    role VARCHAR(255) NOT NULL
);

-- Tabla para almacenar las credenciales de inicio de sesión
CREATE TABLE IF NOT EXISTS login (
    id INT AUTO_INCREMENT PRIMARY KEY,
    username VARCHAR(255) NOT NULL,
    password VARCHAR(255) NOT NULL
);

-- Insertar un usuario inicial para pruebas
INSERT INTO login (username, password) VALUES ('admin', 'admin123');

npm install mysql 
ALTER USER 'root'@'localhost' IDENTIFIED WITH mysql_native_password BY '1234';
FLUSH PRIVILEGES;

