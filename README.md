# my personal coding standards and style
Hi! This is my personal coding standards and style when I make my own wbesites. I made this repository for the sake of documentation, **to get myself to think about my code**, and to hopefully give other developers some ideas.


I ~~stole~~ got the idea from [thelifemgmt](https://github.com/thelifemgmt)'s [Coding Standards & Styleguide](https://github.com/thelifemgmt/coding_standards "thelifemgmt's Coding Standards & Styleguide")

**Some good reference links**

* http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/
* Another Link
* Another Link

I also keep forgetting how to center things properly, so until I do, here's a pretty neat link:
https://css-tricks.com/centering-css-complete-guide/

## Type Attributes

* Do not add `type="text/css" to` stylesheet link tags
* Do not add `type="text/javascript"` to javascript script tags

http://stackoverflow.com/questions/5409114/is-type-text-css-necessary-in-a-link-tag

tldr Different file types may have been avilable in HTML4 but were dropped and never used.

Example:
```
<!-- Good -->

<link rel="stylesheet" href="style.css">
<script src="js/script.js"></script>`


<!-- Bad -->

<link rel="stylesheet" type="text/css" href="style.css">
<script type="text/javascript" src="js/script.js"></script>`
```


## Project Organization

* Always keep two directories, `src` (for Source) and `dist` (for Distribution)
* `src` will include all of the files of the project before compilation and concatnation. 
* `dist` will include only concatnated and compiled assets. Do not include SASS, 

Things to think about:
* Should libs like bootstrap and jquery be inside the css and js directories or make a "libs" directory?
* Are different views considered resources? Because in a way, they kind of are... 

*** NOT FINISHED !! **
Example:
```
├── //root
|
├── views
|   ├── page0.php //Eg. Homepage
|   ├── page1.php //Eg. About Us
|   └── page2.php //Eg. Contact Us
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
    |   └──   libs
    |         └──   jquery.js
    |
    ├── sass
    |   └── compiled.scss
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
    |           ├── grid
    |           |   └── _grid.scss
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




Some more stuff coming `soon™`.

I left this GitHub editor style link here for me becasue I know I'll need it again at some point.
[don't mine me c:](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet "(old man voice) GET OUTTA HERE!!")
