**Charts are far better for displaying data visually than tables and have the added benefit that no one is ever going to press-gang**
**them into use as a layout tool**

**What is the A great way to get started with charts ?**

is with Chart.js, a JavaScript plugin that uses HTML5’s canvas element to draw the graph onto the page.

**To see how to use chart there are 3 steps :**

* one will show the number of buyers a fictional product has over the course of 6 months, this will be a line chart. 

* the second will show which countries the customers come from

* this will be the pie chart; finally we’ll use a bar chart to show profit over the period.

**Setting up**
The first thing we need to do is download Chart.js.
* Copy the Chart.min.js out of the unzipped folder and into the directory you’ll be working in.
* Then create a new html page and import the script:

<!DOCTYPE html>
<html lang="en">
    <head>
        <meta charset="utf-8" />
        <title>Chart.js demo</title>
        <script src='Chart.min.js'></script>
    </head>
    <body>
    </body>
</html>

**BASIC USAGE**

*The <canvas> element*
 *the <canvas> element has only two attributes, width and height.  the canvas will initially be 300 pixels wide and 150 pixels high. 
  The element can be sized arbitrarily by CSS, but during rendering  the image is scaled to fit its layout size: if the CSS
  sizing doesn't respect the ratio of the initial canvas, it will appear distorted.*
  FALLBACK CONTANT :
 *For example, we could provide a text description of the canvas content or provide a static image of the dynamically rendered content.
  This can look something like this:*
  
  
  <canvas id="stockGraph" width="150" height="150">
  current stock price: $3.15 + 0.15
</canvas>

<canvas id="clock" width="150" height="150">
  <img src="images/clock.png" width="150" height="150" alt=""/>
</canvas>

## DRAEING SHAPES WITH CANVAS 
**Drawing rectangles**

Unlike SVG, <canvas> only supports two primitive shapes: rectangles and paths (lists of points connected by lines). All other shapes must be 
created by combining one or more paths. Luckily we have an assortment of path drawing functions which make it possible to compose very complex shapes.
  
  **There are three functions that draw rectangles on the canvas:**

* fillRect(x, y, width, height)
Draws a filled rectangle.
* strokeRect(x, y, width, height)
Draws a rectangular outline.
* clearRect(x, y, width, height)
Clears the specified rectangular area, making it fully transparent.

### Applying styles and colors
**there are two important properties we can use: fillStyle and strokeStyle.**

* fillStyle = color
Sets the style used when filling shapes.
* strokeStyle = color
Sets the style for shapes' outlines.

**A fillStyle example**

function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  for (var i = 0; i < 6; i++) {
    for (var j = 0; j < 6; j++) {
      ctx.fillStyle = 'rgb(' + Math.floor(255 - 42.5 * i) + ', ' +
                       Math.floor(255 - 42.5 * j) + ', 0)';
      ctx.fillRect(j * 25, i * 25, 25, 25);
    }
  }
}


### Drawing text
**The canvas rendering context provides two methods to render text:**

fillText(text, x, y [, maxWidth])
Fills a given text at the given (x,y) position. Optionally with a maximum width to draw.
strokeText(text, x, y [, maxWidth])
Strokes a given text at the given (x,y) position. Optionally with a maximum width to draw.

* A fillText example
The text is filled using the current fillStyle.

function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  ctx.font = '48px serif';
  ctx.fillText('Hello world', 10, 50);
}

	* A strokeText example
The text is filled using the current strokeStyle.

function draw() {
  var ctx = document.getElementById('canvas').getContext('2d');
  ctx.font = '48px serif';
  ctx.strokeText('Hello world', 10, 50);
}

  
  
  
  
  
  
  
  
  
  
  
  
  
  
