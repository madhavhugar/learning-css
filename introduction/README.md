# Introduction + CSS Basics

## Shortcuts

- To create a div element type in `div` and hit tab

- To create 10 div elements type in `div*10` and hit tab

- To create a h1 element with a class tag `heading` type in `h1.heading` to get `<h1 class="heading"></h1>`

- To create a h1 element with a id tag `heading` type in `h1.heading` to get `<h1 id="heading"></h1>`


## Definition

> CSS => style sheet lanaguage to create rules how HTML elements should be displayed

## How to write CSS

Three styling methods:

- inline styling: not the best practice, might lead large and messy code and duplicated code
- internal styling: not the best practice again
- external styling: 


## CSS selectors

style element: best practice to be placed in head element; 
we use selector to apply styles

selecting items preference:
- last in preference 
- id; class; html-tag-names

## CSS combinators

`(space)` descendant combinators

```
    section p {
        ...
    }
```

`>` child combinators

```
    section > p {
        ...
    }
```

`+` adjacent sibling 

```
    section + p {
        ...
    }
```

`~` general sibling 

```
    section ~ p {
        ...
    }
```

## CSS colors

colors can be specified using:
- color names: modern browsers support 140 color names
- rgb values: rgb(red, green, blue); rgba(red, green, blue, opacity) eg. `rgb(255, 0, 0); rgba(255, 0, 0, 0.5)`
- hexadecimal: #ffffff (white); #000000 (black); #ff00000 (red); #00ff00 (green); #00000ff (blue)

## Inheritance

Elements inherit css styling from their parent elements. By default, the closer parent styles take precedence.

## Text formatting

font-size; text-align[left, right, justify, center] (works only with block level element); font-family; font-weight; font-style[italics, normal]

Block element: take up full width that is available on the page
Inline element: take up width that is required to display the content of an element

explored google fonts: https://fonts.google.com/

## Box Model

![box model](box-model.png)

- border can be specified using: `border: 5px #ff0101 solid;` which translates to `border: border-width border-color border-style`. Each of these values can be independently set as well
- padding can be specified using: `padding: 30px 50px 70px 90px;` which translates to `padding: padding-top padding-right padding-bottom padding-left;`. When we want to set a given value on top & bottom (100px) and another value on left & right (50px) we can do this: `padding: 100px 50px`. And when we want to apply the same value (100px) for all sides, we can do this: `padding: 100px`.
- margin can be specified using: `margin: 30px 50px 70px 90px;` (padding rules apply here too...)

#### Box sizing

Let us set:
- width === 300px 
- height === 300px

- (default) When the property `box-sizing: content-box;` padding and border are not included within height and width
- When the property `box-sizing: border-box;` padding and border are included within height and width

If we want to center a block level element perfectly we can do so by setting 
1. margin as auto 
2. by setting a value to width

 Eg. `margin: 100px auto` centers the block element in the center on the horizontal axis, but does not do the same on the vertical axis (since 100px is set)

## Pseudo classes

> A CSS pseudo-class is a keyword added to a selector that specifies a special state of the selected element(s). For example, :hover can be used to change a button's color when the user's pointer hovers over it.

```css
/* Any button over which the user's pointer is hovering */
button:hover {
  color: blue;
}
```
Pseudo-classes let you apply a style to an element not only in relation to the content of the document tree, but also in relation to external factors like the history of the navigator (:visited, for example), the status of its content (like :checked on certain form elements), or the position of the mouse (like :hover, which lets you know if the mouse is over an element or not).

## Pseudo elements

**Pseduo classes**: define special state of an element (`a:hover`)
**Pseudo elements**: define style for specific part of an element (`h1::after`)

> A CSS pseudo-element is a keyword added to a selector that lets you style a specific part of the selected element(s). For example, ::first-line can be used to change the font of the first line of a paragraph.

```css
/* The first line of every <p> element. */
p::first-line {
  color: blue;
  text-transform: uppercase;
}
```

## Measurement Units

In general, css supports: Absolute and Relative

- Absolute: are fixed units
    - Pixel(px) (1px === 12.54cm), Centimeter(cm), Millimeter(mm), Inch(in), Points(pt), Pica(pc)
As web devs, we usually use Pixels, other units are not recommend to be used


- Relative units specify length relative t0 another property
    - em, rem, vw, vh, %

In case of relative units, the unit is relative to the value set on the parent element or the root element

While em is relative to the font-size of its direct or nearest parent, rem is only relative to the html (root) font-size.

## Positions

To align elements in place, we need to use css positions. We have five different types of positions:

- static: positioning is the default. It defines the position of a given box essentially as an unpositioned element – it flows in the normal rendering sequence of the web page. Static positioned elements are not affected by the top, bottom, left, and right properties.

- relative: An element with position: relative; is positioned relative to its normal position. Setting the top, right, bottom, and left properties of a relatively-positioned element will cause it to be adjusted away from its normal position. Other content will not be adjusted to fit into any gap left by the element.

- absolute: An element with position: absolute; is positioned relative to the nearest positioned ancestor (instead of positioned relative to the viewport, like fixed).
However; if an absolute positioned element has no positioned ancestors, it uses the document body, and moves along with page scrolling.

    if the parent elements have position as static and the child element has absolute, the child element will move according to body element. To ensure child element moves in accordance with it's parent element, we need to set the parent element position to be `relative` or `absolute`.

    If an element has position absolute and at the same time it has no height and width set, then the element acts as an inline element

- fixed: An element with position: fixed; is positioned relative to the viewport, which means it always stays in the same place even if the page is scrolled. The top, right, bottom, and left properties are used to position the element

- sticky: An element with position: sticky; is positioned based on the user's scroll position.
A sticky element toggles between relative and fixed, depending on the scroll position. It is positioned relative until a given offset position is met in the viewport - then it "sticks" in place (like position:fixed). we also need to set the top element of the position

z-index: is used to specify the stack order of an element

## Overflow

overflow works only for block level elements with a specified height

The CSS overflow property controls what happens to content that is too big to fit into an area.

The overflow property has the following values:

- visible - Default. The overflow is not clipped. The content renders outside the element's box
- hidden - The overflow is clipped, and the rest of the content will be invisible
- scroll - The overflow is clipped, and a scrollbar is added to see the rest of the content
- auto - Similar to scroll, but it adds scrollbars only when necessary
