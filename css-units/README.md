# ![Intermediate CSS - CSS Units](./assets/hero.png)

**Learning objective:** By the end of this lesson, students will be able to use different types of CSS units, such as pixels, percentages, and ems

We use CSS units to specify the size of elements in a CSS stylesheets. There are many different types of units to choose from, but they can broadly divided into two categories: **absolute units** and **relative units**.

tktk LEVELUP

## Absolute units

Absolute units are based on a fixed physical measurement, such as inches or pixels. Some examples of absolute units include:

- `px`: Pixels are the most common type of absolute unit. They are based on the resolution of the device that is displaying the web page.
- `in`: Inches are a physical unit of measurement.
- `cm`: Centimeters are another physical unit of measurement.
- `mm`: Millimeters are a smaller unit of measurement than centimeters.
- `pt`: Points are a unit of measurement that is based on the typographic point system.


## Relative units

Relative units are based on the size of another element on the page. Some examples of relative units include:

- `em`: Ems are based on the font size of the parent element.
- `rem`: Rems are similar to ems, but they are based on the font size of the root element.
- `%`: Percentages are based on the size of the container element, and as a result are always relative to the size of that element.  
- `vw` - 1% of width
- `vh` - 1% of height

## Which units to use

The type of CSS units that we should use depends on the specific property that we are styling. For example, if we are styling the width of an element, we would typically use an absolute unit, such as pixels. This is because we want the element to be a specific width, regardless of the device that it is being displayed on.

However, if we are styling the font size of an element, we might want to use a relative unit, such as ems. This is because we want the font size of the element to be relative to the font size of the parent element. This will ensure that the font size of the element is always consistent with the rest of the page.

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

