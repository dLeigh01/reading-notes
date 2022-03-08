# Basics of HTML, CSS, & JavaScript

## Text

<!--From HTML&CSS by Jon Duckett-->

HTML has six levels of headings, ranging from `<h1>` to `<h6>` with 1 being the largest.

the `<p>` tag will create a paragraph, which shows up on a new line between each tag by default.

to make characters appear bold, use `<b>`, for italics, use `<i>`.

for things like chemical formulas and mathematical equations, you sometimes require superscripts and subscripts, those can be achieved using `<sup>` and `<sub>` respectively.

if you have more than two spaces in your code, the browser registers it as only one through white space collapsing, so you can use extra spaces to make your code easier to read if necessary. If you actualy *want* to add a line break, you can use the `<br />` tag. To add a line into the break, you use `<hr />` instead.

many HTML editors have a visual editor as well as a code view. The visual editor looks more like a word processor, while the code view allows you to manually edit things.

semantic markup doesn't do anything for the visuals of your page, but they give extra information about your code. A common thing these affect is the way a screen reader interprets your page.

`<strong>` is like a semantic version of bold, and indicates the words contained in it have a strong importance.

`<em>` is a semantic version of italics, and indicates words that give the sentance a subtle change in meaning.

the two most common elements used for quotations are `<blockquote>`, which is used for longer quotes, and `<q>`, which is used for shorter quotes.

if you are using an acronym or abbreviation, you can add code that spells out exactly what it stands for using `<abbr title="meaning here">`.

if you are citing a source, you can use `<cite>` to give it the correct semantics.

the first time you use a term in something like an academic research paper, you can assign it the `<dfn>` tag, which indicates the place it is first defined.

to display details about the author of a page, you would use an `<address>` tag.

if you are making changes to something, you can use the `<ins>` and `<del>` tags to indicate things that have been added and removed, and if you have changed information that you don't want removed you can use `<s>`.

## Introducing CSS

in HTML, every different element is treated as a box, some of these boxes are inline and some are not, but the key to understanding CSS is knowing these boxes exist. CSS works by associating rules with HTML elements, allowing you to change how the content of any specific element is displayed. The two pieces of a rule are:

- the selector - indicates which elements the rule will apply to.
- the declaration - indicates how the elements in the selector will be styled.

the declaration is made up of two parts as well,

- the property - indicates the aspect of the element being changed.
- the value - specify the settings of the change indicated by the property.

to use external CSS, you put the `<link>` tag in the head of an HTML file. Within that link, `href` specifies the path to the CSS file, `type` specifies the type of document, and `rel` indicates the relationship between the current page and the file being linked.

to use internal CSS, you can place a `<style>` tag within the HTML page itself and write CSS within that tag, however, internal CSS is not best practice and an external sheet allows multiple pages of the website to make use of it.

CSS selectors allow you to target more specific things on a page than just element types.

- a Universal Selector will target all items on a page, ex `*`
- a Type Selector will target an element name, ex `<h1>`
- a Class Selector will target any element that has been assigned to that class, ex `.classID`
- an ID Selector will target one specific item, ex `#ID`
- a Child Selector will target elements only in the correct pathway, ex `li>a`
- a Descendat Selector will target elements anywhere within the correct parent element (even if it is not a direct child), ex `p a`
- an Adjacent Sibling Selector will target elements only directly after the other specified element, ex `h1+p`
- a General Sibling Selector will target any sibling elements, rather than only the one directly afer, ex `h1-p`

CSS is a cascading style sheet, which means if two different selectors are aiming at the same element with different property values, they will be resolved by either whichever came last, whichever is more specific, or whichever is more important.

if you specify a larger element, then the elements within it will also take on some styling you had done through inheritance, which means you needn't apply styling to every element in your HTML page.

sometimes, CSS will appear differently in different browsers, and as such it is important to see how your site looks from multiple sources before you launch it.

## Basic JavaScript Instructions

<!--From JavaScript&JQuery by Jon Duckett-->

in JavaScript, a script is a series of instructions that can be followed one-by-one. Each step in this process is called a statement, and every statement should end with a semicolon and start on a new line. These statements can be organized into code blocks, which are sections of code surrounded by curley bracers that help to keep your code organized and readable. Also note that JavaScript is case sensitive, so variable names need consistent casing, and any difference becomes a new variable entirely.

it is good practice to input comments that describe what your code is doing, which can help yourself and others to understand your code. To write a multi line comment, you use `/* */`, for a single line you only need to preceed the comment with `//`.

variables are where the script stores any temporary information it requires and are declared using a keyword such as `var` or `let` followed by a unique name. You can then assign it a value either while it is being declared or later on using the name followed by `=` and whatever value you want it to hold.

there are three different basic data types in JavaScript:

- numeric data - any sort of number
- string data - any letters and other characters (this will be enclosed in quotes)
- boolean data - can only have a value of true or false

once a variable has been assigned a value, you can still change it using the same method as you used to give it a value in the first place and the original value will be overwritten.

rules for naming variables:

- the name must begin with a letter, $, or _
- the name can only contain any of the previous characters as well as numbers
- you cannot use keywords or reserved words (like null or var)
- all variables are case sensitive
- use a name that describes what the variable is
- if the name contains more than one word, use camelCase to differentiate them

an array is a special type of variable that stores lists. To assign values to an array, you use the same method as with other variables, only this time you place the values you are assigning within square brackets, separated by commas. The values within an array act as a numbered list, with the first value being indexed under 0 rather than 1. To access any specific value, you list the array name, followed by the index number of the variable in square brackets, ex `list[3]`.

when you are assigning a value to a variable, it is specifically known as an expression, and can be done through just adding a single value, or by putting multiple values together and storing the result in another variable. The assignments are done using operators, which are signs like `=` and `>`.

arithmetic operators include:

- `+` - addition
- `-` - subtraction
- `/` - division
- `*` - multiplication
- `++` - increment
- `--` - decrement
- `%` - modulus (gives division remainder)

order of operations is important to recall when using arithmetic oprators, as the program will perform the operations in the correct order.

the only operator for strings is `+`, which concatenates things into strings.

## Decisions and Loops

on occasion, you will come across areas where a decision needs to be made, and the different results should run different parts of your code. To determine which part of the code needs to be used, you set a condition. There are two components to a decision:

- the expression is evaluated and returns a value
- the conditional statement says what to do

the condition usually involves comparing one value to another, in which case you use comparison operators which will always come back with a value of true or false. Usually a condition is made up of two operands and one operater, ex `(score >= pass)`. The operand also can be more than a single value, ex `((score1 + score 2) > highScore)`.

- `==` - is equal to
- `!=` - is not equal to
- `===` - is strictly equal to (same contents and data type)
- `!==` - is strictly not equal to
- `>` - greater than
- `<` - less than
- `>=` - greater than or equal to
- `<=` - less than or equal to

logical operators allow you to compare the results of multiple comparison operators. Logical expressions are evaluated from left to right, so if you place a boolean value first it will stop and not check the second value, resulting in a short-circuit evaluation.

- `&&` - logical and
- `||` - logical or
- `!` - logical not (this is placed outside the expression and inverts the boolean value)

if statements will check for a condition and only run the subsequent block of code if the condition evaluates to true. An if else statement has a second block of code that will only run if the first condition evaluates to false.

[`[`< table of contents`]`](code201.md)

[`[`< home`]`](README.md)