---
title: How to integrate Mongoengine into Pylons
author: Mike
layout: post
permalink: /2010/09/how-to-integrate-mongoengine-into-pylons/
dsq_thread_id:
  - 138798586
views:
  - 76
categories:
  - Tech
tags:
  - mongodb
  - mongoengine
  - pylons
  - pymongo
  - python
---
Integrating Mongoengine into Pylons is really quick and painless if you know where to put stuff.

&nbsp;

### Add your DB settings to your development.ini file

*`mongodb.host = host[,replHost2]<br />
	mongodb.port = port<br />
	mongodb.db = db_name<br />
	mongodb.username = uname<br />
	mongodb.password = pass`</p> 

</em>

### Connect to MongoDB in config/environment.ini

At the top, include Mongoengine

*`from mongoengine import connect`*

And at the bottom, just before we return, include the following line:

*`# Connect with Mongoengine<br />
	connect(config[&#39;mongodb.db&#39;], host=config[&#39;mongodb.host&#39;], port=int(config[&#39;mongodb.port&#39;]), username=config[&#39;mongodb.username&#39;], password=config[&#39;mongodb.password&#39;])`*

&nbsp;

### Add your models

Now we can create our models just like in the [Mongoengine documentation][1].

 [1]: http://hmarr.com/mongoengine/tutorial.html#defining-our-documents