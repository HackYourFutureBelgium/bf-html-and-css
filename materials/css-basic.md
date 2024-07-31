# CSS

## What is CSS?

- **CSS** stands for **Cascading Style Sheets**.
- It describes how HTML elements are displayed on screen.
- CSS can control the layout of multiple web pages simultaneously.
- External stylesheets are typically stored in `.css` files.

## Syntax

```css
selector {
  property: value;
  property: value;
  property: value;
}
```

## Selectors

### Simple Selectors

```css
/* This is a comment */

*,
*::after,
*::before {
  box-sizing: border-box;
}

p {
  text-align: center;
  color: red;
}

.paragraph {
  text-align: center;
  color: red;
  font-size: 1.2rem;
  font-family: "Courier New", Courier, monospace;
  font-weight: bold;
}

p.paragraph {
  text-align: center;
  color: red;
}

#paragraph {
  text-align: center;
}
```

### Combinator Selectors

```css
/* Descendant selector: Select all <p> inside section */
section p {
  color: #21211f;
}

/* Child selector: Select all <p> which are direct children inside section */
section > p {
  color: #21211f;
}

/* Adjacent Sibling selector: Select <p> that come immediately after <div> */
div + p {
  color: #21211f;
}

/* General Sibling selector: Select all <p> siblings of <div> */
div ~ p {
  color: #21211f;
}
```

### Pseudo-class Selectors

```css
/* A pseudo-class defines a special state of an element. */

/* Visited link */
a:visited {
  color: #00ff00;
}

/* Mouse over link */
a:hover {
  color: #ff00ff;
}

/* Active link */
a:active {
  color: #0000ff;
}

/* Select the first <p> which is the first child of another element */
section p:first-child {
  color: blue;
}

/* Select the first <p> which is the first child of another element */
section p:nth-child(1) {
  color: blue;
}
```

### Pseudo-element Selectors

```css
/* Style specific parts of an element. */

h1::before {
  content: url(./smiley.gif);
}

h1::after {
  content: url(./smiley.gif);
}
```

### Attribute Selectors

```css
a[target="_blank"] {
  background-color: yellow;
}
/* Select any class "hide" or "hide-" */
[class|="hide"] {
  background: yellow;
}
/* Select any class starting with "hid" */
[class^="hid"] {
  background: yellow;
}
/* Select any class ending with "den" */
[class$="den"] {
  background: yellow;
}
/* Select any class containing "te" */
[class*="te"] {
  background: yellow;
}

input[type="text"] {
  width: 150px;
  display: block;
  margin-bottom: 10px;
  background-color: yellow;
}
```

## Color

```css
section > h2 {
  color: #21211f;
  /* 
  color: hsl(60, 3%, 13%);
  color: rgb(34, 34, 32);

  An HSL color value is specified with: hsl(hue, saturation, lightness).
  Hue is a degree on the color wheel (from 0 to 360):
  0 (or 360) is red
  120 is green
  240 is blue
  Saturation is a percentage value: 100% is the full color.
  Lightness is also a percentage; 0% is dark (black) and 100% is white.
  */
}
```

## Background

```css
div {
  background-color: #fff;
  background-image: url(../assets/html-css.png);
  background-repeat: no-repeat;
  background-position: top;
}
```

## Border

```css
p {
  border: 2px red dashed;
}
```

## Margin

```css
p {
  margin: 2px 3px 4px 5px;
  /* 
  margin: 10px 20px; 
  */
}
```

## Icons

```html
<!DOCTYPE html>
<html>
  <head>
    <script
      src="https://kit.fontawesome.com/a076d05399.js"
      crossorigin="anonymous"
    ></script>
  </head>
  <body>
    <div>
      <i class="fas fa-car"></i>
    </div>
  </body>
</html>
```

## Links

```css
/* Unvisited link */
a:link {
  color: red;
}

/* Visited link */
a:visited {
  color: green;
}

/* Mouse over link */
a:hover {
  color: hotpink;
}

/* Selected link */
a:active {
  color: blue;
}
```

## Lists

```css
ul {
  list-style: none;
}
```

## Display

```css
h1 {
  display: none;
}

h2 {
  visibility: hidden;
}
```

## Width

```css
div {
  width: 20%;
  /* 
  width: 500px;
  max-width: 700px; 
  */
}
```

## Position

```css
/* Default value is static */
div {
  position: relative;
}

div span {
  position: absolute;
  top: 30px;
  left: 50px;
}
/*
static: Static positioned elements are not affected by the top, bottom, left, and right properties.

fixed: Positioned relative to the viewport, always stays in the same place even if the page is scrolled.

relative: Positioned relative to its normal position. Adjusted with top, right, bottom, and left properties.

absolute: Positioned relative to the nearest positioned ancestor. Uses the document body if no positioned ancestors are found.

sticky: Positioned based on the user's scroll position.
*/
```

## Z-Index

```css
/* z-index controls the stacking order of elements */

img {
  position: absolute;
  left: 0px;
  top: 0px;
  z-index: -1;
}
```

## Overflow

```css
/* overflow controls content that is too big to fit into an area. */

div {
  width: 200px;
  height: 65px;
  background-color: coral;
  overflow: visible;
  /*
  overflow: hidden;
  overflow: scroll;
  overflow: auto;   /* Add scroll only when necessary */
  */
}
```

## Float

```css
img {
  float: right;
  /* 
  float: left;
  float: none; 
  */
}
```

## Display Inline-block

```css
/* 
inline: Can't set height and width; top and bottom margin and padding are not respected.
inline-block: Can set height, width; top and bottom margin and padding are respected.
block: Adds a line break after the element.
*/
span {
  display: inline-block;
  /* 
  display: block; 
  display: inline; 
  */
}
```

## Units

```css
/* 
Absolute units:
cm
mm
in  (1in = 2.54cm)
px 
pt 

Relative units:
em: 2em means 2 times the size of the current font.
rem: Relative to the font-size of the root element.
vw: Relative to 1% of the width of the viewport.
vh: Relative to 1% of the height of the viewport.
%: Relative to the parent element.
*/
h1 {
  font-size: 60px;
}
```

## Specificity

```css
/* 
1. Inline styles: Example: <h1 style="color: pink;">
2. IDs: Example: #navbar
3. Classes, pseudo-classes, attribute selectors: Example: .test, :hover, [href]
4. Elements and pseudo-elements: Example: h1, ::before 
5. Universal selector * 
*/
```

## !important

```css
/* 
!important rule overrides all previous styling rules for that specific property on that element.
*/
#my-id {
  background-color: blue;
}

.my-class {
  background-color: gray;
}

p {
  background-color: red !important;
}
```
