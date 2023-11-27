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

## JSON
```js
// JSON a objeto
const json = `{
  "name": "Manz",
  "life": 99
}`;

const user = JSON.parse(json);

// objeto a JSON
const user = {
  name: "Manz",
  life: 99,
  talk: function () {
    return "Hola!";
  },
};

JSON.stringify(user);
```

## Destructuracion
```js
const user = {
  name: "Manz",
  role: "streamer",
  life: 99
}

const { name, role, life } = user;
const { name, role: type, life } = user;
const { name, role = "normal user", life } = user;

// Reestructurando
const user = {
  name: "Manz",
  role: "streamer",
  life: 99
}

const fullUser = {
  ...user,
  power: 25,
  life: 50
}

// Copia sin referencia
const user = {
  name: "Manz",
  role: "streamer",
  life: 99,
  features: ["learn", "code", "paint"]
}

const fullUser = {
  ...structuredClone(user),
  power: 25,
  life: 50
}
```

## Iteradores
```js
const animals = ["Gato", "Perro", "Burro", "Gallo", "Ratón"];

Object.keys(animals);     // [0, 1, 2, 3, 4]
Object.values(animals);   // ["Gato", "Perro", "Burro", "Gallo", "Ratón"]
Object.entries(animals);  // [[0, "Gato"], [1, "Perro"], [2, "Burro"], [3, "Gallo"], [4, "Ratón"]]

// convertir array en objeto
const keys = ["name", "life", "power", "talk"];
const values = ["Manz", 99, 10, function() { return "Hola" }];

const entries = values.map((value, index) => [keys[index], value]);
const user = Object.fromEntries(entries);
```
