---
tags: composición de funciones, programación funcional, JavaScript
Creado: 2025-06-10
Relacionado: programación tácita, refactorización, compose
---

# Composición de funciones en programación funcional

La composición de funciones es una técnica fundamental en la programación funcional que consiste en construir funciones grandes a partir de funciones pequeñas y reutilizables. Esto permite escribir código más modular, fácil de mantener y de probar. En JavaScript, la composición se logra encadenando funciones, de modo que la salida de una se convierte en la entrada de la siguiente.

Por ejemplo, usando una función compose:

```js
const compose = (f, g) => x => f(g(x));
const toUpper = str => str.toUpperCase();
const exclaim = str => str + '!';
const shout = compose(exclaim, toUpper);
console.log(shout('hola')); // 'HOLA!'
```

Esta técnica facilita la refactorización del código, permitiendo dividir tareas complejas en pasos simples y reutilizables.

---
#### Referencias
- Video: Composición, programación funcional en JavaScript, parte 7 