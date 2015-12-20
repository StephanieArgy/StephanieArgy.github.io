---
layout: page
title: Advanced Web Dev Tools, Week Two
permalink: /pcsnotes_c3_w2/
---

[JSON](#json)
[Command Line Tools](#commandLineTools)

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
##Command Line Tools