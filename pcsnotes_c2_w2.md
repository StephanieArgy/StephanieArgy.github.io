---
layout: page
title: Primer Pro, Week Two
permalink: /pcsnotes_c2_w2/
---

* [Responsive Design](#responsiveDesign)
* [Responsive Images](#responsiveImages)

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

In CSS, start with the styles for the smallest size screens, then use media queries to add refinements for bigger versions:

```
(STYLES FOR MOBILE)

@media....

(STYLES FOR LARGER SCREENS)

```

How do you use breakpoints?

As a designer, what's the best way to engage people?  A lot of ads have garish colors and motion to distract people from the real content.

**RESPONSIVE DESIGN/MOBILE-FIRST IS THE EDGE OF DESIGN: Everyone is still arguing about how to do it, so we'll have to learn it ourselves.**

Testing design on mobile devices is a pain in the neck. 

Typography:

Rule of thumb is that you want to have 70-80 characters per line of text (70-80 rem).  Shorter lines are easier to read, because all the characters are in one's eyespan. So, in text-heavy sites, keep the lines short. Also, full justification makes it easier to read. 

Slab fonts present boldly (for headlines).  (Also, bigger line height.)  All of this is controllable in CSS. 

<a name="responsiveImages"></a>
##Responsive Images

Images in responsive design are a big problem, still unsettled. In the future, it will be easier.
A **picture** tag is in development, but still not supported in all browsers. 

Steps for good images:

1. Use the right format.
  * JPEG - For photographs, tonal images.
  * SVG - Solid colors - Vector art, solid color graphics. (Open source)
  * PNG - For images with transparency, more colors, better compression. PNG-24 has good color, but doesn't compress as well as JPEG.
  * GIF - Transparency, animation. (PNG was developed because of proprietary conflicts with Unisys; GIF transparency isn't as good as PNG, but PNG can't do animation yet.)
2. Compress the hleoo out 9of small-screen images, and use relative sizes. 

In the **image** tag, use the smallest possible version. Then to get the bigger version for bigger screens, put this in the CSS under the media query:

```
.myImageClass {
  content: url(biggerImage.jpg);
  width: __%;
}
```

Another way to style:
```
<div class="picture">
NO IMAGE SPECIFIED
</div>
```

CSS

* Mobile - No image
* Medium - One image
* Large - Different image

Can also use **content** and crop to show a more specific part of the image.

###SVG

Vector-based images, can scale as big or small as necessary, with no degradation.

Place to get SVGs: [The Noun Project](https://thenounproject.com/)

SVG is based on XML, which is similar to HTML. Can be dropped right into the HTML as part of the code. 

**You can also open an SVG in your text editor and change it.**

It comes with default height and width, which can be changed to make the image smaller by default, then in CSS, it can be scaled up for bigger screens.

Because SVGs are just text, they can also be manipulated by JavaScript.

###Resources on (Responsive) Typography:

Jason Santa Maria:

* [<cite>On Web Typography: A List Apart Article</cite> article](http://alistapart.com/article/on-web-typography)
* [<cite>Basic Typography: The Basics</cite>](https://ia.net/blog/responsive-typography-the-basics/)

And [a list of other resposnsive typography resources.](http://www.awwwards.com/responsive-typography-a-roundup-of-the-best-articles-and-tutorials.html)

