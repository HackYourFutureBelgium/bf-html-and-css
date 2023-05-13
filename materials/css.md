# CSS

> What is HTML ?

- CSS stands for Cascading Style Sheets
- CSS describes how HTML elements are to be displayed on screen.
- CSS can control the layout of multiple web pages all at once
- External stylesheets are stored in CSS files

## Syntax

```css
selector {
  property: value;
  property: value;
  property: value;
}
```

## Selector

### Simple selector

```css
/* This is a comment  */

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

### Combinator selector

```css
/* descendant selector : select all <p> inside section */
section p {
  color: #21211f;
}

/*  child selector : select all <p> which are direct children inside section */
section > p {
  color: #21211f;
}

/*  Adjacent Sibling  selector : 
both div and p must have the same parent and it will select all <p> which
come after <div> immediately 
*/
div + p {
  color: #21211f;
}

/*  General Sibling  selector : 
both div and p must have the same parent and it will select all <p> which
are sibling to <div> and come after the <div>
*/
div ~ p {
  color: #21211f;
}
```

### Pseudo-class selector

```css
/* A pseudo-class is used to define a special state of an element. */
/* visited link */
a:visited {
  color: #00ff00;
}

/* mouse over link */
a:hover {
  color: #ff00ff;
}

/* selected link */
a:active {
  color: #0000ff;
}

/* it will select the first <p> which is the first child of another element */
section p:first-child {
  color: blue;
}
/* it will select the first <p> which is the first child of another element */
section p:nth-child(1) {
  color: blue;
}
```

### Pseudo-element selector

```css
/* A CSS pseudo-element is used to style specified parts of an element.

For example, it can be used to:

Style the first letter, or line, of an element
Insert content before, or after, the content of an element */

h1::before {
  content: url(smiley.gif);
}

h1::after {
  content: url(smiley.gif);
}
```

### Attribute selector

```css
a[target="_blank"] {
  background-color: yellow;
}
/* any class "hide", or "hide-" */
[class|="hide"] {
  background: yellow;
}
/* any class start with "hid" */
[class^="hid"] {
  background: yellow;
}
/* any class end with "den" */
[class$="den"] {
  background: yellow;
}
/* any class contain "te" */
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

## color

```css
section > h2 {
  color: #21211f;
  /* 
  color: hsl(60, 3%, 13%);
  color: rgb(34, 34, 32);
   */
}
```

## background

```css
div {
  background-color: #fff;
  background-image: url(../assets/html-css.png);
  background-repeat: no-repeat;
  background-position: top;
}
```

## border

```css
p {
  border: 2px red dashed;
}
```

## margin

```css
p {
  margin: 2px 3px 4px 5px;
  /* 
  margin: 10px 20px; 
  */
}
```

## icons

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

## links

```css
/* unvisited link */
a:link {
  color: red;
}

/* visited link */
a:visited {
  color: green;
}

/* mouse over link */
a:hover {
  color: hotpink;
}

/* selected link */
a:active {
  color: blue;
}
```

## lists

```css
ul {
  list-style: none;
}
```

## display

```css
h1 {
  display: none;
}

h2 {
  visibility: hidden;
}
```

## width

```css
div {
  width: 20%;
  /* 
  width: 500px;
  max-width: 700px; 
  */
}
```

## position

```css
/* default value is static  */
div {
  position: relative;
}

div span {
  position: absolute;
  top: 30px
  left: 50px;
}
/*
static : Static positioned elements are not affected by the top, bottom, left, and right properties.

fixed :is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled

relative: is positioned relative to its normal position.Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position

absolute: is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed).
However; if an absolute positioned element has no positioned ancestors, it uses the document body

sticky: is positioned based on the user's scroll position.
*/
```

## Z-index

```css
/* 
z-index : controls which element should be placed in front of, or behind, the others 
*/

img {
  position: absolute;
  left: 0px;
  top: 0px;
  z-index: -1;
}
```

## overflow

```css
/* 
overflow  controls what happens to content that is too big to fit into an area. 
*/

div {
  width: 200px;
  height: 65px;
  background-color: coral;
  overflow: visible;
  /* 
  overflow: hidden; 
  overflow: scroll; 
  overflow: auto;   add scroll only when necessary 
  */
}
```

## float

```css
img {
  float: right;
  /* 
  float: left;
  float: none; 
  */
}
```

## display-inline-block

```css
/* 
inline : can't set the height and the width of the element, top and bottom margin and padding are not respected 
inline-block : you cab set the height, width and top and bottom margin and padding will be respected 
block : add a line break after the element.
*/
span {
  display: inline-block;
  /* 
  display: block; 
  display: inline; 
  */
}
```

## units

```css
/* 
Absolute units
cm
mm
in  1in= 2.54cm
px 
pt 

Relative units
em  : 2em means 2 times the size of the current font
rem : Relative to font-size of the root element
vw  : Relative to 1% of the width of the viewport
vh  : Relative to 1% of the height of the viewport
%   : Relative to the parent element

 */
h1 {
  font-size: 60px;
}
```

## specificity

```css
/* 
1- Inline styles - Example: <h1 style="color: pink;">
2- IDs - Example: #navbar
3- Classes, pseudo-classes, attribute selectors - Example: .test, :hover, [href]
4- Elements and pseudo-elements - Example: h1, ::before 
5- universal selector * 
*/
```

## !important

```css
/* 
!important rule, it will override ALL previous styling rules for that specific property on that element! 
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
