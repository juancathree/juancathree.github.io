---
layout: default
title: Modulos
nav_order: 10
has_children: false
parent: JS
---

# Modulos

## Exportar
```js
export let number = 42;                  // Se añade la variable number al módulo
export const hello = () => "Hello!";     // Se añade la función hello al módulo
export class CodeBlock { };              // Se añade la clase vacía CodeBlock al módulo

export { number };                   // Se crea un módulo y se añade number
export { hello as greet };           // Se añade otroNombre al módulo
export {
  number,
  hello as greet
};
export default number;
```

## Importar
```js
import { nombre } from "./file.js";
import { brand as brandName } from "./file.js";
import nombre from "./math.js";
import * as module from "./file.js";

import { Howler, Howl } from "howler";  // Bare import ( instalado con npm)
```

## Dynamics import
```js
import("./module.js")                   // Dynamic import
  .then(data => { /* ... */ });

// Opción 1: Se carga functions.js si se cumple la condición
if (number > 42) {
  import("./functions.js")
    .then(module => module.func());
}

// Opción 2: Se carga functions.js interpolando la constante
const filename = "functions";
import(`./${filename}.js`)
  .then(module => module.func());

// Opción 3: Se carga aditional.js sólo si el usuario hace click en el botón
const button = document.querySelector("button.info");
button.addEventListener("click", () => import("aditional.js"), { once: true });
```

## Import maps
Para porder utilizar bare imports.
```js
{
  "imports": {
    "dayjs": "/node_modules/dayjs/esm/dayjs.js",
    "lodash": "/node_modules/lodash-es/lodash.js"
  }
}
```
