# Crear el cliente entity de nuestro proyecto. 

## 1. Crear el paquete models.entity

## 1.1

![image](https://user-images.githubusercontent.com/31961588/194442989-9de95c94-733e-4ee4-b5b6-8c1735a5d81f.png)

## 1.2 

![image](https://user-images.githubusercontent.com/31961588/194443072-ab8a6090-7f90-4e2b-a85b-f4daf9c4dea0.png)


El nombre del paquete no es entity, sino entities, se puede cambiar por la opcion refactor->rename

![image](https://user-images.githubusercontent.com/31961588/194443315-883bb3f3-873a-40d2-9154-139462454f8b.png)

## 1.3 Crear la clase Cliente dentro del paquete models.entities

![image](https://user-images.githubusercontent.com/31961588/194443476-43ed5b8d-6472-4630-b0f4-b585680bf29e.png)

## 1.3.1 

![image](https://user-images.githubusercontent.com/31961588/194444433-190420c7-a819-4999-addb-561626ba0aa7.png)


### 1.3.2 Definir los atributos de la clase cliente

![image](https://user-images.githubusercontent.com/31961588/194675036-f3ce0787-3466-42c9-97da-3e9b2de735ad.png)

### 1.3.3 Generar los métodos getter and setter

![image](https://user-images.githubusercontent.com/31961588/194675071-aaa2a293-bcf4-430c-88ff-d9442cd89e81.png)

### 1.3.4 Implementar en la clase cliente la interfaz serializable

![image](https://user-images.githubusercontent.com/31961588/194675193-087468bf-970b-480d-bd42-ad750628b894.png)

### 1.3.5 Add dependencia de validation en pom.xml

![image](https://user-images.githubusercontent.com/31961588/194676438-1642b101-4d54-4c5d-b6a6-dd8093b4f63c.png)

```Xml
	<dependency>
			<groupId>org.springframework.boot</groupId>
			<artifactId>spring-boot-starter-validation</artifactId>
			<version>2.7.4</version>
		</dependency>
```

### 1.3.6. Especificaciones de los atributos para validar a nivel de bd y memoria. 

![image](https://user-images.githubusercontent.com/31961588/194676894-11e7e215-3451-40f2-8193-1ea8ee283fac.png)

