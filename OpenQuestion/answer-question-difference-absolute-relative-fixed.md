# What is the difference between position: absolute, relative, fixed?

The `position` property in CSS is used to specify the positioning method for an element. The values `absolute`, `relative`, `fixed`, and `sticky` each provide different ways to control the layout and behavior of an element:

### `position: relative;`

- **Definition**: The element is positioned relative to its normal position.
- **Behavior**: It stays in the document flow, but you can use `top`, `right`, `bottom`, and `left` to offset it from its normal position.
- **Use Case**: Useful for making slight adjustments to an element's position without affecting the layout of other elements.

```css
.relative {
  position: relative;
  top: 10px; /* Moves the element 10px down from its original position */
}
```

### `position: absolute;`

- **Definition**: The element is positioned relative to the nearest positioned ancestor (an ancestor with `position: relative`, `absolute`, or `fixed`), or the initial containing block if there is no such ancestor.
- **Behavior**: It is removed from the normal document flow, so it doesn't affect the position of other elements.
- **Use Case**: Useful for positioning elements in a precise location within a container.

```css
.absolute {
  position: absolute;
  top: 10px; /* Moves the element 10px down from the top of its containing block */
  left: 20px; /* Moves the element 20px from the left of its containing block */
}
```

### `position: fixed;`

- **Definition**: The element is positioned relative to the viewport, which means it stays in the same place even when the page is scrolled.
- **Behavior**: It is removed from the normal document flow and doesn't affect the position of other elements.
- **Use Case**: Useful for creating elements that should remain visible regardless of scrolling, such as a fixed header or a back-to-top button.

```css
.fixed {
  position: fixed;
  top: 10px; /* Moves the element 10px down from the top of the viewport */
  right: 20px; /* Moves the element 20px from the right of the viewport */
}
```

### `position: sticky;`

- **Definition**: The element is treated as `relative` until it crosses a specified threshold, at which point it becomes `fixed` within its containing block.
- **Behavior**: It stays in the normal document flow until a defined scroll position is reached, then it sticks to that position until its container is out of view.
- **Use Case**: Useful for elements that should stick to the top of the viewport during scrolling but only within a certain container, such as a sticky header within a section.

```css
.sticky {
  position: sticky;
  top: 0; /* Sticks to the top of the containing block when it reaches the top of the viewport */
}
```

### Summary
- **Relative**: Adjusts position relative to its normal position.
- **Absolute**: Positioned relative to the nearest positioned ancestor or the initial containing block.
- **Fixed**: Positioned relative to the viewport; stays in place during scrolling.
- **Sticky**: Behaves like `relative` until a certain scroll position is reached, then behaves like `fixed` within its containing block.