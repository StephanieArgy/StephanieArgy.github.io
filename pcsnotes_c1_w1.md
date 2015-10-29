---
layout: page
title: Primer Basic, Week One
permalink: /pcsnotes_c1_w1/
---
##Web Foundations: Primer Basic
###Week 1

####Class Tools

* Slack: For class and team communcation. *(By end of first day, install Slack on computer and iPhone.)*
* Chrome: Our browser of choice for the purposes of this class.
* Codepen.io: A playpen for experiments wtih HTML, CSS and JavaScript.
* Git and GitHub.com: Project versioning and online repositories.
* Atom or Sublime: Text editors for writing code. *(Later, I switched to Brackets, which I like most of all)*
* Terminal/Gitbash: For command-line interactions.

####Learning to Learn

Throughout course, keep a growing list of vocabulary terms; define them, then post them online in a <a href="../pcsnotes_glossary/">glossary</a> we will make for ourselves.

This is a code school, so we are of course concerned with technology, but we are also concerned with teamwork, including **pair programming**.

The first thing we need to learn is the process of learning.  One method we will use in class (and on our own) is the **pomodoro technique.**  Named after the Italian tomato-shaped kitchen timer.  Idea is to help us focus better: we make a deal to focus entirely on one task for 25 minutes (then take a short break). And after four pomodoros, take a long break. (It's very important to get up and move around; there are two major occupational hazards of programming - heart disease, from too much sitting, and carpal tunnel syndrome/repetitive stress injury.) 

We need to take control of our learning process and to find what works for us, and what needs practice. 

For homework:

1. Read <a href=http://www.innovationexcellence.com/blog/2014/10/16/25-things-skilled-learners-do-differently/>"25 Things Skilled Learners Do Differently"</a> by Saga Briggs, then pick one (or more) of those techniques to practice.
2. Finish the Treehouse course "How to Make a Website." (Take the quizzes first, and if you pass, skip the lessons and move on.)

Plan on spending 4-5 hours of the next 48 on class work.

Also fill out survey. (Don't look up anything for THIS quiz; on others, you can use reference materials, but this is to get a baseline of what people know.)

To learn, have to work on memory. Three languages to learn, each with its own syntax. Techniques to help process:

1. Make flashcards. (You have to make them yourself and keep them with you.)
2. Take notes by hand. (Draw pictures, too. As primates, we're good at visualizing, so pictures help.)
3

We also have to have work on some particular skills (or un-suppress abilities we may already have): 
ATTENTION TO DETAIL: Have to be able to read for detail, see every character in the code.

Going to use Git. Git sucks. We will interact with it on the command line.

Having a question you need to answer gives you a goal. If there are questions, try Slack (teachers and classmates), as well as Stack Overflow.

In this class, we follow the practices of <a href=http://www.innovationexcellence.com/blog/2014/10/16/25-things-skilled-learners-do-differently/>"agile project management</a>, meaning that we make adjustments along the way, and will adjust the class to meet the needs of the people in it.

***

####A Short Overview of How a Website Works

"Everything I say is just short of a lie." Meaning...there's so much information to cover with coding that if we try to take it all, we'll be paralyzed and never get anything done. And so, we'll start with as little information as we need to function. Always assume that the little island of information that we're seeing is only the tiny tip of a vast undersea mountain peak. Thee's lots more lurking under the surface. 

These days "client browser" aren't just on computers. We have to realize that we're programming for desktop and laptop computers, the mobile web in phones and tablets, applications with embedded browsers (such as Facebook and Flipboard), and the Internet of things (appliances, refrigerators, cars, watches, etc.).

The client browser starts by going to a URL: "Uniform Resource Locator."

The URL consists of a series of parts:

**`https://en.wikipedia.org/wiki/Uniform_Resource_Locator#History`**

* Scheme or protocol: `https://`
* Server domain name: `en.wikipedia.org`
* Port: (Often not visible; HTTP usually runs on port 80)
* Path to resource: `/wiki/Uniform_Resource_Locator`
* Query string (optional): (Usually turns up as a ? after a search)
* Fragment ID (optional): `#History`

#####What happens when a page is loaded?

1. The browser goes out and gets the URL. (The command is literally GET.) A request is sent from the user's client browser to the server where the website is house, by following the steps along the URL.
2. A messsage is sent back.
    * 401 means that the resource requested can't be found.
    * 500, 501, 502 means that the server is down, or that you broke the Internet.
    * 200 means that all is well: "I got it!" The requested information is sent to the client browser.
3. The client browser parses the information that it has received from the server.

What comes back in the server is an HTML file that contains the structure and content of the page, including URLs that link to other resources (such as CSS style sheets and images).  In the old days (maybe five years ago), style was included in the main HTML document sent back by the server. Now, HTML is all about structure: "information architecture." The idea is that HTML is "semantic" -- it's all about meaning.  And that's going to become even more the case, because now, there are more robots than people looking at websites.

The HTML document summons other sorts of resources:

1. Media - The content of the page, including images, video, audio.
2. CSS - Stylesheets that give the page its look (colors, fonts, layout, etc.)
3. JavaScript - The programming that gives the page behavior and allows the user to interact with it and affect it.

From all of these, the browser creates the **Document Object Model** or **DOM**.  We are Document Object Model engineers. The whole HTML/CSS/JavaScript combination comes together as a fast, smooth, interactive experience for the user. And it needs to be fast and smooth, because people will judge and leave a site in three seconds.

Your job as a coder is to make the page load as fast as possible.  (It's all about efficiency.) Your job as a designer is to hold their attention and make it worthwhile for them to stay on the page.

####Codepen: Making Our First Website

We're soon going to be writing our code in a text editor, but first, we're going to start by using codepen-io, so that we can focus on the code without having to worry about all the other parts of the puzzle.

Codepen is a playground for experimenting with code. You can code HTML, CSS and JavaScript all together and see the result instantly.It will be good for the early phases of learning, but it will also be useful later on, to separate out little sections of code and experiment with them in isolation from the rest of a page. 

We'll log in using our GitHub accounts:

1. Go to **codepen.io** and click on SIGN ME UP.
2. On the "Select a Plan" page, scroll down to the bottom, and under "Free Plan," click on SIGN UP.
3. In the new page, click on the "Use Info from GitHub" button.
4. In the GitHub Log-In page, enter your User Name and Password.

Linking to Codepen from GitHub is good, because it helps make you part of the bigger coding community. On GitHub, it's easy to see how much someone has been coding, because under their Profile, there's a Contributions chart that displays green patches on every day that they do something on GitHub. (If you're hiring someone to do some coding, and they don't have green patches on their Contributions chart, be suspicious of them.)

***

####Language Basics

#####HTML

In learning all our programming languages, we'll look for patterns. They will be there in all the languages, but they may look different in each.

For example, **delimiters** are characters that show us the boundaries of things -- in other words, they create limits.. We'll encounter them in different forms, depending on the language that we're using. 

In HTML, an **element** is indicated with **tags**, which look like this: **< >**

Every bit of content in a page has to be inside of a tag.

Most of the time, there's an opening tag (to show where the element starts) and a closing tag (to show where it ends). Each tag contains a **tag name**. Here's an element that shows the most important heading on a page:

```
<h1>content</h1>
```
    
The angle brackets at the beginning and end of the content are the tags; the "h1" inside them is the tag name. 

When you're typing code, a good text editor will automatically close an element, but it's a good habit to always close the tag (that is, make sure the end tag is in place) before you add the content.

Another shortcut in text editors: typing "lorem" and then hitting the TAB key will automatically create a block of lorem ipsum (nonsense placeholder text). There are also more creative incarnations of lorem ipsum available online <a href=" http://designshack.net/articles/inspiration/30-useful-and-hilarious-lorem-ipsum-generators/">here</a>.

As one builds an HTML page, a hierarchical tree structure starts to grow, with elements nested inside of other elements. The structure has meaning.  For example, the tag names of the headings on a page indicates their relative importance: 
* **h1** is the most important heading on the page -- often the title of the page.  (There's usually only one h1 element.)
* **h2** is a subhead.
* **h3** is a less important subhead, and so on, on down through h4, h5 and h6.

Other common tags (and their meanings) include:
* **main** - Holds all of the main content on a page.
* **article** - Holds a self-contained story that could be shared on other sites.
* **aside** - Holds a sidebar.
* **header** - Holds the masthead info at the top of the page, or material at the beginning of a section.
* **p** - Encloses a paragraph of text.
* **ul** - Encloses an unordered (i.e. unnnumbered) list.
* **ol** - Encloses an ordered (numbered) list.
* **li** - Holds a list item that's part of a ul or ol element.
* **footer** - Holds content at the very bottom of the page.

And finally **div** is general element that can hold all sorts of content.

A complete list of HTML tags can be found at <a href="https://developer.mozilla.org/en-US/docs/Web/HTML/Element">https://developer.mozilla.org/en-US/docs/Web/HTML/Element</a> or <a href="http://www.w3schools.com/tags/">www.w3schools.com/tags/</a>.
(The Mozilla Developers Network is an authoritative professional reference source. w3schools is very basic, and while it may be  simpler than MDN, it's often reviled by experienced developers, so take its information with a grain of salt.)

#####CSS

Like HTML, CSS has delimiters, but they look different: **{ }**

A CSS rule looks like this:

```
h1 {
    color: blue;
    }
```

* **h1** is the selector (the part of the HTML content that this rule will be applied to)
* **color** is the property that the rule is affecting.
* **blue** is the **value** to which the **color** property is being set, in this case.
* **:** The colon is a "separator," always found between the property and the value.
* **;** The semi-colon is a "line terminator," which must be at the end of every CSS rule.

You can't memorize all of the CSS properties, but we'll become more familiar with them as we use them regularly. We can also find a reference list at <a href="https://developer.mozilla.org/en-US/docs/Web/CSS/Reference">https://developer.mozilla.org/en-US/docs/Web/CSS/Reference</a> or <a href="http://www.w3schools.com/cssref/">www.w3schools.com/cssref/</a>.

You can also Google "mdn" plus the name of the property, to bring up the information from MDN. For example, Googling **mdn css border** will bring up this page:
<a href="https://developer.mozilla.org/en-US/docs/Web/CSS/border">https://developer.mozilla.org/en-US/docs/Web/CSS/border</a>
(At first, it may be easier to scroll way down the page to the code examples, and start by playing with those.)

CSS can quickly become overwhelming, so to help keep it comprehensible:
1. Have one property per line.
2. List properties in alphabetical order. (There may be some instances where order matters, and you can't -- but in general, try to keep them alphabetical).
