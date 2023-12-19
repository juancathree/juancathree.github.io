---
layout: default
title: Align
parent: Widgets
grand_parent: Flutter
nav_order: 17
---

# Chip
Compact and versatile UI element that represent a piece of information, attribute or action.

```dart
Chip(
  label: Text('Deletable Chip'), // Etiqueta del chip
  avatar: CircleAvatar(
    backgroundImage: AssetImage('assets/avatar_image.jpg'), // Imagen de fondo del avatar
  ),
  onDeleted: () {
    // Acción al presionar el icono de eliminación
    print('Chip deleted!');
  },
  deleteIcon: Icon(Icons.cancel), // Icono de eliminación personalizado
  deleteIconColor: Colors.red, // Color del icono de eliminación
),
```
