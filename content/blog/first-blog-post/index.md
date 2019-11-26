---
title: First Blog Post!
date: "2019-10-20T22:12:03.284Z"
description: "Some issues I stumbled upon diving back into the world of front-end..."
---

When I am in between consulting contracts I build websites.

I am currently finishing up a simple static site for a local restaraunt where my main goals were to:

1. Update their current UI/UX to reflect latest visual and usability trends while implementing their re-branding.

2. Get the site up and running as soon as possible.

My initial instinct was to build the site with React however because of the quick turn around that my clients were expecting I decided to use a framework that I am more familiar with - Bootstrap, and deploy with Github Pages.<br>

As I have been mostly working on the back-end of software before I started this project I had to refresh myself with some basic front-end practices. YAY CSS! I had a friend show me a drawing her intern had sent her describing her feelings towards CSS around this same time, it was a house right-side up but with a chimney drawn out of the underside of the house. I thought this was a great depiction of CSS.

Here is the drawing:

![How CSS Makes Me Feel](css-kristina-kosina.jpg "How CSS Makes Me Feel")

Shout out to Kristina Kosina whom I've never met but I already feel a deep bond through our confusion over CSS styling.

I ended up hacking the site together fairly quickly with just a few (should-be-minor) issues that stood out to me:

1. Dynamic content replacement- I needed to write a function that would switch between an 'Eat' menu div and a 'Drink' menu div upon button click. The main issue was getting jQuery to work, I am not completely sure what was preventing jQuery from rendering. The only thing I could think of was script placement in my 'index.html' file.

<b>Solution:</b><br>
After re-writing functions in every possible way, I ended up writing a vanilla JavaScript function that I was able to implement smoothly. Who knows why I didn't think of this sooner...

1. Adding and removing active classes- My code would work properly in Codepen but not in my site. I then deduced it was interfering with existing code.

<b>Solution:</b><br>
After deleting everything besides the menu buttons whose class I was trying to change, introducing code back into my site piece by piece and testing to see if it would break or not, I figured out that the active class in my navigation was interferring with the active class in my menu buttons. I renamed my navigation 'active' class 'active1' and all was well.

```html
<div id="button-background">
  <button class="button active" id="eat-button" onclick="show('eat-menu')">
    Eat
  </button>
  <button class="button" id="drink-button" onclick="show('drink-menu')">
    Drink
  </button>
</div>
```

```javascript
var header = document.getElementById("button-background");
var btns = header.getElementsByClassName("button");
for (var i = 0; i < btns.length; i++) {
  btns[i].addEventListener("click", function() {
  var current = document.getElementsByClassName("active");
  current[0].className = current[0].className.replace(" active", "");
  this.className += " active";
  });
```

```css
.active,
.button:hover {
  color: blue;
}
```

1. Github Pages is very slow! The mobile menu seems to be a bit laggy as well as the parallax feature on the supporting pages. Should I deploy on Netlify instead? Maybe Github Pages isn't optimized to go fast. I will be redeploying this website on Netflify within the next few days.
   (look into Lighthouse google to find exact performance times, compare with existing site, github pages site, and netlify site)

In the near future I plan to re-write the site in React on Gatsby, and deploy with Zeit.<br>
&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;(Why do I want to do this????)
