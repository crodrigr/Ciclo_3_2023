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
      <title>CSS Template</title>
      <link rel="stylesheet" href="css/estilos.css">
  </head>
  <body>
     <header>
        <h2>Cites</h2>
     </header>
     <section>
        <nav>
           <ul>
              <li><a href="#">Londo</a></li>
              <li><a href="#">Paris</a></li>
              <li><a href="#">Tokyo</a></li>
              <li><a href="#">Paris</a></li>
              <li><a href="#">Tokyo</a></li>
              <li><a href="#">Paris</a></li>
              <li><a href="#">Tokyo</a></li>
              <li><a href="#">Paris</a></li>
              <li><a href="#">Paris</a></li>
             
           
           </ul>
        </nav>
        <article>
          <h1>Londo</h1>
          <p>London is the capital city of England. It is the most populous city in the United Kingdom, with a metropolitan area of over 13 million inhabitants.</p>
          <p>Standing on the River Thames, London has been a major settlement for two millennia, its history going back to its founding by the Romans, who named it Londinium.</p>
          
        </article>
     </section>
     <footer>
      <p>footer</p>
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
  background-color: darkgray;
  text-align: center;
  padding: 10px; 
  font-size: 30px;
  color:aliceblue;
}

nav{
  float: left; 
  width: 15%;
  height: 305px;
  background-color: bisque; 
  padding: 0px;
}

nav ul{
    list-style-type: none;
    margin:0;
    padding: 0;
    width: 203px;
    background-color: #a11212;
}

nav li a{
    display: block;
    color: #000;
    padding: 8px 16px;
    text-decoration: none;

}

nav li a:hover{
    background-color: #555;
    color: white
}

article{
    float:left;
    width: 85%;
    height: 305px;
    background-color: aquamarine;
    padding: 20px;
}

section::after{
    content: "";
    display: table;
    clear:both;
}

footer{
    background-color: cadetblue;
    text-align: center;
    color: aliceblue;
    padding: 20px;
}

```


