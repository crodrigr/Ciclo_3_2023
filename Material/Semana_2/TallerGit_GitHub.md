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


## 7. Historia de las fotos tomadas de nuestro repositorio git local.

![image](https://user-images.githubusercontent.com/31961588/190837438-8e8967ad-4f7b-474a-b2ef-49cfb6a7a52c.png)

## 8. Comando para ver las ramas del git. 

![image](https://user-images.githubusercontent.com/31961588/190837466-58ada30b-b882-430f-8d5f-0be18158d988.png)

## 9. Crear una nueva rama

Se observa que se creo la rama test

![image](https://user-images.githubusercontent.com/31961588/190837540-3a72c462-de03-4506-beb8-2bfdef4e2545.png)

## 10. En la rama test hacer un cambio en index.html y tomar foto. 

![image](https://user-images.githubusercontent.com/31961588/190837596-8b9210e8-9e6d-44d9-b708-562a2eab2142.png)

Se toma la foto y se verifica que fue tomada en la rama test

![image](https://user-images.githubusercontent.com/31961588/190837659-4a117e46-c863-496e-8365-0594bb40d43d.png)

## 11. Cambio de rama de test a master. 

Se observa que carga el archivo index.html de la rama master y no están los cambios que se hicieron en index.html de la rama test del punto 10. 

![image](https://user-images.githubusercontent.com/31961588/190837836-28b68c4b-c609-4c1d-ad30-2df2757cb279.png)

## 12. Hacer un merge de la rama test a master. Es decir copiar lo realizado en test y unirlo a la rama master. 

Se observa que estamos en la rama master y ejecutamos el comando **git merge test** para unir lo que hay en master con lo de test. En el arhcivo index.htlm se agrego el cambo que se hizo en test. 



![image](https://user-images.githubusercontent.com/31961588/190838063-5bdb4423-d95d-484f-8a0b-f481ba440631.png)

