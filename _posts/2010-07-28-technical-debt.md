---
title: Technical debt
author: Mike
layout: post
permalink: /2010/07/technical-debt/
dsq_thread_id:
  - 123122465
views:
  - 50
categories:
  - Tech
  - Tech Industry
tags:
  - process
---
&nbsp;

In my last post I mentioned a term called "technical debt". It's common enough to have a [Wikipedia article][1] describing what it is. The article does a good job explaining "what" it is, but could use some clarification as to why it can be so nasty.

&nbsp;

Technical debt doesn't show up in your accounting, but it can affect your bottom line just as heavily. Whenever you take a technical "shortcut," or accept a sub-optimal solution, you take on technical debt. In crops up obviously in the form of bugs, but more insidiously in the guise of design limitations. The larger a software system grows, the more internal "promises" have been made, that can't easily be changed. These promises are in the form of language choices, platform decisions, API's, 3rd party libraries, and the general structure of your system. A poorly designed system can easily find its way into a situation where it will legitimately take 6 months to implement a feature that only takes an upstart 3 weeks, working from a fresh codebase. That is where technical debt exacts it's interest, in development costs, bugs, and delayed launches.

&nbsp;

On the other hand, it's called debt for a reason. It was taken out in a series of seemingly innocuous loans, but it can be repaid. Major platform refactoring or potentially a rewrite can be very costly, but are possible. During a major overhaul, almost no progress will be made from an external perspective. All of the work is going into fixing the internals. In most cases that I've seen, the best way to deal with this is to focus on designing new features in a better way, given what you've learned from past mistakes. As legacy systems cause problems, transition them over to the new design/platform, and slowly improve the overall health of your projects.

&nbsp;

Please just don't ignore it. Nothing will kill developer morale faster than working in a codebase that they hate and are powerless to fix.

 [1]: http://en.wikipedia.org/wiki/Technical_debt