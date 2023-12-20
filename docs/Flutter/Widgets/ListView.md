---
layout: default
title: List view
parent: Widgets
grand_parent: Flutter
nav_order: 19
---

# List view

```dart
 ScrollController _controller = ScrollController();

ListView.builder(
  itemCount: miLista.length,
  itemBuilder: (BuildContext context, int index) {
    return ListTile(
      title: Text(miLista[index]),
    );
  },
  scrollDirection: Axis.vertical,
  shrinkWrap: true,
  physics: BouncingScrollPhysics(),
  controller: _controller,
),
```
