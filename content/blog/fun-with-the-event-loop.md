---
title: Fun with the Event Loop
date: 2018-12-19T17:11:40.933Z
tags:
  - javascript
  - nodejs
draft: false
---

At the $NewGig we run a lot of services with NodeJS. Unless you live in a
tech-less cave you know Node is “all the rage” these days. I won’t offer my
$0.02 on everyone’s take — that would be a waste of both our time.

Everyone will tell you that “you get to do two things at once!” — which is not
**entirely** true, _its complicated_. But at least you get to think about it
that way. And while many languages are still catching up with asynchronous
operations its easily Node’s biggest advantage. But its not what has me most
excited.

Coming from more classical languages and environments there is a ton of
flexibility I love about NodeJS. The event loop affords you some nice design
choices. In other environments, everything has to happen within the lifecycle of
the request. In order to get even the smallest thing outside of that request
lifecycle, you need to spin up a background message queue, a fully separate
architecture.

Not so in NodeJS because of the event loop. You can send the response back at
any point in time, and defer any Promise’d code onto the stack that will keep
running. Don’t get me wrong, this doesn’t mean background message queues are
dead now. Far from it. And this technique can be easily abused and trash your
performance. But you get to do some very nice, small, operations without running
up a whole separate infrastructure, and re-querying to get all the data you
already have in memory.

So far I’ve been able to do a few things with it.

I’ve increased observability and done so by taking some computationally taxing
comparisons out of the request loop. Sending all that data back out to a message
queue would be a terrible waste of bandwidth, creating needless complexity and
other bottlenecks.

I’ve kept an API endpoint snappy by returning 200 as soon as I get a POST. In
this case I am lucky, because returning an error is useless for the calling
system. I also get to ignore any timeout settings from the caller, and just
happily crunch away on this data, which can actually take some time based on
what we’re doing.

NodeJS is _very, very, flexible_. It is bare bones. And _it is fast_. Layers of
abstraction are powerful, and our entire world of computing is built upon them.
Hundreds of layers by now — _its kind of too much_, but there is no turning back
now. Many other environments add many more layers of abstraction, just to serve
some HTML or JSON text. NodeJS doesn’t. I don’t need more abstractions,
especially leaky ones. Give me power and let me wield it. NodeJS does just that.
