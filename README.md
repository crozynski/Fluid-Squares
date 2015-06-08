# Fluid-Squares

## What is it?

A fluid grid of square units using HTML and CSS.

Fluid Squares preserves a unit's square proportion within a fluid layout. The number of columns also reduce to suit browser or device width using CSS media queries.

It works on all modern desktop browsers. Media queries are written Mobile First. IE8 doesn't support media queries, so the css3-mediaqueries.js polyfill is temporarily included. 

See [www.fluidsquares.com](http://www.fluidsquares.com) for more.

## What problem does Fluid Squares fix?

Without a fix, the result of reducing a browser window's width squashes a fluid grid's squares into rectangles.

To fix this each unit's padding-bottom size is set to match its width in percentages. On top of that each unit is a percentage of the global container to determine how many columns there are.

Setting a unit's width to 25% and padding-bottom to 25% will give you four units in a row that will remain square regardless of screen size or browser window resizing.

## The ingredients

### HTML

The basic structure of each unit is a div for content, which is nested in an anchor element:

````
<a href="url">
<div>content</div>
</a>
````

If you don't want the entire unit to be a link, a class has been created for that purpose. Just remove the anchor element and add class="category" to the div instead.

````
<div class="category">content</div>
````

### CSS

Media queries control the number of columns displayed (1, 2, 3, and 4) on browser resize, as well as providing fine control over font sizes.

It includes a cut down CSS reset to suit this bare bones grid. Replace with a fresh [Reset](http://meyerweb.com/eric/tools/css/reset/) or [Normalize](http://necolas.github.io/normalize.css/) and customise to suit your own needs.

### No wrapper?

It uses the body tag as a wrapper, but would certainly work within a standard div wrapper or HTML5 block elements.