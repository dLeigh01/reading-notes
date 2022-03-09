# HTML Lists, Control Flow with JS, & CSS Box Model

<!--From HTML&CSS by Jon Duckett-->
## Lists

ordered lists are created with the `<ol>` tag. Every item inside that tag should be within a `<li>` tag.

unordered lists are created with the `<ul>` tag, and the items inside use the same `<li>` tag as the ordered list.

definition lists are created using `<dl>` and generally is made up of a list of terms and their definitions. The items within this type of list use `<dt>` for the term itself and `<dd>` for the definition.

you can also create nested lists by adding another list tag within an `<li>`.

## Boxes

by default, boxes are the same size as whatever they contain. To change that, you can use the `height` and `width` properties. The most popular way to declare size is generally with pixels, since they are the easiest to control - if you use percentages the box will scale with the window and when you use ems the size of the box depends on the size of its content.

you can limit the width using `min-width` and `max-width`, which keeps the box size from going too off the rails on different devices. The same goes for height, which can be limited with `min-height` and `max-height`. If the content ends up becoming too big for the box, then you can use `overflow`. `overflow: hidden;` hides anything that doesn't fit in the box and `overflow:scroll;` adds a scrollbar to the box so users can get to the missing content.

every box has three properties that can be altered:

- border - separates the margin from the padding
- margin - is outside of the border and spaces the box out from other boxes
- padding - is inside the border and spaces out the edge of the box from the content

the padding and margin properties are an easy way to add space between items on the page. The space between those items is referred to as white space.

another thing you can mess with is the border. `border-width`, allows you to control the width of any side of the border, `border-style`, can give you a multitude of different border designs, `border-color` changes the color of the border, and `border-radius` controls how rounded its corners are.

if you want to center content, you can set the left and right margins to `auto`, and as long as you've set a width for the box it will move to be centered on the page. To work on older browsers, it also requires `text-align: center;`

`display` allows you to change elements between block and inline, or to hide elements altogether. You can also hide elements using `visibility`, which leaves a space where the box was meant to be.

`border-image` allows you to use an image as the border of a box, by slicing it into pieces and then using thosein a way thats either stretched or repeated to make up the sides of the box.

`box-shadow` will give you a drop shadow around a box that you can offset or blur as needed. you can also use `box-shadow: inset;` to create a shadow *in* the box.

<!--From JavaScript&JQuery by Jon Duckett-->
## Switch Statements

a switch statement starts with a switch value variable, then every case in the switch statement indicates a possible value for that variable and contains code to run if it matches. The entirety of the code sits in one set of curley bracers and each case ends with a `break;` to escape the switch.

if you use an unexpected data type, JavaScript will still attempt to make sense of it using type coercion to change a data type to complete the operation. JavaScript is a weak typing language because the type of variables can change. To avoid type coercion, you should use `===` instead of `==`.

truthy and falsey variables exist in JavaScript, as variables that aren't strictly Booleans, but will still evaluate to be true or false. Because most things like arrays are truthy, they are often used to check whether an element exists within the page.

loops will check a condition and then run a block of code if it returns true, then continue to run that block of code until it returns false.

- for loops run a specific number of times
- while loops will run an unspecified number of times as long as the condition remains true
- do while loops are the same as while loops except they always run at least once

ex

```js
for(var i = 0; i < 10; i++){
  enter code here
}
```

loops are helpful when working with arrays because they allow you to do things like write out every value of an array without knowing how many values it contains. All variables should be declared outside of loops if possible, as otherwise it is recalculated on every loop and uses up browser resources.

[`[`< table of contents`]`](code201.md)

[`[`< home`]`](README.md)
