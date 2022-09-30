# Ejercicios realizados en clase con javascript

## 1.  Collatz

![image](https://user-images.githubusercontent.com/31961588/193165706-9aa92ee9-6399-4cf8-9d25-95b5839474d7.png)

**index.html**

```Html
<!DOCTYPE html>
<html>

<head>
    <title>Aprendiendo JavaScript</title>  
    <script src="app.js"></script>
</head>

<body>

    <h2>Serie de Collatz</h2>
     
    <input id="numb">
    <button type="button" onclick="myFunction()">Submit</button>
    <p id="demo"></p>

</body>

</html>
```

**app.js**

```JavaScript
function myFunction(){
   
   let n = document.getElementById("numb").value;
   let rta=n+"<br>";   
   console.log(n);
   while(n!=1){
       if(n%2==0){
          n=n/2;
       }else{
          n=n*3+1;
       }
       rta=rta+n+"<br>"
       console.log(n); 
   }
   document.getElementById("demo").innerHTML=rta;


}
```

## 2. Dibujo con asteriscos. 


![image](https://user-images.githubusercontent.com/31961588/193166918-ccc9417a-5f51-432d-a2ce-78b2159d0e42.png)

**index.html**

```Html
<!DOCTYPE html>
<html>

<head>
    <title>Aprendiendo JavaScript</title>  
    <script src="app.js"></script>
</head>
<body>

    <h2>Serie de Collatz</h2>
    
    <input id="altura" placeholder="altura">
    <input id="ancho" placeholder="ancho">
    <button type="button" onclick="myFunction()">Submit</button>
    <p id="demo"></p>

</body>
</html>
```
**app.js**

```JavaScript
function myFunction(){
   
   let altura = document.getElementById("altura").value;
   let ancho  = document.getElementById("ancho").value;
   let dibujo="";
   for(let i=0;i<altura;i++){
       for(let j=0;j<ancho;j++){
           dibujo+="*";
       }
       dibujo+="<br>";
   }

   document.getElementById("demo").innerHTML=dibujo;

}
```

## 3. Adivinar número.

![image](https://user-images.githubusercontent.com/31961588/193181477-07d329b6-3b2a-4ffa-9eb3-d023c4c78f96.png)

**index.html**

```Html
<!DOCTYPE html>
<html>
<head>
    <title>Aprendiendo JavaScript</title>   
    <script src="app.js"></script> 
</head>
<body onload="generarNumRamdo()">

<h2>My First JavaScript</h2>
<h1 id="numIntentos"></h1>
<input id="intento" placeholder="intento">
<button type="button" onclick="myFunction()">Submit</button>
<p id="demo"></p>

</body>
</html> 
```

**app.js**

```JavaScript
let valor=0;
let numIntentos=0;

function generarNumRamdo(){
    valor=Math.floor(Math.random() * 100);
    console.log(valor);

}

function myFunction(){

    let intento=document.getElementById("intento").value;
    let pista="";
    if(intento!=valor){
    if(valor>intento){
       pista="El número es mayor";  
    }else{
        pista="El número es menor";
    }    
    }else{
       pista="Correcto!";
    }
    numIntentos++;
    document.getElementById("numIntentos").innerHTML=numIntentos;
    document.getElementById("demo").innerHTML=pista;
    
    
}


```
