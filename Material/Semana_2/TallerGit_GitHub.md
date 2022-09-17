# Taller de Git y GitHub. 

## 1.Crear un directorio en la unidad C que hace referencia al proyecto. 


![image](https://user-images.githubusercontent.com/31961588/190836902-71e0e7ef-ffc6-4107-96f5-9f023c077fbc.png)

## 2. Inicializar git en el directorio creado del proyecto. 

Ingresamos por consola al directorio del proyecto y ejecutamos el comando **git init** esto se hace solo una vez.

![image](https://user-images.githubusercontent.com/31961588/190837075-f3899248-025f-426c-8a5d-78e07c68821b.png)

Se puede observar en el dictorio del proyecto en archivos ocultos que se creo un directorio git. Ahí se lleva el control de cambios. Nunca borrarlo

![image](https://user-images.githubusercontent.com/31961588/190837127-108561ea-2f32-4b97-b3cc-93be9d7c06ee.png)


## 3. Creamos un archivo index.html dentro del directorio del proyecto. 

![image](https://user-images.githubusercontent.com/31961588/190837002-cee8ac2e-0858-45c3-b357-dae3e82ff659.png)

**Código del index**

```Html
<!DOCTYPE html>
<html>
<head>
<title>Hello World!</title>
</head>
<body>
<h1> Hola Mundo.</h1>
</body>
</html>
```
## 4. Con el comando git status se puede revisar el estado de los cambios que tiene los archivos del proyecto. 

Se observa que archivo index.html no esta siendo seguido por el git. Entoces se debe agregar al stage. 

![image](https://user-images.githubusercontent.com/31961588/190837166-18a75cd6-bda8-4f1a-9858-525f23fe4d12.png)

## 5. Agregar cambios de archivos al stage con el comando git add . 

Se observa que el index.html fue agregado al stage y quedo en pendiente su commit (tomar la foto).

![image](https://user-images.githubusercontent.com/31961588/190837258-667639f9-6075-4f53-8d3e-ccf9700f2b54.png)

## 6. Hacer el commit (tomar la foto) de todos los archivos que están en stage. 

Se observa que index.html se hizo el commit y no hay cambios pendientes. 

![image](https://user-images.githubusercontent.com/31961588/190837384-5186ca32-f2ae-4f46-a5df-cadfa353a384.png)


