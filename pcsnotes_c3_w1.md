---
layout: page
title: Advanced Web Dev Tools, Week One
permalink: /pcsnotes_c3_w1/
---

* [jQuery](#jQuery)

##Agenda:

Introductions
Syllabus (and adapations)
Skill Set
Assignment
Textbook (Duckett)

Syllabus is [here](http://portlandcodeschool.github.io/afe/).

Expect to work two hours at home for every hour in class -- 18 hours total work (class + homework) per week.

In each class, will talk about things in a simple way.

Will do pair programming.

Two tracks of assignments:

1. Personal blog
2. Work for "client"

(Side note: Arcade Fire music video made in HTML5 and JavaScript: http://www.justareflektor.com/)

Client Goals --- USER GOALS --- Developer Goals

In this class, too, we're developing skills in four areas:

1. Technology
2. Tools
3. Team
4. Technique

Learning Objective: Observable skill in each area.  Some are specific to a goal, some not. Because this is a class, some of these are already defined.)

**Mainly CSS and JavaScript.**
Not going to cover HTML any more deeply than we already have (Except HTML forms.) 

Topics to be covered: 

* Going to use callbacks (and learn the difference between a "callback and a "promise.") 
* Asynchronous JavaScript (AJAX). Something set up, but that you don't know when it's going to run.
* Chrome Dev Tools, also Firebug and Selenium (to test websites by recording clicks, actions, etc.).
* Task automation
  * For example, Autoprefixer to automatically apply browser-specific CSS prefixes.

By next class:

* Review the syllabus
* Talk to Al by Slack or email about our own personal goals for this class.
* Start our blog.
* SET CRITERIA FOR EACH ASSIGNMENT.

Syllabus, resources, etc. can be found [here](https://github.com/portlandcodeschool/afe).

On Slack, **@channel** or **@group** will send to everyone. Can also send individual messages.

Vocabulary:

```
<ul>
  ....
</ul>
```

**ul** is the tag name.
**\</ul>** is the tag.
The tags and the space in between is the **container**.
The tags and the content within are the **element**.

What affects which CSS rules predominate?

* Proximity -- inline **style** is closer than a **style** block at the top of the HTML page, which is more specific than a separate style sheet. The closer something is, the more dominant it is.
* Specificity -- An **id** is more specific than a **class**, which is more specific than an element.

**CODE EVERY DAY.  It's crucial for us to identify our own gaps and address them.**

Assignments for this course: 

1. Blog
  * Make responsive.
  * Post weekly article.
  * Will add a To Do list. (Can start now.)
  * Will build up up a glossary. (Can start now.)
2. Client site
  * For animal adoption agency.
  
  We'll do the animal adoption site in phrases. In the first phase:
  
  1. Statuc site: One page.
  2. Carousel of animal images.
  3. List of adoptable kittens.
  
  Technical requirements for this phase:
  
  1. Bootstrap. (No customization.)
  2. CReate list from a JSON array of objects.
  
  This class is about data-driven sites. Going to generate content via JavaScript.
  
  **JavaScript Objects** remember things.  Animal properties might be:
  
  1. Species
  2. Age
  3. Breed
  4. Gender
  5. Size
  6. Weight
  7. Color
  8. Description
  9. Image URL
  
**Build what you need, add more later.**

Going to work project up into increasing complexity. Every character, every line of code is a point of failure. The more code you have, the less reliable it is.

Pair programming: Intense form of collaboration.

There are different models for pair programming. Think of it is a road rally, with a driver (focusing on staying on the road) and a navigator (focusing on winning the race). The Driver has hands on the keyboard; the Navigator does the strategic work.

Benefits:

* Two pairs of eyes.
* Two people learn the code at the same time.

(Some shops do solo coding, followed by code walk-throughs, so that everyone becomes familiar with the code.)

Cultivate a dual state: working AND observing the process.

***

<a name="jQuery"></a>
##jQuery

jQuery is a library written in JavaScript. It is used to select elements and then do things with those.

From w3schools tutorial:

<blockquote>
 Basic syntax is: **$(selector).action()**

    * A $ sign to define/access jQuery
    * A (selector) to "query (or find)" HTML elements
    * A jQuery action() to be performed on the element(s)
 
</blockquote>

**$** - Shorthand for "jQuery," opens the library.

jQuery can be used to get info:

* **.html()** - Gets the content of the selected item, including its markup (but only from the **first** element).
* **.text()** - Gets text ONLY (no markup, so it ignores HTML tags and spacing).