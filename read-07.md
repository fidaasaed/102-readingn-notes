# Modian Modeling
**Domain modeling is the process of creating a conceptual model for a specific problem. And a domain model
that's articulated well can verify and validate your understanding of that problem.**

*what is the  tips to follow when building your own domain models?*
* Model its attributes with a constructor function that defines and initializes properties.
* Model its behaviors with small methods that focus on doing one job well.
* Create instances using the new keyword followed by a call to a constructor function.
* Store the newly created object in a variable so you can access its properties and methods from outside.
* Use the this variable within methods so you can access the object's properties and methods from inside.

**What is the function of Generate random numbers**
*To model the random nature of user behavior, you'll need the help of a random number generator. Fortunately, the JavaScript standard library includes a Math.random() function for just this sort of occasion.*

*this is for examle the methods can be added to a constructor function's prototype*

var EpicFailVideo = function(epicRating, hasAnimals) {
  this.epicRating = epicRating;
  this.hasAnimals = hasAnimals;
}

EpicFailVideo.prototype.generateRandom = function(min, max) {
  return Math.floor(Math.random() * (max - min + 1)) + min;
}

var parkourFail = new EpicFailVideo(7, false);
var corgiFail = new EpicFailVideo(4, true);

console.log(parkourFail.generateRandom(1, 5));
console.log(corgiFail.generateRandom(1, 5));

## HTML
**What is the uses of tables ?
The table element is used to add tables to a web page.** 
*A table is drawn out row by row. Each row is created with the <tr> element. Inside each row there are a number of cells 
represented by the *td* element or <th> if it is a header .*
You can make cells of a table span more than one row or column using the rowspan and colspan attributes.
 For long tables you can split the table into a thead, <tbody>, and <tfoot>.
  
  
  ![image](https://user-images.githubusercontent.com/79834102/111896017-56cfa480-8a1f-11eb-9ec7-912da047b35c.png)



### jS
 **An object is a series of variables and functions that represent something from the world around you.**
*In an object, variables are known as properties of the object; functions are known as methods of the object*
*Web browsers implement objects that represent both 
the browser window and the document loaded into the browser window.and **JavaScript also has several built-in objects such as :**
           * String
           * Number 
           * Mat
           * Date
*Their properties and methods offer functionality that help you write scripts. Arrays and objects can be used to create complex data.
Functions allow you to group a set of related statements together that represent a single task. Functions can take parameters (informatiorJ required 
to do their job)and may return a value.*


![image](https://user-images.githubusercontent.com/79834102/111896199-64d1f500-8a20-11eb-90ef-c69379995a17.png)


