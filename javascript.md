# Dynamic Web Pages with Javascript

## Javascript

javascript is a lightweight compiled programming language with first-class-functions. It is, in fact, not related to java and they are two very different languages.

## Input Output

an example of how to get input from a user

`first name: <input id="first_name">`
`last name: <input id="last_name">`
`<button id="say">Say hi!</button>`
`<div id="result"></div>`
`<script>`
`function say_hi() {`
    `var fname = document.getElementById('first_name').value;`
    `var lname = document.getElementById('last_name').value;`
    `var html = 'Hello <b>' + fname + '</b> ' + lname;`
    `document.getElementById('result').innerHTML = html;`
`}`
 
`document.getElementById('say').addEventListener('click', say_hi);`
`</script>`

## JavaScript Variables

you can declare a variable using
- `var`
- `let`
- `const`
- or nothing

variables are containers for data values.

### When to Use Var vs Const vs Let

`let` and `const` are more recent additions than `var`, so if you're coding for an older browser, `var` should be used. Otherwise, `const` should be used for general rules and `let` should be used if the value of the variable is likely to change.

### Javascript Identifiers

all javascript variables must be identified with unique names, which can be a single character or something more descriptive.
- names can contain letters, digits, underscores, and dollar signs
- names must begin with a letter, $, or _
- names are case sensitive
- reserved words cannot be used as names

### The Assignment Operator

`=` is used to assign a value to a variable.

### JavaScript Data Types

javascript variables can hold number and text strings. To differentiate for the variable assignment, strings are placed in quotations and numbers are not.

### Declaring a JavaScript Variable

`var nameHere` is the correct way to declare a variable with no value. You can then assign it value afterwords using `=` or you can assign it while you're declaring it. You should generally declare all variables at the beginning of your script

### One Statement, Many Variables

you can declare as many variables as you want in one line as long as they're separated by a comma.

### Re-Declaring JavaScript Variables

if you re-declare a variable with the same name, it will still have the same contents.

[< back](README.md)