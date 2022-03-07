# Introductory HTML and JavaScript

## HTML

### Structure

the use of headings and subheadings creates a hierarchy of information in any document, and different topics are often separated by space. This same thing is achievable in HTML using code words such as `<body>` and `<h1>` which are called tags. Anything the tags encompass, including the tags themselves, are called an element.

- elements usually consist of an opening and closing tag (which has a /) and each tells the browser what it can expect to be within it and where it lies in the hierarchy.
- attributes appear within opening tags and consist of a name (indicating the type of information) and a value (the information for the attribute) with an = sign between them. ex: `<p lang="en-us"></p>`
- `<body>` contains everything that appears in the main browser.
- `<head>` contains any information about the page.
- `<title>` contains what will show on the browser tab.

### Extra Markup

- `<!DOCTYPE>` is used to declare what version of HTML the page is using.
- `<!-- -->` is used to place comments within the code that will not be displayed to the user.
- the id attribute can be used on any element in HTML and is used to identify one specific element. Its name should never start with a number or special character other than an underscore.
- the class attribute can also be used on any HTML element and can denote several elements at a time.
- block elements are any element that automatically start a new line in the browser.
- inline elements will continue on the same line as the previous element.
- `<div>` is the tag used to group text and elements into a block, and is a block element.
- `<span>` is the inline equivalent of div.
- `<iframe>` cuts a window in your page to show another page (commonly used to show google maps). It needs to include width, height, and source, and if you don't want scroll bars, you can add the seamless attribute.
- `<meta>` stays in the head of the page and give information about the site.
- escape characters are codes used to write characters that are reserved by HTML, such as angle brackets.

### HTML5 Layout

in the past, authors would use `<div>` to separate all the elements of a page, now we have tags that allow us to separate elements in a way that tells what is contained inside that is consistant between sites.

- the `<header>` and `<footer>` elements can be used for the main header and footer of the page or for individual sections.
- the `<nav>` element contains the primary navigation for the site (as in navigation between pages and such rather than links to outside sources).
- the `<article>` element contains anything that can stand alone and have the ability to be nested.
- the `<aside>` element contains information related to, but not strictly necessary to understand, an article if it is contained within one, or contains information for the page as a whole when used outside of an article tag.
- the `<section>` element groups related content.
- the `<hgroup>` element groups together header tags to seem like they are one element.
- the `<figure>` element contains things like images and videos that are referenced in an article and `<figcaption>` sets the caption for whatever is contained in the figure tag.
- the `<div>` element can be used whenever there is no suitable replacement that fits your needs in grouping multiple elements together.
- HTML5 made the ability to use an `<a>` tag to make entire sections of content into a link into a normalized usage.
- since older browsers will read everything as an inline element, CSS should be used to ensure all block elements are treated as such.

### Process and Design

sites should be designed for a target audience, so it is important to know who you are targeting. Think about things like what country the majority of visitors will be from, what age range they will be, and their level of education.

once you have your target demographic established, knowing why they want to use your site is the next most important thing that should be impacting your content and design choices. You should know:

- their motivation for visiting your site (such as for work or for entertainment).
- their goal now that they are on your site (do they want information? Products? Is it time sensitive?).

creating a list of reasons why someone might be visiting your site is a useful way to guide your design.

once you know your target demographic and their reason for being there, your next step is finding out what information is necessary to them (do they know who you are? What differentiates you from competitors?).

how often you expect people to visit your site should guide how often you will need to update it. More frequent updates requires more resources, so it is important to know what the necessary amount is to avoid more work than necessary.

after figuring all the rest of that out, you can create a site map.

- a site map is a diagram of the structure of the site.
- card sorting (writing necessary information on cards and then sorting them into groups by how related they are) is a good way to place info in your site map.
- a wireframe is a simple sketch of the actual layout of your pages combined with the key information for each page from your site map.

the design of a website is important not only for aesthetic, but to showcase important data to site visitors. The organization of a page, making things more or less prominent depending on their priority, is necessary to ensure it is easily understandable.

- prioritizing
    - parts of the page need to look distinct to break up the information.
    - a visual hierarchy (differentiating items in order of importance using size, color, and style) helps to lead viewers through the page rather than dumping them in the middle of it.

- organizing
    - grouping together related content makes the page more comprehensible.
    - keeping a similar style for similar types of information will make it easier for a visitor to find a particular type of content.

grouping related info together can help with the cohesiveness of a design, some different types of grouping are:

- proximity (items placed closer together are viewed as more related than those that are far apart)
- closure (even when placing items into a complex design, leave space for an imaginary box around them, that keeps the group apart from other items subconsciously)
- continuance (items are percieved as more related if they are placed in a line or a curve)
- white space (leaving a bigger space between unrelated items than related ones)
- color (placing a background color behind related items to show their connection)
- borders (drawing a line around related items separates them from other items)

we are wired to see similar designs as related items, and you can help that by having consistency between similar items. Use of headings is also helpful in telling a user whether a specific chunk of information is useful to them.

navigation is also a very important piece of design, as it helps visitors to navigate your site and gives them a first look at your organization. The three most important parts of a good nav system are to be:

- concise (it should be easy to read and ideally no more than 8 links)
- clear (the type of info on any given page should be predictable based on the name)
- selective (only the navigation should go here, not the login page or terms and conditions)
- context (the user should be able to know where they are in the site based on the nav menu)
- interactive (links should be big enough to click and should change visually when the user interacts with them)
- consistent (secondary navigation can change between pages, but the primary should always remain the same)

## JavaScript

### What is a Script and How Do I Create One?

a script is a series of instructions a computer follows to achieve a goal that can run different sections of itself in response to whichever situation it finds itself in.

to write a script, you need your end goal and a list of what needs to happen to accomplish it.

- define the goal: decide what you want the computer to achieve.
- design the script: split the goal into individual tasks and then figure out what individual steps must be taken to complete each task.
- code each step: each step you created needs to be written in JavaScript.

it is often easier to figure out your necessary steps and the order in which they need to be completed by first putting them into a flowchart.

### How Do Computers Fit in With the World Around Them?

computers don't know what things in the world are, and as such they need models to tell them.

- objects represent physical things and can have its own properties, events, and methods.
- properties are the characteristics of an object that differentiate it from others. Each property has a name and a value that tells you abour each individual instance of an object.
- events are the computer's way of understanding something just happened that it can respond to by triggering a specific section of code.
- methods can retrieve or update values of different properties for objects.

to change the content of HTML using JavaScript, it is important to understand how the browser interprets your web page.

1. recieve a page as HTML code
2. create a model of the page and store it in memory
3. use a rendering engine to show the page onscreen

all major browsers can use an `interpreter` to translate JavaScript to useable instructions for the computer.

### How Do I Write a Script for a Web Page?

there are three different languages that work together to make up a basic web page through progressive enhancement (building on top of each other to focus on one aspect of the design process at a time).

- HTML holds the content of the page, as well as giving it structure and semantics.
- CSS changes how the HTML is presented.
- JavaScript changes how the page behaves and adds interactive functions.

when you create a script, you generally want to house it in its own .js file and call it in your HTML page using the tag `<script>`. It is possible to write JavaScript inline in HTML, but it is not best practice.

to use objects and methods in JavaScript, you use the format `object.method(parameters);`.

JavaScript will run wherever it is placed within your HTML, which allows you to move where something specific shows up by moving the script call, or allows you to call the same thing multiple times in different places.

[`[`< table of contents`]`](code201.md)

[`[`< home`]`](README.md)