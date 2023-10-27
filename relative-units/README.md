# ![Intermediate CSS - CSS Units](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to understand and use relative units in CSS.

## Relative units

We use CSS units to specify the size of elements in a CSS stylesheets.  Relative units are based on the size of another element on the page. Some examples of relative units include:

- `em`: Ems are based on the font size of the parent element.
- `rem`: Rems are similar to ems, but they are based on the font size of the root element.
- `%`: Percentages are based on the size of the container element, and as a result are always relative to the size of that element.  
- `vw` - 1% of the viewport's width.
- `vh` - 1% of the viewport's height.

## Which units to use

The type of CSS units that we should use depends on the specific property that we are styling. For example, if we were styling the width of an element, we could use `%` so that the element always takes up the same amount of its available container. 

For font size, `rem` is a great option. `rem` is predictable - the value will always be based off the same root value. Note that `rem` is based off of the root element's font-size, which defaults to `16px`.

For example: 
- 1rem = 16px
- 1.5rem = 24px
- 0.5rem = 8px

Unlike `px` units, `rem` is responsive. As the root font size changes, all of the relative values will change accordingly. This has big implications for accessibility - suppose a user changes their preferred font size to 18 in their browser settings. Now, `1rem` equals `18px`s, and so forth: 

- 1rem = 18px
- 1.5rem = 27px
- 0.5rem = 9px

All of our relative units update accordingly, and the font size of the element is dynamically consistent with the rest of the page. 

Here are some examples of how to use CSS units:

```css
/* Set the width of an element to the entire view width */
div {
  width: 100vw;
}

/* Set the font size of an element to 24 pixels  */
p {
  font-size: 24px;
}

/* Set the margin of an element to 10% of its container element */
img {
  margin: 10%;
}
```

Pitfalls when specifying height and width
- scenario where you need min-height/width because other units cant solve that problem
tktk min-height, min-width

