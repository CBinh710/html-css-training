# How to use :before, :after CSS properties?

The `::before` and `::after` pseudo-elements in CSS allow you to insert content onto a page without it needing to be in the HTML. While the end result is not actually in the DOM, it appears on the page as if it is. Here's how you can use them:

1. **`::before` Selector:**
    - The `::before` selector inserts content before the content of each selected element.
    - Use the `content` property to specify the content you want to insert.
    - For example, to insert some text before the content of each `<p>` element:
        ```css
        p::before {
            content: "Read this: ";
        }
        ```
    - You can also style the inserted content using other CSS properties like `background-color`, `color`, and `font-weight`.

2. **`::after` Selector:**
    - The `::after` selector inserts content after the content of each selected element.
    - Similar to `::before`, use the `content` property to specify the content you want to insert.
    - Example:
        ```css
        div::after {
            content: "after";
        }
        ```
    - Remember that pseudo-elements are written after pseudo-classes in CSS.

