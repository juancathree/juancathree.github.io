---
layout: default
title: Expanded
parent: Widgets
grand_parent: Flutter
nav_order: 11
---

# Expanded
Is used within a Row or Column to allocate available remaining space to its child widgets.
```dart
 Column(
  children: [
    Container(
      height: 100.0,
      color: Colors.red,
      child: Center(
        child: Text(
          'Not Expanded',
          style: TextStyle(color: Colors.white),
        ),
      ),
    ),
    SizedBox(height: 20.0),
    Expanded(
      flex: 2, // Flex factor para el Expanded
      child: Container(
        color: Colors.green,
        child: Center(
          child: Text(
            'Expanded',
            style: TextStyle(color: Colors.white),
          ),
        ),
      ),
    ),
    SizedBox(height: 20.0),
    Container(
      height: 100.0,
      color: Colors.blue,
      child: Center(
        child: Text(
          'Not Expanded',
          style: TextStyle(color: Colors.white),
        ),
      ),
    ),
  ],
),
```
