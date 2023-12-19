---
layout: default
title: Center
parent: Widgets
grand_parent: Flutter
nav_order: 8
---

# Center
Is used to center-align its child widget within the available space both vertically and horizontally.

```dart
Container(
  width: 200.0,
  height: 100.0,
  color: Colors.blue,
  child: Center(
    child: Text(
      'Hello, Center!',
      style: TextStyle(color: Colors.white),
    ),
  ),
)
```
