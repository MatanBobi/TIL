## Problem
Until now, it wasn't possible to animate the height of a div for a collapse-expand component.

## Solution
CSS now offers to animate the height of a div using `display: grid`.


```css
.grid {
  display: grid;
  grid-template-rows: 0fr;
  transition: grid-template-rows 0.5s ease-in-out;
}

.grid.open {
  grid-template-rows: 1fr;
}

.grid-inner {
  overflow: hidden;
}
```

## Compatability
At the moment of writing, this feature is compatible in all 4 major browsers.
