6. Cuál es la salida del siguiente código? Explique por qué ocurre.

```
console.log(0.1 + 0.2 === 0.3);
```

####Respuesta
Esto tiene que ver con la precision con la que se manejan los float en Javascript,
esto hace que al evaluar `0.1 + 0.2` produzca `0.30000000000000004` lo que es distinto a `0.3`.

