---
layout: page
title: Primer Pro, Week Four
permalink: /pcsnotes_c2_w4/
---

<cite>Donald in Mathmagic Land</cite>
Wolfson

###JavaScript Exercise:

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
  9. Attribute -- **input[type="text"]**
  10. Psuedo-classes -- **a:hover**
  11. Pseudo-elements -- **.container:before**
  
  Once an object has been returned, it can then be operated on by a method:
  
  ```
  $(____).click();
  ```
  
  **Method-chaining**
  
  ```
  $( ).parent.( ).click( )
  ```
  
Methods return an object, which is passed along -- **Traversal**

You don't really need traversal, could just use IDs and classes, but this is neater.

The big three things you do:

1. SELECT.
2. TRAVERSAL.
3. MANIPULATION

###event.preventDefault();

Buttons were designed around 1995, when forms were a hot new deal. The defaule behavior sends off information and refreshes the page. Because of backward compatibility, can't eliminate that behavior, but you can overrule it.

