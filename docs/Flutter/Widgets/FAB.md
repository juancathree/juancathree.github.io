---
layout: default
title: FAB
parent: Widgets
grand_parent: Flutter
nav_order: 13
---

# FAB

```dart
floatingActionButton: FloatingActionButton(
  onPressed: () {
    // Acción al presionar el botón flotante
    print('FloatingActionButton pressed!');
  },
  child: Icon(Icons.add), // Icono del botón flotante
  backgroundColor: Colors.blue, // Color de fondo del botón flotante
  foregroundColor: Colors.white, // Color del icono del botón flotante
  elevation: 6.0, // Elevación del botón flotante
  tooltip: 'Add', // Texto que aparece al mantener presionado el botón flotante
  splashColor: Colors.green, // Color del efecto splash al presionar el botón flotante
),
floatingActionButtonLocation: FloatingActionButtonLocation.endFloat,
```
