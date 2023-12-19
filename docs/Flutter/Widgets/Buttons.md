---
layout: default
title: Buttons
parent: Widgets
grand_parent: Flutter
nav_order: 4
---

# Buttons

## Elevated button
```dart
ElevatedButton(
  onPressed: () {
  // Acción al presionar el botón
  print('Button pressed!');
  },
  onLongPress: () {
  // Acción al mantener presionado el botón
  print('Button long pressed!');
  },
  style: ElevatedButton.styleFrom(
    primary: Colors.blue, // Color de fondo del botón
    onPrimary: Colors.white, // Color del texto del botón
    padding: EdgeInsets.all(16.0), // Espaciado interno del botón
    elevation: 8.0, // Elevación del botón
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.circular(10.0), // Bordes redondeados
      side: BorderSide(color: Colors.black, width: 2.0), // Borde del botón
    ),
  ),
)
```

## Text button
```dart
TextButton(
  onPressed: () {
    // Acción al presionar el botón
    print('Button pressed!');
  },
  onLongPress: () {
    // Acción al mantener presionado el botón
    print('Button long pressed!');
  },
  style: TextButton.styleFrom(
    primary: Colors.red, // Color del texto del botón
    onSurface: Colors.yellow, // Color del texto cuando el botón está presionado
    padding: EdgeInsets.all(16.0), // Espaciado interno del botón
    textStyle: TextStyle(
    fontSize: 18.0,
    fontWeight: FontWeight.bold,
    fontStyle: FontStyle.italic,
    letterSpacing: 1.5,
    wordSpacing: 2.0,
    ),
    backgroundColor: Colors.blue, // Color de fondo del botón
    side: BorderSide(
      color: Colors.black, // Color del borde del botón
      width: 2.0,
    ),
    shape: RoundedRectangleBorder(
      borderRadius: BorderRadius.circular(10.0), // Bordes redondeados
    ),
  ),
)
```

## Icon button
```dart
IconButton(
  icon: Icon(Icons.thumb_up),
  onPressed: () {
    // Acción al presionar el botón
    print('Button pressed!');
  },
  color: Colors.green, // Color del icono
  splashColor: Colors.yellow, // Color del efecto splash
  tooltip: 'Like', // Texto que aparece al mantener presionado el botón
  iconSize: 40.0, // Tamaño del icono
  padding: EdgeInsets.all(16.0), // Espaciado interno del botón
  alignment: Alignment.center, // Alineación del icono dentro del botón
),
```
