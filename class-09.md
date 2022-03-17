# Forms and JS Events

<!-- from HTML&CSS by Jon Duckett -->
## Forms

forms allow users to perform many functions online, such as registeration, and shopping.

there are several form controls useable to collect information from users.

- adding text
  - text input - single line, good for emails or names
    - `<input type="text" name="inputIdentifierHere">` optional `<maxlength="">`
  - password input - like text input, but masks the entered characters
    - `<input type="password" name="inputIdentifierHere">` optional `<maxlength="">`
  - text area - for longer areas of texts
    - `<textarea>`
- making choices
  - radio buttons - for when a user needs to pick one of a number of options
    - `<input type="radio" name="inputIdentifierHere" value="valueForThisButton">` optional `checked="checked"` to autoselect this value on load
  - checkboxes - for when a  user can select or unselect one or more options
    - `<input type="checkbox" name="inputIdentifierHere" value="valueForThisBox">` optional `checked="checked"` to autoselect this value on load
  - drop down boxes - when a user must pick an option out of a list
    - `<select name="inputIdentifierHere">` `<option value="valueForThisBox">` optional `selected="selected"` to autoselect this value on load `multiple="multiple"` to allow the user to select multiple options
- submitting forms
  - submit buttons - to submit data from your form
    - `<input name="inputIdentifierHere" value="valueForThisBox">`
  - image buttons - allow you to use an image
    - `<input type="image">`
- uploading files
  - file upload - allows users to upload files
    - `<input type="file" name="inputIdentifierHere">`
- button and hidden controls
  - `<button>` allows you to control how your button looks
  - `<input type="hidden" name="insertIdentifierHere">` puts form controls on the page that are invisible to the user
- `<label>`is used to help with screen readers and can either wrap around the entire input with the text description at the start or be on a separate line and use the `for` attribute to identify which input it is labeling.
- grouping form elements
  - `<fieldset>` will group the elements in a form together and `<legend>` can follow it to identify what the purpose of the group is
- date input
  - `<input type="date" name="insertIdentifierHere">`
- email and URL input
  - `<input type="email" name="insertIdentifierHere">` will check the format is valid
  - `<input type="url" name="insertIdentifierHere">` will check the format is valid
- search input
  - `<input type="search" name="inputIdentifierHere">` optional `placeholder="placeholderTextHere"`

how forms work: a user submits information to the server, the name of each form control and its data is processed by the server, the server creates a new page to send back based on the registered info. To differentiate between data, all the info is sent using name/value pairs, ex `username=dana`. If the value is text, it will be whatever the user types, if the value is an option, it will be assigned based on whatever the user chose.

a form is created with the `<form>` element and an `action` attribute containing the URL for the page on the server recieving information from the form. It will be sent using either the `get` (values are added to the end of the URL, ideal for short forms) or `post` (sent as HTTP headers, good for if the user needs to submit a file or the form is long/contains sensitive data) `method` attribute. If not `method`, the `id` attribute is used to differentiate the data in the form from the rest of the page.

## Lists Tables and Forms

`list-style-type` allows you to conrol the shape and style of a bullet point.

`list-style-image url("#")` allows you to specify an image to act as a bullet point.

`list-style-position` allows you to either put the marker `outside` or `inside` your block of text.

table properties:

- `width` - sets the width of the table
- `padding` - sets the space between the border of the cell and its content
- `text-transform` - converts the contents of headers to uppercase
- `letter-spacing` / `font-size` - adds addition styling to table headers
- `border-top` / `border-bottom` - sets borders above and below table headers
- `text-align` - aligns the writing to the left of some cells and the right of others
- `background-color` - changes the background color of alternating rows
- `:hover` - highlights a row when the users mouse goes over it.

if you have empty cells, you can use `empty-cells` to specify whether or not their borders should be shown

you can specify whether there should be gaps between cells using `border-spacing` and `border-collapse`

an easy way to ensure your inputs line up is to use `<label>` to give them names, then float the names to the left and give them a fixed width so their input boxes will start in the same place.

`cursor` allows you to control how the cursor is displayed to users/

## Events

event types:

- UI Events
  - load - webpage has finished loading
  - unload - webpage is unloading
  - error - browser encounters an error
  - resize - browser window has been resized
  - scroll - user has scrolled up or down
- keyboard events
  - keydown - user presses a key (repeated)
  - keyup - user releases a key
  - keypress - character is being insertes (repeated)
- mouse events
  - click - user presses and releases a button over the same element
  - double click - user presses and releases a button twice over the same element
  - mousedown - user presses a mouse button while over an element
  - mouseup - user releases a mouse button while over an element
  - mousemove - user moves the mouse
  - mouseover - user moves the mouse over the element
  - mouseout - user moves the mouse off an element

when an event has occured it has fired or been raised, these events will trigger scripts or functions

- focus events - an element gains or loses focus
  - focus/focusin - an element gains focus
  -blur/focusout - an element loses focus
- form events - a user interacts with a form element
  - input - value on any `<input>` or `<textarea>` has changed
  - change - value in `select-box` `checkbox` or `radio-button` changes
  - submit - user submits a form using a button or key
  - reset - user clicks on a form's reset button
  - cut - user cuts content from a form field
  - copy - user copies content from a form field
  - paste - user pastes content to a form field
  - select - user selects some text in a form field
- mutation events - the DOM structure has been changed by a script
  - DOMSubtreeModified - change has been made to document
  - DOMNodeInserted - node has been inserted as a direct child of another node
  - DOMNodeRemoved - node has been removed from another node
  - DOMNodeInsertedIntoDocument - node has been inserted as a descendant of another node
  - DOMNodeRemovedFromDocument - node has been removed as a descendant of another node

when a user interacts with HTML it has three steps (known as event handling) to trigger JavaScript code

- select the element node/nodes you want the script to respond to
- indicate which event will trigger the response
- state the code that will run when the event occurs

three ways to bind an event to an element

- HTML event handlers - not best practice, don't do this
- traditional DOM event handlers - allow you to separate JavaScript from HTML, only can attach a single function to any event
- DOM level 2 event listeners - favored way of handling events, allow one event to trigger multiple functions
  - `DOMelement.addEventListener('event', functionName [,boolean])`, to call use `variableName.addEventListener('blur', checkUsername, false)`
  - takes properties, the event you want it to listen for, the code you want it to run, boolean value (usually set to false)

event flow

- event bubbling - event starts at the most specific node and flows out to the least specific one
- event capturing - even starts at the least specific node and flows inward to the most specific

event object tells you about the event and the element it happened upon

the event object has changing methods the default behavior of an element and how its ancestors respond to the event

- preventDefault() - prevents default behavor
- stopPropogation() - stops element from flowing up to its ancestors

[`[`< table of contents`]`](code201.md)

[`[`< home`]`](README.md)
