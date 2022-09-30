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
