# Taller maquetación sitio web con html y css

## 1. Crear el proyecto 

![image](https://user-images.githubusercontent.com/31961588/192122220-5954394f-c329-42cd-8e0a-94061d525e83.png)


Creamos un directorio donde vamos a tener nuestro archivo index.html y estilos.css. La forma de implementar los estilos en css se va ser por medio externo importando el archiv css

![image](https://user-images.githubusercontent.com/31961588/192122151-5b0127b1-9ec1-459c-a2a9-b2169cdd1709.png)

**index.html**

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
            <li><a href="#">Londo</a></li>
            <li><a href="#">Paris</a></li>
            <li><a href="#">Bogotá</a></li>
            <li><a href="#">Cartagena</a></li>
            <li><a href="#">New York</a></li>
            <li><a href="#">Miami</a></li>
            <li><a href="#">Buenos Aires</a></li>
            <li><a href="#">Lima</a></li>
        </ul>
    </nav>   
    <article>
        <h1>London</h1>
        <p>London is the capital city of <a href="#">England</a>. It is the most populous 
            city in the United Kingdom, with a metropolitan area of over 13
            million inhabitants.</p>
        <p>Standing on the River Thames, London has been a major settlement 
           for two millennia, its history going back to its founding by the Romans, 
           who named it Londinium.</p>
        <p>Lorem Ipsum es simplemente el texto de relleno de las imprentas y archivos de texto. 
            Lorem Ipsum ha sido el texto de relleno estándar de las industrias desde el año 1500,
             cuando un impresor (N. del T. persona que se dedica a la imprenta) desconocido usó una 
             galería de textos y los mezcló de tal manera que logró hacer un libro de textos especimen.
              No sólo sobrevivió 500 años, sino que tambien ingresó como texto de relleno en documentos
               electrónicos, quedando esencialmente igual al original. Fue popularizado en los 60s con 
               la creación de las hojas "Letraset", las cuales contenian pasajes de Lorem Ipsum, y 
               más recientemente con software de autoedición, como por ejemplo Aldus PageMaker, 
               el cual incluye versiones de Lorem Ipsum.</p>
    </article>
</section>
<footer>
    <p>Footer</p>
</footer>
</body>
</html>
```

**estilos.css**
```Css
*{
  box-sizing: border-box;

}

body{
  font-family: Arial, Helvetica, sans-serif;
}

header{
  background-color:darkgrey;
  padding: 30px;
  text-align: center;
  font-size: 35px;
  color: white;  
}

nav{
  float:left;
  width: 30%;
  height: 300px;
  background-color: beige;
  padding-top: 5px;
}

nav ul{
  list-style-type: none;
  margin: 0;
  padding: 0;
  width: 100%;
  background-color: #f1f1f1;
}

nav li a {
  display: block;
  color: #000;
  padding: 8px 16px;
  text-decoration: none;
}

nav li a:hover{
   background-color: #555;
   color: white;  
}



article{
  float: left;  
  padding: 20px;
  width: 70%;
  background-color: aqua;
  height: 300px;
}

section::after{
  content: "";
  display: table;
  clear: both;
}

footer {
  background-color:cornflowerblue;
  padding-top: 20px;
  padding-bottom: 20px;
  padding-left: 20px;
  padding-right: 20px;
  text-align: center;
  color: aliceblue;
}
```


