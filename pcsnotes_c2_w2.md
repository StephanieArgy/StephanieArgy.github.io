---
layout: page
title: Primer Pro, Week Two
permalink: /pcsnotes_c2_w2/
---

* [Responsive Design](#responsiveDesign)

"Minimum Viable Product" - In this case, the minimal class assignments that cover all the concepts, plus a hierarchy of optional steps.

<a name="responsiveDesign"></a>
##Responsive Design

Tonight, will work from this document: [ResponsiveDesign.pdf](https://github.com/StephanieArgy/primer/blob/master/assets/presentations/ResponsiveDesign.pdf).

1. Build for mobile experiences.
2. Build on that mobile experience by progressively adding to it.

The core of the site is the most important thing, and that will be our focus.

Underlying principles - Use:

1. Fluid adaptive measurements.
2. Media queries (will learn a little about syntax).
3. Responsive images.
4. Responsive typography. (Will only start the conversation about this -- then talk more later).

*Head First Mobile Web* is a great book; its authors work in Portland.

**PROGRESSIVE ENHANCEMENT**

The typical modern webpage is about 1MB. BUT most people on the planet use SMS text messaging; to reach the most people possible, start with HTML only, and tiny images.

1. **HTML-Only** -- Make it work on feature phones. What's the most important content on the page? How do you do navigation with one column?
2. HTML + CSS (for smartphones).
3. Medium screens.
4. Large screens. (For people watching on their TVs, optimize for someone sitting 10 feet away.)

When designing for HTML, always ask, "Can I make this simpler?" You have to focus -- **WHAT ARE WE DOING?"** You don't get fancy animations.

The mobile experience is very diverse: it may be very focused or very distracted. The user may also move between screens during their experience (especially as part of purchasing processes).

To start a responsive design:

**1. Control/set the viewport:**

'''
<meta name="viewport" content="width=device-width, initial-scale=1.0">
'''

From [w3schools](http://www.w3schools.com/css/css_rwd_viewport.asp):

<blockquote>
A <meta> viewport element gives the browser instructions on how to control the page's dimensions and scaling.

The width=device-width part sets the width of the page to follow the screen-width of the device (which will vary depending on the device).

The initial-scale=1.0 part sets the initial zoom level when the page is first loaded by the browser.
</blockquote>

Helps with retina displays.  *Do not use a large fixed width.*

**2. Units of Measure - Fluid Layouts.**

%
em - Based on parent element.
rem - "root em," based on root.
vw/vh - Text is proportional to window.

HOWEVER, don't make line-height or margins based on relative units.

**3. Media Queries**

The reason it's called a "query": it's asking, "What kind of a device are you?" (And you can also ask about its orientation.)

There are two ways to use media queries:

1. In the HTML (often used for print versions of a document)
2. In your style sheet, using the **@media** query.

'''
@media screen and (min-width: ___px) {}
'''

(For small screens, will use **display:none;** a lot.)