# my personal mark-up standards and style
Hi! This is my personal mark-up standards and style when I make my own wbesites. I made this repository for the sake of documentation, **to get myself to think about my code**, and to hopefully give other developers some ideas.


I ~~stole~~ got the idea from [thelifemgmt](https://github.com/thelifemgmt)'s [Coding Standards & Styleguide](https://github.com/thelifemgmt/coding_standards "thelifemgmt's Coding Standards & Styleguide")



## HTML5 Formatting Rules

* Always indent children elements. An exception below...
* Always indent using *only* the "tab" character `(ascii: 9)`. Never use "space" characters `(ascii: 32)`. 
* Always include an `alt=""` attribute to `<img>` tags.
* Always create a `<label>` tag for an `<input>` tag.
* Try to use the [BEM (Block Element Modifier)](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/) naming convention when possible.
* Avoid using `"` and `'` in your content. Use `&lsquo;`/`&rsquo;` and `&ldquo;`/`&rdquo;` (`‘`, `’`, `“`, `”`) instead. 
* Never close self-closing tags such as `<hr>`, `<br>`, `<img>`, or `<input>`.
* Never use inline css or inline javascript.
* Never use an `id=""` attribute unless it's for an `<input>` tag. 

HTML5 Usage & Styling example:
```
<figure>
	<img src="/res/imgs/latte_coffee.png" alt="A picture of a good old cup of coffee.">
	<figcaption>
		A good cup of &ldquo;Starbucks&rdquo; coffee.
	</figcaption>
</figure>

```

Terminology & Styling example
```
<tag attribute="value">
	content
</tag>
```

## CSS3/SASS Formatting Rules
##### CSS3

* Always place an opening curly brace (`{`) inside a newline *after* the selector.
* Always place a space after the semi-colon (`:`) before defining your value.
* Always indent children proerties & values. An exception below...
* Always keep contextually close selectors next to each other in your code.
* Always name the types of styles that are going to be defined inside the document at the top of the document.

CSS3 Usage & Styling example:
```
/* .coffee */
/* .tea */

/* .coffee */
/*************************************/
.coffee
{
	//Some styles
}

.coffee__header
{
	//Some styles
}



/* .tea */
/*************************************/
.tea
{
	//Some styles
}

.tea--earl-gray
{
	//Some styles
}
```

Terminology & Styling example
```
selector
{
	property: value;
}
```

##### SASS
* Always prefix partial sass files with an underscore (`_`). Eg. `_variables.scss`,`_fonts.scss` and `_settings.scss`.
* Always use partials that compile into one `style.scss` file using `@import _partial.scss`.
* Always place the appropriate styles/varaibles in the appropirate files.
* Always use camel casing for variables. eg. `$colorPrimary: #123456`

Terminology & Styling example
```
@import _partial.scss;
$colorPrimary: #123456; 
```


## Indenting Exceptions (both HTML5 and CSS3/SASS)
* (HTML5) You can pass up indenting for headers if the length of the content is relatively short.
* (CSS3/SASS) You can pass up indenting if you're defining only one property in a series of related elements.

##### HTML Formatting Rules
```
<section>
	<h1>Coffee</h1> <!-- Exception. Content is small. -->
	<p> <!-- Non-exception. Content is too large. -->
		Coffee is a brewed drink prepared from roasted coffee beans, which are the seeds of berries from 
		the Coffea plant. The genus Coffea is native to tropical Africa, Madagascar, and the Comoros,
		Mauritius and Réunion in the Indian Ocean.
	</p>
</section>
```

##### CSS3/SASS
```
h1, .h1{ font-size: 72px;}
h2, .h2{ font-size: 64px;}
h3, .h3{ font-size: 48px;}
h4, .h4{ font-size: 36px;}
h5, .h5{ font-size: 28px;}
```

## Javascript Formatting Rules
* Always prefix a javascript hook class with a `js-`, to create something like `.js-parralx`.
* Never give a javascript hook class any css properties.

## Head tag, Type Attributes and Proper linkage.

* Always comment segemnts in the `<head>` tag. Eg. "Libraries", "Stylesheets", "Meta tags", etc.
* Always include js scripts at the bottom of the document unless it breaks the page/documentation states otherwise.
* Never add a `type="text/css"` attribute to stylesheet `<link>` tags.
* Never add a `type="text/javascript"` attribute to javascript `<script>` tags.


Example:
```
<head>
	<!-- PAGE INFO & META TAGS -->
	<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
	
	<meta charset="UTF-8">
	<meta name="author" content="Omrii">
	<meta name="description" content="Head tag & Type Attributes example.">
	<title>Title of page</title>
		
		
	<!-- STYLESHEET -->
	<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->

	<!-- PROJECT STYLESHEET -->
	<!-- BOOTSTRAP CSS -->
	<!-- FONT-AWESOME CSS -->
    	<link href="/res/libs/css/style.css" rel="stylesheet">
    
</head>
<body>
	<!-- Content -->

	<!-- LIBRARIES -->
	<!--~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~-->
	 
	<!-- JQUERY JS -->
	<script src="/res/libs/js/jquery.min.js"></script>
</body>
```

## File Naming & Project Organization

* Always use dash characters (`-`) when wanting to spacing something. Eg. `bg-primary.png`.
* Always use lowercase letters.
* Always start with zero when enumerating files. (Eg. `bg0.png`, `bg1.png`, `bg2.png`, etc...)
* Always name the home page html file "`homepagefile.html`".

Some filenames:
```
nav-companylogo.png
nav-companylogo-large.png
hero-bg-mp4.mp4
hero-bg-webm.webm
```

Project example:
```
//root
|
├── views //All of the pages in the website.
|   ├── page0.php
|   ├── page1.html
|   ├── homepagefile.php
|   └── includes
| 	├── header.html
|   	└── footer.html
|
├── libs //(Libraries)
|   ├── css
|   |   ├── bootstrap.css
|   |   └── awesomefont.css
|   |
|   └── js
|       ├── jQuery.js
|       └── angularJS.js
|
└── res //(Resources)
    ├── graphics
    |   ├── picture0.png
    |   ├── picture0.jpg
    |   ├── logo.svg
    |   └── favicon.ico
    |
    ├── js
    |   ├── app.js
    |   └── functions.js
    |
    ├── sass
    |   ├──   helper
    |   |   ├── _typography-helper.scss
    |   |   ├── _buttons-helper.scss
    |   |   ├── _lists-helper.scss
    |   |   ├── _inputs-helper.scss
    |   |   ├── _header-helper.scss
    |   |   └── _footer-helper.scss
    |   ├──   layout
    |   |   ├── _typography.scss
    |   |   ├── _buttons.scss
    |   |   ├── _lists.scss
    |   |   ├── _inputs.scss
    |   |   ├── _header.scss
    |   |   └── _footer.scss
    |   ├── _fonts.scss
    |   ├── _variables.scss
    |   ├── _reset.scss
    |   └── style.scss
    |
    └── fonts
        ├── font0.ttf
        ├── font0.eot
        ├── font1.woff2
        └── font1.svg
```


## Website testing
Sometimes you will overlook/misuse your markups. Use these websites to check if they're okay.
* https://gsnedders.html5.org/outliner/ 
* Outlining article: https://www.smashingmagazine.com/2011/08/html5-and-the-document-outlining-algorithm/
* http://html5doctor.com/
* https://toolbox.seositecheckup.com/ (15 Free checks *per account ;)*)
* https://developers.google.com/speed/pagespeed/insights/

### Other references

**Some useful reference links**
* https://css-tricks.com/centering-css-complete-guide/ Ways to center things
* https://css-tricks.com/gulp-for-beginners/ Gulp for beginners
* http://clubmate.fi/sass-maps-syntax-examples-and-good-things/ Sass maps
* https://css-tricks.com/almanac/properties/t/text-rendering/ Cool extra typography thing
* http://codepen.io/chris22smith/pen/pymBWL All of `<input>` `type=""`s

Some more stuff coming `soon™`.

If you've made it through this whole readme then thanks for reading! or just scrolling down here or whatever.

* Responsive images
* ES6
* 

I left this GitHub editor style link here for me becasue I know I'll need it again at some point.
[don't mine me c:](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet "(old man voice) GET OUTTA HERE!!")
