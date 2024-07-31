# CSS Advanced

## Border Radius

```css
/* border-radius: Gives any element "rounded corners" */
.showcase img {
  border-radius: 12px;
  background: #73ad21;
  padding: 20px;
  width: 200px;
  height: 150px;

  /* Example values: */
  /* border-radius: 25px 10px 20px 13px; */
  /* border-radius: 50%; */
}
```

## 2D Transform

```css
/* 
transform: Allows you to move, rotate, scale, and skew elements.
Values: X, Y
- translate(10px, 20px): Moves an element from its current position to a new position.
- rotate(20deg): Rotates an element clockwise (20deg) or counter-clockwise (-20deg).
- scaleX(3): Increases or decreases the element's width.
- scaleY(10): Increases or decreases the element's height.
- scale(2,3): Increases or decreases the size of an element. 2 (width), 3 (height).
- skewX(20deg): Skews an element along the X-axis by the given angle.
- skewY(40deg): Skews an element along the Y-axis by the given angle.
- skew(20deg,40deg): Skews an element along the X-axis and Y-axis by the given angle.
*/

div {
  transform: translate(50px, 100px);
}
```

## 3D Transform

```css
/* 
transform: Allows you to rotate elements in 3D space.
Values:
- rotateX()
- rotateY()
- rotateZ()
*/

div {
  transform: rotateX(150deg);
}
```

## Transitions

```css
/*
transitions: Allows you to change property values over a specified duration.
To create a transition effect, specify:
- The CSS property to animate
- The duration of the effect

Example properties:
- transition-property: background-color
- transition-duration: 3s
- transition-timing-function: linear, ease, ease-in, ease-out, ease-in-out
- transition-delay: 1s;
*/

div {
  background-color: red;
  transition: background-color 3s;
}

div:hover {
  background-color: blue;
}
```

## Animations

```css
/*
animations: Allows elements to gradually change from one style to another.
To use CSS animation, define keyframes for the animation.
*/

@keyframes box-move {
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

/* Element to apply the animation to */
div {
  width: 100px;
  height: 100px;
  position: relative;
  background-color: red;
  animation-name: box-move;
  animation-duration: 10s;
  animation-delay: 2s;
  animation-iteration-count: 3;
  /* animation-iteration-count: infinite; */
}
```

## Tooltip

```css
/* 
tooltip: Specifies extra information about something when the user moves the mouse pointer over an element.
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

## Variables

```css
/*
Variables: Create a variable with global scope inside the :root selector.
Variable names start with --, e.g., --primary-color.
Use var(--name) to insert the variable value.
*/

:root {
  --primary-color: #1e90ff;
}

p {
  color: var(--primary-color);
}
```
