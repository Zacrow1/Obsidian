---
tags: [Asincronía, Callbacks, Promesas, JavaScript]
Creado: 
Relacionado: funciones.md, entrada_y_salida_en_node.md
---

# Asincronía y Callbacks en JavaScript

## Callbacks
```js
function saludarDespues(nombre, callback) {
  setTimeout(() => {
    callback(`Hola, ${nombre}`);
  }, 1000);
}
saludarDespues('Ana', mensaje => console.log(mensaje));
```

## Promesas
```js
function promesaSaludo(nombre) {
  return new Promise((resolve, reject) => {
    if (nombre) {
      resolve(`Hola, ${nombre}`);
    } else {
      reject('Nombre no proporcionado');
    }
  });
}
promesaSaludo('Juan').then(console.log).catch(console.error);
```

## async/await
```js
async function main() {
  try {
    let mensaje = await promesaSaludo('Lucía');
    console.log(mensaje);
  } catch (e) {
    console.error(e);
  }
}
main();
```

---
#### Referencias
a 