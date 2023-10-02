# Setup

Open your Terminal application and navigate to your ~/code/sei/lectures directory:

```bash
cd ~/code/sei/lectures
```
Make a new directory called `intro-to-css`, then enter this directory:

```bash
mkdir intro-to-css
cd intro-to-css
```

Create a folder called `css`:

```bash
mkdir css
```

Then, create an `index.html` file, as well as a `style.css` file that lives inside the `css` folder. These files will hold your work for this lecture:

```bash
touch index.html css/style.css
```
With the files created, open the contents of the directory in VS Code:

```bash
code .
```

Open the `index.html` file and add HTML boilerplate. Then make use of the `style.css` file by adding this line inside the `<head>` tag:

```html
<link rel="stylesheet" href="/css/style.css">
```


Add the following HTML below the closing `</head>` tag:
```html
<body>
  <article>
    <a href="#about">About Section</a>
    <h1>Intro to CSS</h1>
    <p id="about">More About CSS</p>
    <div>This is a DIV</div>
    <div class="crazy">This is another DIV</div>
    <div class="crazy super-cool">
      <p>This is a paragraph inside of the third DIV</p>
    </div>
    
    <h3 id="comments-title">Comments</h3>
    <ul class="top-level-list">
      <li>Comment One</li>
      <li class="super-cool">Comment Two</li>
      <li>
        Comment Three
        <ul>
          <li>First Reply to Comment Three</li>
          <li>Second Reply to Comment Three</li>
        </ul>
      </li>
    </ul>
  </article>
</body>
```

Add the following code inside of `style.css`:

```css
body {
  font-family: Helvetica, Tahoma, Verdana, sans-serif;
}

h1 {
  text-align: center;
}
```


Open the `index.html` file in your browser. 
