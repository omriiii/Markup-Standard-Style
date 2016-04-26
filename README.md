# my personal coding standards and style
Hi! This is my personal coding standards and style when I make my own wbesites. I made this repository for the sake of documentation, **to get myself to think about my code**, and to hopefully give other developers some ideas.


I ~~stole~~ got the idea from [thelifemgmt](https://github.com/thelifemgmt)'s [Coding Standards & Styleguide](https://github.com/thelifemgmt/coding_standards "thelifemgmt's Coding Standards & Styleguide")

**Some good reference links**

* http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/
* Another Link
* Another Link

https://css-tricks.com/centering-css-complete-guide/

## HTML Formatting Rules
*** NOT FINISHED !! ***

* Always comment segemnts in the `head` tag. Eg. "Libraries", "Stylesheets", "Meta tags", etc.
* Always indet child every child element.
* Always indet using *only* the "tab" character `(ascii: 9)`. Never use 4 "space" characters `(ascii: 32)`. 
* Never close self-closing tags such as `hr`, `br`, `img`, or `input`.
* Always include an `alt` attribute to `img` tags.

## Type Attributes

* Never add a`type="text/css"` attribute to stylesheet `link` tags.
* Never add a `type="text/javascript"` attribute to javascript `script` tags.

In HTML5 the default value for the `type` attribute will always be text so it's not needed with those two tags.

Example:
```
<!-- Good -->

<link rel="stylesheet" href="style.css">
<script src="js/script.js"></script>`


<!-- Bad -->

<link rel="stylesheet" type="text/css" href="style.css">
<script type="text/javascript" src="js/script.js"></script>`
```

## CSS3 Animations
*** NOT FINISHED !! ***

* Always use the `transform` property when animating elements with CSS.

## Project Organization
*** NOT FINISHED !! ***

* Always keep two directories for your project, `src` (for Source) and `dist` (for Distribution)
* `src` will include all of the files of the project before compilation and concatnation. 
* `dist` will include only concatnated and compiled assets. Do not include SASS files.

Things to think about:
* Different html pages that are included in the website. includes directory maybe? (things like navbar.html)

Example:
```
//root
|
├── views //All of the pages in the website.
|   ├── page0.php //Eg. Homepage
|   ├── page1.php //Eg. About Us
|   └── page2.php //Eg. Contact Us
|
├── libs //(Libraries)
|   ├── css
|   |   ├── bootstrap.css
|   |   └── bootstrap.min.css
|   |
|   └── js
|       ├── jQuery.js
|       ├── jQuery.min.js
|       ├── angularJS.js
|       └── angularJS.min.js
|
└── res //(Resources)
    ├── css
    |   └── style.css //compiled and concatnated style.scss
    |
    ├── graphics
    |   ├──   picture0.png
    |   ├──   picture0.jpg
    |   ├──   logo.svg
    |   └──   favicon.ico
    |
    ├── js
    |   ├──   app.js
    |   └──   functions.js
    |
    ├── sass
    |   └── style.scss
    |       └── project
    |           ├── _project-fonts.scss
    |           ├── _project-styles.scss
    |           ├── _project-variables.scss
    |           |
    |           ├── components
    |           |   ├── _buttons.scss
    |           |   ├── _lists.scss
    |           |   └── _inputs.scss
    |           |
    |           ├── partials
    |           |   ├── _header.scss
    |           |   ├── _masthead.scss
    |           |   └── _footer.scss
    |           |   
    |           └── globals
    |               ├── _mixins.scss
    |               ├── _typography.scss
    |               ├── _reset.scss
    |               └── _base.scss
    |
    └── fonts
        ├──   font0.ttf
        ├──   font0.eot //.eot is used for IE
        ├──   font1.ttf
        └──   font1.eot //.eot is used for IE
```



# Notes
Some more stuff coming `soon™`.

I left this GitHub editor style link here for me becasue I know I'll need it again at some point.
[don't mine me c:](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet "(old man voice) GET OUTTA HERE!!")
