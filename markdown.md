# Function-scope-js

****
 **scope** 
 - El scope es el alcance de una variable, puede ser de dos tipos, global y local.

      *Una variable cuyo scope es global*.
        - **Ejemplo:**
     
    ```js 
     var a = 1;
     function global() {
        console.log(a);
     }

     global();
     console.log(a);
    ```
      *Una variable cuyo scope es local*.
        - **Ejemplo:**
     
    ```js 
    function local() {
      var a = 2;
      console.log(a);
    }
    local();
    console.log(a);     
    ```


1. **Variables globales**
 - Son aquella que no estan dentro de una funcion.
 - Todos nuestros elementos tienen acceso a ella.
 - Tiene que estar declaradas fuera de la funcion.
 
     **Existen seis variables globales porque se encuentra fuera de una funcion**

 ```js 
  var $inputCard = $('#card-number');// linea 6
  var $inputMonth = $('.input-month');// linea 7
  var $inputYear = $('.input-year');// linea 8
  var $buttonNext = $('#next');// linea 9
  var regexOnlyNumbers = /^[0-9]+$/;// linea 10
  var labelErrorOrSuccessMessages = $('label[for="card-number"]');// linea 12

```

2. **Variables locales**
  - Que esta dentro de una funcion
  
 ```js 
   var regex = /^[0-9]+$/;//linea 37
   var creditCardNumber = soloNumeros(longitud(numberCard));// linea 45
   var arr = [];//linea 47
   var sumaTotal = 0;//linea 48
   var index = creditCardNumber.length - 1//linea 49
```
3. **funciones Global**
- Solo podemos ver una funcion global
 ```js 
 $(document).ready(function() {]);//linea 1
  
```

4. **funciones Local**

 ```js 
 //Existe una funcion que esta dentro del evento input
 $inputCard.on('input', function() {});//linea 14
 function activeButton() {};//linea 19
 function desactiveButton() {};// linea 24
 function longitud(input) {};// linea 29
 function soloNumeros(input) {};// linea 36
 function isValidCreditCard(numberCard) {};// linea 44
  
```
5. **funciones de callback**

 ```js 
  
```

6. **funciones expresions**

 ```js 
  
```
7. **funciones statement**
- 
 ```js 
  
```
8. **clousure**

 ```js 
  
```

9. **contextos de ejecucion** 

 ```js 
  
```
10. **funciones forman parte de la pila de ejecucion (stack execution)** 

 ```js 
  
```
11. **funciones forman parte de la cola de eventos (event queue)**

 ```js 
  
```