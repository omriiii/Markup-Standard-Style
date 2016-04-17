# my personal coding standards and style
Hi! This is my personal coding standards and style when I make my own wbesites. I made this repository for the sake of documentation, **to get myself to think about my code**, and to hopefully give other developers some ideas.


I ~~stole~~ got the idea from [thelifemgmt](https://github.com/thelifemgmt)'s [Coding Standards & Styleguide](https://github.com/thelifemgmt/coding_standards "thelifemgmt's Coding Standards & Styleguide")

**Some good reference links**

* http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/
* Another Link
* Another Link

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








Some more stuff coming `soon™`.

I left this GitHub editor style link here for me becasue I know I'll need it again at some point.
[don't mine me c:](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet "(old man voice) GET OUTTA HERE!!")
