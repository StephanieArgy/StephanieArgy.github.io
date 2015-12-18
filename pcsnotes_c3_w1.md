---
layout: page
title: Advanced Web Dev Tools, Week One
permalink: /pcsnotes_c3_w1/
---

* [Class Agenda](#classAgenda)
* [jQuery](#jQuery)
* [Chrome Developer Tools](#chromeDevTools)
* [Glossary Assignment](#glossaryAssignment)

<a name="classAgenda"></a>
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

> Basic syntax is: **$(selector).action()**
>
>* A $ sign to define/access jQuery
>* A (selector) to "query (or find)" HTML elements
>* A jQuery action() to be performed on the element(s)

**$** - Shorthand for "jQuery," opens the library.

jQuery can be used to get info:

* **.html()** - Gets the content of the selected item, including its markup (but only from the first element).
* **.text()** - Gets text ONLY (no markup, so it ignores HTML tags and spacing).

###Setting Content

Can put text in brackets, to change content.

Pseudo-selectors
Pseudo-elements

###Chaining

.method().method(); (etc.)

###Prepend()/Append() vs. .before()/.after()

Prepend(append) inserts content at the beginning (end) of the selected element (but inside of it).
Before (after) insert content before (after) the matched element (and outside of it).
Demo [here](http://jsfiddle.net/xtb51wed/)

###Events

Goodle "MDN events." There are LOTS!

This kind of programming is called "event-driven programming." We set up functions that run when events happen.  (e.g. when user clicks on something, something happens.)

###Traversing the DOM

Can use .next() or .prev()

```
console.log($('white').prev().html());
```

Here, jQuery will take the element BEFORE the one that has the calass of **white**, and feed that element into the .html() method.

Other methods:
[.find()](https://api.jquery.com/find/)
[.not()](https://api.jquery.com/not/)

When you're debugging jQuery, it acts like an element, but it's not. It's a jQuery obj3ect that's a representation of an element.  You're actually manipulating a very complex model. There are a lot of similarities between jQuery objects and the DOM.

```
$(document).ready(function () {
});
```
"document" = the Document Object Model (DOM)
".ready means it's fully loaded.

View Dev Tools > Network tab > Disable cache > Reload.

***

<a name="chromeDevTools"></a>
##Chrome Developer Tools

Can set a **break point**. Pauses the execution of the script so that you can examine what's happening at that point. Two types: 

* Manual - Pause script execution at a specific line of code.
* Conditional - Pause script execution when a specified condition is met.

Google info on breakpoints [here](https://developers.google.com/web/tools/chrome-devtools/debug/breakpoints/add-breakpoints?hl=en).

**Scope** - Variables inside a function don't exist outside that variable; **global** variables can exist anywhere.
When defined inside a function:

```
var name [Makes a local functin that will only exist inside that function.]
name [Makes a global function]
```

Also, learn to use **stepping**:
[https://developers.google.com/web/tools/chrome-devtools/debug/breakpoints/step-code?hl=en](https://developers.google.com/web/tools/chrome-devtools/debug/breakpoints/step-code?hl=en)

Can watch an expression, e.g. **$wordList**.

If you look inside jQuery objects, you can see what's going on. 

If you're interested in working your way down the [**call stacks**](https://developer.chrome.com/devtools/docs/javascript-debugging).

<a name="glossaryAssignment"></a>
##Glossary assignment:

Housed on this [repo](https://github.com/Auraelius/glossary), full version of jQuery available [here](https://github.com/Auraelius/glossary/commit/9f534d51d9af046a3248527393db73350555dac0).

```
 <aside>
      <h3>Glossary</h3>
      <p>Knowing the vocabulary terms of web development is required. Here are a few I've picked up along the way.</p>
      <dl>
        <dt>Foo</dt>
        <dd>A throw-away word that people seem to use everywhere. It means whatever people need it to mean at that particular usage.</dd>
        <dt>Bar</dt>
        <dd>See "Foo"</dd>
      </dl>
  </aside>
```

dl= "dictionary list"
dt, dd -- Not used much anymore, but good.


```
var d = initDictionary();
```

Iterators:

You may have no idea how many items you're going to add, so you use a type of array with the form **.each(array, callback)**.  Succinct way of interating.

```
$.each(d, function (index, entry) {
  $worldList.append("<dt>" + entry.word</dt>)
})
```

For each "each," runs function, returns "entry," then runs the script in the brackets.

***

How to add a glossary:

In personal blog, start buliding a glossary of terms. Will store in the DOM (which will forget it), then in the browser (which will remember it till the cache is flushed), then a database (later).

**kittons.json**
Kitten database: name, age, imageURL, description.
Process: Pulling database of information.

*Treehouse: Interactive Websites* gives a lot of jQuery in context.

Soon...**yeoman.io** - Web app generator.

Going to go deeper into development tools later on.

Bootstrap is a quick way to throw something together.

Different techniques for pair programming remotely, including Skype. (Person who's driving can share their screen remotely.)

In early 2000, had outsourced a lot of work to India, but after 9/11, couldn't fly. Got good at rworking remotely. Good to start in person, then go remote.

Next iteration, will have different partners.

Online tutoral: Setting up tools environments:
[http://webdesign.tutsplus.com/series/the-command-line-for-web-design--cms-777](http://webdesign.tutsplus.com/series/the-command-line-for-web-design--cms-777)

Tools that know how you work, so they reduce errors.

* Grunt -- Biggest for JavaScript (so there's a lot of documentation)
* Gulp -- Newer, with a different syntax. (Very JavaScriptish).

As developer, will constantly upgrade one's tools.

Monday: Will start with overview and show-and-tell of project so far, then more work. This iteration of the project will be due next Wednesday.