---
title: Reading Code Is Hard
date: 2019-02-24T18:02:33.187Z
tags:
  - programming
  - code
  - software engineering
draft: false
---

## And what that tells us about “good” vs “bad” code

I don’t think I have to convince anyone that reading code is hard. Often its so
hard we throw up our hands and rewrite it. There is a saying that “tech-debt is
any code that you didn’t write”. Because reading code is hard.

I don’t think I’m going out on a limb when I say: **rewriting
shipped-and-working code just because you find it hard to read is absolutely the
wrong move**. You are actively destroying learned knowledge embedded in that
code. _Knowledge is value_.

Engineers who know that learned knowledge is value document their code. _They
document code because reading code is hard_. Reading sentences describing why
the code does what it does is easy. That is a way to **protect your code** from
being rewritten and discarded—a way to protect the value you’ve created through
your learning. When you find yourself learning about why an existing piece of
code does what it does, and there isn’t documentation—go ahead and document it.
_Even without changing code you can add value to it_.

I have the good fortune to be volunteering some time helping folks learn to
code. I’m coming to a realization that—they actually know how to “code”. Or
rather, they know how to think through a problem in its constituent steps. And
they can break steps into smaller steps. What they don’t know is “how to speak
computer”. The syntax trips them up constantly. And they don’t have a good map
of concept—>syntax. This is why reading code is hard. And its why junior
engineers out of college have, largely, the same problems. They may be better
with syntax purely out of having spent more time with it, comfort, but they
still lack a map that translates a concept into syntax. That is something that
comes with confidence and experience.

When people say “Good code is eas(ier) to read” they aren’t saying that reading
code is hard. They are saying that; this code is probably documented, and this
code _**clearly demonstrates the concept the code is implementing**_. Bad code
obfuscates what is really happening. Good code makes it front and center. Good
code plainly states what was learned in order to write it and why it was
written.
