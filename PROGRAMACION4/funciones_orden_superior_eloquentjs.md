---
tags: funciones de orden superior, programación funcional, JavaScript
Creado: 2025-06-10
Relacionado: currying, composición de funciones
---

# Funciones de orden superior (Según Eloquent JavaScript)

Las funciones de orden superior son aquellas que pueden recibir otras funciones como argumentos o devolverlas como resultado. Son fundamentales en JavaScript y permiten crear abstracciones poderosas para manipular datos y controlar el flujo del programa.

Ejemplo clásico:

```js
function greaterThan(n) {
  return m => m > n;
}
const greaterThan10 = greaterThan(10);
console.log(greaterThan10(11)); // true
```

También se usan para crear utilidades como map, filter y reduce:

```js
const numbers = [1, 2, 3, 4];
const even = numbers.filter(n => n % 2 === 0);
console.log(even); // [2, 4]
```

Más detalles y ejemplos en el capítulo 5 de Eloquent JavaScript: [https://eloquentjavascript.net/05_higher_order.html](https://eloquentjavascript.net/05_higher_order.html)

---
#### Referencias
- Eloquent JavaScript, Capítulo 5: Higher-order Functions 