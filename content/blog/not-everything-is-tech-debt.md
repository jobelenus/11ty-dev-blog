---
title: Not Everything Is Tech Debt
date: 2019-05-03T17:43:36.107Z
tags:
  - technical debt
  - software engineering
  - management
draft: false
---

## There are two stories here, and one is about risk

[Tech Debt won’t kill you. I firmly believe that](https://blog.jobelenus.dev/blog/technical-debt-will-not-kill-you/).
However, I realize that people believe certain things are “technical debt” when
they really aren’t. This happens because they don’t have another term to capture
what is happening. So they turn to “tech debt” as an umbrella term.

_**Let’s stop doing that**. Let’s offer up another phrase to more accurately
capture what is happening._

Technical debt are decisions that will eventually need to be re-visited after a
certain amount of time. On a long enough timeline, every single thing is
technical debt. Eventually even computers will change so fundamentally that
you’ll need to change even the simplest code.

_**But some decisions escalate risk.**_ That is not technical debt. Even if it
is a technical decision in nature, it is not debt. It won’t eventually become a
problem. It is a problem in the very moment you’ve made the decision.

This is why technical debt will not kill you. Escalating risk will absolutely
destroy you, your product, and your company. Here are a few things I’ve
experienced that escalate risk.

Sometimes it isn’t even about code. All business systems include the humans that
use those systems. A lack of communication between the people changing the
system (engineers) and the people using the system is one of the riskiest
propositions of all. That goes both ways. Without managing changes, explicitly,
on how people are going to use the system differently, or what changes are being
proposed is going to cause chaos.

I have seen corner-cases ignored with the explicit statement of **“that won’t
happen”.** I guarantee you’re wrong, I guarantee that it will happen. Once it
does happen you better have an answer. There is a clock running from the moment
you deploy until that corner-case is hit, and you have zero control over how
fast, and how randomly that clock ticks. The bigger your system and the more
people are on it, the faster it ticks. Its one thing to not address a
corner-case, _but one surefire way to make it worse_; not even alerting within
the system that the corner-case was hit.

Those are some higher-risk examples. But let me give you a lower-risk example:
[not enough logging](https://medium.com/@jobelenus/observability-a-goal-efca46b5ba9a).
Once a system is even close to something we consider “complex” there will be
unexpected errors. Errors that don’t seem to be possible. Errors you cannot
possibly hope to reproduce in dev. Errors that won’t stop. If you don’t have all
the data you need to solve it at hand, you’ve added just a little bit of risk.
If you’re experiencing this problem now I highly recommend looking into
[honeycomb.io](http://honeycomb.io/) (Disclaimer: I do not work there, they are
just that awesome).
