---
title: Layers, Complexity, and Trends
date: 2020-10-15T15:30:44.198Z
tags:
  - architecture
draft: false
---

There is a short post that I cherish called:
[Complexity Has To Live Somewhere](https://ferd.ca/complexity-has-to-live-somewhere.html).
Sometimes engineers need to be reminded that if everything was simple, clean,
and easy, we wouldn't be getting paid. It is our job to create the interfaces,
the abstractions, and the patterns that place the complexity where it belongs.

The truly insidious part about complexity is accidental complexity. To use a
metaphor it is: "the cost of doing business."
[Accidental complexity is all the other crap that you have to do before you can do what you need to do.](https://twitter.com/paulbiggar/status/994249934143549441)
There are lots of reasons for accidental complexity; leaky abstractions, tech
debt, and technical decisions made before your time.

I've written before how writing software is more of an artisan process than a
construction process. And it is because this is still a young immature industry,
despite how large and monied it is. We're still learning how to do this. Humans
have been constructing buildings for thousands of years, we've figured out a few
things and standardized on nearly everything. That said, there are still leaky
abstractions and technical debt in construction.

I live in a house constructed in 1905. This has taught me a lot. Nothing is
square, level, or plumb. That said, if you've ever walked into new
construction—nothing is square level or plumb there either. Over that time there
have been decisions and bad work. As an unskilled construction worker I can get
by fixing things in this house. But the true expert, the master of their craft
in construction and carpentry, can walk in here and produce work that results in
perfection despite what is underneath.

We aren't close in the tech to allowing unskilled workers to make real progress.
Hell, we're still trying to help ourselves.

Most of the startups that cater to other developers are working to eliminate
accidental complexity for others by taking it on themselves and asking folks to
pay for it. Many open source projects, I'm looking at you Kubernetes, are
designed explicitly for removing this accidental complexity. To band together
and try to make managing all the servers in a data center look like managing a
single server. You can only reason about things that can fit inside your head.
K8s is an operational metaphor that tries to get everything into your head so
you can reason about it.

I look at Lambdas, and messaging services (whether it's AMPQ or Kafka), and I
see the attempt to make a distributed system made up dozens of CPUs and hundreds
of gigs of memory operate as if it was on one system. By making servers "not
matter" you can think about your running application as a logic puzzle that runs
on one system.

This is not limited to system design. We do this when we architect our code as
well. We create interfaces and patterns that put complexity in the one spot
where it is necessary to deal with. And we attempt to wall off each different
complexity from one another.

This is the trend we've been on in cloud computing—eliminating anything and
everything we can that makes applications _look_ distributed. We don't always
succeed. Just like in construction nothing is level, square, or plumb. When the
abstractions leak we need the experts, the master artisans.

We are trying desperately to do more with less. Fewer engineers, fewer meetings,
because those are the most expensive pieces of this puzzle, the network effect
born by communicating. I'm not sure we're succeeding yet, but we're trying like
hell.
