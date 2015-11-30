---
layout: page
title: Primer Pro, Week Three
permalink: /pcsnotes_c2_w3/
---

[HTML Only](#htmlOnly)
[Bootstrap](#bootstrap)

<a name="htmlOnly"></a>
##HTML Only

The next assignment is even more freeform, but with specific technologies. We're going to introduce Bootstrap.  (Good idea to watch Treehouse>Framework Basics).

[**git stash**](https://git-scm.com/docs/git-stash) - Puts changes into a side box: records the current state of the working directory and the index, but lets you go back to a clean working directory.

**IMPORTANT NOTE: DO NOT START FILE NAMES WITH AN UNDERSCORE FOR GITHUB! This broke my site so it wasn't publicly viewable.**

###Strategies for sliding menu:

Have all content in section, float **nav** off to the side (by margin or position).

Think of design of interaction first.

1. Spec
2. Steps
3. Technology

Take control of the nav div.

* Title
* Logo
* Nav
* CONTENT

There's a risk with Googling code you don't understand -- like a pianist who can't play whas she hears.  Designs will end up looking like code you can borrow.

####Start by paper prototyping:

1. What boxes do I have and how should they move?
2. Think about animation.
3. BoxeS: State, styling.

**JavaScript** just swaps out one element or state for another.**

####Keep a clean desk.

Make sure that code is neat, and also check every few minutes that editor can udnerstand it (indentation, etc.)  "Put away your tools," so that your workbench is how you want to see it when you come back.  Be a little reflective: "Is this the best my code could look?"

####Typos

Our primary medium is text. It's so hard to see what's happening.

1. Have someone else look at it, because they may be able to see what you've missed.
2. Run it through a LINT:
  * [HTML](https://validator.w3.org/)
  * [CSS](http://jigsaw.w3.org/css-validator/)
  * [JavaScript](http://eslint.org/)

(There are lots of other linters available. Running your code through a linter won't solve problems but will give you a place to start looking for what's wrong.)

<a name="bootstrap"></a>
##Bootstrap

