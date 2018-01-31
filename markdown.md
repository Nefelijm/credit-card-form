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
 -Se da cuando llamo a una funcion y le envio por parametro otra funcion un callback) esperando que la función que llamé se encargue de ejecutar esa función.
 ```js 
  $inputCard.on('input', function() {
    isValidCreditCard($(this).val().trim());
  });//Linea 14-15

 function longitud(input) {
  if (input.trim().length === 16) {
    return input;//linea 29-30
  }
 }

function soloNumeros(input) {
  var regex = /^[0-9]+$/;
  if (regex.test(input)) {
    return input;
  }
 }//Linea 36-41
  
```

6. **funciones expresions**
    - Una expresión siempre devuelve un valor como resultado

7. **funciones statement**
    - Una sentencia realiza alguna acción
 ```js 
     function activeButton() {};//linea 19
     function desactiveButton() {};// linea 24
     function longitud(input) {};// linea 29
     function soloNumeros(input) {};// linea 36
     function isValidCreditCard(numberCard) {};// linea 44
  
```


8. **funciones forman parte de la pila de ejecucion (stack execution)** 
 - Son Aquellas funciones que primero se crea en el contexto de ejecucion Global para luego formar hacer parte d ela pila de ejecucion.

 ```js 
     function activeButton() {};//linea 19
     function desactiveButton() {};// linea 24
     function longitud(input) {};// linea 29
     function soloNumeros(input) {};// linea 36
     function isValidCreditCard(numberCard) {};// linea 44
  
```
9. **funciones forman parte de la cola de eventos (event queue)**
- Espera que la pila este vacia para que esta empiece a ejecutarse (Entra los que estaban en la cola para ser parte d ela pila).
 ```js 
  $inputCard.on('input', function() {});
	//linea 14
```

Alumna: Joñoruco Morales Nefeli