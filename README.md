# my personal coding standards and style
Hi! This is my personal coding standards and style when I make my own wbesites. I made this repository for the sake of documentation, **to get myself to think about my code**, and to hopefully give other developers some ideas.


I ~~stole~~ got the idea from [thelifemgmt](https://github.com/thelifemgmt)'s [Coding Standards & Styleguide](https://github.com/thelifemgmt/coding_standards "thelifemgmt's Coding Standards & Styleguide")

**Some useful reference links**

* https://css-tricks.com/centering-css-complete-guide/
* https://css-tricks.com/gulp-for-beginners/
* Another Link


## HTML Formatting Rules

* Always indent children elements. A few exceptions below...
* Always indent using *only* the "tab" character `(ascii: 9)`. Never use "space" characters `(ascii: 32)`. 
* Always include an `alt=""` attribute to `<img>` tags.
* Always create a `<label>` tag for an `<input>` tag.
* Try to use the [BEM (Block Element Modifier)](http://csswizardry.com/2013/01/mindbemding-getting-your-head-round-bem-syntax/) naming convention when possible.
* Avoid using `"` and `'` in your content. Use `&lsquo;`/`&rsquo;` and `&ldquo;`/`&rdquo;` (`‘`, `’`, `“`, `”`) instead. 
* Never close self-closing tags such as `<hr>`, `<br>`, `<img>`, or `<input>`.
* Never use inline css or inline javascript.
* Never use an `id=""` attribute unless it's for an `<input>` tag. 

Example:
```
<!-- Tag Usage & Styling example -->
<figure>
	<img src="url(/res/imgs/latte_coffee.png)" alt="A picture of a good old cup of coffee.">
	<figcaption>
		A good cup of &ldquo;Starbucks&rdquo; coffee.
	</figcaption>
</figure>

```
```
<!-- Terminology & Styling example -->
<tag attribute="value">
	content
</tag>
```

## CSS/SASS Formatting Rules
*** NOT FINISHED !! ***

##### CSS

* Always place an oprning curly brace (`{`) inside a newline *after* the selector.
* Always place a space after the semi-colon (`:`) before defining your value.
* Always keep contextually close selectors next to each other in your code. (Example below...).
* Always label the types of styles at the top of the document.

Code example
```
/* coffee */
/* tea */

/* coffee */
/*************************************/
.coffee
{
	//Some styles
}

.coffee__header
{
	//Some styles
}



/* tea */
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
* Always prefix partial sas files with an underscore (`_`). Eg. `_variables.scss`,`_fonts.scss` and `_settings.scss`.
* Always use partials that compile into one `style.scss` file using `@import _partial.scss`.
* Always place the appropriate styles/varaibles in the appropirate files.

Terminology & Styling example
```
@import _partial.scss;
```


## Indenting Exceptions (both HTML and CSS/SASS)
* (HTML) You can pass up indenting for headers if the length of the content is relatively short.
* (CSS/SASS) You can pass up indenting if you're defining only one property in a series of related elements.

##### HTML
```
<section>
	<h1>Coffee</h1>
	<p>
		Coffee is a brewed drink prepared from roasted coffee beans, which are the seeds of berries from 
		the Coffea plant. The genus Coffea is native to tropical Africa, Madagascar, and the Comoros,
		Mauritius and Réunion in the Indian Ocean.
	</p>
</section>
```

##### CSS/SASS
```
h1, .h1{ font-size: 72px;}
h2, .h2{ font-size: 64px;}
h3, .h3{ font-size: 48px;}
h4, .h4{ font-size: 36px;}
h5, .h5{ font-size: 28px;}
```

## Head tag, Type Attributes and Proper linkage.

* Always comment segemnts in the `<head>` tag. Eg. "Libraries", "Stylesheets", "Meta tags", etc.
* Always include js scripts at the bottom of the document unless it breaks the page/documentation states otherwise.
* Never add a `type="text/css"` attribute to stylesheet `<link>` tags.
* Never add a `type="text/javascript"` attribute to javascript `<script>` tags.

In HTML5 the default value for the `type` attribute will always be text so it's not needed with those two tags.

Example:
```
<head>
    <!-- PAGE INFO & META TAGS -->
	<!---------------------------------------------->
	
	<meta charset="UTF-8">
	<meta name="author" content="Omrii">
	<meta name="description" content="Head tag & Type Attributes example.">
	<title>Title of page</title>
		
		
	<!-- LIBRARIES -->
	<!---------------------------------------------->

	<!-- BOOTSTRAP CSS -->
    	<link href="/res/libs/css/bootstrap.min.css" rel="stylesheet">
    
</head>
<body>
	<!-- Content -->

	<!-- LIBRARIES -->
	<!---------------------------------------------->
	 
	<!-- JQUERY JS -->
	<script src="/res/libs/js/jquery.min.js"></script>
</body>
```

## CSS3 Animations
*** NOT FINISHED !! ***

* Always use the `transform` property when animating elements with CSS.
* You have a lot of options! Pick the best ones: https://api.jqueryui.com/easings/

## Resource File Naming

** Note! Kind of iffy about the first two rules. Considering merging them or something... **

* Always use underscores characters (`_`) to specify catagorical context to  about the contents of the file (Eg. "nav", "hero", "footer")
* Always use dash characters (`-`) to specify an attribute/charactristic about the contents of the file. (Eg. "large", "owen", "min")
* Always use lowercase letters.
* Always start with zero when enumerating files. (Eg. `bg0.png`, `bg1.png`, `bg2.png`, etc...)

Example:
```
nav_companylogo.png
nav_companylogo-large.png
hero_bg-mp4.mp4
hero_bg-webm.webm
```
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
    |   ├── style.min.css
    |   └── style.css
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
    |   ├──   _fonts.scss
    |   ├──   _variables.scss
    |   ├──   _buttons.scss
    |   ├──   _lists.scss
    |   ├──   _inputs.scss
    |   ├──   _header.scss
    |   ├──   _footer.scss
    |   ├──   _typography.scss
    |   ├──   _reset.scss
    |   └──   style.scss
    |
    └── fonts
        ├──   font0.ttf
        ├──   font0.eot
        ├──   font1.ttf
        └──   font1.eot
```


## Website testing
Sometimes you will overlook/misuse your markups. Use these websites to check if they're okay.
* https://gsnedders.html5.org/outliner/ 
* Outlining article: https://www.smashingmagazine.com/2011/08/html5-and-the-document-outlining-algorithm/
* http://html5doctor.com/
* https://toolbox.seositecheckup.com/ (15 Free checks *per account ;)*)
* https://developers.google.com/speed/pagespeed/insights/

### Other references
Some more stuff coming `soon™`.

I left this GitHub editor style link here for me becasue I know I'll need it again at some point.
[don't mine me c:](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet "(old man voice) GET OUTTA HERE!!")
