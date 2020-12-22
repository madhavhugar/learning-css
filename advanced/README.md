# Advanced CSS

## Backgrounds

![background attributes](backgrounds_part1.png)

![more background attributes](backgrounds_part2.png)

## Gradients

![gradient attributes](gradientsv1.png)

The following attributes can be set to achive the below:

![gradient effect](gradientsv2.png)

Gradients are also used with images. We can set the following attributes:

![gradient attributes with image](gradientsv3.png)

To achieve this:

![gradient effect on image](gradientsv4.png)

## Shadows

We can use the shadow attributes:

![shadow attributes](shadowsv1.png)

to get:

![shadow effects](shadowsv2.png)

## Transitions

- (req) transition-property: defines the property you want to add effect to
- (req) transition-duration: defines how long you want the transition to continue
- (optional) transition-delay: delay time of effect
- (optional) transition-timing-function: different speeds of effects while effect happens

For setting `transition-timing-function: cubic-bezier` use reference: https://cubic-bezier.com/

shorthand notation for the transition property is: `transition: width 1s 1s ease-in`

for setting multiple transitions: `transition: width 1s 1s ease-in, background-color 5s;`


## Transforms

The transform CSS property lets you rotate, scale, skew, or translate an element. It modifies the coordinate space of the CSS visual formatting model.

We can set the transform attributes to animate objects:

![transform functions 1](transformsv1.png)

![transform functions 2](transformsv2.png)

See [demo](https://developer.mozilla.org/en-US/docs/Web/CSS/transform)

## Animations

Keyframes and properties

- (req) animation-name: the keyframe name
- (req) animation-duration:
- (optional) animation-delay: 
- (optional) animation-iteration-count: for looping animations
- (optional) animation-direction: allows animation in a specified direction [normal, reverse, alternate, alternate-reverse]
- (optional) animation-timing-function: [ease, linear, ease-in, ease-out] similar to tranform functions
- (optional) animation-fill-mode: related to starting and ending position of element

Short form:

`animation: <keyframe-name> 4s ease-in 2s infinite alternate both`

