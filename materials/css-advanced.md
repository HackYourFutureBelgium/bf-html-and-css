# CSS

## border-radius

```css
/* border-radius :  you can give any element "rounded corners" */
.showcase img {
  border-radius: 12px;
  background: #73ad21;
  padding: 20px;
  width: 200px;
  height: 150px;

  /* 
  border-radius: 25px 10px 20px 13px; 
  border-radius: 50%; 
  */
}
```

## 2D transform

```css
/* 
transform allows you to move, rotate, scale, and skew elements.
values :   X     Y
translate(10px, 20px) : moves an element from its current position to a new position.
rotate(20deg) : rotates an element clockwise(20deg) or counter-clockwise(-20deg).
scaleX(3) : increases or decreases the element width.
scaleY(10) : increases or decreases the element height.
scale(2,3) : increases or decreases the size of an element. 2(width), 3(height).
skewX(20deg) : method skews an element along the X-axis by the given angle.
skewY(40deg) : method skews an element along the Y-axis by the given angle.
skew(20deg,40deg) : method skews an element along the X-axis and Y-axis by the given angle
*/

div {
  transform: translate(50px, 100px);
}
```

## 3D transform

```css
/* 
transform:  allows you rotate element in 3D
values :  
rotateX()
rotateY()
rotateZ()
*/

div {
  transform: rotateX(150deg);
}
```

## transitions

```css
/*
transitions allows you to change property values, over a given duration.
To create a transition effect, you must specify two things:

the CSS property you want to add an effect to
the duration of the effect

transition-property:background-color 
transition-duration: 3s
transition-timing-function: linear, ease, ease-in, ease-out, ease-in-out
transition-delay: 1s;
*/

div {
  background-color: red;
  transition: background-color 3s;
}

div:hover {
  background-color: blue;
}
```

## animations

```css
/*
animation : allows an element gradually change from one style to another.
To use CSS animation, you must first specify some keyframes for the animation.
*/

@keyframes color-change {
  0% {
    background-color: red;
    left: 0px;
    top: 0px;
  }
  25% {
    background-color: yellow;
    left: 200px;
    top: 0px;
  }
  50% {
    background-color: blue;
    left: 200px;
    top: 200px;
  }
  75% {
    background-color: green;
    left: 0px;
    top: 200px;
  }
  100% {
    background-color: red;
    left: 0px;
    top: 0px;
  }
}

/* The element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: color-change;
  animation-duration: 10s;
  animation-delay: 2s;
  animation-iteration-count: 3;
  /* animation-iteration-count: infinite;    */
}
```

## tooltip

```css
/* 
tooltip : used to specify extra information about something 
when the user moves the mouse pointer over an element 
*/

.tooltip {
  position: relative;
  display: inline-block;
}

/* Tooltip text */
.tooltip .tooltip-text {
  visibility: hidden;
  width: 120px;
  position: absolute;
  z-index: 1;
}

.tooltip:hover .tooltip-text {
  visibility: visible;
}
```

## variables

```css
/*
To create a variable with global scope, declare it inside the :root selector.
The :root selector matches the document's root element.
the variable name must start with two --   ex: --primary-color
we can use the var(--name) to insert the variable value
*/
:root {
  --primary-color: #1e90ff;
}

p {
  color: var(--primary-color);
}
```
