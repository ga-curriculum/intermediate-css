# Intermediate CSS - Level Up - Margin Collapsing

![Hero image](./assets/hero.png)

Margin collapsing is a behavior that occurs when the margins of adjacent block-level elements overlap. This can cause the margins to merge together, resulting in a larger margin than expected.

Margin collapsing only occurs between vertically adjacent block-level elements. Inline elements and floated elements do not collapse their margins.

Here are some examples of margin collapsing:

  1. In this example, the margins of the `.box1` and `.box2` elements will collapse, resulting in a single margin between the two elements.
  
  ```html
  <div class="container">
    <div class="box1"></div>
    <div class="box2"></div>
  </div>
  ```

  2. In this example, the margin of the `.box` element will not collapse with the margin of the paragraph element, because the paragraph element is an inline element.
  
  ```html
  <p>This is a paragraph.</p>
  <div class="box"></div>
  ```

  3. In this example, the margin of the `.box1` element will not collapse with the margin of the image, because the image is a floated element.

  ```html
  <div class="container">
    <div class="box1"></div>
    <img src="image.jpg" alt="Image">
    <div class="box2"></div>
  </div>
  ```

### How to prevent margin collapsing

There are a few ways to prevent margin collapsing:

- **Add padding**: Adding padding to the parent element will create a space between the parent element and its children, preventing their margins from collapsing.

- **Float the elements**: Floating the elements will prevent their margins from collapsing.

- **Use *flexbox* or *grid*: CSS flexbox and grid layouts provide more control over the layout of your elements and can be used to prevent margin collapsing. 
