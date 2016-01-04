---
layout: page
title: Advanced Web Dev Tools, Week Four
permalink: /pcsnotes_c3_w4/
---

* [More Command Line details](#commandLineDetails)
* [Backend as a Service](#BaaS)
* [Style Guides](styleGuides)

<a name="commandLineDetails"></a>
##Command Line Details

(These are very random and I need to learn more about the command line to really understand my notes.)

$ cd
$ pwd
$ ls -al

.bashrc

Aliases
Bash command shortcuts

```
alias glo = 'git log --graph --oneline --decorate --tags
```

Environment variable called PATH

```
export PATH = $PATH:/Applications/Postgres.app/Contents/Versions/9.3/bin
```

Makes computer follow that path. Can force it into another path:

```
export PATH = "/usr/local/bin:$PATH"
```

###Ruby on Rails stuff

(Can store keys for API's etc. 

[Mandrill](http://blog.mandrill.com/) gives you "whitelisting" for MailChimp: spammer's dream.

Node Version Manager

```
function parse_git_branch {
  git branch --no-color 2>dev/null (etc. -- INCOMPLETE)
}
```

PS1 = "${TITLE}" (Can change to put in other details, such as date, user, machine, path)


<a name="BaaS"></a>
##Backend as a Service

* The Why of Servers
* Architecture and components
* Installfest
* Simple verification of functionality
* Refactor glossary and kitten site

Old mode was "star topology." Now, it's a mesh topology, like Bit Torrent.

  <figure><img src="../images/Star_Topology.png" class="starTopology">
    <figcaption>Star Topology</figcaption>
  </figure>
  
  <figure><img src="../images/454px-True_Mesh_Diagram.svg.png" class="meshTopology">
    <figcaption>Mesh Topology</figcaption>
  </figure>
  
[**Onion Router**](http://www.onion-router.net/) - If a machine has forbidden info in "star," everyone knows th3e path. Onion sends you through a randonm series of machines.
  
Can get involved in effort to mask peoples traffic. Now, the FBI and NSA will investitage ayone running of of these.  Use for **anonymization and encryption**.

###Why do servers exist?

* Provide services: Too much for a phone or a laptop.
* To shar amoung many people -- information, calculation, authentication, persistance (storage), printing, fabrication (at edge of 3D printing revolution)

User of servers to track identity, likle FBI, etc.: [OAuth](http://oauth.net/).

###DIY vs. BUY

* DIY - Flexible, requires development time and backend talent; lower cost.
* BUY - Predesigned but customizable, requires learning time, subscription fees. (Works for what most people need).

If you're running your business correctly, every time data flows, you're getting paid.

###BaaS

A lot of companies are competing to provide server needs.

* [parse.com](http://parse.com/) is very popular.
* [Apigee](http://apigee.com/about/)
* And for others, look up "mobile backend as a service on Wikipedia.

Example of companies going after things that people want/need. Own server can fail under too much traffic. If you have a hit app, and its use spikes in the first 30 minutes of its first day, you have to be ready, with everything working. 

Process:

1. Sign up for service.
2. Install SDK.
3. Integrate SDK into app.

How to use APIs: [Code Academy](https://www.codecademy.com/) has mini-courses (though the one on Apigee is a little out of date.)

REST APIs: URLS are nouns.

Only about ten years old.

[Entity](http://docs.apigee.com/app-services/content/creating-custom-data-entities) -- Anything that can be stored; each one gest a [**universally unique UD (UUID)**](https://en.wikipedia.org/wiki/Universally_unique_identifier). (Lots of people write their own UUIDs.)

The verb comes from HHTP:

* POST - Create write a new word.
* GET - read existing
* PUT - Update
* DELETE

Simple but the things you can do with it are complex. Lots of palaver and marketing around it.

Apigee offers various language APIs. All functionality is abstracted and encapsulated in an object.

```
var options;
var client = new Usergrid.Client(options, function(){....});
client.createEntity(options, funciton(){...});
client.getEntity(options, function(){....});
```

Once you have an Apiggee.com account, click the second box: Build Sandbox is open to anyone; only use it for class work, not real work.

We'll use: 

1. Sandbox
2. Data

(Tap right, can get all the SDKs.)

Typically, storage of images and media is different than for data.

Glossary:
Create entity: use array of all glossary words.

**update: Entity.save();**

1. Create.
2. Get.
3. Entity save

More steps:

1. Put Apigee JS SDK in folder
2. Define variables. "Type" (singular) will become "collection" (plural).
3. GET to see if anything is there.
4. CREATE

***

We were going to extend the glossary, but we still didn't have a handle on the technique.  This is the current version -- event-driven programming:

Form with BUTTON

&#11015;

(EVENT)

&#11015;

Reads form, sets dictionary variable

&#11015;

Var -- CALLS (**Up till now, this has been in local, synchronous behavior**)

&#11015;

Update DOM

***

What we're aiming for is for there to be a **document.ready event** that sets up the event handlers. The dictionary is displayed -- but when does it it exist?

Button CLICK event > Updates the local dictionary (var) > Dictionary is stored on server > document.ready event > Display dictionary/update DOM.

**THE PROBLEM: Have local var that represents the dictionary. It receives input from the form, outputs updated version to the DOM. But because the exchange processes from the server are now asynchronous, they could get out of whack.**

Mutex Lock -- Can put a hold on the variable for one process. [Thread Synchronization](https://developer.mozilla.org/en-US/docs/Mozilla/Projects/NSPR/Reference/Introduction_to_NSPR#NSPR_Thread_Synchronization)

Two-way data-binding -- One of the things that's supposed to be so great about angular.js.

<a name="styleGuides"></a>
##Style Guides

[Slides.com Overview](http://slides.com/auraelius/style-guides-11#/)

Five different kinds of style guides:

1. Content/editorial
2. Branding/identity
3. Development style giude and coding
4. Human interface
5. Front end

(In slide.com presentation, there are links to examples of style guides.) Google's style guide is a mix of front-end and code.

Patterns are similar to style guides: http://ui-patterns.com/patterns.  "Recurring solutions that solve common design problems."

Automated style reader: stylifyme.com.  (Type in a website, and it'll generate a simple, limited style guide.)

Quick, easy static style guide: http://www.poormansstyleguide.com/  (Provides HTML, to which styles can then be applied. Will show all sorts of features. Inventories styles for elements, lets you see your styles applied. Black-and-white text only.  To see colors applied...)


```
HTML:
<h1 id="colors">Colors</h1>
<div class="row">
  <div class="color-swatch one"> (Etc.)
    (Label underneath)
  </div>
</div>

SCSS:
color-swatch {
  width: 100px;
  height: 100px;
}

.one {
  background-color: $colorVariableOne;
}
```

Repeat for as many swatches as necessary.

This is NOT a dynamic style guide. 

Do do a live style guide (untested method):

1. Install Yeoman.
2. Install **generator-styleguide** (Full directions [here](https://www.npmjs.com/package/generator-styleguide))

To start a styleguide project, you will have to install Yeoman and Hologram globally.

### install Yeoman

```
$ npm install -g yo
```

### Install Hologram

```
$ gem install hologram
```

(You might have to install the Hologram gem with sudo, depending on your permissions.)

To install generator-styleguide from npm, run:

```
$ npm install -g generator-styleguide
```

Finally, initiate the generator:

```
$ yo styleguide
```

### To create a new component:

```
$ yo styleguide:component
```

Other options:

* [Barebones](http://barebones.paulrobertlloyd.com/)
* [Pattern Primer](http://patternprimer.adactio.com/)
* Lots more [here](http://alistapart.com/blog/post/style-guide-generator-roundup)

Another option is to make "style tiles," as described by [Samantha Toy Warren](http://samanthatoy.com/style-tiles/).

Clients will resist style guides, but if you dive right into CSS, you'll make a mess.

***

"Literate programming" - [Donald Knuth](http://www-cs-faculty.stanford.edu/~uno/). Write for the person reading the code; sprinkle comments throughout the code so that it makes sense.

Most of the time these days, front-end code comes from the server you'er workingon.

"Callback hell" -- You have no idea wher eyou are.

```
$().ready(function(){
  initDictionary() 
    callback() // one exists
      getDictionary()
        callback() //I have data
          (Update DOM)
});
```

When talking to a server, have to update the DOM when data is ready. Someone is leaving breakcrumbs; will go back to callback when data arrives.

Process here:

1. Runs init, looks for entity. If it exists, it runs and gets Dictionary.
2. GetDictionary - Calls dictionary and objects with words.

Add word: PUT.

**POST is create; PUT is update.**

The thing that took the most time was not knowing where the server was. The next step: relational data between new entries.

Technique to pass in callback: 

```
function functionName (callback){
  //callback code
}
```

Can display data in two different places because of the passed-in "callback." (Front page displays three latest terms.)

To conclude on Apigee: their JavaScript SDK is clunky. Hope other SDKs are easier to use.

[PianoPushPlay](http://www.pianopushplay.com/55837358e4b0fdbf809290a4/): Was a PCS capstone project.
