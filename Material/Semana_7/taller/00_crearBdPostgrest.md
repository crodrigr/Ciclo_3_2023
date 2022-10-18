# Configuración de postgrest 

## 1 Crear usuario de postgrest

### 1.1 Usuario

![image](https://user-images.githubusercontent.com/31961588/196477072-e81916bc-4cbe-4c6f-b255-2b736ab940ad.png)

### 1.2 Pasword

![image](https://user-images.githubusercontent.com/31961588/196475394-a0c9fc0d-8339-40b7-a782-877a81749df2.png)


### 1.3 Permisos

![image](https://user-images.githubusercontent.com/31961588/196475779-410623e4-7659-4969-b8a5-26caf809748f.png)

### 1.4 

![image](https://user-images.githubusercontent.com/31961588/196477337-2fcff7bb-e2e7-47e5-9493-c3fde0891933.png)


**Configuración en mysql**

```Properties
spring.datasource.url=jdbc:mysql://localhost:3306/db_mintic_12
spring.datasource.username=root
spring.datasource.password=admin
spring.datasource.driver-class-name=com.mysql.cj.jdbc.Driver
spring.jpa.database-platform=org.hibernate.dialect.MySQL57Dialect
spring.jpa.hibernate.ddl-auto=create-drop
logging.level.org.hibernate.SQL=debug


server.port=${PORT:8083}

```

## 2 Crear la base de datos

### 2.1 

![image](https://user-images.githubusercontent.com/31961588/196480224-e83a1b83-65e5-4f34-97cc-3cdfcbf18aac.png)

## 2.2

![image](https://user-images.githubusercontent.com/31961588/196480652-ff034b57-ed68-421c-9a71-d84e3f0f8f5e.png)
