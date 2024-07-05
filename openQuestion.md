<h3>1. Should we use tables in HTML? Why?</h3>

Why Use Tables:

Semantic Purpose: Contrary to the misconception that tables are unsemantic, they actually semantically indicate tabular data. When you have data that fits the tabular format, using tables is the right choice.

Accessibility: Tables are essential for accessibility. However, avoid using them for layout purposes (e.g., designing page structure). Screen readers read tables from top to bottom, left to right, so using tables for layout can lead to accessibility issues.

Grouping and Structure: HTML tables allow you to group rows into head, body, and foot sections. You can also group columns using the COLGROUP and COL elements. This provides additional structural information and helps with printing long tables.

When NOT to Use Tables:

Layout: Never use tables for layout purposes. They should not be used as design aids. Instead, use CSS and semantic elements like div, section , and aside for layout.

Responsive Design: Tables are not suitable for responsive design. If you want your web application to look good on various devices, avoid using tables for layout.

<h3>2. What HTML tags have property display: inline, block, inline-block?</h3>

inline: display a properties as an span tag

block: display a properties as an p tag

inline-block: display a properties as an inline container
![image](https://github.com/CBinh710/html-css-training/assets/160686508/b4b4f41c-e2f2-4089-a4c8-9e0b9010c1bd)

<h3>3. When will we use section, article tags?</h3>

article: Independent, self-contained content (like a complete blog post).
<article>
    <h2>Google Chrome</h2>
    <p>Google Chrome is a web browser developed by Google, released in 2008. Chrome is the world's most popular web browser today!</p>
</article>

<article>
    <h2>Mozilla Firefox</h2>
    <p>Mozilla Firefox is an open-source web browser developed by Mozilla. Firefox has been the second most popular web browser since January 2018.</p>
</article>

<article>
    <h2>Microsoft Edge</h2>
    <p>Microsoft Edge is a web browser developed by Microsoft, released in 2015. It replaced Internet Explorer.</p>
</article>

section: Grouping content thematically (like chapters in a book).

<section>
    <h2>Main Content</h2>
    <article>
        <h3>Article 1</h3>
        <p>This is the first article in the main content section.</p>
    </article>
    <!-- More articles can go here -->
</section>
<h3>4. How to use :before, :after CSS properties?</h3>

1.::before:

The ::before pseudo-element inserts content before the content of a selected element.

You can use the content property to specify the content you want to insert.

Example:

div::before {
    content: "before";
}

In this example, the word “before” will appear before the content of every div element.

2.::after:

The ::after pseudo-element inserts content after the content of a selected element.

Similar to ::before, you can use the content property to define the content you want to insert.

Example:

div::after {
    content: "after";
}

In this case, the word “after” will appear after the content of every div element.
