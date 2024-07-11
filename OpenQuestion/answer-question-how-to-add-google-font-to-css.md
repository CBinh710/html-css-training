
# How to add a google font to the CSS?
### Steps to Add Google Font to CSS

1. **Find and Select a Google Font:**
   - Visit the [Google Fonts website](https://fonts.google.com/) and browse or search for the font you want to use.
   - Once you've chosen a font, click on the "plus" icon next to the font name. This action will add the font to your selection bar at the bottom of the page.

2. **Customize Font Selection (Optional):**
   - In the selection bar, you can adjust font styles (e.g., regular, bold, italic) and character sets (e.g., Latin, Cyrillic) if needed. Google Fonts will generate the appropriate CSS code based on your selections.

3. **Import the Font into Your CSS:**
   - Google Fonts provides a `<link>` tag that you can add to the `<head>` section of your HTML document. This tag imports the font stylesheets into your project.
   - Copy the `<link>` tag provided in the "Embed" section. It will look something like this:
     ```html
     <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
     ```
   - Paste this `<link>` tag inside the `<head>` section of your HTML file. This step ensures that the font styles are loaded and available for use in your CSS.

4. **Apply the Font in Your CSS:**
   - Once the font is imported, you can use it in your CSS styles by specifying the `font-family` property.
   - Example usage in CSS:
     ```css
     body {
         font-family: 'Roboto', sans-serif;
     }
     ```
   - Replace `'Roboto'` with the actual name of the Google Font you imported. The `sans-serif` fallback ensures that if the font fails to load, the browser defaults to a similar sans-serif font.

### Example

Here’s a complete example demonstrating how to add and use a Google Font:

**HTML (index.html):**
```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Using Google Font</title>
    <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
    <style>
        body {
            font-family: 'Roboto', sans-serif;
        }
        .custom-heading {
            font-family: 'Roboto', sans-serif;
            font-weight: 700; /* Example of using a specific font weight */
            font-size: 24px;
        }
    </style>
</head>
<body>
    <h1 class="custom-heading">Hello, Google Fonts!</h1>
    <p>This paragraph uses the Roboto font from Google Fonts.</p>
</body>
</html>
```

In this example:
- We import the Roboto font stylesheets using the `<link>` tag provided by Google Fonts.
- In the `<style>` section of the `<head>`, we specify that the `body` and `.custom-heading` elements should use the Roboto font.
- The `font-weight: 700;` in `.custom-heading` demonstrates how to apply a specific font weight from the imported font.

By following these steps, you can easily integrate any Google Font into your CSS and use it to style text throughout your web pages.