---
title: 'MongoDB Upstart service won&#8217;t start on Ubuntu (solved)'
author: Mike
layout: post
permalink: /2010/08/mongodb-upstart-service-wont-start-on-ubuntu/
dsq_thread_id:
  - 129178445
views:
  - 421
categories:
  - Tech
tags:
  - mongodb
  - ubuntu
  - upstart
---
Wow. Just spent wayyyy to much time chasing down an issue getting a MongoDB Upstart daemon up and running using *mongodb-stable* on Ubuntu 10.4. The short answer is that the DB daemon was uncleanly shut down at some point, and a lock file was lingering. That lock file prevented MongoDB from starting. The solution to this is relatively simple. The database needs to have a repair run on it, which will remove the lock file.

To run the repair:

***`mongod --repair`***

You may have to sudo that, depending upon your particular setup. More info about repair can be found here:&nbsp;<http://www.mongodb.org/display/DOCS/Durability+and+Repair>

If you aren't able to repair because you need a config file specified as well, you're going to have to manually repair each DB on your box.

  1. Forcibly remove the lock on your database: `<em><strong>sudo rm /var/lib/mongodb/mongodb.lock</strong></em>`
  2. Open up the Mongo shell and run&nbsp;`<strong><em>db.repairDatabase();</em></strong>` for each db.

The long issue: Why is it impossible for me to find any useful resources on Upstart, a component of the 10.4 LTS Ubuntu distro? I found absolutely nothing indicating where I could find Upstart logs, or something to help me narrow the search. Good grief.

&nbsp;

<small>Note: Thanks to&nbsp;<a href="http://dirolf.com/">Mike Dirolf</a> for offering a safer solution than my first one. This post has been updated as a result of that.</small>