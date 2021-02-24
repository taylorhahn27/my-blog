---
title: Components
date: "2019-12-03T22:12:03.284Z"
---

Rough Notes:

<h3>Components! Components! Components!</h3>

My definition of a component is an isolated, reusable chunk of code.

Even in the simplest of websites/applications it is easy to end up with an unneccesarily long file with hundreds of lines of unused or duplicate code, creating a giant hard to read mess.<br><br>

Maybe I have...

1. a bunch of code that is commented out that I was considering using at some point
2. code that has been overwritten by other code that is no longer providing any function

<h3>Organization! Organization! Organization!</h3>

This is especially important when dead CSS and Javascript code affects loading performance. Even if the CSS or Javascript is unused, it is still downloaded, parsed, and compiled by the browser.

The way CSS is written creates a very hard to organize file, as
there is only so much labeling you can do to keep things organized.

How many times have I found myself trying to do something seemingly reasonable that should be simple with CSS, only to get derailed in bizarre and unimaginably hair-pulling ways. Maybe I'm wanting to create a responsive navigation menu, align buttons properly in both desktop and mobile, I want to shrink a logo responsively but also maintain center alignment, or a simple styling of a text, but nothing I try seems to have the effect I am going for.

After losing hours and even days on these simple issues, I came across an Elm package called elm-ui.

Blaine had mentioned Elm to me in the past, I even attended a meet-up in San Francisco some months ago.

I've always been very intrigued by the way the Elm team attacks problems as I mentioned above and I am excited to learn more. The language is simple looking and straight forward. In fact, Blaine has been building a blog in Elm and we've been comparing the his to mine (in Gatbsy).

I plan to take a few parts of my current code and re-write them in both Elm and React.

I will then see if I have similar problems to the ones I have been having, no problems, or something in between.

<h3>My current issue:</h3>
Client wants to be able to easily update their restaurant menu items.

Suppose the chef has created a new special for the day and the client wants to easily update the website without having to call me to do so.

How will they be able to do this with no HTML experience?

<h3>Thoughts:</h3> <br>

1. Create a section of code clear enough to read that the client is able to parse it and update whatever needs updating.
2. Remove/isolate the section of code from index.html that is their menu and put it into another file. This way they wouldn't have to become overwhelmed siphoning through html that means nothing to them.

When researching if this is possible (including a separate html file into another html file), I was surprised to find out that there is not a straight forward/easy way to do this.

I came across an article from css-tricks.com called [The Simplest Ways to Handle HTML Includes](https://css-tricks.com/the-simplest-ways-to-handle-html-includes/).

Within this article the author suggests a handful of different work-arounds, all of which require outside tools/libraries.

I would think that the idea of injecting an html component into another html file is something that could be very useful to almost every website created. This would not only keep things a lot cleaner, it would encourage a better style of coding.

I've always been pushed to create programs in reusable components. This includes everything from simple webpages to more complex applications.

I've thought about this issue of restaurants not being able to update their sites quickly and easily since the beginning of this project and I've been considering solutions. I have a few ideas on how to create such a thing.
