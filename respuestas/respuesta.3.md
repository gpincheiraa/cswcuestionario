3. Se pretende realizar una cuenta regresiva en pantalla estilo *NASA*.
   **Explica** por qué la siguiente función está incorrecta, arréglala y luego
   modifícala para que reciba además un parámetro extra `maxCount` que indique
   desde qué número comenzar a contar.

```
function doRegressiveCountAndLaunch(launchingFunction) {
  for (var n = 9; n > 0; n--) {
      setTimeout(function () {
         console.log(n);
      }, 1000);
   }
   launchingFunction();
}

doRegressiveCountAndLaunch(() => console.log('Launch!'));
```

####Respuesta:

**Explicacion**:
El setTimeout en este caso es ejecutado al final, cuando en el **local** execution context
ya ha ejecutado todo, por lo que el for tambien ya fue ejecutado. La variable n llegó a 0
y ahi rompió el ciclo. Para cuando setTimeout se ejecuta, gracias al closure que se forma, 
puede acceder al valor de n, siendo este 0 para ese entonces. 

**Fixing**:

```
function doRegressiveCountAndLaunch(launchingFunction, maxCount) {
  var n = maxCount !== undefined  ?  maxCount : 9;
  var timeoutFn = setTimeout(() => {
      if(n > 0){
        console.log(n);
        doRegressiveCountAndLaunch(launchingFunction, n - 1); 
      }else{
        launchingFunction();
        clearTimeout(timeoutFn);
      }
  }, 1000);
}
doRegressiveCountAndLaunch(() => console.log('Launch!'), 10);
```