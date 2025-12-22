---
title: "Many Hammers, Many Nails"
date: 2018-12-18T20:30:03.250Z
tags:
  - software engineering
  - data modeling
draft: false
---

The best way to save time while solving problems is to use the right tool for
the job. Every one of those hammers in that image has a distinct purpose. If you
ask the master — nicely — he just might explain the tools. There are more and
more tools now, the ecosystem truly is huge. Lots more then when I began my
journey of writing code. It is mind-boggling to try and keep up with everything.

The biggest problems I’ve had during this journey is when I use the wrong tool
for the job. I’m still able to get the job done, and solve the problem. But,
around half-way through I get a nagging thought: “There must be a better way.”
You’re writing code that works against the grain of your tool. Here is a classic
example that has bitten me so often: tracking historical changes in a relational
database. Relational databases are the wrong tool for this job. Because their
strength is keeping the current state normalized, not what has changed along the
way. Depending on what you’re tracking, the right tool may be a time series DB,
or it may be a document store (you always hated locking your tables with ALTERs
didn’t you?).

But in an effort to get things done as quickly as you can, you smash the
historical data into the relational database. You actually have to write a bunch
of code to get this done. And its not the cleanest code in the world either.

One lesson I am trying to take to heart more often — the more code you write the
greater surface area you create for bugs. If you use the right tool you don’t
have to write the ugly code that is full of bugs.

Chances are that if you’ve have perpetually buggy code you have something in
your ecosystem that was not designed for how you’re using it. Square pegs don’t
fit in round holes.

The object here is not “clean code”. The objective is solving the problem, and
saving time. Because time is money. Using the right tools saves you money. And
making good tools is a good way to make money.

That is why there are so many good tools now. The generation of software
engineers before me realized they were using the wrong tool. They went out and
built the right one. There are lots of different problems that people are trying
to solve. That is why there are so many tools. Figuring out what each of them is
good at is now part of our job.

I am very excited about the Streaming architectures that are being developed;
Kafka, Samza, Flink, Storm, etc. There are problems that arise “at scale” where
throwing more boxes at the problem make the problem worse, or at least, don’t
fix the underlying issues. This is a complex problem, so, naturally, these new
systems are very complex. Streaming architectures are being built to handle
issues of ordering (making sure that “A happens before B which happens before
C”) while remaining parallelized (so they can handle hundreds of thousands of
requests per second).

I lay awake at night realizing that the code I agonized over to get just right,
and find those last troubling bugs, reading megabyte after megabyte of logs and
traces, didn’t have to exist at all. Because I was using the wrong tool. And
that the solution I ended up with was actually a bug-riddled poor-man’s version
of these shiny new tools being developed.
