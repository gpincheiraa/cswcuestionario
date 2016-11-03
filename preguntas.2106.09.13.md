Gracias por tomarte el tiempo de responder nuestro cuestionario. Cuando
termines, por favor envíalo a la siguiente dirección de mail:

**contacto@csw.cl**


1. Qué imprime la función `test()` y por que?

```
function test() {
   console.log(bar);
   console.log(foo());

   var bar = 1;
   function foo() {
      return 2;
   }
}

test();
```

2. Qué imprime lo siguiente?. Por qué?

```
console.log(false == '0');
console.log(false === '0');
```

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

4. Implementa la funcion idGenerator de modo que se comporte de la siguiente manera:

```
var gen1 = idGenerator();
var gen2 = idGenerator();

console.log(gen1()); // prints 1
console.log(gen2()); // prints 1
console.log(gen1()); // prints 2
console.log(gen2()); // prints 2
console.log(gen1()); // prints 3
console.log(gen2()); // prints 3
```

5. Qué es `NaN`? Cuál es su tipo? Cómo puedes testear apropiadamente si un valor es igual a `NaN`?

6. Cuál es la salida del siguiente código? Explique por qué ocurre.

```
console.log(0.1 + 0.2 === 0.3);
```

7. Escriba una función `sum` que funcione apropiadamente usando cualesquiera de las siguientes sintaxis:

```
console.log(sum(2, 3)); // result is 5
console.log(sum(2)(3)); // also 5
```

8. Cómo podrías usar `Math.max()` para encontrar el valor máximo en un arreglo?

9. Por qué aparecen `NaN`s en la línea con `parseInt` y cómo lo arreglarías?

```
['1', '2', '3'].map(parseFloat); // [ 1, 2, 3 ]
['1', '2', '3'].map(parseInt); // [ 1, NaN, NaN ]
```

10. Convierta el siguiente código usando ES6:

```
//
function foo (bar) { 
  var zee = ("undefined" !== typeof bar) ? bar : "default"; 
  return zee;
} 

//
var obj = {
  name: "Josefa",

  logHello: function (friendsArray) {
    friendsArray.forEach(function (friend) {
      console.log(this.name + " says hello to " + friend);
    }.bind(this));
  }
}

var friends = ["Pepa", "Pepe", "Pepo"];
obj.logHello(friends);

//
var obj1 = { uno: 1, dos: 2};
var obj2 = {tres: 3, cuatro: 4};
var obj3 = {cinco: 5, seis: 6};
var allObjs = {};
[obj1, obj2, obj3].forEach(function (o) {
  Object.keys(o).forEach(function (property) {
  allObjs[property] = o[property];
  });
});

//
function buildSquareInvader(options) {
  var colors = {
    red: "#ff0000",
    green: "#00ff00",
    blue: "#0000ff",
  };

  // create some local variables for better legibility
  var color = options.color;
  var height = options.height;
  var width = options.width

  return {
    color: colors[color],
    size: width * height,
  };
}

//
var a = [1, 2, 3];
var b = [4, 5, 6];
var allArrayItems = [];
for (var i = 0; i < a.length; i++) {
  allArrays.push(a[i]);
}

for (var i = 0; i < b.length; i++) {
  allArrays.push(b[i]);
}
```

11. Considerando la escala del 1 al 3:

  1. no sé nada
  2. hice un tutorial o leí al respecto
  3. lo uso habitualmente

Cómo te evaluariás en lo siguiente, puedes comentar:

- nodejs
- npm
- browserify
- underscore / lodash / ramda
- mocha
- jquery
- twitter bootstrap
- express
- leaflet
- grunt
- git

Otras bibliotecas, tecnologías o utilitarios que desees mencionar? Califícate usando la escala.