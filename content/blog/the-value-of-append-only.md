---
title: The Value of Append-Only
date: 2019-05-24T17:55:11.240Z
tags:
  - big data
  - architecture
  - software engineering
draft: false
---

When working on complex and distributed systems my goal is to make things **as
simple as possible**. Take a look at how some of the biggest architecture
projects, like Kafka, out there design to be high-performant and fault tolerant;
partitions (or, sharding the data that passes through it), and append-only.
Those are two of the key architectural principles that make Kafka work.

It is hard to reason about these systems, and it is hard to be confident when
identifying just _what exactly is happening_. Ensuring that your operational
data (99% of the times this is your database) is an append-only log of events is
my go-to strategy.

Sometimes that means I have a system-versioned tables (whether supported out of
the box, or enforced with triggers). Sometimes that means there is a process
that runs at a regular interval to “make sense” of the collection of records
that I have. Because that collection is ever changing.

But if you have an important piece of data, that can be mutated by many
different processes, and you’ve got UPDATE statements running over one another
you are quickly going to get confused as to just how you got to your final
state. I don’t care how many logging statements you put in there.

There is a reason these amazing projects use this techniques. They are tried and
true. They are simple. They can be reasoned about.

You may not be building the next great piece of internet or software plumbing.
But it doesn’t mean you can’t use the same techniques.
