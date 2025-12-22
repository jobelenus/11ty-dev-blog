---
title: Engineering in the Time of Product Market Fit
date: 2021-04-03T11:28:18.284Z
tags:
  - culture
draft: false
---

I love reading the latest blog posts from the Slack Engineering team, Will
Larsen and the Stripe crew, and the fingers-crossed-occasional post-mortem on
painful outages. They are a treasure both to observe how these teams are
operating and because freely sharing knowledge and experience is rare today. I
am jealous to have the experience of service migrations under the load of tens
of thousands of daily active users, or even millions. It creates a whole new
level of challenge.

But that is not where me and my team are today. Not yet at least. There is no
doubt that having these teams as a guide post, as a north star to start moving
towards. It is invaluable to have a list of known possible issues next to
possible solutions to evaluate. No, we are still searching for market fit. That
means we have different engineering challenges.

We have all heard of the seed-round startup asking themselves "Should we use k8s
or not?" and chuckling to ourselves, knowing that its the wrong question. It
shows that they don't know what is important yet.

Engineering in the time of Product Market fit is about being able to present
**something** to your potential customers As Fast As Possible. There is one
truth—No One Knows Anything. Your organization **does not know** what customers
will buy. Having the answer to that is called Product Market Fit. You don't have
it yet.

I've learned that the best mindset for working in this environment is to expect
that you're going to delete, shelve, and entirely ignore **most** of what you're
building right now. Because no one wants it. This is a tough concept for some
engineers who treat their code like _the precious ring_. As the saying goes
today for servers: cattle, not pets. So it goes for your code and your prototype
designs, learn to let go.

Time is a finite resource and the two largest constraints on your time is money
and attention. You have a limited amount of runway. You only have so many
attempts at gaining your customers attention. You only get to make a first
impression to a new customer once. The more and more missed attempts and your
potential customers will start ignoring you because they think they know what
you're about.

The challenge today is to find the sweet spot. _Just_ enough tooling to make
development _just_ easy enough to turn around MVPs to put in front of your
customers to test. Because some of your tooling will end up being ignored and
unused. The most important thing is getting the MVP out ASAP. The more time you
spend on tooling, the less time you're spending on the actual MVP. The more time
you spend on future proofing the less time you're spending on MVP. Don't
optimize, don't scale. Until the moment you have to. Make plans. Don't act on
them. It is a test of willpower and focus.
