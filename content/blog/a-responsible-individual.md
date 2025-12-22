---
title: A Responsible Individual
date: 2019-04-12T17:33:33.062Z
tags:
  - management
  - software engineering
draft: false
---

There are tons of opinions and ideas on how to get software engineers to work
together, and I’ve shared some of my own before. I think the crucial one to get
right is coming to the idea of a Directly Responsible Individual. Whether it is
a bug, a feature, a service, part of a product, or the whole product (for
smaller products) there should be **one DRI**.

I believe this the most effective, and most natural way to do our work. I
believe this is, more or less, how open source projects tend to work. Single
individuals own features, parts of the project, bug fixes, and processes. And
decisions flow through those individuals.

## How It Works

It is very simple. The DRI is the source of truth for that indivisible thing.
And “indivisible” is how you decide how many DRI’s you need to have. The DRI is
where the buck stops. They are fundamentally responsible for what they are given
to work on. For a sports example; the coach is the DRI of the team, when the
team fails to perform the coach gets fired. Why? Because there was zero question
who was responsible for the on-field performance of the team.

The DRI gets the final say. You can imagine this as if they have a 51% voting
majority on every part of their project. Ownership in the strict sense of the
word. They should, of course, ask for input, feedback, and opinions from others
on their team and others not on their team. The individual knows their piece is
but one piece of the greater whole, and everyone is working towards reaching the
final goal. But the decisions ultimately rests with them. Why? Because the
responsibility of delivery rests with them. You cannot give them full
responsibility without full autonomy, otherwise you’re sabotaging them from the
start.

## How It Can Work For You

The list of responsibilities you give to the DRI is up to you. If TDD is
important to you, make it their responsibility too. If you want them to fully
document their project, from goals to decisions to user training, go ahead. If
you don’t have a dedicated DevOps team you can make it the DRI’s responsibility
to manage the project in production. Of course, if you have a DevOps, or a
product team responsible for documentation, or a QA team, etc, those teams ought
to have their own responsibilities. Make the lines crystal clear.

Whether everyone works on their own, is paired up, or a mix of the two there
should still be a single DRI. If you’re pairing, give them each a related thing
to own. And they can switch during the day as to whose project they are working
on, who is making the final decision.

Whether you have teams of three, or teams of eight, or twenty, you should be
able to chop up the work into indivisible pieces. Naturally, there will be
pieces that have to work closely together; two different pieces sharing the same
data store and data models, many pieces using one API service, etc. But so long
as you have defined and documented interfaces, you can surface discussions
around a ChangeLog when things need to change.

## Why It Works

I believe this works because owning what you’re working on gets you invested in
doing a good job. It’s yours, no one else’s. Since it doesn’t belong to anyone
else, it will reflect you and your choices.

There can be no buck-passing; “Oh, I thought someone else was going to do that,”
and there can be no wondering about why something didn’t get done. There can be
no disagreement as to how something ought to work, because one person makes that
decision. The only question becomes: is it performing?

## How It Fixes Management

This makes management’s job much clearer; _**they now have one job and that job
is to set context.**_ Your manager, or lead, doesn’t have to wondering whether
or not they should “jump in” and help you out. You can ask them. When you feel
they are deciding things for you, you get to say: Thank you for your input, I
will make the decision. Both micromanagement and drive-by-management need to be
shut down, because it is no longer their job to make decisions. Their job is to
set the context.

Management needs to give you the reasons why we’re doing this work. They need to
give you the end goal, the job your software needs to do. They need to tell you
what you’re starting with, and where you’re headed. They don’t get to decide the
path you’re going to take.
