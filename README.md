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
---
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

---
## Utilización de la propiedad Drag&Drop
>Vamos a crear nuestro propio reproductor de SoundCloud, para ello vamos a utilizar la potencia de la api de SoundCloud para buscar canciones y reproducirlas, el reproductor base nos mostrará un formulario donde nos solictará el artista a buscar, y nos mostrará un listado de caractulas en miniatura de los resultados, estos podrán ser arrastrados  aún contenedor que mostrará la carátula en grande y pondrá en marcha la música.

### Condiciones
Debemos crear una cuenta en SoundClud para obtener un ClientId para poder acceder a la API, para ello una vez registrados y logueados en la plataforma ponemos en marcha cualquier reproductor de soundCloud abrimos las herramientas de desarrollo y buscamos el siguiente link https://api.soundcloud.com/tsub/subscribe?registrationID=  al final dispondremos de un parametro denominada client_id y lo copiamos es nuestro id de cliente.
Disponéis de las referencias al SDK de SoundCloud:
https://developers.soundcloud.com/docs/api/sdks

De los cuales y más importantes son:
Inicializaión de SoundCloud en:

```javascript
SC.initialize({
	client_id: [client-id]
});
```
Para la búsqueda de canciones por autor
```javascript
SC.get('/tracks',{
	q:autor}).then(function(tracks){
  \\Aquí realizamos todo el proceso de dibujo en pantalla de las caratulas.
 }
 ```
 Para obtener informacion de la canción y poner en marcha el reproductor
 ```javascript
 SC.stream('/tracks/'+id).then(function(player){
			//console.log('canción' + JSON.stringify(player));
			player.play();
		}).catch(function(error){
			alert('Error :'+error.message);
		});
  ```
  A partir de estas especificaciones podéis investigar y añadir nuevas funcionalidades.
  
  ---
  ## Utilización de la geolocalización
  >Vamos a crear una aplicación para geolocalizarnos para ello presentaremos en un mapa de google maps nuestra posición.
  ### Características.
  >Utilizando la api de HTML5 localizaremos nuestra posición para colocarnos en pantalla utilizaremos la siguiente petición a la api de google maps.
  ```javascript
  http://maps.googleapis.com/maps/api/staticmap?center=" + latitude + "," + longitude + "&zoom=13&size=300x300&sensor=false"
  ```
 
