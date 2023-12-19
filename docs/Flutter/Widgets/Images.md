---
layout: default
title: Images
parent: Widgets
grand_parent: Flutter
nav_order: 15
---

# Images

```dart
 Image.network(
  'https://example.com/image.jpg', // URL de la imagen en línea
  width: 150.0, // Ancho de la imagen
  height: 150.0, // Altura de la imagen
  fit: BoxFit.cover, // Ajuste de la imagen dentro del contenedor
  color: Colors.blue, // Color aplicado a la imagen
  colorBlendMode: BlendMode.colorBurn, // Modo de mezcla de color
  alignment: Alignment.center, // Alineación de la imagen dentro del contenedor
  repeat: ImageRepeat.repeat, // Repetición de la imagen (puede ser repeat, repeatX, repeatY, noRepeat)
),
```

