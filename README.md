# Ejercicio 1
### Código inicial
```js
var num2 = 0;
function suma(num1) {
	return function() {
		return num1 + num2;
	}
} 
var suma2 = suma(2);
console.log(suma2(5)); // Debería mostrar 7 de resultado
var suma12 = suma(12);
console.log(suma12(76)) // Debería mostrar 88 de resultado.
```

### Solución planteada 
```js
function suma(num1) {
	return function(num2) {
		return num1 + num2;
	}
} 
var suma2 = suma(2);
console.log(suma2(5));
var suma12 = suma(12);
console.log(suma12(76))
```
Tenemos una función anónima con dentro de otra función (un clousure), por lo que se está tomando la variable global "var num2 = 0", entonces lo que haremos es borrarla  y espedificarla como parámetro el la función anónima para que así tome directamente los valores que se le otorga al último.
