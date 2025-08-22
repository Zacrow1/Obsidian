---
tags: funciones de orden superior, programación funcional, JavaScript
Creado: 2025-06-10
Relacionado: currying, composición de funciones, aplicación parcial
---

# Funciones de orden superior

Las funciones de orden superior son aquellas que pueden recibir otras funciones como argumentos o devolverlas como resultado. Este concepto es fundamental en la programación funcional y permite crear código más flexible y reutilizable. En JavaScript, las funciones de orden superior se utilizan para abstraer patrones de procesamiento de datos, como map, filter y reduce.

Por ejemplo, una función que recibe otra función como argumento:

```js
const isEven = num => num % 2 === 0;
const result = [1, 2, 3, 4].filter(isEven);
console.log(result); // [2, 4]
```

También pueden devolver funciones:

```js
const add = x => y => x + y;
const add10 = add(10);
console.log(add10(20)); // 30
```

Las funciones de orden superior permiten construir abstracciones poderosas, como la función reduce, que generaliza la acumulación de valores:

```js
const reduce = (reducer, initial, arr) => {
  let acc = initial;
  for (let i = 0; i < arr.length; i++) {
    acc = reducer(acc, arr[i]);
  }
  return acc;
};
console.log(reduce((acc, curr) => acc + curr, 0, [1, 2, 3])); // 6
```

---
#### Referencias
- Material de clase Semana 3, Programación 4, Universidad Jala 