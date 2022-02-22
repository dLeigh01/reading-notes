# The Coder's Computer

## Text Editors

### What is a Text Editor?

A text editor is a piece of software on your computer or in your browser through which you can write and manage text.
Some important features are
  - code completion
  - syntax highlighting
  - theme variety
  - various available extentions
  - 
### Using your Computer's Software

Mac computers come with 'Text Edit" and Windows come with "Notepad", which are both text editors, which you can try over downloading a new program, but they're very bare in terms of features. If you are using these, they must be used in plain text (no bold italics or the likes) and all of your code should go in a single file with appropriate extensions.

### Third Party Options

Notepad++
  - free
  - windows exclusive
  - very popular
  - includes syntax highlighting and code completion
  - zoom feature
  - online community/chat room/wiki page

BB Edit
  - $50 for full version
  - less expansive version is free
  - go to for mac computers

Visual Studio Code
  - free
  - avilable for windows mac and linux
  - contains emmet for HTML and CSS
  - syntax highlighting, themes, extensions, and code completion

Atom
  - free
  - available for windows, mac, and linux
  - comes from github
  - syntax highlighting, themes, and extensions

Brackets
  - free
  - available for windows mac and linux
  - made by adobe
  - only supports HTML, CSS, and JavaScript
  - live preview

Sublime Text
  - $70 for full version
  - fast and responsive
  - syntax highlighting, code completion, themes, and extensions

### The Difference Between Text Editors and IDEs

while a text editor edits text, an IDE (Integrated Developement Environment) mixes together a text editor, a file manager, a compiler, and a debugger.

## The Command Line

### What is a Command Line?

a command line/terminal is a text based system interface that gives feedback in text after each command.

### The Shell, Bash

The shell is a part of the OS defining how the terminal looks and operates, bash (bourne again shell) being the most common variant.
the command `echo $SHELL` will display what your current shell is.

### Shortcuts

When you enter commands, they are stored and can be re-accessed using the up and down arrow keys, and edited using the left and right arrow keys.
When you're typing a path, hitting tab will auto complete the name. If you use this on a file with a space in the name, the terminal will automatically escape any spaces in the name.

## Basic Navigation

### Console Commands

Where am I?
  - `pwd` (print working directory) says which directory you are in.
  - `ls` (list) displays what is in the current directory (can also be run with extra parameters)

Absolute vs Relative Paths
  - `/` denotes the **root** directory and always preceeds an **absolute** path
  - **relative** paths will not start with a slash and specify things in relation to your current position
  - `~` is shorthand for your home directory `/home/USER`
  - `.` is shorthand for your current directory
  - `..` is shorthand for your previous directory

Moving
  - `cd [LOCATION]` (change directory) changes your location to the given directory

## More About Files

### Everything is a File

everything in your system is counted as a file for the intents of linux

### Linux is an Extensionless System

a file extension is generally the 2-4 characters at the end that denote its file type, but Linux checks inside the file to determine what type it is rather than read the extension.
`file [PATH]` will let you know what sort of file something is

### Linux is Case Sensitive

it is possible to have two or more files with the same name, but differently capitalized letters. ALso, terminal commands can sometimes have different uses based on different cases.

### Spaces in Names

spacing is how separate items are denoted in the command line, so you couldn't use files with names that include a space unless you specify it is a single argument using `'some quotes'` or an `escape\ character`

### Hidden Files and Directories

if a file or directory name begins with `.` (full stop) then it is hidden. The only thing necessary to change a file status between hidden and visible is to change the name to include or disallow the `.`
`ls -a` will show hidden files and directories along with the normal items
