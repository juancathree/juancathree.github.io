---
layout: default
title: Text field
parent: Widgets
grand_parent: Flutter
nav_order: 14
---

# Text field

```dart
final TextEditingController _textController = TextEditingController();
final FocusNode _textFocus = FocusNode();

TextField(
  controller: _textController,
   focusNode: _textFocus,
  onChanged: (value) {
    // Acción al cambiar el texto
    print('Text changed: $value');
  },
  onSubmitted: (value) {
    // Acción al enviar el formulario (pulsar Enter en el teclado)
    print('Form submitted: $value');
  },
  decoration: InputDecoration(
    labelText: 'Enter text', // Etiqueta del campo de texto
    hintText: 'Type something', // Texto de ayuda dentro del campo de texto
    prefixIcon: Icon(Icons.person), // Icono que aparece antes del texto
    suffixIcon: IconButton(
      icon: Icon(Icons.clear),
      onPressed: () {
        // Acción al presionar el icono de borrar
        print('Clear button pressed!');
      },
    ),
    border: OutlineInputBorder(), // Decoración del borde del campo de texto
    filled: true, // Rellenar el fondo del campo de texto
    fillColor: Colors.grey.shade200, // Color de fondo cuando está rellenado
    errorText: 'This is an error', // Texto de error
    errorStyle: TextStyle(color: Colors.red), // Estilo del texto de error
    helperText: 'This is helper text', // Texto de ayuda
    helperStyle: TextStyle(color: Colors.blue), // Estilo del texto de ayuda
    contentPadding: EdgeInsets.symmetric(vertical: 10.0, horizontal: 10.0), // Relleno del contenido
  ),
  style: TextStyle(fontSize: 18.0, color: Colors.black), // Estilo del texto
  keyboardType: TextInputType.text, // Tipo de teclado a mostrar
  obscureText: false, // Ocultar el texto (por ejemplo, para contraseñas)
  maxLength: 10, // Longitud máxima del texto
  maxLines: 1, // Número máximo de líneas
  cursorColor: Colors.red, // Color del cursor
  cursorWidth: 3.0, // Ancho del cursor
  cursorRadius: Radius.circular(5.0), // Radio del cursor
  autocorrect: true, // Autocorrección del texto
  enableSuggestions: true, // Habilitar sugerencias del teclado
  textAlign: TextAlign.start, // Alineación del texto
  textInputAction: TextInputAction.done, // Acción del botón "Hecho" del teclado
),
```
