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

### 4. Calculadora

![image](https://user-images.githubusercontent.com/31961588/193433046-a3e335c8-3b10-4c3a-88e9-80296e9f3b77.png)

**index.html**

```Html
<!DOCTYPE html>
<html>

<head>
  <title>Aprendiendo JavaScript</title>
  <script src="app.js"></script>
  <link href="https://cdn.jsdelivr.net/npm/bootstrap@5.2.1/dist/css/bootstrap.min.css" rel="stylesheet"
    integrity="sha384-iYQeCzEYFbKjA/T2uDLTpkwGzCiq6soy8tYaI1GyVh/UjpbCx/TYkiZhlZB6+fzT" crossorigin="anonymous">
  <link rel="stylesheet" href="styles.css" />

</head>

<body>

  <nav class="navbar navbar-expand-sm bg-dark navbar-dark">
    <div class="container-fluid">
      <ul class="navbar-nav">
        <li class="nav-item">
          <a class="nav-link active" href="#">Calculadora</a>
        </li>
      </ul>
    </div>
  </nav>
  <div class="container ">
    <div class="row m-5 bg-primary ">
      <div class="col-sm-4 "></div>
      <div class="col-sm-4 ">
              <div class="row p-5">
                <div class="col-sm-8 border ">
                  <form id="forma">
                    <div class="mb-3">
                      <label for="operandoA">Operando A</label>
                      <input type="number" class="form-control" placeholder="Escribir operando A" id="operandoA">
                    </div>
                    <div class="mb-3">
                      <label for="operandoB">Operando B</label>
                      <input type="number" class="form-control" placeholder="Escribir operando B" id="operandoB">
                    </div>
                    <div class="mb-3">
                      <label for="resultado">Resultado</label>
                      <input type="text" class="form-control" placeholder="0" id="resultado" disabled>
                    </div>            
                  </form>
                  <p id="error" class="text-danger"></p>
                </div>
                <div class="col-sm-4 border">
                  <button type="button" onclick="calcular(1)" class="btn btn-warning botones">+</button>
                  <button type="button" onclick="calcular(2)" class="btn btn-warning botones">-</button>
                  <button type="button" onclick="calcular(3)" class="btn btn-warning botones">*</button>
                  <button type="button" onclick="calcular(4)" class="btn btn-warning botones">/</button>
                </div>
        </div>
      </div>
      <div class="col-sm-4"></div>
    </div>
  </div>
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.1/dist/js/bootstrap.bundle.min.js"
    integrity="sha384-u1OknCvxWvY5kfmNBILK2hRnQC3Pr17a+RTT6rIHI7NnikvbZlHgTPOOmMi466C8"
    crossorigin="anonymous"></script>
  <script src="https://cdn.jsdelivr.net/npm/@popperjs/core@2.11.6/dist/umd/popper.min.js"
    integrity="sha384-oBqDVmMz9ATKxIep9tiCxS/Z9fNfEXiDAYTujMAeBAsjFuCZSmKbSSUnQlmh/jp3"
    crossorigin="anonymous"></script>
  <script src="https://cdn.jsdelivr.net/npm/bootstrap@5.2.1/dist/js/bootstrap.min.js"
    integrity="sha384-7VPbUDkoPSGFnVtYi0QogXtr74QeVeeIs99Qfg5YCF+TidwNdjvaKZX19NZ/e6oz"
    crossorigin="anonymous"></script>
</body>

</html>
```

**app.js**

```JavaScript

let calcular = (tipoOp) => {
    const forma = document.getElementById("forma");
    let operandoA = forma['operandoA'];
    let opernadoB = forma['operandoB'];
    operandoA = parseInt(operandoA.value);
    opernadoB = parseInt(opernadoB.value);
    let resultado = obtenerRta(tipoOp, operandoA, opernadoB);
    if(resultado!=-1){
      document.getElementById("error").style.display="none";
      forma['resultado'].value = resultado;
    }else{
        forma['resultado'].value = 0;
        document.getElementById("error").style.display="block";
        document.getElementById("error").innerHTML="Datos no validos";   
    }
}

let obtenerRta = (tipo, opA, opB) => {
    let resultado = 0;
    switch (tipo) {
        case 1:
            resultado = opA + opB;
            break;
        case 2:
            resultado = opA - opB;
            break;
        case 3:
            resultado = opA * opB;
            break;
        case 4:
            resultado = opA / opB;
            break;
    }
    if (isNaN(resultado)) {
        return -1;
    } else {
        return resultado;
    }

}
```

**sytles.css**

```Css
.botones{
   display: block;
   width: 50px;
   height: 50px;
   margin: 8px;  
   font-size: 25px;

}
```




