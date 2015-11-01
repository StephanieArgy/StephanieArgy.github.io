---
layout: page
title: Primer Basic, Week Two
permalink: /pcsnotes_c1_w2/
---
##Web Foundations: Primer Basic
###Week 2

* [Agile Project Management](#agile)
* [Git Basics](#git_basics)

<a name="agile"></a>
####Agile Project Management

In this class, we follow the practices of agile project management, meaning that we make adjustments along the way, and will adjust the class to meet the needs of the people in it.

Agile projects are managed in short bursts.  Development used to be in very long cycles, but now it's in short phases -- three, four weeks. You can't get a lot of work done, but you're always able to ship something.

In an agile workflow, the whole t3eam gets together every morning and does a "stand up." We're going to do the same thing, focusing on three questions:

1. What have you accomplished *since the last class session*?
2. What are you going to accomplish *today*? (The one thing you most want to get done.)
3. What are you blocks? (What's in the way of your One Thing You Most Want to Get Done?)

<a name="git_basics"></a>
####Git Basics

#####Resources:

1. Cheatsheet for Git: [http://www.git-tower.com/blog/git-cheat-sheet/](http://www.git-tower.com/blog/git-cheat-sheet/)
2. Basic Git training at [https://training.github.com/](https://training.github.com/).
3. For a deep, advanced view of Git, there's an eBook called *Pro Git*: [GitSCM](http://git-scm.com/book/en/v2)
 
[tryGit](https://try.github.io/levels/1/challenges/1) is highly recommended as a starting point: it's a web-browser based series of tutorials and exercises.

#####THINGS NOT TO DO:

1. Don't put spaces in folder names.
2. Never go into the **.git** file.
3. **And above all, NEVER PUT A REPO INSIDE A REPO!**

Always know where you are in the file structure. To see if you're in a repository, you can use **ls -al** and make sure that there's no **.git** file, or you can use the command **git status**.  (More on that one shortly.)

#####What's Happening in Git

It can help to create a mental picture of what's happening when you're using git. This is one possible visual metaphor: 

<img alt="GitMentalImage" src="/images/GitMentalImage.jpg" width="300px">

Think of folders and files as being stuck on clear piece of mylar. All active work is being done in the **working directory.**