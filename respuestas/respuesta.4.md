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

**Respuesta**: [Ejemplo funcionando](https://jsbin.com/hutova/edit?js,console)

```
const idGenerator = () => {
  var n = 1;
  return function(){
    return n++;
  }
};
```
