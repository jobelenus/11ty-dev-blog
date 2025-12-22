---
title: "Ruffled Role Feathers, Why We Need Generalists"
date: 2019-11-02T20:17:00.597Z
image: /../public/img/fullstack.jpeg
tags:
  - fullstack
draft: false
---

This image has been the source of a lot of consternation lately. It seems that a
lot of people think the role of "Full Stack Developer" is "way too many things
for one person to possibly know", and consequently "if anyone claims to know all
this, they must be fibbing."

<!-- excerpt -->I don't think there is a problem with the role of Full Stack Developer. Disclaimer: I am one. Obviously I am biased, but clearly I am not the only one who thinks this arrangement is a good thing. Full Stack is a generalist role. We need generalists. With all the talk of how good "T-Shaped" individuals are for organizations, I'm surprised to hear as much negative press for the role as I do.<!-- break -->

There are some problems with this image though. It exaggerates the issue on the
"top bun". Everyone loves to pick on the browser, CSS, and JavaScript.

You don't have to know "Bootstrap". That is just HTML5 and CCS3. If you know how
HTML and CSS _really work_ in the browser Bootstrap, or the next CSS framework
that comes along, is trivial to learn how to use. Today, because of how good the
browser CSS support is, these frameworks are entirely unnecessary to use. Save
your users a 20kb payload, and write your own CSS. It's fast and easy to do
today.

Similarly, because of how good ES5 support is in browsers, fetch, and the new
document selectors, jQuery is another obsolete technology. And again, you can
save your users 30+kb payload.

I think the real problem with the "full-stack" role is that its focused on
specific tools and frameworks, rather than the the basics: how the browser
works, how the languages and runtimes work, and how the datastores work.

In my view you can take ReactJS, and Angular off the image. I dislike React, and
have never really used it. I've used a lot of VueJS, which isn't on there for
some reason. Now my framework of choice is Svelte. Why? Because it is the
framework where you **mostly write plain javascript, maybe using some components
that at really just closures**. That is my issue with ReactJS, at some point
you're not _really_ writing JS anymore, you're actually writing code in a domain
specific language for a shadow DOM that manipulates a node graph. Where did the
browser go? How many abstractions are between you and the user now?

I absolutely believe that if someone wants to specialize then they should. I
consistently amazed by what they are capable of doing, and I would be lost
without them. **But we need generalists.** This is not too much for one person
to know. We always have parts where we are "deeper" and parts where we are
"shallower" in our knowledge. But we know all the pieces, and we know how they
fit together.

For me AWS and admin/ops-y things are my shallowest part. My deepest part is
certainly in the meat & cheese of this image.

Why do we need generalists? The single most expensive part of every single
project is communication. Even still, in our world of constant and instant
communication, it is the most expensive part. It takes the most time, and the
most effort, to keep a team pointed in the direction they need to go today, this
week, this month, this year. Its not just the manager's job, it is the job of
every leader, no matter their title. **This is where generalists shine.** You
can help everyone understand and synthesize the details with your broad
knowledge and experience.

When you know the full stack, you can be sure that all the pieces are going to
fit. You can be amazed at what an expert can do—but you know where it fits in
with everything else. You know if any of their choices may cause a problem with
another choice in your stack. If no one can see through the entire stack
problems and issues will surprise you. Engineering departments hate surprises.

Make sure someone in your org can eat the whole burger!
