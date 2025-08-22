---
tags: [Funciones, JavaScript, Callbacks, Ámbito]
Creado: 
Relacionado: estructuras_de_control.md, asincronia_y_callbacks.md, funcional_programming.md
---

# Funciones en JavaScript

## Declaración de funciones
```js
function saludar(nombre) {
  return 'Hola ' + nombre;
}
```

## Expresiones de función
```js
const sumar = function(a, b) {
  return a + b;
};
```

## Funciones flecha (arrow functions)
```js
const multiplicar = (a, b) => a * b;
```

## Parámetros y argumentos
```js
function mostrarDatos(nombre, edad = 18) {
  console.log(nombre, edad);
}
mostrarDatos('Ana');
```

## Ámbito de variables en funciones
Las variables declaradas dentro de una función solo existen ahí.

## Funciones como valores y callbacks
```js
function operar(a, b, operacion) {
  return operacion(a, b);
}
console.log(operar(2, 3, sumar));
```

---
#### Referencias
a 