---
title: MTTR is the Most Valuable Piece
date: 2019-07-12T18:20:50.497Z
image: /../public/img/horse-race.jpeg
tags:
  - startup
  - software engineering
  - releases
draft: false
---

## Mean-time-to-release should not be undervalued

Releasing code to production is a process. The process has to be quick, simple,
and repeatable. If that process is slow, or wrought with problems and caveats
people aren’t going to want to do it. Just like water follows the path of least
resistance—**so do people**. If it is easier to not release something it won’t
be released.

Releasing code to production is also a muscle. If you stop exercising it will
atrophy. Your ability to create production code will suffer.

Code that isn’t in production is not producing value for your customers, and
thus your company/organization. Production is the only environment that matters
(this is why we also “test in prod”).

Increasing your mean-time-to-release means shipping code faster and more often.
If this muscle is strong the world is your oyster. Once you identify
opportunities you can move on them, because your shipping muscle is strong. Once
you identify problems you can fix them, because your shipping muscle is strong.

Shipping small pieces quickly is also a de-risk strategy. Making small changes
reduces the surface area for problems. If you ship one small piece, and
something breaks you know precisely where to look for causes. It doesn’t even
have to break—if behavior changes in your system, or even your users, you know
what caused it. Because you shipped a small change.

If you ship a giant overhaul, and something breaks—good luck finding it quickly
and fixing it quickly. The risk of large changes is larger than just the size of
the change. Thanks, network effect.

This is not about “being fast”, or “being faster than the competition.” MMTR is
a process and a muscle. It sharpens your ability to write production-ready code,
because you’re going to ship it right away. It de-risks problems by observing
what happens in your systems after each small change ships. It allows you to be
nimble and respond by creating value for your customers. After all, it is about
what you can do for them.
