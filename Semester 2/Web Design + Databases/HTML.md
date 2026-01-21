Hyper Text Markup Language
Structure of a web page

Interpreted by the browser
Browsers are both forward and backward HTML compatible

HTML5
Last major html version recommended
Introduces semantic markup
Seperates structure, presentation and behaviour

Single or double quotes can be used

Consists of tags to format web content
```
<b>Bold Text</b>
```
Many, but not all have an ending tag
```
<br>
<img>
```
Never skip an ending tag if one is needed. 
It may render, but might break

Elements can be nested
```
<html>
<body>
<h1>My Heading</h1>
<p>my paragraph</p>
</body>
</html>
```

Tags are not case sensitive, but lowercase is best practice

Starting tag can contain attributes in name,value pairs
```
<img src="img.png" width="500" height="500>
```

Very important for use with javascript:
```
<div id="main" class="mainContent"></div>
```
**id** uniquely identifies an element for e.g. javascript
**class** identifies a group of elements e.g. css

Boolean Attributes
- checked
- selected
- disabled
- readonly
```
<input type="checkbox" name="fruit" value="Apple" checked="checked">
```

Comments
```
<!-- This is a comment -->
```

Lists
<ul> is unordered - bullet poitns
<ol> is ordered - numbered