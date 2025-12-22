---
title: RDBMS + ORMs are too good. It is a problem.
date: 2018-12-21T17:14:01.104Z
image: /../public/img/its-a-trap.jpeg
tags:
  - software engineering
  - architecture
draft: false
---

I’m being a little tongue-in-cheek. But only a little. With the success of Ruby
on Rails, Django, and a dozen PHP frameworks (not even mentioning the MS stack),
all web developers have a standard choice for their flavor of programming
languages. And, like IBM, no one gets fired for choosing the standard
object-relational mapping on top of a relational database — no matter which one
you choose.

Don’t misunderstand me, these frameworks are all fantastic, and each one has
something that makes it unique. I even have my favorite. Back when I was in
college (I won’t tell you when) none of these frameworks existed. Heck, JSON
existed only as a spec, but most people wouldn’t find out about it, and start
using it, until well after I graduated. We wrote queries and managed our
databases by hand. And rather than JSON we played around with SOAP.

Back then there was a lot less data. A lot less. And data was orderly. Prior to
relational databases business data was entered into spreadsheets; VisiCalc,
Lotus, Quattro. The only interface to those programs was a screen and keyboard,
not programmatically. RDBMs allowed for programmatic access over a network. But,
on the whole it was the same data that mapped easily into a spreadsheet.

Not anymore. Now our data is messy. Very messy. So messy we can’t agree how to
fix it just yet, or what a “fix” even looks like. We know we have a lot of
questions and the answers are in the data. Somewhere.

Based on my experience, you never know what you’re looking for in the data ahead
of time. When you translate messy data into nice clean related tables you’re
going to lose things. The solution is: leave it messy. There is real value in
messy data. But the problem is that messy data doesn’t work with ORMs and RDBMs.

That is why its a problem that these systems are so easy. I’ve been baited into
believing I will have nice, clean, data. But, after being bit, I know better
than to be fooled again. RDBMs systems make me so happy when its easy — because
it should be.

> “Easy things should be easy, and hard things should be possible.” — Larry Wall

The thing is **messy data isn’t hard anymore**. It’s only hard in these systems.
ORM + RDBMs won’t go away, they will always have a place. But they have to share
now. There are other systems, and they are gaining ground, where messy data is
easy.
