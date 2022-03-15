# Object-Oriented Programming and HTML Tables

<!--https://github.com/codefellows/domain_modeling#domain-modeling-->
## Domain Modeling

domain modeling is the process of creating a conceptul model in code for a specific problem which describes the various entities and the constraints of the problem domain. An object-oriented model is an entity that stores data in properties and encapsulates behaviors in methods. A well articulated model can validate the understanding of a specific problem and can help with communication between technical and business teams.

<!--From HTML&CSS by Jon Duckett-->
## Tables

a table represents information in a grid format, which allows us to understand complex data by referencing information on two axes. Each block in the grid is refered to as a table cell.

`<table>` is the tag for a table element. `<tr>` indicated the start of each row and `<td>` represents each table cell. `<th>` combined with `scope="column"`/`"row"`gives a heading to either a column or a row. `colspan=""` tells the table how many columns a cell should span across and `rowspan=""` tells the table how many rows a cell should span across.

for proper syntax, you should use `<thead>` to contain the headings, `<tbody>` to contain the body, and `<tfoot>` for any footer elements.

<!--From JavaScript&JQuery by Jon Duckett-->
## Functions, Methods, and Objects

the `new` keyword combined with the `Object()` constructor will create a blank object you can fill using dot notation.

to update the value of a property, use dot notation or square brackets(square brackets will not work on methods). To delete a value, use the `delete` keyword. If you want to create multiple similarly structured objects, you can create a template using constructor notation by creating the object as a function and using `this.` to assign everything so it can apply to whataver name you use later on. A constructor function is usually named beginning with an UPPERCASE letter. You can then use this constructor function by calling it with the `new` keyword and assigning it to a variable while passing in the arguments it needs.

arrays are a special type of object that holds a related set of key/value pairs, but each key is just the index number.

arrays can store objects and remember their order, and objects can store arrays as values.

browsers come with built in objects that represent things like the window and current page, which act as a toolkit.

- browser object model - contains objects representing the current browser window, history, and screen
  - `window`
- document object model - uses objects to represent the current page with a new object for each element
  - `document`
- global JavaScript objects - represent things JavaScript needs to create a model of.

[`[`< table of contents`]`](code201.md)

[`[`< home`]`](README.md)
