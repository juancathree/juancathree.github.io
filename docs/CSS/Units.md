---
layout: default
title: Units
nav_order: 3
has_children: false
parent: CSS
---

# Units

## Percentages
Percentages let you specify values in percentages of that parent element's corresponding property.
```css
.parent {
  width: 400px;
}

.child {
  width: 50%; /* = 200px */
}
```

## Viewpoints
  - **vw** the viewport width unit represents a percentage of the viewport width. 50vw means 50% of the viewport width.
  - **vh** the viewport height unit represents a percentage of the viewport height. 50vh means 50% of the viewport height.
  - **vmin** the viewport minimum unit represents the minimum between the height or width in terms of percentage. 30vmin is the 30% of the current width or height, depending which one is smaller
  - **vmax** the viewport maximum unit represents the maximum between the height or width in terms of percentage. 30vmax is the 30% of the current width or height, depending which one is bigger

## Fractions
**fr** are fraction units, and they are used in CSS Grid to divide space into fractions.
