---
layout: page
title: Primer Pro, Week Four
permalink: /pcsnotes_c2_w4/
---

<cite>Donald in Mathmagic Land</cite>
Wolfson

###JavaScript and jQuery Exercises:

1. Reading forms -- Simple jQuery way to read/use input.
2. Manipulating the DOM.

```
#(______) - produces a jQuery object (where the item in the parentheses is a selector).
```

  This returns an **object**, which is an element plus extra methods and properties.
  
  The beauty of jQuery -- It understands HTML and CSS selectors.
  
  Types of selectors:
  
  1. Universal selector (*)
  2. Elements
  3. Class
  4. IDs
  5. Descendent -- **#container .box**
  6. Child -- **#container > .box**
  7. General sibling -- **#container ~ .box**
  8. Adjacent sibling -- **#container + .box**
  9. Attribute -- **input[type="text"]** (VERY POWERFUL)
  10. Psuedo-classes -- **a:hover**
  11. Pseudo-elements -- **.container:before**
  
  (Prefer to use single quotes for selectors.)
  
  Once an object has been returned, it can then be operated on by a method:
  
  ```
  $(____).click();
  ```
  
  **Method-chaining**
  
  ```
  $( ).parent.( ).click( )
  ```
  
  .addClass() method takes parapeter of selector element, adds a class that changes the appearance of the element:
  
  ```
  $('p').addClass("myClass);
  ```
  
**.selected** - Class can be semantic.

When you change the DOM, the browser wakes up and bubbles through HTML and changes just the affected elements.

**Hoisting** - Whenever JavaScript runs into a function declaration, it lifts it to the top of the current script of function.
  
Methods return an object, which is passed along -- **Traversal**

You don't really need traversal, could just use IDs and classes, but this is neater.

The big three things you do:

1. SELECT.
2. TRAVERSAL.
3. MANIPULATION.

**event.preventDefault();**

Buttons were designed around 1995, when forms were a hot new deal. The default behavior sends off information and refreshes the page. Because of backward compatibility, can't eliminate that behavior, but you can overrule it.

###JavaScript/jQuery Interaction Assignment

Assignment is [here](https://github.com/StephanieArgy/primer/blob/master/_posts/topics/2014-10-18-Interaction-JavaScript-jQuery.markdown).

One attempt at a solution is [here](http://codepen.io/StephanieArgy/pen/rVXmvR).

Flash of highlight is not gratuitous: calls attention to what has changed on the page. 

Things that are not ncessarily required, but may use.

Why is the **script** element at the bottom of the body element? So that the page is fully loaded BEFORE the JavaScript starts to run. To make extra sure that the script won't run early, can put this at the start of the JavaScript:

```
$(document).ready(function() {} );
```

Sometimes, designers will give you CSS for two different states of an element on the page. 

```
/*Interactive styles*/
.complete {
  text-decoration: line-through;
  color: gray;
}
```


**.toggle();** - Hides/reveals an element without messing with the CSS.


People are trying to make actions on screen reflect the physicality of the real world, so that it feels as though we can use physical intuition. (If tool tips come up too soon or too fast, users feel stupid; if they come up too late/slow, users get bored.)

**this** refers to what was just selected. Can manipulate **this**, OR something related to this (e.g. parent, child).

Start to understand the structure of script.

**$** - Variable name. By convention, some people start variables that contain a jQuery object with a **$**.

Characteristif of jQuery that a lot of methods do two different things depending on their situation.

"Tainted input" -- Places where code can be input into a page via a form.  **Big security risk!**  Can strip out any HTML elements to avoid code.

[Google Analytics](https://www.google.com/analytics/) - How do you know that your idea works?  Need data!

[MailChimp](http://mailchimp.com/) - Free, can link to Google analystics and use as a destination for forms.

Other tools:

[slides.com](http://slides.com/) - For presentations.

[Evernote](https://evernote.com/) - Can search through handwritten notes.

***

**Never feel victimized by complicated technology!**