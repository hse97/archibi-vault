### Anchor Elements 
`<a>` tag to anchor an element 
	`<a href="https://www.theodinproject.com/about">About the Odin Project</a>`
	The opening tag has a href (hypertex reference) that is passed the link we want to go 

### Opening links in a new tab
default links open in the same tab 
to open in a new tab 
`<a href="https://www.theodinproject.com/about" target="_blank" rel="noopener noreferrer">About The Odin Project</a>
	`target="_blank"` sets the destination for the opened page as a new tab 
	`rel="noopener noreferrer"`prevents the opened page from having access to the original webpage that opened it, and prevents the resource from knowing who linked to it 
		security functions

### Absolute and relative links
Absolute Links
	link to other websites on the internet 
Relative links 
	link to other pages within our own website 
	do not include domain names, assumes page's domain is the same as owns 

### Images
`<img>` element 
	it is self closing does not need a closing tag 
	`<img src="https://www.theodinproject.com/mstile-310x310.png">`

### File Directories
`./` putting this before a link tells the code it should look for the file/directory *relative* to the current directory 
`../` goes up two directories relative to the current directory 

### Alt Attribute
for `<img>` elements
	`alt="The alt attribute"` if the image fails to load display this text instead

### Image Size Attribute
for `<img>` elements 
	always specify the size of the image to prevent browser issues
	`height ="310" width="310"` or whatever the img resolution is 