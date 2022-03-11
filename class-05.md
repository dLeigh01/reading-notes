# HTML Images; CSS Color and Text

<!--From HTML&CSS by Jon Duckett-->
## Images

when selecting images for a site, you should ensure that they are relevent, convey the right mood, and are recognizable. If you do not own pictures that fit those requirements, you can pay to use stock photos. It is generally good practice to have a folder in the site directory to hold all of the images you will be using. On bigger sites, you may also want to use subfolders for things like buttons and logos versus product images.

to add an image to your site, you use the `<img>` tag, containing the `src`, which points to the image, `alt` which provides alt text for screen readers, and possibly `title`, which gives the image a title for the browser to have additional information about it. To change the size of an image, to can adjust the `height` and `width` values in CSS. When placing an image, if it is before an elemtn it will act as a block, otherwise if you place it within an element it will run inline.

there are three rules for creating images:

1. save images in the right format - you should always save as either a jpeg, gif, or png
2. save images at the right size - you should save an aimage as the same width and height it will be on the site to preserve quality.
3. use the correct resolution - most web pages only display as 72ppi, so saving an image at a higher resolution is unnecessary and takes longer to load.

if an image has many different colors, you should save it as a jpeg, gif or png should be used for low amounts of color.

if you want a scaleable image, it needs to be a vector image, which allows it to change size without losing quality.

if you want to have a partially transparent image, it needs to be saved as a gif or a png.

in HTML5, the tag `<figure>` lets you contain an image and its caption, `<figcaption>` within the same element so they are grouped together.

## Color

`color` allows you to specify the color of text inside an element using RGB values, hex codes, or any of the pre-specified color names within CSS.

`background-color` sets the color of the box for the element you target.

when picking colors, it is important to keep contrast in mind. If you have low contrast between your text and background, it will make your site difficult to read.

`opacity` allows you to change the opacity of an element with a value between 0 and 1 (1 being completely opaque). This is also defined as `alpha` in hsla.

## Text

typeface terminology:

- main types of fonts
  - serif - has extra details at the edges of characters, considered easier to read
  - sans-serif - have straight ends to letters, can be clearer to read on smaller resolution screens
  - monospace - every letter is the same width, commonly used for code because they align nicely
- xyz
  - ascender - goes above the height of a capital letter
  - cap height - top of flat letters
  - x height - height of the letter x (average)
  - baseline - line the letters sit on
  - descender - goes below the baseline
- weight - adds emphasis and affects white space
  - light
  - medium
  - bold
  - black
- style - changes text angle
  - italics
  - oblique (regular text but diagonal)
- stretch - controls how wide the letters are
  - condensed
  - extended

often when you are choosing a font for your site, you should use a font stack (lining up an amount of fonts in preferential order) in case a user's computer doesn't have your first choice of font installed. To specify font families (like a font stack), you use `font-family`.

`font-size` will edit the size of your text. You can specify the size using either pixels (fixed width), percentages (relative to default size), or ems (relative to parent size).

`@font-face` allows you to specify the path to a font so it will be downloaded to a user's computer, but most fonts cannot be used this way because of licensing.

`font-weight` allows you to bold text, while `font-style` lets you use italics and `text-decoration` gives you underlines, overlines, and strikethroughs (and blink, which turns the text on and off, but you shouldn't generally do that).

`text-transform` gives you the ability to change the caseing of text between all uppercase, all lowercase, or the first letter of each word being capitalized.

`line-height` changes the height of a line of text for more white space between lines.

`letter-spacing` and `word-spacing` affect the kerning of a page (the space between each letter).

`text-align` allows you to define where in the element your text should sit, such left aligned rather than right, justified (each line takes the same amount of spaceexcept for the final line), or centered.

`vertical-align` will align your text to different spots on an inline image.

`text-indent` allows you to indent your first line of text (or de-indent it to remove it from the page while still being in the HTML).

`text-shadow` creates a slightly offset shadow behind your text.

`:first-letter` and `:first-line` will specify the first letter or line inside of the target element for changes.

`:link` and `:visited` allows you to set different styles for links on your page depending on whether or not the user has clicked on them before.

`:hover`, `:active`, and `:focus` change the appearance of elements based on whether a user is hovering over them, being clicked, or is currently interactible, respectively.

attribute selectors allow you to create rules that apply to attributes with specific values, and include:

- existence - `[]` matches a specific attribute, regardless of value
- equality - `[=]` matches a specific attribute with a specific value
- space - `[~=]` matches a specific attribute whose name appears in a list of words
- prefix - `[^=]` matches a specific attribute whose value begins with a specific string
- substring - `[*=]` matches a specific attribute whose value contains a specific string
- suffix - `[$=]` matches a specific attribute whose value ends with a specific string

<!--https://blog.imagekit.io/jpeg-vs-png-vs-gif-which-image-format-to-use-and-when-c8913ae3e01d-->
## JPEG vs PNG vs GIF

jpeg, png, and gifs make up 95% of all images on websites. In general, jpeg should be used for any image with color and intensity that needs to be smooth, png should be used for anything with transparency or that has sharp edges, and gif should be used for animations.

[`[`< table of contents`]`](code201.md)

[`[`< home`]`](README.md)
