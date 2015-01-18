---
title: 'Singular Purpose Servers: The productivity boost of Amazon EC2'
author: Mike
layout: post
permalink: /2010/11/singular-purpose-servers-the-productivity-boost-of-amazon-ec2/
dsq_thread_id:
  - 170314376
views:
  - 111
categories:
  - Tech
tags:
  - Amazon
  - datacenter
  - EC2
  - Google App Engine
  - scalability
---
I'll start this post by saying that any productivity improvements you get from EC2 probably won't be immediate. There are a lot of features that are very powerful once you know how to use them. The time spent migrating to EC2 will probably even put you in the negative at first.

&nbsp;

Everybody has made much hullabaloo about EC2 instances and how they can help with scale. I think most non-techie folks hear this and envision "Well the website started on one server, so we'll just add a second and it will be twice as fast!" Unfortunately, as web applications get more complicated, this isn't always the case. Where does your database run from? Do you need redundancy? Do you need a search index aside from the database? How is the website hosted? Server. Server. Server. Server. And that's not accounting for application specific servers, or central repositories.

&nbsp;

Us techies know that these things can all just be stuffed onto one box. For a bootstrapped operation, this makes a lot of sense, but will have costs in the form of wasted productivity. Clashing libraries (or different/custom versions of the same library), over-cluttered filesystems, conflicting configurations. These are all time sucks &nbsp;to deal with. Even when the environment is set up and stable, it's harder to stay focused in a "busy" environment.

&nbsp;

Amazon's EC2 puts the power in your hands to define your datacenter by how it should be, rather than by many servers you have on hand. Each major functional piece of the system can have it's own server. The micro instances are so cheap that for development work, the incremental cost can be negligible (probably under $100/mo per developer, depending upon your application). Every developer could have their own version of the data center for personal tinkering. The closer your development environment looks to live, the better QA your developers can do for you. The software will get done faster and will be done just plain better. The more "things" a developer has to keep in their head, the harder it is to produce quality work.

&nbsp;

I'll also note that Google's App Engine looks very promising on this front as well, though you have to accept using Google's proprietary datastore. It's probably going to be a compelling force in the next 5 years, but I don't know if I'd single-source myself in on it yet.

&nbsp;

Go for it devs, set up your dream datacenter and get cracking. Feels nice to do it right, huh?