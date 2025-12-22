---
title: Resilient Microservices
date: 2019-03-29T17:32:00.256Z
tags:
  - resilience
  - software engineering
  - management
draft: false
---

An adjective everyone wants to claim: resilient. “Our service/platform is
resilient.” Resilient infrastructure is a topic that many have gone into detail
to teach us all how to achieve it.

But I think we have skipped over something. Something more fundamental.
_**Conway’s Law**_:

> \[O]rganizations which design systems … are constrained to produce designs
> which are copies of the communication structures of these organizations.

If you’re looking to build a resilient system, you better have a resilient
organization, and communication, otherwise you’re going to be ice-skating
up-hill all the time. You may yet achieve your goal. And then one day you’ll
realize you’ve slipped and lost that resiliency.

It comes down to actually creating a culture in your organization that truly
values resiliency. That is the only way you can be sure you’ll continually reach
your goal.

The biggest success story for this topic is Amazon. The first goal wasn’t
resiliency, it was about pleasing their customers. But, Bezos knew without a
resilient system the customer experience was always subject to volatility. We
all know what he did. He separated his teams.

He demanded that when his teams communicated with one another they did so
through official channels. Just like any other customer would. In order to be
absolutely sure the customers would be treated well—he turned teams at the same
company into customers. This is a rather extreme, and useful, form of “dog
fooding” (using what you build).

Rather than just telling everyone to “Be More Resilient”, as if that is a thing
you can expect to work, he introduced a constraint that resulted in changed
behavior. And the result of that behavior was very resilient systems that are
highly regarded by everyone in our industry.
