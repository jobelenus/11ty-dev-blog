---
title: Against the Purists
date: 2019-04-25T17:37:50.217Z
tags:
  - distributed systems
  - software engineering
draft: false
---

## What duplicating data delivers

There are two major upsides to duplicating data. Make no mistake, when I say
“duplicated” I mean it. I mean not-normalized data.

I can already hear the chorus: “One Source Of Truth”. And I agree, there should
be one source of truth _\*in most cases_. But sometimes that doesn’t apply.

Let me define the situation for which this does not apply; a complex,
concurrent, multi-service, and multi-user system. If you’ve got one of those
keep on reading.

I liken this to double-entry bookkeeping. There is not one source of truth. You
only get to the truth when you’re comparing two (or more) records.

This notion of double-entry bookkeeping is the first major upside to
“duplicating” data. Or at the very least, storing it in multiple forms, at
multiple stages along its transformation. Why? Because when something goes wrong
you have a breadcrumb trail to help figure out at which stage it went wrong.
When you only have one source of truth that is constantly being
overwritten—_**and something goes wrong, because something always goes
wrong**_—you’ll never have any insight into what the state of the data was
before the error. It’s gone. Overwritten. Inaccessible.

The second upside is optimization. Often when creating the One Source Of Truth
it is designed strictly and ontologically. All the relationships conform to the
platonic ideal according to the essence and relationships of the object (sorry,
I studied philosophy). This design values ontology higher than the pragmatism of
a running process. Duplicating data flies in the face of this thinking, and
instead optimizes for access patterns; namely how you’re going to read and write
this data.

My recommendation is that your initial source of truth is write-optimized. Make
it _**easy and fast**_ to write your data. The faster and more compact your
writes are in a distributed system the lower the probability of losing (much)
data when problems arise.

Duplicate _and transform your data into as many different shapes_ you need to be
in order to be able to **read fast**.

If you ever want to keep a system performing reliably and fast you have two
options: keep it really really small, or embrace the CAP theorem and data
duplication.
