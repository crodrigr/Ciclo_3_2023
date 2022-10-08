# Crear la base de datos

## 1. Crear la bd del proyecto en mysql

![image](https://user-images.githubusercontent.com/31961588/194676999-c0412b85-caaa-49eb-9810-7b9ef1de5708.png)

## 2. Configuración de la credenciales de conexión de la bd en aplication.properties.

![image](https://user-images.githubusercontent.com/31961588/194677245-3fa88aeb-0407-48f8-923f-7b94ec0dbb12.png)

```Console
spring.datasource.url=jdbc:mysql://localhost:3306/db_mintic_12
spring.datasource.username=root
spring.datasource.password=admin
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.database-platform=org.hibernate.dialect.MySQL57Dialect
spring.jpa.hibernate.ddl-auto=create-drop
logging.level.org.hibernate.SQL=debug
```

## 3. Crear archivo import.sql

![image](https://user-images.githubusercontent.com/31961588/194677468-8b3d9887-ebd8-4968-9784-d5775d9915a6.png)

### 3.1 Abrir import.sql
![image](https://user-images.githubusercontent.com/31961588/194677532-79320acf-178f-4d7c-aaaa-8bb9eb958566.png)


## 4. Insert (datos de prueba) 

![image](https://user-images.githubusercontent.com/31961588/194677807-3b523a53-0f46-4701-a1ad-0552eb262406.png)

```Sql
INSERT INTO clientes (nombres,apellidos,email,telefono,saldo) VALUES("Camilo Ernesto","Rodriguez Moreno","crodrigr@gmail.com","3154887",250000);
INSERT INTO clientes (nombres,apellidos,email,telefono,saldo) VALUES("Maria Celina","Torres Serrano","ctorres@gmail.com","3154887",150000);
INSERT INTO clientes (nombres,apellidos,email,telefono,saldo) VALUES("Juan Carlos","Camargo Perez","jcamargo@gmail.com","3154887",50000);
INSERT INTO clientes (nombres,apellidos,email,telefono,saldo) VALUES("Diego Fernando","Rangel Pinto","drangel@gmail.com","3154887",450000);
INSERT INTO clientes (nombres,apellidos,email,telefono,saldo) VALUES("Pedro Andres","Moreno Oyola","pmoreno@gmail.com","3154887",750000);
INSERT INTO clientes (nombres,apellidos,email,telefono,saldo) VALUES("Juan Carlos","Martinez Puyana","jmartinez@gmail.com","3154887",20000);
INSERT INTO clientes (nombres,apellidos,email,telefono,saldo) VALUES("Diana Milena","Tarazona Suarez","dtarazona@gmail.com","3154887",250000);


```
