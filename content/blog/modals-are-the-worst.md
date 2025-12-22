---
title: Modals Are The Worst
date: 2020-04-25T12:58:53.456Z
tags:
  - design
draft: false
---

This is my "Hot Take" for the front-end world. I truly think modals are bad. Bad
for the end user, and a crutch that too many developers and UX folk rely on.

Let's start with the users because they matter most. We have implemented modals
to take over the whole screen, to be an interruption, and to hide all content
behind it. My challenge for the experience is: replace every modal you have in
your application with a browser `dialog()` call. The only difference is that the
dialog locks the main thread—but you've already locked the thread in the users
mind, so you might as well.

There have been numerous times where I need other data on the screen in the
modal. But I can't see it, its hidden behind the modal. And I can't get to it.
And of course, once you close a modal, whatever you did in there is gone.

Looking at modals on mobile is the nail in the coffin. Due to the screen size it
**must** take up the entire screen. What is the difference between that and
"navigating to a new page" in the mobile UI metaphor? When you actually navigate
to a new screen you get the standard back button right where you expect it,
right where it is like every, single, other, application. By using a modal on
mobile you've confused your user and broken the standard UI metaphor for these
devices.

Using modals is how we developers show our laziness. It is a crutch both in
terms of not wanting to do more work in creating new pages (or states), and not
wanting to think about how to improve the UI so a modal window is unnecessary.
There are lots of possibilities that range from small and unobtrusive like
inline editing, or more fundamental like left/right pane splits (e.g. a list on
the left, detail on the right). I think we really need to start thinking about
task-specific UX where we optimize for what task a user is trying to do. Build a
UI specifically for that task. Don't just throw a modal into the mix because it
_allows_ the user to do something. I am willing to bet it is clunky. And if you
had the job to use that modal window hundreds of times a day, you would quickly
redesign it for something better.

I think the web would be much improved if ad blockers could block every custom
modal window. Add modals to the deny list. There is an up-and-coming HTML
`<dialog>` element, which is a replacement for `dialog()`. Let's build toward
that, and destroy custom modals. I know people will abuse the dialog to take
over the whole window—but it does not have to. And, if it is an HTML element it
can be controlled by the browser; there can be system settings to protect users
when we developers abuse it. I imagine the possibilities of site-lists that
block their use of the element.
