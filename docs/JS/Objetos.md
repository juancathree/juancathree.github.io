---
layout: default
title: Objetos
nav_order: 6
has_children: false
parent: JS
---

# Objetos
```js
const objeto = {};

const player = {
  name: "Manz",
  life: 99,
  power: 10,
};
```

## Propiedades
```js
const player = {};

// add
player.name = "Manz";
player.life = 99;
player.power = 10;

// get
console.log(player.name); 
```

## Metodos
```js
const user = {
  name: "Manz",
  talk: function() { return "Hola"; }
};

user.name;       // Es una variable (propiedad), devuelve "Manz"
user.talk();     // Es una función (método), se ejecuta y devuelve "Hola"
```
