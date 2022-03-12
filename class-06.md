# Problem Domain, Objects, and the DOM

<!--https://simpleprogrammer.com/understanding-the-problem-domain-is-the-hardest-part-of-programming-->
## Understanding the Problem Domain is the Hardest Part of Programming

it is often difficult for beginners to learn code because the problem domain (whatever they are attempting to create) isn't clear to them. Different views on the problem domain can yield different outcomes and make it harder to know what your code is meant to do. Once you understand the problem domain, coding becomes much easier if only because now you have a much clearer idea of what you actually need to accomplish, which means you can give yourself clearer steps to get there.

to get around this you can either attempt to make the problem domain easier, or you can get better at understanding it. Always make sure you know everything you can about what you are trying to do.

<!--https://betterprogramming.pub/intermediate-javascript-whats-the-difference-between-primitive-values-and-object-references-e863d70677b-->
## What's the Difference Between Primitve Values and Object References in JavaScript

all data types in JavaScript can be classified as either primitve values or object references. A primitive value sets the variable directly to that values, while an object reference refers to when a variable is set to an object where the value is stored rather than the value itself.

one major difference between the two is that primitive values are immutable (they cannot be changed) and object values are mutable (they can be changed).

if you are using equality operators on objects, this can mess with the expected outcome, and to check equality you need to iterate through their contents instead of checking the references against each other.

<!--From JavaScript&JQuery by Jon Duckett-->
## Object Literals

objects group together a ser of variables and functions to create a model. Within an object, variables become known as properties and functions become known as methods. In an object, the name of properties and methods is called a key.

literal notation is the most popular way to create an object. ex:

```js
var hotel = {
  name: 'Quay',
  room: 40,
  booked: 25,
  checkAvailability: function() {
    return this.rooms - this.booked;
  }
};
```

you can then access an object's proerties using dot notation, ex(`hotel.name;`) or square brackets, ex(`hotel['name']`).

## Document Object Model

as the browser loads a page, it creates a model called the DOM tree which consists of four types of nodes:

- the document node - starting point for the DOM tree, represents the entire page
- element nodes - any tag(element) on the page
- attribute nodes - anything within the opening tag of an element
- text nodes - what is contained between the tags of an element

to update the DOM tree, you first have to access the elements.

- select a single element
  - `getElementById()` - uses the element's unique ID
  - `querySelector()` - uses a CSS selector and returns the first result
- selecting multiple elements
  - `getElementsByClassName()` - selects all elements within the specified class
  - `getElementsByTagName()` - selects all elements with the specified tag name
  - `querySelectorAll()` - uses a CSS selector to select all matching elements
- traversing between element nodes
  - `parentNode` - selects the parent of the current node
  - `previousSibling`/`nextSibling` - selects the previous or next sibling
  - `firstChild`/`lastChild` - selects the first or last child of the current element

once you've accessed the element you need, then you can work with is.

- `nodeValue` lets you access/update text nodes
- work with HTML content
  - `innerHTML` - accesses child elements and text content
  - `textContent` - specifically targets text content
  - `creatElement()` `createTextNode()` and `appendChild()`/`removeChild()` - allow you to create, and remove nodes from the tree through DOM manipulation.
- access or update attribute values
  - `className`/`id` - lets you update the value of the class or id attributes
  - `hasAttribute()` - checks if an attribute exists
  - `getAttribute()` - gets the value of an attibute
  - `setAttribute()` - updates the value of an attribute
  - `removeAttribute()` - removes an attribute

methods that find elements in the DOM tree are called DOM queries, and should be stored as a variable if you think you'll need to use it more than once. Dom queries can return a single element or a NodeList (a collection of nodes) from which you can then select a single element using its index number like an array or by using `item()`.

if you use innerHTML, you need to be wary of cross site scripting attacks (XSS - when someone places malicious code on your site) or an attacker could access your user's accounts. To defend against XSS, you can validate input going to the server (only allow users to input necessary characters) and do not create any DOM fragments using code from untrusted sources.

modern browsers come with tools that allow you to look at the DOM tree

[`[`< table of contents`]`](code201.md)

[`[`< home`]`](README.md)
