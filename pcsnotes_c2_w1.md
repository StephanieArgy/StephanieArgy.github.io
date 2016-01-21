---
layout: page
title: Primer Pro, Week One
permalink: /pcsnotes_c2_w1/
---

* [Class Overview](#classOverview)
* [JavaScript](#JavaScript)
* [Responsive Design](#responsiveDesign)

***

* [Events](#events)
* [JavaScript Functions and Objects](#javaScriptFunctionsObjects)

This class: Set our own stakes. Decide how hard we want to push ourselves.

<a name="classOverview"></a>
##Overall structure of the class:

###JavaScript

We're going to work on JavaScript basics. Usually you get syntax with concepts, little practical work. But we don't learn as well that way, as by doing things practically -- **goal-driven.**

We have to learn what a programming language is. Treehouse is the way that we'll learn the underlying concepts for what we're doing practically in class.  Going to start by building a menu.

###jQuery

Library of JavaScript code written by someone else. First of two libraries that we'll use.

###Responsive Design

Current start of the art.

* Responsive images.
* Responsive typography.

**Pay attention to the stuff that's the most fun for us.**

###Final Project

Start pulling things together, choose team for final project.

###Bootstrap (another library)

How the pros do it.

<a name="JavaScript"></a>
##JavaScript

People give away books on JavaScript: <a href="http://jsbooks.revolunet.com/" target="_blank">http://jsbooks.revolunet.com/</a>

One of the best is <a href="http://eloquentjavascript.net/">*Eloquent JavaScript</a>.

In learning JavaScript, look for commonalities with HTML and CSS:

* Delimiters
* Name/value pairs
* Blocks - As in CSS, we'll see blocks, but they're used for different things.

Each individual step in a script is a **statement**. Each statment ends in a semi-colon:

```
document.write("This");
```

Comments can be inserted by typing Command + /
(Use lots of comments!)

When testing for bugs, can "comment out" sections of the code, to see if that fixes the problem.

###Variables

Scripts often need to temporarily store bits of information to achieve thier tasks. These are stored in **variables**.

Variables are defined like this:

```
var name-of-new-variable;
```
JavaScript can be contained in the HTML file between **script** tags, or in a external **.js** document.

To assign a value to a variable:

```
variable-name = variable-value;
```

Or, can define the variable and assign it a value at the same time:

```
var name-of-variable = variable-value;
```

###Data Types

* Numbers (don't have quotes)
* Strings (enclosed in either single or double quotes -- but they must match for each string)
* Booleans (true/false)

Arrays are a special type of variable: they hold a list:

1. Wrapped in square brackets.
2. Separated by commas.
3. Zero-based counting system.

```
colors = ['pink', 'yellow', 'green'];
```
(In this case, pink=0, yellow=1, green=2.)

###Arithmetic operators

```
var width = 3;
var height = 2;
area = width * height;
```

Follows order of operations. 

###Concatenation of Strings

**Have to put in all the necessary spaces.**

```
var greeting = "Howdy ";
var name = "Molly.";
var message = greeting + name;
```

###Object-oriented

When people say that JavaScript is an object-oriented language, objects have: 

* Properies
* Methods (things that they can do)

Markup language is static:

* HTML: The world as it is. (static)
* CSS The world as you want it to be. (static)
* JavaScript - What you want to do change the world (**dynamic**)

(In next class, we'll work on **functions**.)

<a name="responsiveDesign"></a>
##Responsive Design

The other main thread of this class is **responsive design**. Next week, we'll make our journals responsive.

1. Customer: Mobile first.
2. Technology: Responsive Design

(App? Website? Hard to tell...)

Want to have one URL that represents our content. You used to have to maintain multiple sites for different types of devices and screens; now, we want universal content. **WE only want to write code ONCE.**

The concept of the "fold" (as in, "above the fold," from newspapers) is changing, but it's still impotrant to give priority to the most important materials.

###Developers' Tools for Responsive Design:

1. Flexible grid -- Percentages, ems, rems (e.g. flexible units of measurement), plus grids (as in Bootstrap).
2. Responsive images (including Scalable Vector Graphics)
3. CSS media queries and screen resolutions.

**Responsive**: Changes smoothly.
**Adaptive**: Changes in jumps.

In older design: When the design gets too wide, it won't expand any farther. Using **max-width**.

Have to have content that works on phones. A lot of countries have really invested in cell phone networks.
**caniuse.com**

Start with the most primitive device, make sure it works, then build up from there: **PROGRESSIVE ENHANCEMENT**.

If you connect your iPhone to your computer, you cna load up your website in progress on your phone.

****

<a name="events"></a>
##Events

Browsers look through a liminted plastic tube at the customer. Events are what we have to work with, to learn about them and what they're doing.

What is an event? Whare the different kinds?

* click
* keydown
* keyup
* mouse (click, hover, movement)
* scroll
* resize
* open
* close

An event can trigger a function. 

What is in a web app?  DOM > HTML > Body> input, p, etc.

**To keep a a function from doing its default behavior: event.preventDefault();


<a name="javaScriptFunctionsObjects"></a>
##JavaScript Functions and Objects

Variables can hold: 

* Numbers
* Strings
* Booleans (true/false)
* Ojbects (Collections of variables and objects and functions)
* Functions
* Arrays

**Statements** represent each step in a program. The semi-colon is a statement separator.

###Functions

Functions let you group a series of statements together to perform a specific task.  Their form looks like this:

```
function name-of-function () {
  ____________;
  ____________;
}
```

To declare a function, by default, you useCamelCase. **Typically, variables are noun phrases, and functions are verb phrases.**  (Also, "function" is a reserved word, so it can't be used for other purposes in JavaScript.)

```
function sayHello(){
  document.write("Hello!");
}
```

The function name is **sayHello(), where the () means "run this."  **To run the function: **sayHello();** (And don't forget the semi-colon at the end!)

Scope -- Rules on how variables are managed.

```
function getArea(width,height){
return width * height;
}
```

Function takes an input, processes it, returns an output.

INPUT ---> PROCESS ---> OUTPUT

In a fuction declaration, inputs go in the parentheses, and outputs get returned:

```
function blahblah(inputs){
  return outputs;
}
```

Input = Arguments

Parameters (stored as variables):

function bakeCake(type){}  -- **type** is the parameter. When the function is called, an argument is provided for that parameter (e.g. lemon, chocolate, etc.).

Most things have both variables and functions. An **object** groups functions and variables to create a model. Inside of an object:
**Variables are called properties.**
**Functions are called methods.**

What's shown on a web page is the **Document Object Model.** The HTML is put into a string.

Everything in an object has a name.

The general principle of object-oriented programming: **Don't do the work for the object; let the object do the work itself.**

this. -- Refers to the property (i.e. variable) attached: **this.room** or **this.booked**

An anonymous function is an unnamed function:

NAMED FUNCTION:

```
function area()(width, height){
  return width * height;
};
```

ANONYMOUS FUNCTION:

```
var area = function(width, height){
  return width * height;
};
```

A named function can be called using its name (either before or after it has been created).

###Objects

Objects can be defined in numerous ways.

LITERAL NOTATION: 

```
var hotel = {
  name: 'Quay',
  rooms: 40,
  booked: 25,
  checkAvailability: function(){
  return this.rooms - this.booked;
  }
};
```

To access objects, you use the **dot operator** or **member operator:

```
var hotelName = hotel.name;
```
(**hotel** is the object, **name** is the property, the dot between is the **dot operator** or **member operator**.) 

OR

```
var hotelName = hotel['name'];
```

Like variables, objects can be updated with a new value:

```
hotel.name = "Park";
```

OR

```
hotel["name"] = "Park";
```

Object Models: 

* Global JavaScript Objects: Not a single model; group of individual objects that relate to different parts of JavaScript, such as data types (strings, numbers, booleans) or concepts (date, math, properties, methods). (e.g. **saying.length** (a property)) or **saying.toUpperCase()** (a method).)
* Browser Object Model: Creates a model of the current browser window or tab. All the parts of the browser that can be accessed through JavaScript.
* Document Object Model: Representation of the current web page.

Look into community; makes it so much easier to learn a language.

After we learn a language, most of our work will involve finding what other people have done.  Main problem is finding documentation, which is why we rely on and learn to use MDN and W3Schools.

The best way to write code: Figure out what you want. Chances are, someone else has written it. **BUT** have to be careful using unknown code, because you may not recognize malware that's been inserted into it. Using Global JavaScript Objects, you know it's been vetted and is safe.

To learn more after we finish Treehouse:

* Duckett/HeadFirst books
* [codeacademy.com](https://www.codecademy.com/) (harder)
* [nodeschool.io](http://nodeschool.io/) (hardest -- uses command line)

Next, quiz:

(Expect 100%. There are code snippets. Can put code into JavaScript console to test it.)<br>
**socrative.com**, Room acbbfac2

JavaScript is **weakly typed**, meaning that the type of variable doesn't have to be declared.

**document.write()** is a method in the Document Object Model.

Can't write numbers to document, because it's all text. So JavaScript interpreter will convert numbers to strings before handing it off to HTML. (There are hidden things going on in all this.)

As you debug, make things up and speculate, rather than saying, "I don't know."

**this.** - Probably the weirdest thing most people run into. (It means: Start where you are, go one layer out until you find that property.)

[Eloquent JavaScript](http://eloquentjavascript.net/) - Very helpful book (and online, for free). It's not so much about language as about thinking about programming.

###Assignment

[http://portlandcodeschool.github.io/primer/assignments/06-introduction-to-javascript-and-jquery/](http://portlandcodeschool.github.io/primer/assignments/06-introduction-to-javascript-and-jquery/)
(Don't do assignment before Treehouse jQuery course.)

Going to use a GitHub gist.
(Gist is a way to share code. Someone might say, "Make me a gist.")
Start with code.

1. Make repo (either local or on GitHub).

2. Get gist: [https://gist.github.com/Auraelius/5a4973be6117691789fd](https://gist.github.com/Auraelius/5a4973be6117691789fd)<br>
**Read every line of the file.**

No Doctype, have to add that. (Can put styles in another document, but CSS isn't important on this assignment.)

**What is important:**

jQuery. Basically a JavaScript library, which people have been working on and building for years. (In this assignment, we have CSS and JavaScript in the HTML document; first and last time we'll do that.)

$ = jQuery function (shortcut notation)

Give it a selector and a method:

```
$(document).ready(function(){}
```

* "document" is the selector.
* "ready" is the method.

The whole thing means: When the document is ready, run this function.

Look for patterns.
The jQuery pattern:

```
$(selector).event (function () {

})
```

To look up jQuery: jquery.com >API Documentation

Start with quiz. It's a study guide, and answering the questions will explain how to do the assignment.Point of this class: A method of learning, more than an exercise in JavaScript. **Learn how to research things.**
