# CSS Transforms, Transitions, and Animations

<!-- https://learn.shayhowe.com/advanced-html-css/css-transforms/ -->
## CSS Transforms

elements may be transformed on a 2-dimensional or 3-dimensional plane using the x, y, and z axes. To add multiple transform values, they need to all be within a single `transform`. `transform-origin` will change the default center point of transforms for an element and `perspective-origin` will change where the vanishing point is placed.

- 2d
  - `rotate` - rotates an element between 0-360 degrees (positive for clockwise, negative for coutnerclockwise)
  - `scale` - changes the apparent size of an element, (.01-.99 for smaller, 1.1+ for larger), use `scaleX` or `scaleY` for only one axis
  - `translate` - moves an element without disrupting the flow of the document
  - `skew` - distorts elements on the x and y axes
- 3d
  - `perspective` - necessary for any 3d transforms, acts like a vanishing point, can be set in the `transform` or on the parent element with the `perspective` property rather than value
  - all 2d values can be used except for `skew`.

for nested 3d elements, `transform-style: preserve-3d` should be applied to the parent so allow the children to appear in their own 3d plane.

if an element is displayed in a way that shows its back, you can either set `backface-visibility` to `hidden`, which makes it invisible when not facing the screen, or leave it as `visible`, which is the default, showing the back of the element.

<!-- https://learn.shayhowe.com/advanced-html-css/transitions-animations/ -->
## CSS Transitions and Animations

for a transition to take place, an element must change state and each state must have a different style, which can be achieved using pseudo-classes.

The four `transition` properties are

- `transition-property` - determines what properties will be altered
- `transition-duration` - the duration in which a transition takes place
- `transition-timing-function` - sets the speed a transition will move at
- `transition-delay` - sets a value determining how long the transition should be stalled for

when a transition needs multiple states, an animation is the better way to go. To set multiple transition points, use `@keyframe` (includes name, breakpoints, and properties). Breakpoints are set using percentages of the total animation. To apply the animation, you use the properties `animation-name` and `animation-duration`. To make an animation run more than once, you can specify an integer or `infinite` with `animation-iteration-count`. `animation-direction` allows you to play an animation backwards, or back and forth. `animation-play-state` allows you to pause and continue an animation from its current state rather than reseting. `animation-fill-mode` indetifies how an element should be styled before, after, or during an animation.

[`[`< table of contents`]`](code201.md)

[`[`< home`]`](README.md)
