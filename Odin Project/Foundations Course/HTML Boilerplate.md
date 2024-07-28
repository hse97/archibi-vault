All HTML documents have the same basic structure called the boilerplate 

### Creating an HTML file 
use the `.html` to indicate a file is an html file 
should always create an `index.html` file 
	`index.html` contains the homepage of our website
	web server by default look for `index.html` files. Not having one causes problems 

### The Doctype 
every html page starts with a doctype declaration 
	tells the browswer what version of HTML it should use to render the doc 
	`<!DOCTYPE html>` uses the most current version of HTML 
![[Pasted image 20240727145654.png]]

### HTML element
after declaring the doctype, need to provide a `<html>` element
	known as root element meaning every other element descends from it
	`<html lang="en">` 
		`lang` is an attritube associated with the given tag i.e `html` in this case
		attributes provide addlt info about HTML elements
			`lang ` specifies the language of the text content in the element in this case. Helps with presentation and accessibility 

### Head Element 
`<head>` element is for important meta-info about the webpage and stuff required for the webpage to render 
Should NOT display content for the webpage 
stuff inside the head element
	`<meta>` element 
		should always be tagged with the charset encoding of the webpage
		`<meta charset="utf-8">`
			ensures webpage will display special symbols and characters properly 
		`<title>` element
			`<title>My First Webpage</title>` 
			gives it a human readable title 
![[Pasted image 20240727145739.png]]

### Body Element
`<body>` final element to complete the HTML boilerplate 
where the content that will be displayed to users goes 
always goes within the `<html>` and after the `<head>` element 
![[Pasted image 20240727145944.png]]

# VSCODE Boilerplate Shortcut
Just type `!` and press enter 