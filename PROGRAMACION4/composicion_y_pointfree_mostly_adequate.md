---
tags: composición de funciones, point-free, programación funcional, JavaScript
Creado: 2025-06-10
Relacionado: currying, funciones de orden superior
---

# Composición de funciones y programación point-free (Según Mostly Adequate Guide)

La composición de funciones consiste en encadenar funciones pequeñas para crear funciones más complejas, permitiendo que la salida de una sea la entrada de la siguiente. En JavaScript, esto se logra con la función `compose`:

```js
const compose = (f, g) => x => f(g(x));
const toUpperCase = x => x.toUpperCase();
const exclaim = x => `${x}!`;
const shout = compose(exclaim, toUpperCase);
console.log(shout('hola')); // 'HOLA!'
```

La programación point-free es un estilo donde se evita nombrar los argumentos intermedios, componiendo funciones directamente:

```js
// Pointful
const shout = str => exclaim(toUpperCase(str));
// Point-free
const shout = compose(exclaim, toUpperCase);
```

Este enfoque hace el código más declarativo y reutilizable, aunque puede dificultar la lectura si se abusa de él. La composición es asociativa y respeta la identidad, conceptos tomados de la teoría de categorías.

Más detalles y ejemplos en el capítulo 5 de Mostly Adequate Guide: [https://mostly-adequate.gitbook.io/mostly-adequate-guide/ch05](https://mostly-adequate.gitbook.io/mostly-adequate-guide/ch05)

---
#### Referencias
- Mostly Adequate Guide, Capítulo 5: Coding by Composing 