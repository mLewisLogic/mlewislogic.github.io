---
title: PeoplePatcher
author: Mike
layout: post
permalink: /2010/08/peoplepatcher/
dsq_thread_id:
  - 127720589
views:
  - 76
categories:
  - Tech
tags:
  - django
  - python
  - twilio
---
I had a mean streak of motivation in me this weekend, and cranked out a quick web-app, start-to-finish.

It's called&nbsp;[PeoplePatcher][1], and the premise is that it allows you to conference call two of your friends together, whether or not they want to talk with each other. It's perfect for getting irritated friends or a feuding couple speaking again.

All you do is give the two numbers that need to be connected, and PeoplePatcher takes care of the rest. The friends will never know who requested the call for them, they will both just get calls that toss them into a phone conference with each other.

In case you're wondering, the web-app was built on top of Django (with a little jQuery sprinkled on for flavor), and the phone integration is courtesy of Twilio.

Go check it out and patch some relationships up!

 [1]: http://www.peoplepatcher.com