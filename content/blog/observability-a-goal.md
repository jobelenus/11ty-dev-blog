---
title: "Observability: a goal"
date: 2019-01-22T17:17:01.260Z
tags:
  - devops
  - observability
  - software engineering
draft: false
---

Observability is an attribute of a system. A system either has it, or does not
have it. Most systems don’t have it. Even if they have some amount of reporting
and system metrics — it doesn’t mean your system is observable.

A system is observable when you can ask questions, new questions, about how its
performing (both technically, and the business goals) **without having to make
any changes or deploys**. As an engineer who has built a lot of systems, I do
not actually think I’ve built one that is observable. It is a high bar — but
worth achieving.

This is a very technical issue, but it is actually a solution to a business
problem. I am very encouraged to see clear communication from engineers about
it. You can follow the #o11y hashtag on twitter. The hashtag and conversation
came out of the DevOps community, which has been focused on merging
infrastructure with their larger product organizations, rather than a line-item
on a budget somewhere.

To make a long story short to create an observable system you have to merge the
monitoring of system health and business metrics. Many times, business metrics
can be very vague and fuzzy. But if you’re an e-commerce site you want to know
how much a 5% slowdown in response time affects order conversion — in order to
know how much to spend on infrastructure & engineering to avoid the 5% slowdown!
Otherwise you’re just guessing. Hitting a quarterly goal is actually very vague
and has a large number of dependencies.

It wouldn’t be hard to write a single report that correlates % slowdown with
order conversions. But then, if you wanted to know “What is our % of repeat
customers when we shipped them something late?” do you have to write another
report? If you do, your system isn’t yet observable. There is nothing wrong with
that. And you have to decide how far you want to go here.

The larger and more complex your system is — the larger the engineering
challenge to get all that data. But if you’re losing this information (because
you’re not capturing it) you don’t know what you don’t know. That is scary. That
is how someone comes along and eats your lunch.
