---
layout: default
title: Selectors
nav_order: 1
has_children: false
parent: CSS
---

# Selectors

## Basic selectors
We can use HTML tags, css class or HTML id.
```html
<p id="idDog-name" class="dog-name roger">Roger</p>
```
```css
/* tag */
p {
  color: yellow;
}

/* tag & class */
p.dog-name {
  color: yellow;
}

/* class */
.dog-name {
  color: yellow;
}

/* multiple class */
.dog-name.roger {
  color: yellow;
}

/* class & id */
.dog-name#idDog-namec {
  color: yellow;
}

p#idDog-name {
  color: yellow;
}

/* id */
#idDog-name {
  color: yellow;
}
```

## Follow document tree
```html
<p>
  My dog name is:
  <span class="dog-name"> Roger </span>
</p>
```
