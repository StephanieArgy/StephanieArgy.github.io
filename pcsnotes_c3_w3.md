---
layout: page
title: Advanced Web Dev Tools, Week Three
permalink: /pcsnotes_c3_w3/
---

This week (Week Three), things will start going faster. Going to transfer kitten site.

On Wednesday:

1. Browser-based test automation
2. Selenium
3. IDE - Integrated Development Environment

Nex week, we have Monday off, but we'll have class on Wednesday and Friday.

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

All of the relevant files are inside the **app** folder, which is the aprent director for the web application.

Important commands:

* yo webapp (Generate the app)
* grunt serve (Preview the app)
* grunt test (Run unit tests on app)
* grunt (Guild optimized, production-ready version of your app)

Bower components: JAvaScript, web dependences, installed by Bower.

