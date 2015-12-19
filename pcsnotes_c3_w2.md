---
layout: page
title: Advanced Web Dev Tools, Week Two
permalink: /pcsnotes_c3_w2/
---

[JSON](#json")

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

Form is a set of name/value pairs.




