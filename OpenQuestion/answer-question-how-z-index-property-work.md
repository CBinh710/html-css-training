# How does the z-index property work?

The `z-index` property in CSS controls the stacking order of elements that overlap within a document. It affects the visibility and overlap of positioned elements.

### Basics of `z-index`

1. **Stacking Contexts:**
   - Each positioned element (an element whose position property is set to anything other than `static`) with a `z-index` value other than `auto` creates a stacking context.
   - A stacking context is a three-dimensional conceptualization of HTML elements along the z-axis (depth).

2. **Layering:**
   - Elements with a higher `z-index` value are stacked in front of elements with lower `z-index` values within the same stacking context.
   - If two elements have the same `z-index`, the one declared later in the HTML source order will appear on top.

### How to Use `z-index`

- **Syntax:**
  ```css
  .element {
      position: relative; /* or absolute, fixed, sticky */
      z-index: 100; /* Specify a numeric value */
  }
  ```

- **Values:**
  - **Integer:** A positive or negative number. Positive values bring the element forward; negative values push it backward.
  - **Auto:** Default value. Elements are stacked according to their position in the HTML hierarchy.

- **Notes:**
  - `z-index` only works on positioned elements (`position: relative, absolute, fixed, sticky`). If an element is not positioned, `z-index` will have no effect.
  - `z-index` values are not limited to integers; they can be fractional, though they are generally treated as integers for stacking purposes.
  - Nested stacking contexts (children within parents with different `z-index` values) affect how elements are layered relative to their ancestors and siblings.

### Examples

- **Simple Stacking:**
  ```css
  .box1 {
      position: absolute;
      z-index: 1;
  }
  
  .box2 {
      position: absolute;
      z-index: 2;
  }
  ```
  - `box2` will be displayed in front of `box1` because it has a higher `z-index`.

- **Negative `z-index`:**
  ```css
  .behind {
      position: relative;
      z-index: -1;
  }
  ```
  - The `behind` element will be positioned behind its parent or siblings with positive `z-index` values.

### Stacking Contexts and Nested Elements

- **Parent-Child Relationships:**
  - A child element with a higher `z-index` than its parent will still be confined to the stacking context of the parent unless the parent itself has a lower `z-index` than another ancestor or sibling.

- **Creating Stacking Contexts:**
  - Any element with `z-index` set to a value other than `auto` will create a stacking context. This means its children can be positioned in relation to it, independently of other parts of the document.

### Practical Use Cases

- **Dropdown Menus:** Ensuring dropdowns appear above other content.
- **Modal Windows:** Overlaying content on top of existing page content.
- **Layered Interfaces:** Managing the visual hierarchy of complex user interfaces.

Understanding `z-index` allows developers to control the visual layering of elements effectively, ensuring elements appear in the desired order on a web page.