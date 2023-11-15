# ![Intermediate CSS - Selectors](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to target specific elements on a page with attribute selectors, pseudo-classes, pseudo-elements, and uncommon combinators.

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

Some common pseudo-classes are:

  - `:active` - Targets elements in their active state, such as clicked links.
  - `:disabled` - Targets disabled form elements like input fields.
  - `:empty` - Targets elements with no children or text content.
  - `:first-child` - Targets the first child element of a parent.
  - `:nth-child` - Targets elements based on their position within a parent.
  - `:nth-of-type`  - Targets elements of a specific type based on their position within a parent.
  - `:focus` - Targets elements that currently have user focus, like input fields.
  - `:hover` - Targets elements when the mouse cursor hovers over them.
 
 ...and many more!

We can also chain pseudo-classes for an extra fun time! `li:nth-child(3):hover`

### 🧠 You do

Use the `:hover` pseudo-class to change the cursor to the little hand-pointer when it’s over any of the elements nested inside the `ul.top-level-list`.

## Pseudo-elements

Pseudo-elements style specified parts of an element.

Here are some examples:

 - `p::first-letter` - Style the first letter of all `<p>` elements 
 - `p::first-line` - Style the first line of all `<p>` elements 
 - `::selection` - Style the part of an element that is selected by the user 
 - `.special::before` - Add content *before* all elements with a class of `.special` 
 - `.special::after` - Add content *after* all elements with a class of `.special`

> 🚨 So many options - so confusing! Yes, but always remember that nobody remembers all of this stuff. You will remember what you use on the job regularly. From there, Google is your best friend.

### 🧠 You do

Use the `::first-letter` pseudo-element to set the size of the “C” in “Comments” to be `60px`.

And here's a link to learn more about [pseudo-elements](https://developer.mozilla.org/en-US/docs/Web/CSS/Pseudo-elements).

## Uncommon combinators

Three of the less common combinators are:

### Child selector (`>`)

The *child selector* is similar to the *descendant selector*, except that it only matches elements that are **direct** children, that is, nested only one-level deep:

```css
/* Selects all <li> tags that are direct children of a <ul.top-level-list> */

.top-level-list > li {
  color: orange;
}
```

After adding this, you’ll notice that our `<li>` elements that are not **direct children** of the `<ul.top-level-list>` are still being colored orange. This is because of *inheritance* which we will discuss soon.

### Adjacent sibling selector (`+`)

```css
li + li {
  color: green;
}
```

This would select `<li>` tags only if they were preceded **immediately** by another `<li>` at the same level (sibling) and give them a color of green.

### General sibling selector (`~`)

Similar to the *adjacent sibling selector*, it selects all instances of the second element that appear after the first element, at the same level:

```css
img ~ p {
  border: 1px solid red;
}
```

Would target all `<p>` tags that are siblings following a `<img>`.

> 🧠 The last component listed in a combination selector determines what is targeted! For example, looking above, only `<p>` elements are selected, not the `<img>`.

## Knowledge Checks

- True/False, as with many things in programming, it's crucial that you have all aspects of CSS memorized, even these intermediate topics
- Which pseudo-class would you use for styling an element when the mouse cursor hovers over it?
- How would you select all `li` elements that are *direct* children of `ul` elements?