---
tags: [Canalizaciones, Filtros, Procesamiento de Datos, Programación Funcional]
Creado: 
Relacionado: estrategias_funcional.md, mapeo_reduccion_tecnicas.md
---

# Canalizaciones y Filtros de Procesamiento de Datos

## ¿Qué es una canalización (pipeline)?
Es una secuencia de funciones donde la salida de una es la entrada de la siguiente, facilitando el procesamiento de datos de forma declarativa.

### Ejemplo básico
```js
const pipeline = (...fns) => x => fns.reduce((v, f) => f(v), x);
const doble = x => x * 2;
const sumarTres = x => x + 3;
const procesar = pipeline(doble, sumarTres);
console.log(procesar(4)); // 11
```

## Filtros
Permiten seleccionar datos que cumplen una condición.
```js
const numeros = [1,2,3,4,5,6];
const pares = numeros.filter(n => n % 2 === 0);
console.log(pares); // [2,4,6]
```

## Uso en procesamiento de datos
- Transformar, filtrar y reducir colecciones de datos de manera encadenada.
- Ejemplo real: procesamiento de logs, datos de sensores, etc. 

---
#### Referencias
a 