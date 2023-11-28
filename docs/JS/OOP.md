---
layout: default
title: OOP
nav_order: 11
has_children: false
parent: JS
---

# OOP

## Clases
```js
class Animal {
  // Propiedades
  name;
  type;

  constructor(name) {
    this.name = name;   // Hacemos referencia a la propiedad name del objeto instanciado
  }

  // Métodos
  hablar() {
    return "Odio los lunes."
  }
}

const pato = new Animal("Donald");
```

## Visibilidad propiedades
```js
class Personaje {
  #name; // privada
  energy = 10;

  constructor(name) {
    this.#name = name;
  }
}
```

## Getters y setters
```js
class Personaje {
  name;
  energy;

  constructor(name, energy = 10) {
    this.name = name;
    this.energy = energy;
  }

  get status() {
    return '⭐'.repeat(this.energy);
  }

  set status(stars) {
    this.energy = stars.length;
  }
}
```

## Metodos
```js
class Animal {
  static despedirse() {
    return "Adiós";
  }

  hablar() {
    return "Cuak";
  }
}

Animal.despedirse();        // Método estático (no requiere instancia): 'Adiós'
Animal.hablar();            // Uncaught TypeError: Animal.hablar is not a function

// el bloque estático static {} se ejecuta nada más declarar la clase
class Animal {
  static {
    console.log("Bloque inicializado");
  }

  constructor() {
    console.log("Constructor ejecutado");
  }
}
// <-- Aquí nos aparece "Bloque inicializado"

// metodo privado
#hablar() {
  console.log("It's me, Mario!");
}
```

## Herencia
```js
// Clase padre
class Forma {
  constructor() {
    console.log("Soy una forma geométrica.");
  }
}

// Clase hija
class Cuadrado extends Forma {
  constructor() {
    super();
    console.log("Soy un cuadrado.");
  }
}
```
