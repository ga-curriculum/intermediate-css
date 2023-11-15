![Intermediate CSS - Level Up - Margin Collapsing](./assets/hero.png)

**Learning objective:** By the end of this lesson, learners will understand the phenomenon of margin collapsing in CSS, including its causes and implications on the design layout. 

# Margin Collapsing

Margin collapsing is a behavior that occurs when the margins of adjacent block-level elements overlap. This can cause the margins to merge together, resulting in a larger margin than expected.

Margin collapsing only occurs between vertically adjacent block-level elements. Inline elements and floated elements do not collapse their margins.

Consider the following styles as you explore the examples below.

```css
div {
  margin: 10px 0;
}

img {
  margin: 10px 0;
}
```

Here are some examples of margin collapsing:

1. In this example, the margins of the `.box1` and `.box2` elements will collapse, resulting in a single margin between the two elements. Div elements are `block` by default.

   ```html
   <div class="container">
     <div class="box1">Box 1</div>
     <div class="box2">Box 2</div>
   </div>
   ```

2. In this example, the margin of the `.box1` element will not collapse with the margin of the image, because the image is an `inline` element by default.

   ```html
   <div class="container">
     <div class="box1">Box 1</div>
     <img src="image.jpg" alt="Image">
     <div class="box2">Box 2</div>
   </div>
   ```

### How to prevent margin collapsing

There are a few ways to prevent margin collapsing:

- **Add padding**: Adding padding to the parent element will create a space between the parent element and its children, preventing their margins from collapsing.

- **Use *flexbox* or *grid*: CSS flexbox and grid layouts provide more control over the layout of your elements and can be used to prevent margin collapsing. 

- **Float the elements**: Floating the elements will prevent their margins from collapsing.