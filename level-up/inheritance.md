# ![Intermediate CSS - Level Up - Inheritance](./assets/inheritance.png)

**Learning objective:** By the end of this lesson students will be able to demonstrate their understanding of css inheritance by overriding inherited styles using the `initial` value.

[Inheritance](https://developer.mozilla.org/en-US/docs/Web/CSS/Inheritance) is a key component of CSS - it dictates that certain properties such as font family or color can be passed from parent elements to child elements implicitly.

This is useful because it prevents us from writing a bunch of repetitive CSS - but sometimes it may have unintended side effects - like when we were using the **child-selector**.

We are able to override inheritance by giving an `initial` value to keys we don't want to inherit from parents. For example:

```css
ul {
  color : red; /* all child elements will have red text */
}

li {
  margin: 5px 0 0 0;
  color: initial; /* will not inherit red text color from parent */
}
```
