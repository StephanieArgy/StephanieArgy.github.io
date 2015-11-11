---
layout: page
title: Primer Basic, Week Three
permalink: /pcsnotes_c1_w3/
---
##Web Foundations: Primer Basic
###Week 3

* [Collaborating Using Git](#git_collaboration)




Going to do teamwork tonight.  Tonight's assignments:

1. Chrome Developer Tools Scavenger Hunt
2. Journal (ongoing)
3. Start of a website for a client.

Normally, when you interact with a client, they specify what they want. From their guidelines, you create a **client brief**, and then a **wireframe.**  And so, we're going to take a client brief and wireframe and code them up.

Because we'll be working as teams, we have to figure out how to collectively edit files that have different people working on them at the same time. The challlenges:

1. Communcation at a distance.
2. Collaboration on editing: 

  * If you're good at this, you can see what everyone else is doing, and...
  * You won't step on each other.
  
For this assignment, we're going to use a project management site. There are many, but we're going to use [Basecamp](https://basecamp.com/), which has To Do lists, discussions, etc.

(If you don't log out of Facebook, Google, Amazon, IMDB, they're tracking every site you visit.)

We learn well by association, and by seeing two things at the same time. [Edward Tufte](http://www.edwardtufte.com/tufte/courses), famed statistician and artist, said that important things need to be within your eyescan.  **You want to have code and its effect visible at the same time; if you continue in this field, invest in more monitors.**

<a name="git_collaboration"></a>
####Collaborating Using Git

There are Git graphical interfaces, including SourceTree -- there's a list [here](http://git-scm.com/downloads/guis). However, in this course, we're going to continue to use the command-line. 

Branches in Git are steps toward a goal. The gh-pages branch, for example, is for hosting the content and making it public. In real work, we don't push into public.

In this next phase of working with Git, we will use it for a team exercise and learn how to collaborate using Git. 

<img src="/images/GitBranches_small.jpg" alt="GitBranches" width="300px">

When you start a repo on GitHub, to bring it to the local drive, you use **git clone** (for the first time only) then **git pull** (for every time after that).

Another simple guide to Git here: [http://rogerdudler.github.io/git-guide/](http://rogerdudler.github.io/git-guide/).

For now, we're working with four branches:

1. Master (local)
2. Master (GitHub)
3. gh-pages (local)
4. gh-pages (GitHub)

In our case, **master** is the best, most recent working code (and on team projects, code we're sharing with one another). **gh-pages** is the code we publish.

The basics of starting a team project:

1. Create a repo.
2. Add collaborators.
3. The collaborators will do a **git clone** to bring the repo to their local drive. The first thing they will get is the **master** branch.  Also, will get the **gh-pages** branch.

Here is the basic team workflow, as demonstrated in the class ["Ping Pong" exercise](http://portlandcodeschool.github.io/primer/assignments/03-collaborating-with-git-and-github-ping-pong/).

Constant process of merging between individual branches and **master**.  To bring collaborators' contributions to one's local working branch: 

1. Do a **git pull** into one's local **master** branch.
2 Moveo into one's local working branch.
3. **git merge master**. 

Then, after one commits some changes on the local working branch:

1. **git checkout master** (to move back into the master branch).
2. **git merge <em>local_working_branch</em>.**
3. **git push** (to update the remote version of the <strong>master</strong> branch).

If you can understand this, you'll be a rockstar. Things move fast when you're on deadline, so keep in constant communication: Slack or Basecamp (or whatever means of communication you're using). Email is not so good -- too many distractions.

The project workflow:

1. In GitHub, create a new repository (public).
2. Use SSH for the clone.
3. On your computer, in Terminal, type **git clone <em>(paste URL here)</em>.**
4. Move into the directory that has the repo.
5. **git branch** (to see where you are).
6. Make new **index.html** file.
7. **git add index.html**.
8. *git commit -m"Initial commit"
9. **git push origin master** (For the first push).

Back in GitHub, can now add collaborators, and GitHub will send them an email notification.

For the collaborators, after they receive the email:

1. **git clone <em>(paste URL here)</em>.**
2. **git branch** (to see where you are, and make sure you're in the **master** branch).
3. **git branch <em>Your_personal_working_branch</em>** (**git branch** followed by a new branch name creates the new branch).
4. **git checkout <em>Your_personal_working_branch</em>**
5. Make changes.
6. **git add <em>any changes</em>**
7. **git commit -m"<em>description of the changes</em>"
8. **git checkout master**
9. **git merge <em>Your_personal_working_branch</em>**
10. **git push**

**WHEN WORKING ON THIS TEAM PROJECT, MAKE CHANGES ON YOUR OWN PERSONAL WORKING BRANCH, NOT THE MASTER BRANCH.**

Then, share the code on the **master** branch.

Project will be a site for a massage therapist. On Basecamp, will have a client brief, design, To-Do's, text documents, a calendar, discussion. Share the To-Do's -- these are self-managed teams, so everyone can choose their own assignments.  When we present the project, everyone will need to be able to explain every piece of code they worked on.

Be careful about images and other content taken from elsewhere. We need to be able to supply a license for everything we use. (Lots of Creative Commons images out there.)

***

Fixed header: Find ways to compensate for space it takes, when jumping to an internal link down the page.

* Could add extra margin at the top of the element, but it might ruin the design.
* Or could make an internal div above the element that we want to link to, then link to the empty div, rather than to the element that we're actually jumping to.

A way to find great public spaces in which to work: [https://workfrom.co/](https://workfrom.co/).

When trapped in Vim, hit *Esc* over and over, and if that doesn't work, Type *i* for insert mode, then *:q!*.