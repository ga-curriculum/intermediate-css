# Intermediate CSS - Level Up - Inheritance

![Hero image](./assets/hero.png)

[Inheritance](https://developer.mozilla.org/en-US/docs/Web/CSS/Inheritance) is a key component of CSS - it dictates that certain properties such as font family or color can be passed from parent elements to child elements implicitly. 

This is useful because it prevents us from writing a bunch of repetitive CSS - but sometimes it may have unintended side effects - like when we were using the **child-selector**.

We are able to override inheritance by giving an `initial` value to keys we don’t want to inherit from parents. For example, to get our desired `<li>` behavior:

```css
li {
  margin: 5px 0 0 0;
  color: initial;
}
```