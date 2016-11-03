2. Qué imprime lo siguiente?. Por qué?

```
console.log(false == '0');
console.log(false === '0');
```

####Respuesta:

El primer console log, imprime true, ya que se hace una comparación no estricta
No tengo claro la prioridad de cohercion pero, el string '0', coherce a false 
(se puede comprobar con Boolean('0')), luego se comparan false con false lo que produce true.

Al contrario en el segundo console log, se hace una comparacion stricta que impide la cohercion
y compara no solo el valor, si no tambien el tipo de datos.