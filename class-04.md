# HTML Links, JS Functions, & Intro to CSS Layout

<!--From HTML&CSS by Jon Duckett-->
## Links

to write a link, you use the structure `<a href="https://linkHere">clickable text</a>`. Links can navigate a user between pages, and it is important to have clear link text for users to be able to easily identify it. To link to another site, you need to use the absolute URL. For pages within your own site, you can use a relative URL, which is just the file path within your code.

for larger sites, you should organize your code by putting different sections of the site into different folders. The top level folder is called the root. Each sub-directory should also have an index.html file for the browser to direct itself to.

to link the users email program, you use the same link semantics, but within href, you preceed the email address you want to direct a message towards with `mailto:`

to open a link in a new window, you add `target="_blank"` after your site address.

you can also link to different spots within the same page by using IDs to identify spots you want to link to and then use `#IDName` for the href.

## Layout

CSS treats all HTML elements as either an inline or block--level box, meaning it either flows within test or start a new line. If one element is inside another, the outer element is know as the parent element. To control where these all are on the page, CSS has positioning schemes.

- normal flow - the paragraphs appear one after the other vertically
- relative positioning - this moves an element somewhere else without affecting the position of the items around it
- absolute positioning - the element is taken out of the flow and other elements act like it doesn't exist.
- fixed positioning - places the element in relation to the browser window rather than the container, does not effect other elements.
- floating elements - the element becomes a block level element that other elements flow around

<!--From JavaScript&JQuery by Jon Duckett-->
## Functions, Methods, & Objects

functions allow you to group a series of statements together to perform a specific task, allowing you to reuse pieces of code. When you run a function from your code, it is known as calling, and you may want to call functions rather than have them all run at once when your page opens. If the function needs information passed in from the page, you put them in the parenthesis and they are called parameters.

to declare a function, you write `function nameHere()` followed by a code block. To call the function, you need only write its name followed by parenthesis. When you're returning a value, you end the function with `return variableName;` If you want to return more than one value, you can use an array.

if you use a function as an expression, it is not necessary to name it, and that is known as an anonymous function. If you want to call a function immediately, you can place parenthesis directly after the closing brackets. Generally you will only use these to avoid naming conflicts between similar blocks of code or assign variables.

variables having different scopes depending on where they are declared. Local variables only exist within a function, and global variables can be accessed by anything.

<!--https://www.codefellows.org/blog/6-reasons-for-pair-programming/-->
## Pair Programming

pair programming involves two roles; the Driver, who is typing and handling all the mechanics, and the Navigator, who guides the Driver without touching the code by thinking about the bigger picture and what needs to come next while scanning for any problems.

learning coding is like learning a new language, and as such it is important to listen to it, speak it, read it, *and* write it. Pair programming touches on all of those skills, and that makes it a good tool to help you learn. The six big reasons for pair programming are:

1. greater efficiency - it is easier to catch mistakes as they show up and as such requires less debugging in the future, and two people working together can often come up with solutions to problems faster than one person alone
2. engaged collaboration - when two people are focused on the same code, both are more engaged and focused and it is harder to get off track.
3. learning from fellow students - working with a teammate can expose you to methods of problem solving you didn't previously think about. Also, generally each partner has a different skill set and they can teach each other what they are best at.
4. social skills - communication is important when working with someone with a different coding style or personality. Having to find the words to talk to them rather than just take over is a valuable career skill.
5. job interview readiness - a common step in the interview process is pair programming to help the interviewer see how well you collaborate, for most roles, this is even more important than technical skills.
6. work environment readiness - many companies need to train fresh graduates on how they operate, while graduates familiar with pairing have one less hurdle to overcome.

[`[`< table of contents`]`](code201.md)

[`[`< home`]`](README.md)
