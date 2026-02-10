---
title: Complexity Has To Live Somewhere
date: 2026-02-08T19:44:42.314Z
tags:
  - management
  - engineering
draft: false
---
I am referencing a [well known piece by Fred Hebert](https://ferd.ca/complexity-has-to-live-somewhere.html) with my title about writing software. It is well worth reading for the first time, or again. But, to get straight to the heart of it:

> Complexity has to live somewhere. If you are lucky, it lives in well-defined places… With nowhere to go, it has to roam everywhere in your system, both in your code and in people's heads. And as people shift around and leave, our understanding of it erodes.

Most modern software ends up being distributed software. Gone are the days of building a successful business with simple CRUD forms and a database. In a distributed system you need to build abstractions and services that get you guarantees. The only way to do that is to have well-defined places that accept specific inputs and handle every error case gracefully without a loss of data. When the boundaries are drawn wrong and the abstractions leak, the definitions are incorrect and your data will be inconsistent and recovery is painful. Because the complexity now lies in the interconnectedness of the pieces—not within individual pieces where you can engineer guarantees. Success under leaky abstractions and bad boundaries is often dependent on consistent latency & ordering, which are always at risk in a distributed system.

When I say “writing the software isn’t the hard part operating it is” this is what I am pointing at. The code to perform the function, even a complex one, isn’t that difficult to write. However, making it perform at scale, under load, with varying latencies, without failing in a hard to recover way is what makes the job hard. To me, it also makes the job interesting and worth doing. This is also what makes our businesses valuable. The only reason we can charge for what we build is if it provides value by handling complexity people are willing to pay for.

I want to extend the analysis to the organization as a whole by bringing in another piece, if a bit jargon-heavy, about the [hierarchy of work and complexity](https://synexia.substack.com/p/the-hierarchy-of-work-is-inescapable). The principle is exactly the same: if your organization’s complexity lies in the connections and relationships between people or departments, you’re in for some pain. But what is the complexity we’re talking about in this case?

The article states that the default mode of operation of an organization is to create specialists that can handle every exception, and place them in hierarchical layers that supervise and quality check. The more exceptions and variability of inputs to the system, the more layers and functions you get. Management’s job is to absorb the complexity and coordinate the layers. This means complexity lives everywhere in your organization.

The solution is not “simply” the cliches of empowerment, or autonomous teams. If the structural logic of specialists and confirmation layers remains, you’re going to get the same outcome. I really recommend you read the full article; there are so many smaller points that are incredibly valuable that I won’t cover here. To focus on my concern:

> Let’s start with a blunt reality: work complexity doesn’t give a damn about your org chart.
> 
> Every organisation, from a hospital to a bakery to a national intelligence agency, must handle, at minimum, four categories of complexity. These aren’t abstract categories; they are the four unavoidable loads that every organisation must assign to someone or something.

These four categories are:

1. Operational, short time span, whole tasks and decisions you make every day
2. Coordination & balancing, sequencing #1 over weeks or months
3. System design, multi-year coherence and integration
4. Long term, regulation, funding, multi-institutional

This is not a hierarchy of expertise or elitism. Everyone working in all of these categories needs to be highly skilled. The vast majority of surgeons and software engineers make a living in category one. Moving from 1-2 into 3-4 turns you back into a “junior” where you need to re-learn what you’re doing. Because it is a fundamentally different job.

> Different kinds of work sit on different inherent time-spans and interdependencies and systems fail when leaders pretend otherwise…
> 
> The truth is that Buurtzorg doesn’t eliminate complexity at all. It simply relocates it into different structures…
> 
> Buurtzorg’s achievement is not that it removed these loads, but that it redistributed them: operational and coordination complexity live inside the teams, while integrative and environmental complexity live in the architecture and the institutional environment. That’s the real design innovation.
> 
> These are organisational physics, not management preferences…
> 
> In a Jaques organisation, people carry these loads through nested managerial roles…
> 
> In Buurtzorg, the organisational systems carry them…

The “Jaques organization” represents the “default” mode of working I described above. The “Buurtzorg organization” (the name of a Dutch healthcare company) represents an alternate “flat” organization. But, not flat-in-name-only; an organization intentionally designed to deal with the four categories of complexity. Again, the question here is “Where does the complexity live?” If the boss, or the founder, or the person who’s been here the longest and knows where the bodies are buried, has to get called in to make decisions or solve problems, and the org is paralyzed without that? You get the picture.

> The work doesn’t get simpler just because the org chart does
> 
> The most persistent myth in modern organisational thinking is that self-management somehow reduces the inherent complexity of the work. This is wishful thinking dressed up as philosophy or some mantra “self-management good, hierarchy bad”.

Teams need to be constructed to own a problem. The whole of the problem. If you divide and scatter the problem it is far too easy for the plot to get lost. And you can’t put the delivered work back together again. The time horizons involved multiply the problem. The longer term the work, the more time for divergence.

> When Buurtzorg nurses make decisions about a patient, they’re not just doing clinical tasks. They’re integrating the entire case: clinical, social, logistical, relational, environmental. In Jaques’ terms, they are doing Stratum-2/3 [ed. weeks to years] work. Not because it’s written on a job description, but because reality demands it. And Buurtzorg’s architecture gives them the whole situation, not a fragment of it. That’s the key. The work itself is not chopped into roles that then need to be stitched back together by a supervisor or cross functional teams. The team owns the whole thing…
> 
> What makes Buurtzorg compelling isn’t the absence of managers. It’s that integrative and environmental complexity are absorbed through architecture and ecosystem design rather than a managerial chain

The article goes on to point out that the longest term work performed by the government and regulatory agencies in the Netherlands is required to create the context in which you can even attempt this kind of organizational operation in the healthcare field!

When I have seen Engineering teams fail repeatedly it is precisely because the conditions for success were not designed for them. They were told to be autonomous, to make decisions; while they lacked information and the people in roles necessary to be successful. All the while all the decisions needed to be run up the chain, and changes would come back down the chain.

> Even in post-managerial organisations, the need for high integrative capability does not disappear. It relocates, from managerial roles to organisational system design.
> 
> Most organisations miss this entirely.
> 
> They copy the self-managing teams and skip the architecture, then blame the teams when coordination collapses.

When I have seen Engineering teams succeed repeatedly it's because they contained the necessary tools and skills, combined with the information and freedom to make binding decisions. And the responsibility to own & manage those binding decisions themselves.

Many day to day Engineering decisions only impact the short term. After the decisions are made, they disappear into the scenery and are mostly forgotten. Some decisions truly do bind you for years. Teams need the experience and skills to know when they are making that kind of decision. That doesn’t mean they’re going to recognize every single one, or that they’ll make the correct decision every time. We are only human.

Teams need the ability to course correct the moment they sense a problem. Even if the decision was made a while ago. Especially if the decision is “load bearing” and limits optionality. To reference my earlier article—we cannot predict the value of what we deliver. Because of that phenomenon we need to retain as much optionality as possible.

The coordination cost of distributing complexity across management layers is too high, too brittle, and too slow. The world keeps speeding up, and the only way to move fast is to construct a system where teams can own complex problems across long time spans.
