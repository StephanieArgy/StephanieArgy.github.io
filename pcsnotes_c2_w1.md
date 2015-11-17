---
layout: page
title: Primer Pro, Week One
permalink: /pcsnotes_c2_w1/
---

* [Class Overview](#classOverview)
* [JavaScript](#JavaScript)
* [Responsive Design](#responsiveDesign)

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


