# Configuraciónd de la base datos

## 1. Crear el esquema en la base datos: db_mintic

![image](https://user-images.githubusercontent.com/31961588/194454092-9179c0fe-ffaf-4d16-a128-9599d30f02fd.png)

## 2. Configuracion de la bd en aplication.propertis

![image](https://user-images.githubusercontent.com/31961588/194455333-cd8ecd46-ed52-4a4e-83ee-e6ce5e017f73.png)

**aplication.properties**

```Console
spring.datasource.url=jdbc:mysql://localhost:3306/db_mintic
spring.datasource.username=root
spring.datasource.password=admin
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.database-platform=org.hibernate.dialect.MySQL57Dialect
spring.jpa.hibernate.ddl-auto=create-drop
logging.level.org.hibernate.SQL=debug
```

## 3. Crear el import.sql para insertar datos de prueba

### 3.1

![image](https://user-images.githubusercontent.com/31961588/194455963-91fabcf8-1db7-445d-bfb5-09f9dbb90bee.png)

### 3.2

![image](https://user-images.githubusercontent.com/31961588/194456041-d82dee68-6a2b-4f47-b493-678cb96e618f.png)

### 3.3 Abri import.sql para colocar los insert de los datos de pruebas

![image](https://user-images.githubusercontent.com/31961588/194456241-ec1da3f0-ec1a-42fc-b90a-0e74ec23ebb3.png)

### 3.4 Crear los insert de pruebas


![image](https://user-images.githubusercontent.com/31961588/194457053-f7fab263-b6fa-4958-be34-5cd2f250f013.png)

**import.sql**

```Sql
INSERT INTO clientes (nombres,apellidos,email,telefono,saldo) VALUES("Camilo Ernesto","Rodriguez Moreno","crodrigr@gmail.com","3154887",250000);
INSERT INTO clientes (nombres,apellidos,email,telefono,saldo) VALUES("Maria Celina","Torres Serrano","ctorres@gmail.com","3154887",150000);
INSERT INTO clientes (nombres,apellidos,email,telefono,saldo) VALUES("Juan Carlos","Camargo Perez","jcamargo@gmail.com","3154887",50000);
INSERT INTO clientes (nombres,apellidos,email,telefono,saldo) VALUES("Diego Fernando","Rangel Pinto","drangel@gmail.com","3154887",450000);
INSERT INTO clientes (nombres,apellidos,email,telefono,saldo) VALUES("Pedro Andres","Moreno Oyola","pmoreno@gmail.com","3154887",750000);
INSERT INTO clientes (nombres,apellidos,email,telefono,saldo) VALUES("Juan Carlos","Martinez Puyana","jmartinez@gmail.com","3154887",20000);
INSERT INTO clientes (nombres,apellidos,email,telefono,saldo) VALUES("Diana Milena","Tarazona Suarez","dtarazona@gmail.com","3154887",250000);
```
