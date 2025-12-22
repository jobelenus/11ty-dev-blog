---
title: "Shared Understanding, Imperfect Representation"
date: 2019-03-13T17:18:45.657Z
tags:
  - management
  - sofware engineering
draft: false
---

## Or, why making software in large teams is really, really, hard

The source code to your application and/or product is a representation. It is a
model of a digital world you are creating. But remember:

> All models are wrong, but some are useful—George Box

All models by definition are conceptual. Until the rise of “knowledge work”
models referred to something tangible, something physical in the world we could
touch. Software is metaphorically compared to construction, but in construction
you have physical boards, nails, screws, and steel. When completed, you have a
building. Software “knowledge work” is the first time (that I am aware of at
least) where _**we create a conceptual model of a referent we cannot touch**_.
Well, we can, but its electricity, it hurts to touch it.

There used to be a time, long ago, in our galaxy, where source code wasn’t a
model. During that historical time your source code was Assembly, an instruction
set for the specific hardware chipset your code would run on. You were
programming, very specifically, about the electrical binary state of memory
addresses. We’ve come a long way and we don’t want to go back.

High level languages are now representational models of a conceptual digital
world that doesn’t actually exist. _**To repeat, all models are wrong**_. And I
don’t just mean bugs here, but truly “what you think is happening, is not what
it really happening.” This truth is why the space for instrumentation,
observability, and server-less (or just containers) is growing exponentially
right now. We are, finally, admitting to ourselves things are complicated and we
cannot simply conceptually reason our way through why N% of our distributed
systems are always broken:

> “We used to have an illusion that we were in control and nothing was broken.
> But our systems are full of emergent behaviors and are broken all the time.”—
> Charity Majors

Today, our languages and code is more powerful and expressive than ever before.
You need fewer engineers to do more. So if you have two-pizza team (or more) you
are probably solving a problem with a very large surface area. We know that the
more nodes — _humans_ — we add to a network — _team_ — the more we will be
forced to communicate.

## Now you have two problems.

The job of technical management is to create a shared understanding in your team
of an imperfect representation. (_Aside: the job of people management is to keep
the humans happy, and working together well. A manager is responsible for
both._) There are some additional things that make accomplishing this task
tricky:

1. The imperfection representation is constantly changing because you are
   constantly making code changes, upgrades, adding new features.
2. The imperfection representation is constantly changing because your users,
   other humans, are constantly changing how they are using your system—even
   more so as your system changes.

There are lots of good tools now to understand what your system is _actually_
doing. There are lots of good tools now for understanding what your users are
_actually_ doing. But within your team(s) no one person has the big picture.
Everyone has a part of the model of how things _ought_ to work. Stitching that
together repeatedly, with little margin for error, is very, very hard. There are
not very many tools that are specialized for that.
