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
