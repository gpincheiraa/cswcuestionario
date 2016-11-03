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

####Respuesta:

La invocacion de test produce:

```
undefined
2
```

**Explicación**: 
Cuando se invoca a test, en su execution context se inicializa bar y la funcion foo. Luego se empieza a ejecutar la función, la linea console.log(bar), imprime undefined, ya que bar fue inicializado pero aun no se le ha asignado el valor **1**, y luego el segundo console.log(foo()), invoca la funcion foo, la que devuelve 2 directo al console log, imprimiendo 2.


