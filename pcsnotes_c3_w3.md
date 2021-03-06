---
layout: page
title: Advanced Web Dev Tools, Week Three
permalink: /pcsnotes_c3_w3/
---

* [Yeoman](#yeoman)
* [Testing](#testing)
* [User Stories](#userStories)
* [Selenium](#selenium)
* [Ajax](#ajax)

This week (Week Three), things will start going faster. Going to transfer kitten site.

On Wednesday:

1. Browser-based test automation
2. Selenium
3. IDE - Integrated Development Environment

Nex week, we have Monday off, but we'll have class on Wednesday and Friday.

<a name="yeoman"></a>
##Scaffolding with Yeoman (and friends)(by Jaime Panaia)

Going to build a web app using the Yeoman scaffolding. What we'll do:

1. Scaffold an app using only a few commands for Yeoman.
2. Use Grunt to customize tasks (live reloads)
3. Customize a Sass file.

**Yeoman: [http://yeoman.io/](http://yeoman.io/)

Doesn't work on its own.  Need:

1. **yo webapp** -- Command to create a new web app.
2. bower search, bower install (to handle dependencies)
3. grunt serve, grunt test -- To preview, test and build.

To install yo, bower and grunt: **$ npm install -g yo bower grunt -cli**

(May need to use sudo to get them to install.)

Make a new directory and go into it:

```
mkdir aaa-yo
cd aaa-yo
```

Once inside the new directory, install web-app generator:

```
$npm install -g generator-webapp
```

(The "-g" makes this global, so you shouldn't have to do this again.)

To start a new web app (still inside the new directory):

```
yo webapp
```

(Choose Bootstrap, Sass, Modernizr, the libsass(y). This will download a ton of files.)

To make grunt watch (and launch the scaffolding):

```
$grunt serve
```

(This will open localhost:9000 - "Allo, Allo!". On command line, will see "Running watch task...waiting...")

Keep that browser window open, open Terminal and your text editor, so that you have multiple pages open:

1. The terminal (for command-line work)
2. The text editor
3. The browser

All of the relevant files are inside the **app** folder, which is the parent directory for the web application.

Important commands:

* **yo webapp** (Generate the app)
* **grunt serve** (Preview the app)
* **grunt test** (Run unit tests on app)
* **grunt** (Build optimized, production-ready version of your app)

Bower components: JavaScript, web dependences, installed by Bower.

gruntfile.js, package.json -- Back-end related dependencies.

gruntfile.js -- Where the watch function comes in.

In our kitten site, we could create branch, use the merge tool. In professional environment, would do this on branches, not in a new repository. (With a project with a lot of history, a new repo would lose all that.)

On Wednesday, we'll be playing wiht Selenium. Do the Treehouse course on Ajax.

Goals for both the glossary and kitten sites: 

* Build list from data.
* Add to list from form.
* Initialize list from defaults.
* Save list to local storage.
* Save list to server (Have to do this next week. Uses Ajax; will learn Ajax and Apigee (server) a week from Wednesday.)

Form > Update > List (Store > Server > Retrieve) > Display > Screen.

**Regression error** -- "Regression" means to go backward, so a regression error is when something that used to work breaks.  (In other words, when making changes, make sure that eveyrthing that used to work still does.)

Test structure: Put data into forom, make sure it works with new features. Get ready to do this in teh context of the glossary, then try it in the kitten app. 

1. Tool chain.
2. Sass
3. Internal system.

Going to build a toy.

"Feature creep" -- Impulse to build possible extra features that may or may not be necessary in the future.

***

Important to use Git, so that you can preserve as much data as possible. You're creating intellectual capital.  **Everyone line of code you create is someone else's property: Your client, or your company, or your future self.**

<a name="testing"></a>
##Testing

* Testing in general: why, how, types.
* Selenium as a tool
* Glossary as a test.  (Will set up a testing environment for the blog and for the kitten site.)

Preconditions for system under test:

1. Stimulus
2. Expected results
3. Actual results

Have to clearly define the stimulus and expected results.

* Verification: Making sure the system does what it's supposed to. (Really hard)
* Validation: Making sure you're building what the client wants. (Almost impossible)

"The market is a conversation."  If people don't buy your product, it isn't working.

Every language uas unit testing frameworks.

Types of tests:

1. Acceptance -- What does the customer want? 
2. Load - Acceptance test run in widespread way
3. Platform - Acceptance test on multiple devices
4. Integration
5. Unit
6. Regression

We're going to focus on accptance testing.

In a well-tested system, it can take days to run one of these tests. Testing is a big deal. There are companies that do platform testing.

<a name="userStories"></a>
##User Stories

What is the system supposed to do?

* Wireframes and mockups
* User stories -- Behavior of site (functionality)
* Scenarios
* Requirements
  * Performance -- How fast, how many users
  * Reliability -- How frequently can it fail? How does it recover?
  * Profitability -- How much does it cost to run?
  * Operability -- Who runs it?

User stories: How the system provides **relevant value to specific user populations.**

###User Story Format:

* **In order to (goal)**
* **As a (role)**
* **I want to (system feature)**

Customers don't give a rat's ass about your website; they care about their goal.

Different users have different roles (And therefore different goals) for the site. So which user/role are we talking about?  If you have a lot of user stories, you're not focused enough.

Each story has one more more scenarios (steps user takes to obtain value):

1. Precondition (e.g. be logged in)
2. Steps
3. Observable result

Feature (description) - In order to get value, explicit system action: "I want to gain some outcome that furthers the goal."

Scenarios written in [Gherkin](https://github.com/cucumber/cucumber/wiki/Gherkin), a language that can be interprested by testing frameworks like [Cucumber](https://cucumber.io/), [Behat](http://docs.behat.org/en/v2.5/), etc.

Steps must be thought of in terms of web development. Customer > > > DOM

Buest user experience comes from connecting with customer goals. Hard! Boog to automate...therefore,  Selenium...

<a name="selenium"></a>
##Selenium
[http://www.seleniumhq.org/](http://www.seleniumhq.org/)

Selenium tools -- all open source:

1. Automates a real web browser via JavaScript to test full stack. But really slow.
2. [WebDriver API](http://www.seleniumhq.org/projects/webdriver/), can write code to translate to selenium to drive browser.
3. [Selenium IDE](http://www.seleniumhq.org/download/) - Works only in Firebox and records actions. (Will play with this tonight.)
4. [Selenium Server](http://www.seleniumhq.org/download/) - Can do parallel tests and load testing.

[Sauce Labs](https://saucelabs.com/) - Will let you run free tests and hook it to GitHub, so that it tests site every time you commit.

Going to use version of tlosarry tool:

1. Find target system: [http://auraelius.github.io/glossary/](http://auraelius.github.io/glossary/)
2. Write simple user story.
3. Write a scenario for storing a word.

User story: 

* **In order to (look up a word)**
* **As a (student)**
* **I want to (add a word)**

Preconditions: Have to be on the webpage.

When I: 

1. Focus on the new word box...
2. Type a word...
3. Focus on the definition box...
4. Type a definition...
5. Click on "Add word to dictionary" button...

Result: 

1. I see new word.
2. I see definition.

In Selenium IDE: 

1. Add **base** URL to top.
2. Toolbar underneath: Most important button is big red record button; activate that to record all the actions.
3. Name the test, replay as necessary.

To run test, in Command: **verifyText**.

Use this to test own glossary, then kitten site.

Selenium results stored a table in an HTML document. All text. Store tests in repo: Make a **tests/selenium** folder.

###Grow your tests

For every scenario, have: 

1. Happy path
2. Error paths.

Bugs:

1. Reproduce bug in Selenium IDE to expose the bug.
2. Write/verify steps of way it should go.
3. Code until it passes. (The can use test in regression tests.)

For help with Selenium IDE, go [here](http://www.seleniumhq.org/docs/02_selenium_ide.jsp).

<a name="ajax"></a>
##Ajax

(Refer to Duckett, Chapter 8)

http has some simple verbs: GET and POST.

Usually when you do a GET, the browser replaces the entire page. It takes a long time to get info and re-render page. 

Create an object:

xhr

* HTTP verb, URL, query string.
* Attach function (){process data from server, manipulate data, modify DOM}

The process:

1. Make object.
2. Define request.
3. Define response.
4. Make request....wait for response...
5. Function runs.

**Ajax lets you add data without refreshing the page. You use jQuery to do this.**

Main problem -- Don't know when it's going to come back. Have to give poeple something so that they don't get bored while waiting for the information/modification.

API is **XMLHttpRequest**

```
//Start by creating and sending the request
var xhr = new XMLHttpRequest;
xhr.open('GET', 'data/test.json', true);
xhr.send;

//When the response arrives from the server, the function will run.
xhr.onload = function (){
  if(xhr.status === 200) {
    //Process response
  }
}

```

(Good idea to check if the data is okay.)

Simplest approach is to have a div for the resopnse text. The DOM will know to re-render only that part of the page.

XML looks like HTML, but tags contain different words.  XML is less error-pr9one than JSON, but JSON is easier to work with. Ned to write JavaSCript or use libraries to translate responses.

###JSON-P (or JSONP) ("JSON with Padding")

For security reasons, browsers don't load Ajax responses from other domains ("cross-domain requests") -- Google, Weather, etc.)  One work-around is to JSONP. Involves adding a script element to the page, because there are no restuctions on the source of a script in a script element.

jQuery does things to make this all easy.

Works on selector: .load()

```
$('#text').onload('ajax.html #test');
```

Methods also have alternatives for failures.

* **url** - Where data comes from
* **data** - Info that comes from the server
* **callback** - Function that is called when the data is returned
* **type** - Type of data to expect

