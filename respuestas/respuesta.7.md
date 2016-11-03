7. Escriba una función `sum` que funcione apropiadamente usando cualesquiera de las siguientes sintaxis:

```
console.log(sum(2, 3)); // result is 5
console.log(sum(2)(3)); // also 5
```

####Respuesta:

```
const sum = (a, b) => {
   if(b){
     return a + b;
   }
  else{
    return (b) =>  a + b;
  }

};
```