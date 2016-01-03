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

***

1. Put Apigee JS SDK in folder
2. Define variables. "Type" (singular) will become "collection" (plural).
3. GET to see if anything is there.
4. CREATE



<a name="styleGuides"></a>
##Style Guides

