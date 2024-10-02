<h1>
  <span class="headline">Intermediate CSS</span>
  <span class="subhead">CSS Boilerplate</span>
</h1>

**Learning objective:** By the end of this lesson, students will be able to explain what CSS boilerplate is and why it's useful.

## CSS Boilerplate

CSS boilerplate refers to a set of pre-defined CSS rules and styles that are commonly used as a starting point in web development. The purpose of CSS boilerplate is to provide a consistent and normalized foundation for styling web pages, making it easier to create cross-browser and cross-platform compatible designs. It is typically used to normalize the behavior of different browsers and to provide a basic set of styles for common HTML elements.

Some of the most common CSS boilerplate rule sets include:

- **Resetting CSS**: This resets all CSS properties to their default values, and is useful for ensuring that all browsers display your web page in the same way.

- **Normalizing CSS**: This normalizes the behavior of different browsers across different platforms, and can help to prevent unexpected differences in the appearance of your web page on different devices.

- **Basic styles for common HTML elements**: This provides a basic set of styles for common HTML elements, such as headings, paragraphs, and lists. This can save you time from having to write these styles yourself.

Here is an example that you could use in your own work:

```css
* {
  box-sizing: border-box
}

body {
  background-color: gray;
  /* Use a system font, if none are available use an available sans-sarif font */
  font-family: system-ui, sans-serif;
  /* Ensures full height compatibility across devices */
  min-height: 100dvh;
  margin: 0;
}
```

If you're curious about `dvh`, check out [this article](https://ishadeed.com/article/new-viewport-units/) for more details.
