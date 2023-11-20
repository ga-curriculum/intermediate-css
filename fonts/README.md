# ![Intermediate CSS - Fonts](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will understand how to choose and implement fonts in web development, including the use of system fonts and importing fonts from Google Fonts.

## System fonts

When choosing a font for our projects, we can use a pre-installed system font, a web-safe font, or import a font from a library like Google Fonts.

System fonts are a good option to use because they are guaranteed to be available on all users' devices. This means that our website will look the same for everyone, regardless of what operating system or browser they are using.

To use a system font in CSS, we specify a special font name (`system-ui`) in the [`font-family`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family) property. By specifying this font name we guarantee we are using a font native to the operating system the user is viewing the site on. 

```css
body {
  font-family: system-ui, sans-serif;
}
```

And here's the result:

![The System UI fonts, and their respective Operating Systems.](./assets/system-ui.png)
Image from [system-fonts on GitHub](https://github.com/system-fonts/modern-font-stacks).

By specifying a fallback font, such as `sans-serif`, we ensure that our text will still be readable even if the requested font isn't available.

## Google Fonts

[Google Fonts](https://fonts.google.com/) are a great option if we want to use a font that is not pre-installed on the user's device. Google Fonts are free to use and have a wide variety of fonts to choose from, including serif, sans-serif, display, and handwriting fonts.

Navigate to [https://fonts.google.com/](https://fonts.google.com/) and choose the font(s) you want. 

Once on the page for a specific font, select the font variations that you want to use on your site (if there are multiple).

![Select the font variation on google fonts](./assets/originals/google-fonts-1.png)

If a sidebar doesn't automatically open after selecting a font variation, open it by clicking on the **shopping bag** icon in the top right:

![Select the shopping bag icon](./assets/originals/google-fonts-2.png)

Next, choose `<link>`:

![Select link](./assets/originals/google-fonts-3.png)

Copy the entire shaded block and paste it into the `<head>` of your HTML document above your external stylesheet. 

```html
<!DOCTYPE html>
<html>
<head>
  <link rel="preconnect" href="https://fonts.googleapis.com">
  <link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
  <link href="https://fonts.googleapis.com/css2?family=Montserrat:wght@100&display=swap" rel="stylesheet">
  <!-- external stylesheet below -->
  <link rel="stylesheet" href="./css/style.css">
</head>
```

> ❓ Why do we need to add the google font stylesheet above our stylesheet?

Keep in mind that if you decide to add more Google fonts to your project, you'll need to update the html link.

### Apply your new font

After linking or importing your new font, make sure to apply it to either the entire HTML page by updating the `font-family` property in the body or to specific text elements by modifying their `font-family` property individually.

```css
body {
  font-family: 'Montserrat', sans-serif;
}
```

Check out the [Web-safe Fonts Level Up](../level-up/web-safe-fonts.md) for more details on fonts that are safe to use in web development.
