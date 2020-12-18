# Introduction

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