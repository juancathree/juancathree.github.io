---
layout: default
title: Scaffold
parent: Widgets
grand_parent: Flutter
nav_order: 1
---

# Scaffold
It is a fundamental building block for creating an app's visual layout and structure.

- **appBar:** bar at the top, which display a title, actions, and other widgets.
- **body:** define the primary content of the app.
- **floatingActionButton:** used for primary actions.
- **drawer:** to set up a navigation drawer.
- **bottomNavigationBar:** navigation bar at the bottom of the screen.

```dart
void main(){
  runApp(
    MaterialApp(
      home: Scaffold(
        appBar: AppBar(
          title: Text('AppBar navigation'),
        ),
        body: Text('Awesome!'),
      ),
    )
  );
}
``` 
