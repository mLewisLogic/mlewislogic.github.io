---
title: Why your startup should be using MongoDB
author: Mike
layout: post
permalink: /2010/08/why-your-startup-should-be-using-mongodb/
dsq_thread_id:
  - 129316491
views:
  - 300
categories:
  - Entrepreneurship
  - Tech
tags:
  - mongodb
  - sql
  - startup
---
[<img alt="MongoDB logo" class="alignright size-full wp-image-60" height="90" src="/wp-content/uploads/2010/08/mongoDB1.png" title="MongoDB" width="217" />][1]Here's a hint. It isn't because it's better than (insert-your-brand-here)SQL. I'm not even going to address that debate right now. It simply has to do with *product iteration*.

&nbsp;

I love [MongoDB][2] as a technology, but I'm not even going to argue this from a tech perspective. The point that I want to address here is pivoting. MongoDB scales, it shards, it map-reduces, yadda yadda yadda. I love it for those things, but for a seed-stage startup, it's single biggest asset is the fact that it is schema-less, and does it beautifully.

&nbsp;

SQL is phenomenal for enforcing rigidity onto tightly defined problems. It's fast, mature, stable, and even a mediocre developer can JOIN their way out of a paper bag. Save it for your next government defense contract. Build your startup's tech on the assumption that your business premise *will* change, and that you need to be ready for it. Your data schema is a direct corollary with how you view your business' direction and tech goals. When you pivot, especially if it's a significant one, your data may no longer make sense in the context of that change. Give yourself room to breath. A schema-less data model is MUCH easier to adapt to rapidly changing requirements than a highly structured, rigidly enforced schema.

&nbsp;

This advice applies equally to great solutions such as [Cassandra][3], [CouchDB][4], etc. Whatever your flavor is, make sure to give yourself options. Use the most powerful and flexible technologies available to you. If a startup decided to develop their core technologies in C, under the pretenses that "It will handle more traffic per server," I'd laugh in their faces. You won't get that traffic if another company comes along and can crank out better features, and ten times faster than you. Pre-optimization is at the heart of all software evil, and it applies to data design as well. Bring SQL back into rotation after you've found your market, and a specific project calls for it. When you're first searching for that market, use the most flexible tools you can. Use tools that let you move fast, and allow you to salvage as much work as you can from efforts that dead-ended or required a pivot.

 [1]: /wp-content/uploads/2010/08/mongoDB1.png
 [2]: http://www.mongodb.org/
 [3]: http://cassandra.apache.org/
 [4]: http://couchdb.apache.org/
