9. Por qué aparecen `NaN`s en la línea con `parseInt` y cómo lo arreglarías?

```
['1', '2', '3'].map(parseFloat); // [ 1, 2, 3 ]
['1', '2', '3'].map(parseInt); // [ 1, NaN, NaN ]
```

####Respuesta

parseFloat, solo acepta un argumento, por lo que la salida es correcta.

Sin embago parseInt recibe dos parametros, *string* y *base*, mientras que map, llama al callback que se le pasa con 3 parametros *currentValue*, *index*, *array*.

Por lo tanto en el stack de llamados en map se esta produciendo lo siguiente:

```
parseInt('1', 0); // Que produce 1
parseInt('2', 1); // Que produce NaN
parseInt('3', 2); // Que produce NaN
```

1 es valido en base decimal, que se intuyó desde el string '1'
2 no es un numero valido en base 1
3 tampoco es valido como numero binario.

**Para esta respuesta me apoyé en la [documentación](https://developer.mozilla.org/es/docs/Web/JavaScript/Referencia/Objetos_globales/parseInt)*** 
