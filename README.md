# Actvidades para practicar las API de HTML5
Actividades Html5 

## Utilización de  WebStorage
> Crea una aplicacion TO-DO en el que dispongamos de una ventana con un TextBox donde iremos añadiendo nuestras tareas ha realizar  y un botón para añadirlas.
> Debajo de la misma aparecera el listado de las tareas añadidas, similar al comportamiento que se puede ver en  [ToDo](http://todomvc.com/examples/jquery/#/all).
>Condiciones que debe de cumplir.
* Las tareas deben almacenarse en el localStorage.
* Para almacenar se debe cuantificar las existentes en el localStorage y sumarle una para establecer  en el par que se almacena en el localstorage la key de ellas. Por ejemplo si existen dos ya la siguiente se almacenará de la siguiente forma: { '3','[Tarea ha realizar]'}
* Se creará un botón de borrado de todas  a la vez.
* Se comprobará que no existe nada más almacenado en el localstorage la primera vez que se ejecuta la aplicación. en el caso de existir deberá lanzarse un mensaje que pregunte si quiere eliminarlo, de esta manera nos aseguramos de que en la primera ejecución no hay nada que ensuce la aplicación.
* Se debe utiliza BootStrap y Jquery para la ejecución de la actividad.

## Utilización de WebWorkers
> Crea una aplicación para calcular una serie de Fibonacci a partir de un WebWorker, para ello le pediremos el número de iteraciones y el resultado será presentado en pantalla, el algoritmo utilizado:
```javascript
 
 function calcularFibonacci(valor)
 {
    var i, 
    fibo = 1, 
    fibo2 = 1, 
    for(i = 0; i < valor; i++) { 
       fibo = fibo + fibo2; 
       fibo2 = fibo - fibo2; 
       return fibo; 
    }
}
```
> El webWorker devolverá un array que presentará en pantalla dando la relación
