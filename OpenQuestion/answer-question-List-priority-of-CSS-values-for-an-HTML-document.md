# List priority of CSS values for an HTML document
In CSS, the priority of styles determines which rules are applied when multiple rules conflict. This priority is determined by the cascade, specificity, and source order. Here's the list of CSS values in order of their priority And number 1 will overwrite number 2 and so on:

### 1. **!important Declarations**
- The `!important` declaration overrides any other declarations (except inline styles with `!important`).
```css
/* This will override any other conflicting style declarations */
p {
  color: blue !important;
}
```
### 2. **Inline Styles**
- Styles applied directly to an HTML element using the `style` attribute have the highest priority.
```html
<div style="color: red;">This text will be red.</div>
```

### 3. **ID Selectors**
- Selectors using the ID of an element have high specificity.
```css
#unique-element {
  color: green;
}
```

### 4. **Class, Attribute, and Pseudo-class Selectors**
- Selectors using class names, attributes, and pseudo-classes have medium specificity.
```css
.class-name {
  color: yellow;
}

a[href="example.com"] {
  color: orange;
}

a:hover {
  color: purple;
}
```

### 5. **Type and Pseudo-element Selectors**
- Selectors using element types and pseudo-elements have low specificity.
```css
p {
  color: brown;
}

p::first-line {
  color: pink;
}
```

### 6. **Universal and Inherited Styles**
- The universal selector (*) and styles inherited from parent elements have the lowest specificity.
```css
* {
  color: black;
}
```

### 7. **Browser Default Styles**
- These are the default styles applied by the browser to elements when no other styles are specified.

### Cascading and Source Order
- When selectors have equal specificity, the order of appearance in the stylesheet matters. The last declared style in the source code wins.

### Combining Specificity
- Specificity is calculated as a sum of the different types of selectors. The more specific a rule, the higher its priority.
  - Inline styles: 1,0,0,0
  - ID selectors: 0,1,0,0
  - Class, attribute, and pseudo-class selectors: 0,0,1,0
  - Type and pseudo-element selectors: 0,0,0,1

### Example
Given the following CSS and HTML:
```html
<head>
  <style>
    .class-name {
      color: yellow;
    }

    #unique-element {
      color: green;
    }

    p {
      color: blue;
    }
  </style>
</head>
<body>
  <p id="unique-element" class="class-name">Hello, World!</p>
</body>
```

The text "Hello, World!" will be green because the ID selector `#unique-element` has higher specificity than the class selector `.class-name` and the type selector `p`.