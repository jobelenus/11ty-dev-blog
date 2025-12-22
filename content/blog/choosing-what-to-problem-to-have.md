---
title: Choosing What Problem To Have
date: 2020-05-01T11:46:52.790Z
tags:
  - architecture
draft: false
---

Most of our engineering decisions these days are about choosing which problems
you want to have. For me, this realization came off the back of the
popularization of the CAP theorem. Learning that the natural constraints of a
distributed system force you to pick availability or eventual consistency, means
you have to choose what problem you want to have. Would you rather your system
have slower responses, or even be down? Or, would you rather have data "look...
off" for a while, and write rules to manage conflicts, or heaven forbid, manage
some manually. While the big players are building for the route of eventual
consistency, it is absolutely legitimate to choose availability. This is a
thorny, if abstract problem, but choosing your problems exist on smaller scales
too.

A recent example of this for me is dealing with any sort of data
de-normalization. There are a lot of engineering choices to make here around
transactions, code simplicity and reuse, and managing the cost of compute time.
Often times the simplest and easiest to reason about implementation is a
standard ETL every X hours. The problem you've chosen to have is that for N
hours your data is out-of-date. That is another easy problem to explain and
understand to people. But, this is not always a viable problem to deal with.

I love database triggers and procedures for these sorts of operations when the
cost of compute is low enough. No matter how many points throughout the code
that touch this data, the database is always the commonality, so code-reuse is
essentially nil. Putting the operation in the database handles the transaction
issue; the original operation is not completed until the trigger finishes. This
works well enough when the compute cost is low, when its high you're going to
slow down a high traffic db with locks.

If you put the ETL operation in a separate re-usable codebase that operates in a
different transaction, and the compute cost is high, you have the potential for
race conditions based on how you're kicking off your tasks and guarantees of
run-once. Sometimes the constraints of your work chooses the problems you are
going to have.

I see this playing out on the front end as well. I am, apparently, in the
minority who thinks that the problems React and its ecosystem brings are not
worth the benefit. I do not want and I don't want my customers to have; giant
payloads and big cpu loads (especially for lower end devices). I honestly don't
even think the developer experience is even that good. There are some upsides
that have some second order problems: there are tons of components and packages.
Like Python, there is a package for whatever you need to do. However, this
leaves you a problem to solve: you are going to have to fight against the grain
to make it all come together and look the way you actually need. My pet theory
is that this is why there are so many front-end jobs. You can pick a template,
theme, or even Facebook, Google, or Bootstrap design system and then grab a
machete to make it match your brand. That is not a problem I want. The
second-order problem is that developers only know how, or want to solve,
problems with React. Many have lost track of the underlying things we are trying
to solve in the browser, and trying to deliver to the user. This is when people
are capable of being blind-sided because they've lost the forest for the trees.
They never see the next thing coming. And there are lots of possibilities on the
front end that don't include shadow DOMs or JAMstacks. The JAMstack is a great
solution to bringing the fastest first-paint to the user by pushing content as
far as you can to the edge, which means it has to be static. That is one way to
solve sending giant payloads—putting it as close to the user as possible.

If we aren't continually paying attention to which problems we are good at
solving, capable of solving, as a team, we run the risk of picking a problem
that can do some damage, by accident.
