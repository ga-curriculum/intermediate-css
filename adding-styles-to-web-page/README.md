# ![Intermediate CSS - Adding Styles to a Web Page](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to use inline, internal, and external stylesheets and understand CSS precedence.


There are three ways to add styling to a web page:

  1. Inline styles
  2. Internal stylesheets
  3. External stylesheets

These three techniques are not mutually exclusive; you can use one or more of them on the same webpage.

## Inline styles

An **inline** style can be used to apply styling to a single element using the `style` attribute.

Using inline styles breaks our separation of concerns by mixing content with presentation; therefore, avoid using this technique unless there’s a good reason to do so, for example, when testing or debugging styles.

> ⚠️ Several JS libraries and frameworks such as AngularJS add inline styles dynamically to perform their magic. ReactJS even encourages the use of inline styling “components” dynamically. However, in general, developers rarely use inline styling for their application’s CSS.

To demonstrate inline styling, let’s use it to change the color of the font:

```html
<h1 style="color: green">Intro to CSS</h1>
<h2>Three Ways to Add Styles</h2>
```

## Internal Stylesheets

The next technique available to add styling is **internal stylesheets**.

An internal stylesheet is created by using a `<style>` element nested within the document’s `<head>` element:

```html
<head>
  <meta charset="UTF-8">
  <title>Intermediate CSS</title>
  <!-- bring in an external stylesheet -->
  <link rel="stylesheet" href="css/style.css">
  <!-- inline stylesheet -->
  <style>
    h1, h2 {
      color: red;
    }
  </style>
</head>
```

Inline stylesheets are not the preferred method to add styles to your web page.

## External Stylesheets

We can also add styling using **external stylesheets**. Styling a page using **external stylesheets** is considered a best practice. This is because it provides the best separation of concerns, along with reusability and maintainability.

External stylesheets are separate files with a `.css` extension and are “linked” to the document using the `<link>` element.

We already linked our external stylesheet during setup, but this is the line responsible for doing that:

```html
<head>
  <meta charset="UTF-8">
  <title>Intro to HTML and CSS</title>
  <!-- bring in an external stylesheet -->
  <link rel="stylesheet" href="/css/style.css">
</head>
```

> 🧠 The `href` path, in this case, is relative to `index.html`. Also, the `rel` attribute stands for “relationship”.

Let’s add a CSS rule inside our new style.css file to test it out:

```css
h1, h2 {
  color: blue;
}
```

## Precendence

When multiple CSS styles are defined for a single element, browsers use a mechanism called **precedence** determine which one to apply. 

Inline styles have the highest precedence, followed by inernal stylesheets and then external stylesheets.

This hierarchy means that if more than one type of stylesheet is being used, any inline styles will override those defined in interal or external stylesheets. 

One exception to this rule, however, is the `!important` declaration. This can be used to override any other style, regardless of the stylesheet precedence. 

> ⚠ Use the `!important` declaration sparingly. Overuse can make your CSS difficult to maintain and debug. 

> ❓ In the following code, which rule do you think will take precedence?

```html
<!DOCTYPE html>
<html>
<head>
  <link rel="stylesheet" href="/css/style.css">
  <style>
    p {
      color: red !important;
    }
  </style>
</head>
<body>
  <p style="color: blue">This is a paragraph.</p>
</body>
</html>
```

