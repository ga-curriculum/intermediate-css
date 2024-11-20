<h1>
  <span class="headline">Intermediate CSS</span>
  <span class="subhead">Setup</span>
</h1>

Open your Terminal application and navigate to your ~/code/ga/lectures directory:

```bash
cd ~/code/ga/lectures
```

Make a new directory called `intermediate-css`, then enter this directory:

```bash
mkdir intermediate-css
cd intermediate-css
```

Create a directory called `css`:

```bash
mkdir css
```

Then, create an `index.html` file, and a `style.css` file that lives inside the `css` directory. These files will hold your work for this lecture:

```bash
touch index.html css/style.css
```

With the files created, open the contents of the directory in VS Code:

```bash
code .
```

Open the `index.html` file and add HTML boilerplate. Then make use of the `style.css` file by adding this line inside the `<head>` tag:

```html
<link rel="stylesheet" href="./css/style.css">
```

Add the following HTML below the closing `</head>` tag:

```html
<body>
  <article>
    <a href="#about">About Section</a>
    <h1>Intermediate CSS</h1>
    <p id="about">More About CSS</p>
    <div>This is a DIV</div>
    <div class="fun">This is another DIV</div>
    <div class="fun super-cool">
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
    <form>
      <label for="name">Name:</label>
      <input type="text" id="name">
      <label for="year">Year:</label>
      <input type="number" id="year">
    </form>
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
