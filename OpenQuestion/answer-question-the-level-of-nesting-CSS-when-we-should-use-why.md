# What is the level of nesting CSS we should use? Why?
The level of nesting in CSS should be kept minimal for several reasons:

1. **Readability**: Deeply nested CSS can become difficult to read and understand. Keeping nesting shallow makes it easier for developers to quickly grasp the structure and styles of a page.

2. **Maintainability**: With minimal nesting, maintaining and updating CSS becomes more straightforward. Deeply nested styles can be cumbersome to modify, especially when changes need to be made across multiple levels of the hierarchy.

3. **Specificity**: Excessive nesting increases the specificity of selectors, which can lead to issues with overriding styles. High specificity makes it harder to manage styles and can lead to unexpected results when trying to apply new styles or overrides.

4. **Performance**: While modern browsers are efficient at parsing CSS, deeply nested selectors can still have a slight impact on performance, especially on large web pages with complex styles. Keeping nesting shallow helps ensure that CSS is parsed and applied more efficiently.

## Recommended Practices

1. **Use Classes**: Rely on class selectors rather than deep nesting of element selectors. Classes are reusable and provide a clean way to apply styles without unnecessary depth.

2. **Avoid Over-qualifying Selectors**: Avoid combining element selectors with classes unnecessarily. For example, use `.button` instead of `button.button`.

3. **Limit Nesting Levels**: Aim to limit nesting to 2-3 levels deep. If you find yourself needing more levels, consider restructuring your HTML or CSS.

4. **Use Preprocessors Wisely**: If you use CSS preprocessors like Sass or LESS, be mindful of their nesting capabilities. It's easy to get carried away with nesting in preprocessors, but the same principles of minimal nesting apply.

### Example of Minimal Nesting

Instead of deeply nested CSS:
```css
.header .nav .nav-item .nav-link {
  color: blue;
}
```

Prefer a flatter structure:
```css
.header-nav-link {
  color: blue;
}
```

Or use classes effectively:
```html
<nav class="header-nav">
  <a class="nav-link">Home</a>
  <a class="nav-link">About</a>
</nav>
```
```css
.header-nav .nav-link {
  color: blue;
}
```