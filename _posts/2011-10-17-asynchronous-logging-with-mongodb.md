---
title: Asynchronous logging with MongoDB
author: Mike
layout: post
permalink: /2011/10/asynchronous-logging-with-mongodb/
views:
  - 63
dsq_thread_id:
  - 446146139
categories:
  - Programming
  - Tech
---
One specific use case for MongoDB is as a user activity store. It's simple, scalable, and can be done asynchronously (as long as occasional failure is tolerable).

How? The gist is to keep your records in an array that you atomically push to.

MongoDB's documentation (http://www.mongodb.org/display/DOCS/Updating#Updating-%24push) should get you started on understanding how atomics work. Whenever you get a new event/activity that needs logging, just $push it to your array for storage or later processing. Make sure you set safe=False for whatever Mongo driver you're using. That will let it be done asynchronously, mostly eliminating the front-end cost of the operation.

Note: Mongo's $push operation can get pretty slow on really large lists, so take that into consideration.