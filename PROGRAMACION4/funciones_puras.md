Este video explica las funciones puras e impuras en JavaScript [00:00:07].

El video cubre los siguientes puntos:

* **Tipos de datos en JavaScript** [00:00:33]:
    * **Simples o primitivos**: Guardan valores atómicos, como números, flotantes, caracteres y booleanos [00:00:59].
    * **Compuestos o estructurados**: Albergan más de un elemento, como arreglos, cadenas de caracteres y objetos. Estos se pasan por referencia [00:01:24].

* **Paso por referencia** [00:01:43]:
    * Se explica cómo JavaScript maneja la memoria para los tipos de datos primitivos y compuestos [00:01:50].
    * Cuando se llama a una función con un tipo de dato primitivo, se crea una copia del valor [00:06:23].
    * Cuando se llama a una función con un tipo de dato compuesto (como objetos o arreglos), se toma la dirección de memoria del objeto original, lo que significa que cualquier modificación dentro de la función afectará al objeto original [00:06:45].

* **Funciones impuras** [00:10:16]:
    * Son funciones que modifican el objeto original que se les pasa como argumento. El video demuestra esto con un ejemplo donde se agrega una propiedad a un objeto o un elemento a un arreglo, y el objeto/arreglo original se ve afectado [00:09:18].

* **Funciones puras** [00:10:16]:
    * Para que una función sea pura, no debe modificar el objeto original [00:10:23].
    * La solución es crear una copia del objeto o arreglo que se recibe como argumento antes de realizar cualquier modificación. Esto se puede hacer utilizando el operador `spread` [00:10:40]. De esta manera, la función devuelve un nuevo objeto/arreglo con los cambios, mientras que el original permanece inalterado [00:11:19].

---

## Explicación técnica: ¿Qué es una función pura en JavaScript?

Una **función pura** es una función que, dada la misma entrada, siempre devuelve la misma salida y no produce efectos secundarios observables fuera de su ámbito. Es decir, no modifica variables externas, no altera los argumentos que recibe (si son objetos o arreglos), ni interactúa con el entorno externo (como la consola, archivos, bases de datos, etc.).

### Características de una función pura

1. **Determinismo**: Siempre que se le pasen los mismos argumentos, devuelve el mismo resultado.
2. **Sin efectos secundarios**: No modifica nada fuera de su propio ámbito, ni variables globales, ni los objetos/arreglos recibidos como argumento.

### Ejemplo de función impura

```javascript
function agregarElementoImpuro(arr, elemento) {
    arr.push(elemento); // Modifica el arreglo original
    return arr;
}

const original = [1, 2, 3];
const resultado = agregarElementoImpuro(original, 4);
// original ahora es [1, 2, 3, 4] (¡fue modificado!)
```

En este ejemplo, la función es impura porque modifica el arreglo original recibido como argumento.

### Ejemplo de función pura

Para que una función sea pura, debe evitar modificar los argumentos originales. En el caso de objetos o arreglos, esto se logra creando una copia antes de realizar cualquier cambio. En JavaScript, una forma común de hacerlo es usando el operador **spread** (`...`):

```javascript
function agregarElementoPuro(arr, elemento) {
    return [...arr, elemento]; // Crea un nuevo arreglo, no modifica el original
}

const original = [1, 2, 3];
const resultado = agregarElementoPuro(original, 4);
// original sigue siendo [1, 2, 3]
// resultado es [1, 2, 3, 4]
```

Aquí, la función es pura porque no altera el arreglo original, sino que devuelve uno nuevo con el cambio.

### ¿Por qué son importantes las funciones puras?

- **Predecibilidad**: Son más fáciles de razonar y probar, ya que su salida depende solo de sus entradas.
- **Facilitan el testing**: No dependen del estado externo ni lo modifican.
- **Ayudan en la programación funcional**: Permiten componer funciones y trabajar con datos inmutables.

### Resumen técnico

- Los **tipos de datos primitivos** (números, booleanos, strings) se pasan por valor, por lo que no hay riesgo de modificar el original.
- Los **tipos de datos compuestos** (objetos, arreglos) se pasan por referencia, por lo que una función impura puede modificar el original.
- Para mantener la pureza, se debe crear una copia antes de modificar objetos o arreglos, usando técnicas como el operador spread (`...`), `Object.assign`, o métodos como `slice()` para arreglos.