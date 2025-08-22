---
tags: [Estrategias, Composición, Currificación, Memoización, Programación Funcional]
Creado: 
Relacionado: funciones_orden_superior_y_paradigmas_declarativos.md, canalizaciones_filtros.md
---

# Estrategias en Programación Funcional

## Composición de funciones
Permite construir funciones complejas a partir de funciones simples.
```js
const compose = (f, g) => x => f(g(x));
const doble = x => x * 2;
const sumarUno = x => x + 1;
const dobleMasUno = compose(sumarUno, doble);
console.log(dobleMasUno(3)); // 7
```

## Currificación
Transforma una función de varios argumentos en una secuencia de funciones de un solo argumento.
```js
const suma = a => b => a + b;
console.log(suma(2)(3)); // 5
```

## Memoización
Optimiza funciones costosas almacenando resultados previos.
```js
function memoizar(fn) {
  const cache = {};
  return function(x) {
    if (cache[x]) return cache[x];
    const resultado = fn(x);
    cache[x] = resultado;
    return resultado;
  };
}
const cuadrado = memoizar(x => x * x);
```

## Recursividad
Una función se llama a sí misma para resolver problemas complejos.
```js
const factorial = n => n <= 1 ? 1 : n * factorial(n - 1);
```

## Lazy evaluation (evaluación perezosa)
Evalúa valores solo cuando son necesarios.
```js
function* generador() {
  let i = 0;
  while (true) yield i++;
}
const gen = generador();
console.log(gen.next().value); // 0
console.log(gen.next().value); // 1
```

---
#### Referencias
a 