### Basic Syntax
1. Selector
2. Declarations
	1. property-value pair
![[Pasted image 20240728115231.png]]
	`<div>` is a basic HTML element. Empty container. Generally best not to use but good for learning and simplicity. 

### Selectors
refer to the HTML elements that the CSS rules apply to 
what is actually being 'selected'

Universal Selector
	will select elements of any type
	syntax for it is a simple `*` in front of the element 
Type Selector 
	selects all elements of given type 
	syntax for it is the name of the elements 
	`div { color: white; }` all div elements would be white 
Class Selectors
	Selects all elements of certain class
	class are just attributes given to an HTML element 
	syntax is `.classType{...}`
	define class of html element:
		`<div class="alert-text">Please Agree</div>`
	style it with css
		`.alert-text{ color: red; }` 
	can add multiple classes to the same element, use white space to separate the classes 
ID Selectors
	select element with given ID 
	difference from class is elements can only have ONE id 
	syntax is `#ID {...}` 
	define ID of html element 
		`<div id="title">My Element</div>`
	style with CSS 
		`#title { color: red; }` 
Grouping Selectors
	Can share CSS styling between 2 elements while also given them their own unique styling 
	syntax is separation with a comma 
![[Pasted image 20240728120702.png]]
Chaining Selectors 
	chain multiple properties together to apply styling to elements that have both properties 
	I.e Elements that share the same class, but have different IDs we can apply styling to just one of them 
![[Pasted image 20240728121357.png]]
	2 elements sharing one class but having a different 2nd class 
	apply styling to just one of them with: 
		`.subsection.header { color: red; }`
		applies red coloring to just the first `<div>` 
	can be used with ID or other attributes 
		`.subsection#preview { color: blue }`
			would apply styling to an HTML element of class `subsection` and with ID `preview`
Descendant Combinators 
	allows you to style elements only if they are descendants from a defined attribute 
	Snyntax is `.ancestor .child { ... }`
	i.e elements of class `child` will only be styled if if it nested inside of an element with class  `ancestor`
![[Pasted image 20240728122142.png]]
	No limit to how many combinators you can add 

### Basic CSS Properties
Color and Background
	`color` sets element color
	`background-color` sets element background color
		accept keywords, HEX, RGB, and HSL values 
		[CSS Legal Color Values](https://www.w3schools.com/cssref/css_colors_legal.php)
Typography basics and text-align
	`font-family` sets value for fonts 
		best to use a list, browser goes down the list till it finds a supported one, issues if no supported font
		2 categories:
			Font family names like `"Times New Roman"`, uses quotes b/c spaces
			Generic family name like `serif`, no quotes because one word
		`font-family: "Times New Roman", serif;`
	`font-size` 
		should not have any white space
		`font-size: 22px`
	`font-weight` affects boldness of text, needs font to support the weight
		value can be a keyword or a number between 1 to 1000
		`font-weight: bold`
		`font-weight: 700`
	`text-align` aligns text horizontally within an element 
		usually uses keywords
		`text-align: center`
Image Height and Width
	by default `<img>` will have the same height/width as the raw image
	to adjust without losing proportions use `auto` for one of them and adjust the other 
		`img { height: auto; width: 500px; }`
	best practice to always include height/weight info to prevent page shifting once image loads 
### How to Add CSS to HTML 
External CSS
	most common
	works by linking a CSS file to an HTML file inside the `<head>` tags with a self closing `<link>` element 
		`<head>`
			`<link rel="stylesheet" href="styles.css">`
		`</head>`
	self closing `<link>` element 
		`rel="stylesheet"` specifies the relationship between the HTML and CSS files
		`href="styles.css"` is the location of the CSS file used. In this case it assumes its in the same dir as the HTML file 

Internal CSS
	embeds CSS into the HTML file directly 
	the CSS styling is placed inside the `<head>` tags in the HTML file 
		`<style>...</style>` with CSS inside nested in the `<head>` tags
	styling is the same just doesn't link anywhere 
Inline CSS 
	adds styling to a single element 
	added directly to the opening tag 
		`<div style="color: white; background-color: black;">...</div>`
	only useful when needing a specific style on one element 
	