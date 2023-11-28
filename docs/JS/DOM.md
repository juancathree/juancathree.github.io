---
layout: default
title: DOM
nav_order: 12
has_children: false
parent: JS
---

# DOM
Las siglas DOM significan Document Object Model, o lo que es lo mismo, la estructura del documento HTML.

## Seleccionar elementos
```js
const page = document.getElementById("page");   // <div id="page"></div>

const items = document.getElementsByClassName("item");  // [div, div, div]
console.log(items[0]);      // Primer item encontrado: <div class="item"></div>

// Obtiene todos los elementos con atributo name="nickname"
const nicknames = document.getElementsByName("nickname");  // [input]

// Obtiene todos los elementos <div> de la página
const divs = document.getElementsByTagName("div");         // [div, div, div]

const page = document.querySelector("#page");               // <div id="page"></div>
const info = document.querySelector(".main .info");         // <div class="info"></div>

// Obtiene todos los elementos con clase "info"
const infos = document.querySelectorAll(".info");

const links = document.querySelectorAll("#menu a");
```
