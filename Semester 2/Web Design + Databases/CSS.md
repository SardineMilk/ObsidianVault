*Cascading Style Sheet*

A style sheet is a set of style rules,
allows you to make a style and apply it to many elements based on a selector.

#### Selector
A selector locates and selects elements based on tag name, class name , id.. atc

##### *Example..*
selector {
	property: value;
	property: value;
}

##### *Example for a button..*
	button {
		background-color: white;
		color: red;
		}

##### **Selector Types**
- Element-type (div)
	- HTML: <div></div>
	- ![[Pasted image 20260128093530.png]]

- ID (#name)
	- HTML: <button id='btnSave'>Save</button>
	- ![[Pasted image 20260128093314.png]]
	- CSS:
		btnSave { background-colour: white;
		color: orange;}

- class (.name)
	- HTML: <button class=.MyStyle>OK</button>
	- ![[Pasted image 20260128093426.png]]
	- CSS:
		.MyStyle { background-colour: white;
		color: orange;}


#### Style Sheets

Inline (bad maintainability)
- within a tag

Embedded (selectors)
<style>
p {font-size:14px;}
</style>
- use selectors..
- many styles within a page

External (selectors)
- separate file with styles
- very maintainable, uses selectors
- <link rel='stylesheet' type='text/css' href='default.css'/>


##### Box Model

Margin  > Border > Padding > Content

	main{
		margin: 15px;
		- can do margin-left etc but can just do
		margin: 15px 20px 15px 20px (Top,Right,Bottom,Left)
		- ^clockwise
		border: 10px;
		padding: 25px red;
		border: 15px;
		background-color: yellow;
	}


### Div
<div></div>
A box
Can contain other html content
Allows for CSS to be applied over all contained html

### Comments
Same as html
/* This is a single line comment \*/


### Properties
**Typography**
font-size
font-weight
font-family
line-height
text-align

**Colours**
color
background-color
background-image
border-color

**Positioning**
margin
border
padding

### Flexbox
Designed for mobile
Allows elements to resize based on page dimensions and other elements
### Grid Layout
Rows and columns


