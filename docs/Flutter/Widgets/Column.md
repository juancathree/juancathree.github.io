---
layout: default
title: Column
parent: Widgets
grand_parent: Flutter
nav_order: 9
---

# Column

```dart
Column(
  mainAxisAlignment: MainAxisAlignment.center, // Alineación vertical del contenido
  crossAxisAlignment: CrossAxisAlignment.stretch, // Alineación horizontal del contenido
  mainAxisSize: MainAxisSize.max, // Tamaño principal de la columna
  children: [
    Container(
      height: 100.0,
      color: Colors.red,
      child: Center(
        child: Text(
          'Widget 1',
          style: TextStyle(color: Colors.white),
        ),
      ),
    ),
    SizedBox(height: 20.0), // Espaciado entre widgets
    Container(
      height: 100.0,
      color: Colors.green,
      child: Center(
        child: Text(
          'Widget 2',
          style: TextStyle(color: Colors.white),
        ),
      ),
    ),
  ],
),
```
