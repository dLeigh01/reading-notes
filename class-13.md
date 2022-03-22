# Local Storage

<!-- http://diveinto.html5doctor.com/storage.html -->
## The Past, Present, and Future of Local Storage for Web Applications

native clients hold an advantage over web application in persistent local storage because the operating system typically provides an abstraction layer for storing and retrieving application-specific data. If it requires local storage beyond key/value pairs, you can do many things like embeding your own database. Web applications, however, do not have this. Cookies are commonly used for persistent local storage, but they are

- included with every HTTP request
  - slows down you application by transmitting the same data over and over
  - sends unencrypted data over the internet
- limited to 4KB, which is not enough to be useful

what we would rather have is

- a lot of storage space
- client side
- persists beyond a page refresh
- isn't transmitted to the server

web storage was at one point part of HTML5, but was split out. Web Storage is a way for web pages to store named key/value pairs locally on the client browser that persists even if you exit the browser, is never transmitted to the remote web server, and is implemented natively.

before using web storage, you should generally write a function to check whether the browser supports it. Data is also only stored as strings in web storage, so when retrieving it you will need to use things like `parseInt()`.

`setItem()` will create an item/override an existing value and `getItem()` will retrieve an existing value. web storage can also be treated as an array and values can be accessed using square brackets. `removeItem()` will remove something entirely.

you can tell when something has been changed using `addEventListener('storage')`.

web storage by default only has 5 megabytes, and you cannot get more storage space.

[`[`< table of contents`]`](code201.md)

[`[`< home`]`](README.md)
