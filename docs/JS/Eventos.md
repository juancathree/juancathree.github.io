---
layout: default
title: Eventos
nav_order: 13
has_children: false
parent: JS
---

# Eventos

## Mediante HTML
```html
<script>
  function doTask() {
    alert("Hello!");
  }
</script>

<button onClick="doTask()">Saludar</button>
```

## Mediante JS
```js
const button = document.querySelector("button");
button.onclick = function() {
  alert("Hello!");
}
```

## Event Listener
```js
const button = document.querySelector("button");
button.addEventListener("click", function() {
  alert("Hello!");
});

button.removeEventListener("click", action);
```
