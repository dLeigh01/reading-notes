# Audio, Video, Images

<!-- from HTML&CSS by Jon Duckett -->
## Images

you can control the size of images using the `width` and `height` properties in CSS, and specifying the size of an image helps the page to load more smoothly. Generally, sites have a specific set of sizes they use for their images, and you can specify those sizes and then change the image with classes of small medium and large.

when aligning images, you could float the size class, or you could create a whole separate class for items that need to be aligned to the left or right of the page. If you want to center the image, you should use `display:block` to make it a block level element and set the margins to auto.

`background-image` allows you to place an image behind any HTML element. `background-repeat` can be used with `repeat`, the default, `repeat-x`, repeated horizontally only, `repeat-y`, repeated vertically only, and `no-repeat` the image is only shown once. `background-attachment` specifies whether the background should stya in one place or move with the user with the values `fixed` and `scroll`. `background-position` specifies where an image should be placed in the window if it is not repeated. `background-image` can also create a gradient. When you use a background image, it should generally be made low contrast so the text on top of it is legible, or you should be a screen (a semi-transparent background) between the text and the image.

using CSS, you can create a link that changes styles when a user mouses over it and when they click on it by setting a background image for the button with three different styles of the same button so only one can be seen, then each one moves to the next is visible when each event occurs

## Practical Information

search engine optimization (SEO) is the practice of trying to get your site closer to the top of search results. On-page techniques are things you can do within your pages for SEO, like including keywords people are likely to use to find a site like yours and including them in the HTML. Off-page techniques are things like getting other sites to link to you, as search engines often rank by the number of sites that link to yours.

to identify key words and phrases for SEO, you can brainstorm, words people may associate with you, organize the different concepts of your site and pick out the categories that stick out the most, research with things like adwords that show you keywords related to words you enter, compare how much competition you are dealing with for the top search slots on any specific keyword, refine your ideas to chose the most relevent keywords, and map out which are the best possibilities for your site based on all the information you gathered.

once people start visiting your site, you can see the analytics of how they found you, what they saw, when they left, etc.

to put your site out on the web, you need a domain name (web address) and web hosting (uploading your site to a wbe server so other people can see it). To transfer everything to the web hosting company, you use file transfer protocol (FTP), which allows you to transfer files across the internet to the computer hosting your site.

## Flash

any animation or movie you put on your site is called a flash movie. Flash is used less nowadays because it is not supported by apple and it doesn't always meet accessiblity requirements.

<!-- https://developer.mozilla.org/en-US/docs/Learn/JavaScript/Client-side_web_APIs/Video_and_audio_APIs -->
## Video and Audio APIs

`<video>` and `<audio>` allow us to embed video and audio into web pages. If you give it a `controls` attribute, then it will enable default controls on the player, but the default controls are not very helpful, so the best way to go about it is to create your own controls. You can do so using `HTMLMediaElement` which can do things like `.pause()` and `.play()`. A good way to style the new controls you creat is to download a font that uses characters as common icons, such as the play and pause symbols.

[`[`< table of contents`]`](code201.md)

[`[`< home`]`](README.md)
