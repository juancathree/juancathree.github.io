---
layout: default
title: Funciones
nav_order: 3
has_children: false
parent: JS
---

# Funciones

## Funciones por declaracion
```js
function saludar() {
  return "Hola";
}

saludar(); // 'Hola'
```

## Funciones por expresion
```js
const saludo = function saludar() {
  return "Hola";
};

saludo(); // 'Hola'
```

## Funciones anonimas
```js
const saludo = function () {
  return "Hola";
};

saludo(); // 'Hola'
```

## Callbacks
```js
const fB = function () {
  console.log("Función B ejecutada.");
};

const fA = function (callback) {
  callback();
};

fA(fB);
```

## Autoejecutables
```js
// Función autoejecutable
(function () {
  console.log("Hola!!");
})();

// Función autoejecutable con parámetros
(function (name) {
  console.log(`¡Hola, ${name}!`);
})("Manz");
```

## Arrow functions
Una buena práctica es utilizar funciones tradicionales como las funciones de primer nivel y, luego, en su interior o en callbacks, utilizar funciones flecha.

```js
const func = () => {
  return "Función flecha.";
};

const func = () => "Función flecha."; // 0 parámetros: Devuelve "Función flecha"
const func = (e) => e + 1; // 1 parámetro: Devuelve el valor de e + 1
const func = (a, b) => a + b; // 2 parámetros: Devuelve el valor de a + b
```
