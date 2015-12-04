---
layout: page
title: Primer Pro, Week Three
permalink: /pcsnotes_c2_w3/
---

[HTML Only](#htmlOnly)
[Bootstrap](#bootstrap)
[Immersion Classes](#immersion)
[More Bootstrap](#moreBootstrap)

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

Every browser has a CSS interpreter and a JavaScript engine.

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

Boostrap is a front-end framework developed by Twitter years and years ago. It's one of the older, but necesssary better frameworks.

To start using it, go to: **getbootstrap.com**

Advantages:

* It allows mobile first design with minimal effort.
* It embodies UI principles that most people find attractive.
* Using Bootstrap, you can get close to what professionals are using. 

The trade-off is you have to learn to use someone else's code, and read the documentation on it. It's a different skillset, but also important.

You also have to learn to plan.

###Elements of Bootstrap

####1. Layouts

Bootstrap has four built-in breakpoints, which will automatically crush to a single column on mobile devices.

####2. Grids

Bootstrap uses a grid system based on 12 columns. This means that we have to think in terms of a new unit of measurement: columns. There's also a **.row** class.  **With Bootstrap, we have to include rows and columns as classes.

####3. Components

These are things you see in every app, like an app with a nav bar. To learn how to use components (or any other part of Bootstrap, go that particular part of the documentation. Just as much work as doing your own coding.)

###For our next assignment:

1. Use the Bootstrap default theme.
2. Single page, scrolling, responsive site.
3. Sticky navbar and fixed footer.
4. Bootstrap Carousel plug-in.

We will have a week to do this assignment. End up with something you'd be proud to show.

***

Ways of moving nav divs out of the way:

* z-index
* off-canvas

<a name="immersion"></a>
##Immersion Classes

(Perhaps irrelevant, since PCS has closed -- and yet there's great info here on how the classes were structured, what they covered, and the philosophy behind them.)

Immersion classes -- 13 weeks long, exercise heavy. (6-8 hours each day).

What should people know coming in? **COMMAND LINE.**

Course builds up to capstone projects. In the past, those have included:

* Photo-sharing app.
* Runkeeper-style app ("Treksmith").
* Map game.

In programming, and especially JavaScript, people have similar problems. Frameworks (React, Angular, Backbone, etc.) solve clusters of problems quickly, but each one has a different paradigm.

Had guest speakers.  Most people who finish the course end up in junior developer roles ($40,000-$50,000/year).

The course is taught as if people have never programmed before.

End up with:

* How to build a website.
* Databases.
* Core JS, jQuery, Angular, Express.

In the job market, will be competing with recent computer science grads who don't have soft skills. Also, computer science can be about theory over practicality.

Buildings things with software is still a craft; too early to think of as engineering and coding.

Hard to test mobile apps.  "Behavior driven design." Testing for mobile is a nightmare: some companies pare it down, only support a few browsers and devices.

JavaScript has a vast array of possibilities; it's a very popular language.

Unity is a game library programmed in JavaScript.

###Disadvantages of JavaScript

* Kind of a mess; no one really sat down and designed for tis first ten years.
* Callbacks -- Unlilke any other language, so it's therefore harder to learn. ("Callback" is restoration of elements to their original state.)

The computer industry is fashion-oriented, and right now JavaScript is trendy. Don't really have a choice right how: you need to learn JavaScript. Lots of r3esources to get better -- for instance, a great node group here in Portland.  Can't think of any other language I would recommend right now.  All of the jobs/money involve JavaScript. 

"JavaScript is a horrible language that you fix with more HTML."

Python: A lot of scientists and third-graders use it.

Trend of last ten years has been **dynamic programming.**

Would be cool if JavaScript could leverage media queiries, but it can't. (Bootstrap takes care of that, though.)

**if(window-width>320px))...**

(Have to make sure JavaScript window and media queries are set the same.

**Can only have one set of navigation.**

###Final project: 

Could also do another JAvaScript project.  Choices:

1. JavaScript project
2. Bootstrap project of own design. (Very well-defined.)

Define self-assigned requirements for project in the GitHub readme.md.  Do some scribble wireframes. Build to that spec.

<a name="moreBootstrap"></a>
##More Bootstrap

**getbootstrap.com**

For this assignment, don't want to have to customize, so look for a design appropriate for this project. (This will look like eveyr other Bootstrap site.)

Would love to see a sticky header, sticky footer and fixed nav.  Get familiar with Bootstrap documentation. Also, look at Bootstrap's components for inspiration (though that's really a solution chasing a problem).

To use Bootstrap CDN, you need links to CSS and to JavaScript and jQuery.

In Codepen, use "Latest version of JS/JQ," paste in the URL frojm Bootstrap.