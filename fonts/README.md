# ![Intermediate CSS - Fonts](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will understand how to choose and implement fonts in web development, including the use of web-safe fonts and importing web fonts from Google Fonts.

## web-safe Fonts

When choosing a font for our projects, we can either use a pre-installed **web-safe font**, or we can import a web font from a library like **Google Fonts**.

Web-safe fonts are a good option to use because they are virtually guaranteed to be available on all users' devices. This means that our website will look the same for everyone, regardless of what operating system or browser they are using.  Here are fonts that are available on the vast majority browsers:

- Arial (sans-serif)
- Verdana (sans-serif)
- Tahoma (sans-serif)
- Trebuchet MS (sans-serif)
- Times New Roman (serif)
- Georgia (serif)
- Courier New (monospace)
- Brush Script MT (cursive)

To use a Web-safe font in CSS, we specify the font name (e.g. Arial) in the [`font-family`](https://developer.mozilla.org/en-US/docs/Web/CSS/font-family) property.

```css
body {
  font-family: Arial, sans-serif;
}
```

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

## Knowledge Checks

- True/False: in the unlikely event that a browser does not contain a web-safe font, it is a good idea specify a backup, such as `sans-serif`
- True/False: Google fonts are available on all browsers by default
- Once you've linked to a Google font in your html, how do you use it?