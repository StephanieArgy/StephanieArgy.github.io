---
layout: page
title: Advanced Web Dev Tools, Week Two
permalink: /pcsnotes_c3_w2/
---

* [JSON](#json)
* [Command Line Tools for Developers](#commandLineTools)
* [Sass Basics](#sassBasics)

Three major themes in this course:

* **Data-Driven Websites**
  * Review jQuery
  * Build HTML from data (jQuery)
  * Update data from a form
  * Local storage of data (JSON, API)
  * Ajax storage of files (Ajax)
  * Backend as a service (Apigee, Orchestrate -- This is a very competitive market)
* Custom CSS
  * CSS Preprocessors: SASS vs. LESS
  * Debug with Source Maps
  * Automatic style guides (very cutting edge)
* Tools

<a name="json"></a>
##JSON

Tonight, we'll work on JSON, referring to Duckett (Chapter 8, JSON and Ajax)

Data, NOT an object. Just a text-data structure. Not the most efficient, but it has a lot of advantages (including that it's readable by humans).

Everything is a string, even numbers.

You can next data structures:

```
"top-level" [
  {"object1": "object2"},
  {"thing1": "thing2"}
]
```

Has a JSON object built in: 

To change a JavaScript object to a string: **JSON.stringify();**

To change a string to a JavaScript object: **JSON.parse();**

An **API** is an interfact between two programs. We're going to use APIs a lot in this class. API has a set of objects, and has methods.

**UML (Unified Modeling Language)** - Name, methods, properties.

One of the APIs is web storatge API. (GMAIL used t o allow you to read mail offline; info stored locally.)

Data objecst are stored locally so that the web browser can access them.

A **cookie** is a very small data object that your website can store on soemone's computer. Very small and restricted.

WebDB -- Database, only supported by one browser. 

Left with local storage: 

* **Session** (like cookies) - Can only be accessed by domain that set the data. (Later, we'll talk about cross-domain data storage.) Session is lost as soon as the tab is closed, adn is not accessible to all open windows and tabs.
* **Local** - Local object. Stored when tab is closed; all open windows and tabs can access the data.

Going to use local for our glossary. Not perfect: can run out of room.

Going to store **key** and **value**.

1. Take object  ----  Retrieve
2. Stringify it ----  Parse
3. Store it     ---- Return

Form is a set of name/value pairs. Have to create a form (above the word list):

```
<form action="url">
  
</form>
```

To make a classical form do things, you need a Submit button. (JavaScript can respond in other ways, but we'll still  use a button.)

How to get data from form:

1. Have to create an event listener.
2. Retrieve values for the word and definition.
3. Have to save, then get dictionary.

Want to have a clean interface between the program and data structure, and only communicate via these two medthods -- setting up our own little API.

How to pull:
**localStorage.getItem('theDictionary')**

Can only store strings; have to return an object so use **JSON.parse** with JSON in lower functions, never need to change again.

**displayDictionary**

Look at Developer Tools>Resources

Can see resources in use, such as session storage and local storage. Can even edit in the debugger.

It allows you to see what is being stored.

Inefficient!

1. Recreates every time...
2. ...even words it already knows.

Store each word, not enetire dictionary; but need unique IDs.  Also, can store multipole definitions.

To work on later (on our own):

1. Store word-by-word (not entire dictionary).
2. Local caches -- Only write to server when something changes.

MORE POSSIBLE TRAINING:

Vitamin T -- Division of Acquent, a national sourcing company: **https://vitamintalent.com/learning/**

They give an entry test and have a free learning environment; if you pass the final, they'll offer you an interview.

<a name="commandLineTools"></a>
##Command Line Tools for Developers

The command line interface (CLI) is more powerful than a GUI.

1. Software is always changing.
2. Every character is a potential point of failure, an opportunity for mistakes to creep in.

You used to have to fill out a form to make any changes to software, and to "check out" drives.

###Goals/Benefits of Command Line Tools

They keep tools:

* Updated
* Organized 
* Configuration Management
  * Define/control versions (e.g. jQuery)
  * Manage change
  * Avoid surprises
  * Reduce errors
* Steamline repetitive tasks (e.g. with Yeoman)
* Automate
  * Preprocessing
  * Project scaffolding
  * Deployment preparation
  * Major/minor tasks

Some developers believe, "If I have to do it twice, I should script it."
  
Typically, in production you constrain change as the project progresses.
  
Semantic versioning - Assigning unique and meaningful version names or numbers: **x.y.z**  The "x" is a major version, and a change to that may mean that things that used to work will now break.

Some JavaScript tools for front-end development:

* Scaffolding: Yo
* Project management: Bower, npm
* Build system: Gulp, Grunt

**sudo** (SuperUser Do) - Try to avoid, in general. Bypasses all permissions; better to try and attempt as yourself.

###Package Managers

Package managers oversee files/paths, dependencies (other packages), manifests; they install scripts and run procedures. There are many different kinds, including:

* Ruby -- Package manager called **gem**.
* Homebrew is a package manager for Mac.

Two package managers are particularly important for web developers:

* [npm](https://www.npmjs.com/) (which does NOT stand for node package manager, even though many people think it does). npm is a big deal. Probably already installed on our machines.
* [bower](http://bower.io/) - Front-end package manager for components.

node.js -- JavaScript engine (i.e. a virtual machine that interprets and execute JavaScript code) and modules (small parts that combine to make one big program). Has Chrome v.8 JavaScript engine, libraries, APIs.

Tightly controlled by one company, even if it is open source. In 2014, a version was forked and became **io.js**. Made copmany behind node.js move faster, get better. In September, 2015, node.us and io.js reunited:
http://thenewstack.io/io-js-and-node-js-have-united-and-thats-a-good-thing/

For our purposes, lots of tools to install. Can use node.js or Homebrew (but not both).

**Bower** was written for node.js, but for front-end projects. Works with manifest file to install correct components. 

Homework for Wednesday:

1. Install node.js
2. Do [Command Line for Web Design](), (Parts 1-3, or more)

**Developing our tool chain.**

Next iteration:

* Better blog.
* Animal adoption agency site: Ability to add a new kitten, with storage.

____

**To give dimension to an empty div, put in &nbsp;.**

Alias is a name for a program that lives elsewhere. To make an alias using the command line: Type **ln -s** followed by the link location, then the link name.

```
ln -s foo.txt bar
(Makes a soft link called "bar" that points to foo.txt)
```

(To learn more about making links from the command line, type **man ln** to open that page in the command-line manual.)

<a name="sassBasics"></a>
##Sass Basics

Some of the features that Sass allows:

1. Nesting
2. Variables (**@name: value;**)
3. Mix-ins - (**@mixin mixinName{*Contents of mixin*}**), then to call the mixin: **@include mixinName;**
4. Partials: Separate files for colors, varabiles, sizes globals, mixins, reset, etc. Start with an underscore: **_colors**. To bring in another style sheet: **@import ____"**
5. Sass libraries: Compass, Bourbon
6. Operators (mathematical, color, etc.)
7. Control directives and expressions (@if, @each, etc.) (@if condition { *Then this code happens* })

Lots more. Documentation [here](http://sass-lang.com/guide).
Also, tutorials at [The Sass Way](http://thesassway.com/).

###Command Line Tools > Package Managers > Preprocessors

We start with HTML and CSS, because that's how browsers speak. 

As we've seen with JavaScript, it's nice to have variables. We can't add those to HTML or CSS (because they have to maintain backward compatibility), so we have to make a new language that lets us work with variables, then converts those to something that any browser can unedertsand. That's what a preprocessor does.

JAVASCRIPT PREPROCESSORS
TypeScript -- JavaScript preprocessor that's more strongly typed.
CoffeeScript -- Simpler JavaScript

CSS PREPROCESSORS
Stylus -- Some people think it's even better than Sass, but it's not as popular, well-document or desireable for potential employees. 
Sass -- The canonical version of Sass was originally built in Ruby; we use a version built in node (ported from the Ruby version).

HTML PREPROCESSORS
Jade -- In the tutorial that we'll use.
Haml -- Very popular

Online, there are converters:
HTML > Haml: http://htmltohaml.com/
CSS > Sass: http://sebastianpontow.de/css2compass/

Source Maps are a way of debugging preprocessors: http://webdesign.tutsplus.com/tutorials/how-to-use-source-maps-for-better-preprocessor-debugging--cms-22735

###Prefixers

Many newer CSS features require vendor prefixes to work on different browsers. The prefixes eventually become superfluous as features become more widely accepted. Tools can handle the prefixes for you. **The tool knows more than you do.**

