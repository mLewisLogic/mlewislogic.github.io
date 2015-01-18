---
title: MongoDB now supports sharding
author: Mike
layout: post
permalink: /2010/08/mongodb-now-supports-sharding/
dsq_thread_id:
  - 126915993
views:
  - 47
categories:
  - Tech
tags:
  - mongodb
---
Excuse my nerd freak-out, but this is really cool.

[MongoDB][1] is a great database system that combines a lot of the querying power with the flexibility and scalability of key-value stores. It's the DB I used in my [Socialgraph][2] system, and I fell in love with it really fast. It's incredibly easy to use, and requires much less rigidity than traditional SQL solutions.

&nbsp;

I won't bore you with my extensive take one it, but suffice to say that I've used it before and absolutely love it. If you feel like SQL is slowing you down or holding you back, I'd really recommend giving MongoDB a trial.

&nbsp;

The inclusion of production sharding in the MongoDB [1.6 release][3] is big news because of the scalability that comes with it. If (fingers crossed) your product requires so much bandwidth that one server no longer cuts it, expansion is as simple as provisioning a new server, and letting MongoDB take care of the details. Goodbye app-level hacks and &nbsp;routing layers.

 [1]: http://www.mongodb.org/
 [2]: http://www.cleverkoala.com/socialgraph/
 [3]: http://blog.mongodb.org/post/908172564/mongodb-1-6-released