# Taller maquetación sitio web con html y css

## 1. Crear el proyecto 

![image](https://user-images.githubusercontent.com/31961588/192122220-5954394f-c329-42cd-8e0a-94061d525e83.png)


Creamos un directorio donde vamos a tener nuestro archivo index.html y estilos.css. La forma de implementar los estilos en css se va ser por medio externo importando el archiv css

![image](https://user-images.githubusercontent.com/31961588/192122151-5b0127b1-9ec1-459c-a2a9-b2169cdd1709.png)

```Html
<!DOCTYPE html>
<html>
<head>
<link rel="stylesheet" href="css/estilos.css">
<title>Page Title</title>
</head>
<body>
<!-- cabecera: tilulo y logo  -->
<header>
    <h2>Cities</h2>
</header>
<!-- sección principal de sitio web -->
<section>
    <nav>
        <ul>
            <li>Londo</li>
            <li>Paris</li>
            <li>Tokyo</li>
        </ul>
    </nav>
    <article>
        <h1>London</h1>
        <p>London is the capital city of England. It is the most populous 
            city in the United Kingdom, with a metropolitan area of over 13
            million inhabitants.</p>
        <p>Standing on the River Thames, London has been a major settlement 
           for two millennia, its history going back to its founding by the Romans, 
           who named it Londinium.</p>
    </article>
</section>
<footer>
    <p>Footer</p>
</footer>
</body>
</html>
```


