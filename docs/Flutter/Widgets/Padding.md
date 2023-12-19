---
layout: default
title: Padding
parent: Widgets
grand_parent: Flutter
nav_order: 3
---

# Padding
Adds empty space around its child widget.

```dart
Padding(
  padding: EdgeInsets.all(16.0), // Espaciado uniforme en todos los lados
  child: Container(
    color: Colors.blue,
    height: 100.0,
    width: 200.0,
    child: Center(
      child: Text(
        'Hello, Padding!',
        style: TextStyle(color: Colors.white),
      ),
    ),
  ),
)
```
