---
title: Progressive Delivery
date: 2019-03-10T17:17:32.820Z
image: /../public/img/you-must-be-this-tall.jpeg
tags:
  - continuous integration
  - sofware engineering
draft: false
---

## The thing that comes after continuous delivery

There is no question, CI/CD has taken over as the you-must-be-this-tall to enter
the “cool kids club”. There are plenty of organizations where they have zero
interest in going there, no judgement to them. But in addition to being
technologically “cool” CI/CD has immense business value—there is zero doubt
about it. But is CI/CD the end-all-be-all? No, there is still more to do.

Progressive delivery is what is next. There are plenty of folks who have been
doing this for a while. There just wasn’t a name for it yet. If you don’t have
continuous deployment its very very unlikely you’ve be able to achieve
progressive delivery. Now let me define what I’m talking about.

Progressive delivery is a mechanism that slowly rolls out the new changes to
your user base, according to your choices. Under normal deployment scenarios,
once your new code goes live every user gets the newness immediately. Of in the
case of feature flags, they are binary, on or off. Once you flip it, every user
gets it. There are two cases where having a mechanism that controls how many
users get a feature becomes incredibly useful.

The first obvious case is error mitigation. If you have a change to a critical
path feature you can slowly roll this out. You can start with 5% of your user
base, then 10%, watching to see if your error rates increase at all. And you can
pull the plug. Note: this does not mean you should stop testing and make your
live users test things for you—all your users will leave if you do that.

The second case is when you have a complex system full of negative and positive
feedback loop experiences with your users. In a complex system you cannot assume
that changing a behavior in feature X will have a desired outcome for user
behavior Y. It’s too complex; humans are irrational meat-popsicles. So you can
make a feature change, that is fully-functional by all objective measurements
(e.g. it doesn’t cause 500 status errors) but that has the wrong desired
outcome. Note: if you don’t have an
[observable system you’ll never be able to know X, Y, or nearly anything else about your system](https://blog.jobelenus.dev/blog/observability-a-goal/).

Note that this is a slight, but meaningful, difference to an A/B test. In an A/B
test you have a 50:50 split, otherwise varied sample sizes will make it hard to
trust your numbers. In my experience A/B tests are generally “smaller” in scope
and focused on a very narrow behavior (_**even if that narrow scope is
incredibly important**_) like driving more conversions by changing the sign-up
flow. You could, of course, progressively deploy to a 50:50 status if you were
worried about the efficacy of the A/B test. Progressive delivery and A/B tests
are in the same ballpark, but if you have progressive delivery you get A/B “for
free.”

In a strange turn of events at my $currentGig a co-worker and I managed to build
a progressive delivery application! We didn’t set out to solve exactly that
problem, but once we were done I realized what we did. It is engineered for our
specific deployment environments, and we built it in NodeJS, with the
proxy-middleware package. It only took us two days to build and test, complete
with respectable observability and sampling. I only point this out to show that,
once you’ve decided what your priorities are doing the actual work is not that
difficult. We’re standing on the shoulders of our deployment platform and event
monitoring vendor, so if you don’t have those, you should look into that.
