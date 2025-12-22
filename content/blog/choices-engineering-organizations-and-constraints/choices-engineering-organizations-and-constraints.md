---
title: "Choices: Engineering, Organizations, and Constraints"
date: 2020-04-04T14:19:27.358Z
image: /images/screen-shot-2020-04-04-at-10.38.28-am.png
tags:
  - culture
  - software engineering
draft: false
---

I have not found a better distillation of the gordian knot that is modern
software development. There was a time when one person could, effectively, have
the entire computer in their mind and produce good software. That time is long
since past. Due to the technical and economic choices we have made, and are
living with, we are forced to work together. Michael Feathers is, I think,
holding up mob programming as a solution to the problem. I absolutely think it
is one possible solution. I think there is at least one other possible solution.
The each have their own constraints and I want to walk through them as a thought
exercise.

## Mob Programming

What are the constraints around mob programming? Most teams have been doing it
in-person. As work moves towards remote teams we are going to lose the
high-fidelity of in person communication and bonding as a team. As teams become
more distributed across timezones getting people together at the same time is
going to be more difficult. As remote participants it is a lot harder to stay
focused on people on the other side of a screen than if they were in person. One
constraint that remains in place whether it is in person or remote is the
increased importance of personalities gelling. Programming can be a very intense
mental activity at times, and, to me, it can start to feel like letting someone
in your head. You're going to be with these people for many hours a day—there
are going to be interpersonal problems. The makeup of these teams, and
management of these issues is crucial for long-term success. Any issues that
would have come up in a team that is not mob programming are going to be
multiplied by mob programming. These are real constraints that are going to
require a lot of effort on the part of people managers. The folks working very
closely together are going to need to be fully mature adults capable of managing
their own emotions and being socially aware. These two traits are not something
we commonly find in certain areas of our industry.

## One Person Per Service

I'm not sure I've ever seen someone fully describe what I am about to try and
describe. I'm not sure anyone we have all heard of, that I could point to, has
done this. I think my principle here is: crystal clear divisions of
responsibilities.

There has been a consistent trend in the industry around best practices of
making things smaller, less dependent, and more frequent. One example: make
smaller commits that are atomic, and deploy each of them, don't work for a week
on a feature branch, push 100 commits, and have to figure out merge-hell on
Friday when you are trying to deploy. A second example is a preference for
(responsibly using) microservices over monorepos, the goal has been to create
less dependencies and smaller environments. I think I am advocating for that in
terms of Engineering Org design as well.

If software is best when designed by one mind, let one mind be responsible for
one service. It's design, its environment, running it in production. If one mind
is going to do this, as I said in the open, it has to be small enough to fit in
the head of one mind. I think this fits in with microservices very well.

What are the constraints around this kind of approach? Communication between
these minds becomes the single most important criteria for success. I maintain
that we've seen an organization do this: Amazon. They removed "insider access"
to teams within the company, making everyone rely on documented interfaces to
work together. They created an artificial constraint in order to elicit a
behavior they wanted. That level of communication is not easy, after all, how
many companies and products have good documentation with clear technical
writing? Not many (not even Amazon I would argue, it is plentiful, but is it
clear?). Another critical issue here is a bus factor of 1. Your internal
documentation and code quality has to be very high.

So what do you do with all the people if there are just going to be single-folks
running around? Maybe your bus factor is not 1, maybe its 2, because you pair a
more senior engineer with another engineer closer to entry-level. This is a very
clear mentorship model, with a clear sponsorship, promotion, and "graduation"
experience—you get your own service. (In my experience mentorship situations
become difficult when folks don't recognize they ought to be acting more like a
mentor, or more like a mentee.) All these folks with services are going to need
underlying building blocks. There are always common elements in any software
design. Other people can work on those building blocks, with clear documented
interfaces and responsibilities. I can imagine this growing into a structure
similar to the way the open-source community operates today.

Mob programming is an attempt to solve a communication problem. Adopting it
creates an artificial constraint: there is only one keyboard, in order to elicit
a new behavior: you must communicate to get code written. I think I am merely
flipping the situation. My artificial constraint: one person, one service, in
order to elicit a new behavior: good written communication.

I want to embrace remote-first approaches, embrace distributed teams, embrace
asynchronous teams. Doing that requires good written communication. You can
always ask people to do it, but until its actually required to make progress,
you don't really know what you are going to get.

![](./screen-shot-2020-04-04-at-11.36.20-am.png)

We are all trying to solve the same problem, trying to come up with what works
for us. What works for one group, one company, won't work for another. There is
not one way.
