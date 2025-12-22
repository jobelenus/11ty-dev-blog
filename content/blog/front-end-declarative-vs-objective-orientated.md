---
title: 'Front-End: Declarative vs Objective-Orientated'
date: 2020-03-26T15:21:00.490Z
draft: false
---
I've always been far more of a programmer than a designer. I don't think I've ever personally liked anything I've designed on the web. It's been good enough, sometimes, and other times not so much. But I find myself squarely on the side of the designers on this one.

First off, CSS is a programming language. Full stop. If you don't think so, you're part of the problem. What designers have been able to do with this declarative programming on the front-end is nothing short of amazing. I've written CSS files with hundreds, and even a thousand, lines, that does the same work these masters can do in a tenth as many lines. People like Andy Bell, Heydon Pickering, and many others.

The React folks of the world have, quite naturally, come to the conclusion that object-oriented encapsulated components are the one true, best, and only way to build designs on the front-end. For logic—that may be true, but for design I think this is patently false. Once you believe this you start writing things like this: ["Margin considered harmful"](https://mxstbr.com/thoughts/margin) and making things infinitely more complicated, just to keep the precious components.

CSS rules are not meant to be encapsulated. Why not? Because it is a declarative language. SQL works the same way. There are absolutely exceptions to the rule where you do want that, but you don't optimize for exceptions. You allow them to happen. Which CSS does on its own perfectly well. There are certainly things we can do that make it easier on the developer **and** leverage CSS (looking at you Svelte). CSS-in-JS is optimizing for exceptions and breaking CSS in order to have encapsulation.

Rather than refusing to use only margin (or only padding, or only X) in your CSS components, why don't you get the CSS out of JS entirely. Learn from the masters about how to use CSS properly.

CSS is not an object orientated language. So let's not try and shove it into that box. Not only does it result in poor developer experience that you need to twist yourself into knots, it results in a massive proliferation of rules that both increase the payload size of our applications, and slows down the browser performance.