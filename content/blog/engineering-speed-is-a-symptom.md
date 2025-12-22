---
title: Engineering Speed is a Symptom
date: 2020-02-02T02:43:43.968Z
tags:
  - software engineering
draft: false
---

I think the speed of a team is the result of a function, it is the symptom of a
working environment. It doesn’t happen by simply standing up and demanding that
people work faster. Engineering teams deliver quickly when they have confidence.
I don’t mean individual self-confidence, or a level on Maslow’s hierarchy of
needs. And I certainly don’t mean the overconfidence of someone’s ego. That
function is transferable experience of production systems, that results in
engineering speed. A working environment is one that produces this transferable
experience in engineers.

This is what my experience as a Technical Lead has taught me. Each individual
has their own baseline, and their own limits. Not everyone shows up to work
together starting in the same mental place. And not every company needs the same
pace—a seed startup and a publicly traded company need different pieces at
different speeds. There are always impediments and roadblocks that slow anyone
down. Confidence comes from experience, and the experiences required, I think,
are very specific. You know people have the right kind of experience its
transferable. That means they come into a new scenario confident—and deliver on
that confidence. But first I want to talk about what I believe are red-herrings.

Here are two things everyone thinks you absolutely need in order to go fast.
There is no doubt these things help, but they are not required—that is a myth.
Whether you have these or not you still need confidence that comes from
experience. Neither of these give you experience or confidence.

# Tests & CI/CD systems

Test coverage is a hotly debated topic. How much should coverage should you
have? What does it mean when you have X% coverage? How do you know it is enough,
or not enough? How long is too long for your test suite to run before it starts
slowing your people and processes down? Unit tests prove one thing, that a
highly specific input for an isolated piece of code results in a highly specific
output. There is zero doubt that is useful in certain times and places.

But as the bugs grow the number of test cases grows. As the codebase grows the
test cases and the number of bugs grow. That doesn’t sound fast, or that it
scales, to me. I’ve seen teams that have a lot of tests and these teams still
move slowly, because they aren’t confident in what their system is doing and
therefore are unsure how to keep moving forward.

Having a CI/CD system doesn’t necessarily give you confidence either. It is
definitely helpful that the deployment of code is according to a consistent
process, if only that it saves a human time and removes some possibilities of
human error. It is a tool, just because you use a tool doesn’t mean you’re a
confident craftsman.

# Staging environments that match production

Once a system reaches sufficient complexity no other environment can ever match
the real live environment. It doesn’t matter if you’ve set it up exactly the
same way. It doesn’t have the same traffic, and it doesn’t have the same random
collisions of events that are the ones that cause problems in production. I
don’t understand why people think they cannot live without a fully-matching-prod
staging environment for day-to-day operations. There is no doubt it is useful
for certain things at certain times. But staging environments do not bring that
much difference from working on your laptop. That is a learning curve that
happens pretty quickly during engineering, and then it plateaus. Forever.
Therefore staging doesn’t bring confidence.

These three things are so common I am sure people cannot imagine living without
them. Someone who has had these tools ought to be able to live without them.
Why? Because their level of confidence isn’t given to them by these tools. At
times these tools can help them gain confidence, but it is never the fundamental
piece. These tools give you false confidence. You can spot the difference
between false confidence: teams still move slowly, and are worried about making
changes.

# We need to understand the reality of our systems

There is nothing that is at all like your production system. Nothing approaches
behaving like it. The only way to gain the experience that will make you
confident is by living in your production system. Unit tests bear almost zero
resemblance to production. Poking around with features based on old data on
staging is not living in prod either.

Living in prod means watching users use your system. Whether that is standing
over the shoulder of users (if you can be so lucky), or having enough
observability to determine what is really happening. Standard monitoring that
tells you your P95 is ~200ms is not enough. Outliers matter, because the
outliers are real users having real problems that are going to complain about
your product on twitter. They are going to stop using it, and stop paying for it
one day.

Living in prod means knowing what your system is actually designed to do, and
knowing how it works. I’ve been shying away from high-level abstractions and
large dependencies more and more these days. Especially ones I don’t control or
deeply understand. The more you understand about the fundamentals of your system
the more confidence you’ll have. Who knows when the next left-pad exploit is
going to hit your system—make sure you’re depending on things you need, and
understand.

Defensive code that runs in prod is more important than unit tests. As a tech
lead I find that I am writing more code to do tasks I’ve done before. Why? I am
writing code that is noisy and fast to debug in production because I have a team
to support. My job is not to write as much code as I can. Now my job is about
communicating and being an example. Communicating examples of failure in
production is extremely valuable information for my team. Especially when I may
not be the one supporting a particular piece of code in the future.

The big reason that trunk-based development and continuously shipping small
changes are rising in popularity is because when you make small changes you
ought to know exactly what should change in your system. And you better be
watching your system after you ship to make sure that it changed, and it is the
only thing that changed. Observing what you ship brings confidence. Your CI/CD
system is pretty useless when you work on long-lived branches and ship a lot of
changes at once. Your tool is sitting idle most of the time. That does not
instill confidence.

Confidence is not about intelligence. It is about experience. Usually people get
experience through pure time on the ground. But that takes a long time, and
plateaus quickly unless that person gets involved in every different part of the
org and code. If you put that person in a new place how much of their experience
is transferable? Almost none of it, and they quickly lose any confidence they’ve
built up.
