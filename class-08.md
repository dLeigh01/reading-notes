# CSS Layout
<!--https://web.dev/learn/css/layout/-->
the `display` property can determine if the box it is applied to acts as an inline or block element, nad it can determine how any child elements should behave, such as becoming a flex container allowing the children to use flex properties.

the two main mechanisms that go into layout rules for multiple elements are `flexbox` and `grid`.

`flexbox` is for a single dimension, having elements sit next to each other either on the x or y axis. They will not wrap around each other, but that can be adjusted using `align-items`, `justify-content`, and `flex-wrap`. You can also control each item's size with `flex-grow`, `flex-shrink`, and `flex-basis`.

`grid` is designed to control multi-axis layouts and allows you to control any elements with `display: grid`. `grid-row` and `grid-column` control how many spaces in the grid a single item will take up.

when not using `grid` or `flexbox` there are still methods you can use to change the normal flow or your elements, such as `inline-block`, which gives you some characteristic of a block element while still running inline. `float` instructs an element to float in the specified direction, allowing other elements to flow around it.

`position` changes how an element behaves in the normal flow of the document and relates to other elements. It can be used with `relative`, `absolute`, `fixed`, and `sticky`.

[`[`< table of contents`]`](code201.md)

[`[`< home`]`](README.md)
