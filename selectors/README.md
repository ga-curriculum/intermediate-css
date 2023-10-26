


# ![Intermediate CSS - Selectors](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to target specific elements on the page with attribute selectors, pseudo-classes, pseudo-elements, and uncommon combinators.

## Attribute selectors

[**Attribute selectors**](https://developer.mozilla.org/en-US/docs/Web/CSS/Attribute_selectors) allow us to target elements based on their attributes. For example, we can use the following attribute selector to target all elements with the `href` attribute:

```css
a[href="#about"] { /* Targets anchor tags with an 'href' set to "#about" */
  background: red;
  top: 0;
  position: fixed;
} 

input[type="checkbox"] { ... } /* Targets checkbox inputs */
```

## Pseudo-classes

[**Pseudo-classes**](https://developer.mozilla.org/en-US/docs/Web/CSS/pseudo-classes) allow us to target elements not just based upon their class, type, id, or position in the document, but also their state. For example, whether an `<input type="checkbox">` is checked or not.

Some common pseudo-classes are `:active`, `:disabled`, `:empty`, `:first-child`, `:nth-child`, `:nth-of-type`, `:focus`, `:hover`, and many more!

We can also chain pseudo-classes for an extra fun time! `li:nth-child(3):hover`

### 🧠 You do

**Use the `:hover` pseudo-class to change the cursor to the little hand-pointer when it’s over any of the elements nested inside the `ul.top-level-list`.**

## Pseudo-elements

Pseudo-elements style specified parts of an element.

Here are some examples:

`p::first-letter`: Style the first letter of all `<p>` elements `p::first-line`: Style the first line of all `<p>` elements `::selection`: Style the part of an element that is selected by the user `.special::before`: Add content *before* all elements with a class of `.special` `.special::after`: Add content *after* all elements with a class of `.special`

> 🚨 So many options - so confusing! Yes, but always remember that nobody remembers all of this stuff. You will remember what you use on the job regularly. From there, Google is your best friend.

### 🧠 You do

**Use the `::first-letter` pseudo-element to set the size of the “C” in “Comments” to be 60px.**

And here's a link to learn more about [pseudo-elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements).

## Uncommon combinators

Three of the less common combinators are:

- The **child selector** (`>`)
  The *child selector* is similar to the *descendant selector*, except that it only matches elements that are **direct** children, that is, nested only one-level deep:
  ```css
  /* Selects all <li> tags that are direct children of a <ul.top-level-list> */
  .top-level-list > li {
	  color: orange;
  }
  ```
  After adding this, you’ll notice that our <li> elements that are not **direct children** of the <ul.top-level-list> are still being colored orange. This is because of *inheritance* which we will discuss soon.

- The **adjacent sibling selector** (`+`)
  ```css
  li + li {
    color: green;
  }
  ```
  This would select <li> tags only if they were preceded **immediately** by another <li> at the same level (sibling) and give them a color of green.

- The **general sibling selector** (`~`)
  Similar to the *adjacent sibling selector*. Selects all instances of the second element that appear after the first element, at the same level:
  ```css
  img ~ p {
	  border: 1px solid red;
  }
  ```
  Would target all <p> tags that are siblings following a <img>.

> 🧠 The last component listed in a combination selector determines what is targeted! For example, looking above, only <p> elements are selected, not the <img>.


