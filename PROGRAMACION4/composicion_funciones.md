---
tags: composición de funciones, programación funcional, JavaScript
Creado: 2025-06-10
Relacionado: currying, funciones de orden superior
---

# Composición de funciones

La composición de funciones consiste en combinar dos o más funciones para crear una nueva función, donde el resultado de una función se convierte en el argumento de la siguiente. En notación matemática, F∘G significa F(G(x)).

Ejemplo sencillo:

```js
function double(x) { return x * 2; }
function square(x) { return x * x; }
const compose = (f, g) => x => f(g(x));
const doubleThenSquare = compose(square, double);
console.log(doubleThenSquare(3)); // 36
```

Para componer varias funciones:

```js
const compose = (...functions) => arg => functions.reduceRight((result, fn) => fn(result), arg);
const double = x => x * 2;
const square = x => x * x;
const subtractTen = x => x - 10;
const combined = compose(subtractTen, square, double);
console.log(combined(5)); // 90
```

La composición permite construir operaciones complejas a partir de funciones simples, facilitando la reutilización y claridad del código.

---
#### Referencias
- Material de clase Semana 3, Programación 4, Universidad Jala 