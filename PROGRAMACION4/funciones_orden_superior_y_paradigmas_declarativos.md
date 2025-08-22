---
tags: [Funciones de Orden Superior, Declarativo, JavaScript, Programación Funcional]
Creado: 
Relacionado: introduccion_a_es6_y_funcional.md, estrategias_funcional.md
---

# Funciones de Orden Superior y Paradigmas Declarativos

## ¿Qué es una función de orden superior?
Una función de orden superior es aquella que recibe una o más funciones como argumento y/o devuelve una función como resultado.

### Ejemplo básico
```js
const aplicarOperacion = (a, b, operacion) => operacion(a, b);
const suma = (x, y) => x + y;
console.log(aplicarOperacion(2, 3, suma)); // 5
```

## Paradigmas Declarativos
En la programación declarativa, se describe el "qué" se quiere lograr, no el "cómo". JavaScript permite escribir código declarativo usando funciones como map, filter y reduce.

### Ejemplo de código imperativo vs declarativo
```js
// Imperativo
let resultado = [];
for (let i = 0; i < 5; i++) {
  resultado.push(i * 2);
}
// Declarativo
const resultado2 = [0,1,2,3,4].map(x => x * 2);
```

## Composición de funciones
Permite encadenar funciones para crear flujos de procesamiento de datos.
```js
const agregarUno = x => x + 1;
const duplicar = x => x * 2;
const procesar = x => duplicar(agregarUno(x));
console.log(procesar(3)); // 8
```

## Aplicaciones prácticas
- Validación de datos
- Procesamiento de colecciones
- Middleware en frameworks como Express 

---
#### Referencias
a 