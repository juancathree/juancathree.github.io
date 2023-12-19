---
layout: default
title: App Bar
parent: Widgets
grand_parent: Flutter
nav_order: 12
---

# AppBar

```dart
appBar: AppBar(
  title: Text('AppBar Example'), // Título de la AppBar
  backgroundColor: Colors.blue, // Color de fondo de la AppBar
  centerTitle: true, // Centrar el título
  elevation: 4.0, // Elevación de la AppBar
  leading: Icon(Icons.menu), // Widget que se coloca antes del título
  actions: [
    IconButton(
      icon: Icon(Icons.search),
      onPressed: () {
        // Acción al presionar el ícono de búsqueda
        print('Search button pressed!');
      },
    ),
    IconButton(
      icon: Icon(Icons.settings),
      onPressed: () {
        // Acción al presionar el ícono de configuración
        print('Settings button pressed!');
      },
    ),
  ],
)
```
