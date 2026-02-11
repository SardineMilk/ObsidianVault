
Websites should accommodate a range of screen sizes

Responsive Web Design
- Frontend solution
Adaptive Web Design
- Backend solution


Progressive Web Apps (PWA)
- Uses web standards like JavaScript and JSON
- HWML only? Yes
- RWD accesses the viewport size, then hides/stacks/shrinks

### Responsive Web Design
Requires all of these to be true RWD

#### Viewport
```
<head>
<meta name="viewport" content="width=device-width, initial-scale=1.0>
</head>
```
Vertical scroll good
Don't use large fixed with elements
don't let content rely on a particular viewport
Use CSS media queries to apply different styling for small and large screens
- use 1% not 5px
#### Grid View
Not grid layout
12 columns, width adds to 100%
All html elements must have `box-sizing: border-box;`
`.menu { width: 25%; float: left;}`
`.main { width: 75%; float: left;}`

#### Media Queries
`@media` rule only includes a block of CSS properties if a certain condition is met
```
@media only screen and (max-width: 600px) {
	body {
		background-color: blue;	
	}
}

```
#### Responsive Images

`width` property
`max-width` means it can't scale lower than this

### Adaptive Web Design
Serve a different website for different screen sizes