---
tags: closure, programación funcional, JavaScript
Creado: 2025-06-10
Relacionado: currying, funciones de orden superior
---

# Closure

Un closure en JavaScript es una función que recuerda el entorno en el que fue creada, es decir, tiene acceso a variables externas incluso después de que la función externa haya finalizado. Esto permite crear funciones con estado privado y es fundamental para técnicas como currying y aplicación parcial.

Ejemplo de closure:

```js
function outerFunction(x) {
  return function (y) {
    return x + y;
  };
}
const closureExample = outerFunction(5);
console.log(closureExample(3)); // 8
```

En este ejemplo, la función interna recuerda el valor de 'x' aunque la función externa ya terminó su ejecución.

---
#### Referencias
- Material de clase Semana 3, Programación 4, Universidad Jala 