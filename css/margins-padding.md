Three important properties control the space that surrounds each HTML element: `padding`, `margin`, and `border`.

An element's `padding` controls the amount of space between the element and its border.  An element's `margin` controls the amount of space between an element's border and surrounding elements.

Instead of specifying an element's padding-top, padding-right, padding-bottom, and padding-left properties, you can specify them all in one line, like this:

```
  your-element {
    padding: 10px 20px 10px 20px;
    margin: 10px 20px 10px 20px;
  }```

These four values work like a clock: top, right, bottom, left, and will produce the exact same result as using the side-specific padding instructions.  This is called `Clockwise Notation` and works for both padding & margin.
