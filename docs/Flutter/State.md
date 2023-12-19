---
title: State
layout: default
nav_order: 3
parent: Flutter
---

# State

## Statless Widget
Are used when the UI elements does not need to maintain any mutable state.

```dart
class StatelessDemo extends StatelessWidget{
  const StatelessDemo({super.key});

  @override
  Widget build(BuildContext context){
    return Scaffold(
      appBar: AppBar(
        title: Text('Hi')
      ),
    )
  }
}
```

## Stateful Widget
Are used when the UI elements need to maintain mutable state.

```dart
class MyStatefulWidget extends StatefulWidget {
  @override
  _MyStatefulWidgetState createState() => _MyStatefulWidgetState();
}

class _MyStatefulWidgetState extends State<MyStatefulWidget> {
  int counter = 0;

  void incrementCounter() {
    setState(() {
      counter++;
    });
  }

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(
        title: Text('StatefulWidget Example'),
      ),
      body: Center(
        child: Column(
          mainAxisAlignment: MainAxisAlignment.center,
          children: [
            Text(
              'Counter Value:',
              style: TextStyle(fontSize: 20.0),
            ),
            Text(
              '$counter',
              style: TextStyle(fontSize: 40.0, fontWeight: FontWeight.bold),
            ),
          ],
        ),
      ),
      floatingActionButton: FloatingActionButton(
        onPressed: incrementCounter,
        child: Icon(Icons.add),
      ),
    );
  }
}
```
