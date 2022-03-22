# Chart.js and Canvas

<!-- https://www.webdesignerdepot.com/2013/11/easily-create-stunning-animated-charts-with-chart-js/ -->
## Chart.js

charts are better for displaying data visually than tables, as they are easier to look at and convey data more quickly. Chart.js is a plugin for JavaScript that allows you to draw graphs onto the page using `<canvas>`.

<!-- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Basic_usage -->
## Basic Usage of Canvas

`<canvas>` has two attributes, `width` and `height` which are both optional, with a default of 300x150px. Whenever you are using this element, you should provide fallback content for older versions of the browser that can't use the element. Because of the ability to use fallback content, `<canvas>` is not a self-closing tag. When you have the element set up in HTML, you then need to pull it into JavaScript and use the `getContext` function to obtain its drawwing functions.

<!-- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_shapes -->
## Drawing Shapes with Canvas

the canvas grid is also known as the coordinate space, each grid coordinate acts as 1 pixel on the canvas, and the origin is placed at the top left, (0,0). `<canvas>` only supports rectangles and paths, but you can combine things to create other shapes.

to draw a rectangle, you use `fillRect(x, y, width, height)` for a filled rectangle, `strokeRect(x, y, width, height)` for a rectangle outline, or `clearRect(x, y, width, height)` to clear out a space in the shape of a rectangle.

to draw a path, you start with `beginPath()`, then you specify where each point is starting at `moveTo()` and drawing to `lineTo()` or `arcTo()`, and then you can use, `closePath()` to add a straight line to the beginning of the current sub-path, `stroke()` to draw the outline of a shape, and `fill()` to fill the path's content area. you can also draw lines using `bezierCurveTo()` and `quadraticCurveTo()`, but those are more complex.

<!-- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Applying_styles_and_colors -->
## Applying Styles and Colors

the two important properties for coloring on the canvas are `fillStyle` (sets the style for filling shapes) and `strokeStyle` (sets the style for shapes' outlines). You can draw with semi transparency using either `globalAlpha` or by assigning a semi-transparent color to the stroke or fill style.

there are also several properties that allow us to style lines:

- `lineWidth` - sets the width of future lines
- `lineCap` - sets the appearance of the end of lines
- `lineJoin` - sets the appearance of corners
- `miterLimit` - limits how thick a junction can become
- `getLineDash()` returns the current line dash pattern array containing an even number of non-negative numbers
- `setLineDash(segments)` - sets the current line dash pattern
- `lineDashOffset` - specifies where to start a dash array on a line

you can also create gradients in `<canvas>` using `createLinearGrandient()`, `createRadialGradient()`, and `createConicGradient()`. Once you have the gradient created, you can add its colors using `gradient.addColorStop(position, color)`

`createPattern(image, type)` creates a new pattern object.

<!-- https://developer.mozilla.org/en-US/docs/Web/API/Canvas_API/Tutorial/Drawing_text -->
## Drawing Text

you can use two methods to render text, `fillText(text, x, y, [, maxWidth])` which fills text at the given coordinates or `strokeText(text, x, y, [, maxWidth])` which strokes text at the given target. You can also use `measureText()` to get more information with a `TextMetrics` object.

[`[`< table of contents`]`](code201.md)

[`[`< home`]`](README.md)
