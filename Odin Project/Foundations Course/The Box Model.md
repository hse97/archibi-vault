where the elements get placed on the page 
uses `margin`, `padding`, and `borders` 
everything is a box 
	boxes can have boxes nested inside of them
	apply an outline to every element with 
		`* { outline: 2px solid red; }`  
`padding`
	increases the space between the border of the box and the content of the box 
`border`
	adds space (even a pixel or two) between the margin and the padding
`margin` 
	increases the space between the borders of a box and the borders of adjacent boxes 
A common convention is to use a `border-box` or `conent-box` to all elements
	`* { `
		`width: 200px;`
		`height: 200px;`
		`box-sizing: content-box/border-box;`
		`}`
		`content-box`
			using this sets the content box size to the height/width values
		`border-box`
			using this sets the border box size to the height/width values
	It goes `margin` then `border` then `padding` then `content`
		setting an element to `border-box` and then adding padding wont change the box size because the box size is determined by `border-box` and `padding` is nested inside of the `border`. So adding padding just crunches the `content` 
		opposite for setting to `content-box` 
		if you set `content-box` then set `padding` box will increase in size because `padding`  is outside of `content` so it would be the `content-box` size + the `padding` size

### Margins
determines the space around the box, outside of any defined borders
`.box {`
	`margin: 0 3em 0 3em;` 
	`}`
margin takes 4 values 
	`<margin-top> || <margin-right> || <margin-bottom> || <margin-left>`
if not given a parameter it assumes some based off given paramters
Auto and Centering 
	`margin` can also accept value of auto, tells browser to define margin for you 
		typically assumes 0 but will use whatever free space
	`auto` is good for horizontal centerign
		`.containter { width: 980px; margin: 0 auto; }`
			element is given a specific width 
			the left and right margins are set to auto 
