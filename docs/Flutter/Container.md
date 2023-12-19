---
layout: default
title: Container
nav_order: 3
parent: Flutter
---

# Container
Is a versatile layout element used to wrap arrange child widgets.

```dart
Container(
  alignment: Alignment.center, // Alineación del contenido dentro del contenedor
  padding: EdgeInsets.all(16.0), // Espaciado interno del contenedor
  margin: EdgeInsets.all(16.0), // Margen externo del contenedor
  height: 200.0, // Altura del contenedor
  width: 300.0, // Ancho del contenedor
  decoration: BoxDecoration(
    color: Colors.blue, // Color de fondo del contenedor
    border: Border.all(
      color: Colors.black, // Color del borde
      width: 2.0, // Ancho del borde
    ),
  ),
  borderRadius: BorderRadius.circular(10.0), // Bordes redondeados
  boxShadow: [
    BoxShadow(
      color: Colors.grey,
      blurRadius: 5.0,
      offset: Offset(2.0, 2.0),
    ),
  ],
),
```
