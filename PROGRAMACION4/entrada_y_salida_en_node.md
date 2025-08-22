---
tags: [Node.js, Entrada, Salida, Archivos, JavaScript]
Creado: 
Relacionado: asincronia_y_callbacks.md, estructuras_de_control.md
---

# Entrada y Salida en Node.js

## Leer y escribir en consola
```js
console.log('Mensaje en consola');

const readline = require('readline');
const rl = readline.createInterface({
  input: process.stdin,
  output: process.stdout
});
rl.question('¿Cómo te llamas? ', (nombre) => {
  console.log(`Hola, ${nombre}`);
  rl.close();
});
```

## Leer y escribir archivos
```js
const fs = require('fs');
fs.writeFileSync('saludo.txt', 'Hola mundo');
let contenido = fs.readFileSync('saludo.txt', 'utf8');
console.log(contenido);
```

---
#### Referencias
a 