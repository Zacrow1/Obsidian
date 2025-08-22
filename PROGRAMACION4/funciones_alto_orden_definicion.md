---
tags: funciones de alto orden, high order functions, JavaScript, programación funcional
Creado: 2025-06-10
Relacionado: map, filter, funciones de orden superior
---

# Definición de funciones de alto orden

Las funciones de alto orden (high order functions) son aquellas que pueden recibir otras funciones como argumentos o devolverlas como resultado. Son fundamentales en JavaScript y permiten crear abstracciones poderosas.

Ejemplo de función de alto orden:

```js
const onLess = (a, b, fn) => (a < b ? fn(a, b) : undefined);
onLess(2, 5, (x, y) => console.log(`${x} es menor que ${y}`));
// 2 es menor que 5
```

También son comunes funciones como filter:

```js
const isEven = n => n % 2 === 0;
console.log([1, 2, 3, 4].filter(isEven)); // [2, 4]
```

---
#### Referencias
- Video: ¿Qué son las High Order Functions en Javascript? 