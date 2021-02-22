# Brief CSS Cheat Sheet
This document is intended to have a generic cheat sheet about what type of things you can do with CSS. Mostly for technical points(alignment, units, selectors) except basic level properties.

### **Table Of Contents**
* [Selectors](#selectors)
    * [Simple Selectors](#simple-selectors)
        * [Element Selector](#element-selector)
        * [Class Selector](#class-selector)
        * [ID Selector](#id-selector)
    * [Pseudo Selectors](#pseudo-selectors)
    * [Combinator Selectors](#combinator-selectors)
    * [Attribute Selectors](#attribute-selectors)
* [Units](#units)
    * [Absolute](#absolute-lengths)
    * [Relative](#relative-lengths)
* [CSS Box Model](#css-box-model)
    * [Display](#display)
        * [Flexbox](#flexbox)
        * [Grid](#grid)
* [Advanced Properties & Functions](#advanced-properties-&-functions)
    * [Transition](#transition)
    * [Animations(keyframes)](#animations)

****
<br>

# Selectors 
> See [link](https://www.w3schools.com/cssref/css_selectors.asp) for full list of selectors:

## Simple Selectors 

#### Element Selector
- `p{}`
- `h2{}`

#### Class Selector
- `.class-name{}`

#### ID Selector 
- `#some-id{}`

## Combinator Selectors
- `h2 + a {}`   | _first next 'a' after h2_
- `textarea ~ button{}` | _(general sibling selector) Every button after a textarea but in same parent._
- `ul > li {}`| _all 'li' elements where the parent is a 'ul' element_
- `ul li {}` | _any 'li' that propagates up to ul (doesn't matter being a grandchild etc)_
- `ul, p` | _all 'ul' and 'p' elements_ 

## Pseudo Selectors
- `h2:hover{}` | _Mouseover_
- `ul:first-child{}`
- `li:last-child{}`
- `li:nth-child(2){}`
- `li:only-child{}` | _li element which is only child in a parent_
- `#fb-link:visited{}`
- `h2::after{}` | _Insert something after the content of each 'h2' element_
- `h2::before{}` | _Insert something before the content of each 'h2' element_


## Attribute Selectors
- `h2[class=card-top]{}`
- `img[src^="../img"]{}` | _all images that **starts** with this particular source_
- `img[src$="../img"]{}` | _all images that **ends** with this particular source_
- `img[src*="../img"]{}` | _all images that **contains** this particular source_

# Units
*Viewport: the windows size of browser.
## Absolute Lengths
- cm, mm, in, px, pt
## Relative Lengths
- em (rem) | _Relative to font-size (root)_
- vw, vh | _Relative to width/height of the viewport*_
- % | _Relative to the parent el_

# CSS Box Model

## Display
> See [link](https://www.w3schools.com/cssref/pr_class_display.asp) for full list of display properties.

- `inline` 
- `block` | _height/width available, starts on new line_
- `inline-block` | _inline but h/w available_
- `flex` : [(see flexbox below)](#flexbox)
- `grid` : [(see grid below)](#grid)

### **Flexbox**
An element that is split into two parts; container & items.

A display types that comes with a range of properties allowing you to arrange items easily.

> See [link](https://css-tricks.com/snippets/css/a-guide-to-flexbox) for detailded guide to flexbox.

#### `flex-direction`: 
- row | row-reverse | column | column-reverse
#### `flex-wrap` : 
- nowrap | _one line, default_
- wrap | _wrap onto multiple lines_
- wrap-reverse
#### `justify-content / align-items / align-self` :
Horizontal alignment / Vertical alignment / Own vertical alignment of particular item in box.
#### `flex-basis / flex-grow` :
Minimum width of item / Multiplier to fill spaces
#### `flex-shrink` :
If you go below min-width or flex-basis, you lose flex-grow. Flex-shrink begins.

Opposite of flex-grow. Multiplier to lose width.

### **Grid**
A display type to activate certain layout features.

> See [link](https://css-tricks.com/snippets/css/a-guide-to-flexbox) for detailded guide to grid.

#### `grid-template-columns / grid-template-rows`: 
Defines the number and width/height of columns/rows.

#### `grid-columns / grid-rows : 1/3` : 
Assigned to an item in grid.

Starting from first column, take 3 columns. (same for rows)

#### `justify-content / align-content` :
Align-content is for multi line flexible boxes. So this one instead of align-items.

# Advanced Properties & Functions

## Transition
Change property values smoothly, over a given duration.

`transition: background 2s ease`
> See [link](https://www.w3schools.com/css/css3_transitions.asp) for full description.

## Transform
#### `transform: translate(x,y)` : Change place accordingly.
#### `transform: scale(x,y)` : Size.
#### `transform: rotate(90deg)`
> See [link](https://www.w3schools.com/css/css3_transitions.asp) for detailed description.

## Animations
```
div {
  animation-name: example;
  animation-duration: 4s;
}
@keyframes example {
  0% {background-color: red;}
  25% {background-color: green;}
  50% {background-color: black;}
  100% {background-color: yellow;}
}
```
Turning into yellow from starting red through green and yellow for 4 seconds.
> See [link](https://www.w3schools.com/css/css3_animations.asp) for detailed description.


