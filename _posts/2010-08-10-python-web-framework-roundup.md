---
title: Python Web Framework Roundup
author: Mike
layout: post
permalink: /2010/08/python-web-framework-roundup/
dsq_thread_id:
  - 127823781
views:
  - 388
categories:
  - Tech
tags:
  - django
  - open source
  - pylons
  - python
  - tornado
  - turbogears
  - twisted
  - web frameworks
  - web.py
---
Over the last 5 months, I've had the opportunity to develop web-apps using 5 different Python web frameworks. Those frameworks are Django, Pylons, Turbogears, Plone/Zope and web.py. Each has their own flavor, and could be useful for different projects. If you're thinking about starting a web project, and you already know the virtues of Python*, then it's good to know the pros and cons of some of the major frameworks.

&nbsp;

### [Django][1]<span class="Apple-style-span" style="font-weight: normal; font-size: 12px; "><a href="http://www.djangoproject.com/"><img alt="Django logo" class="alignright size-full wp-image-51" height="41" src="/wp-content/uploads/2010/08/Django.gif" title="Django" width="117" /></a></span>

In short, Django is a really phenomenal framework. Sorry to jump on the bandwagon, but getting up to speed was really painless. On the other hand, I didn't feel like the structure of things was going to seriously hamper expansion/scalability anytime in the very near future. It's a [MVC][2]&nbsp;(technically a [MVT][3]) framework, like most modern web frameworks out there. This keeps things nice, neat and organized, so long as you keep with convention. Basically, they start you out with a bunch of "buckets" and say "ok, your data layer goes here, your logic goes here, and your presentation layer goes here." You don't *have* to follow suite, but that is why you're using a framework, right? I used Django for the back-end at [PeoplePatcher][4].

**Pros:** Easily [the most popular][5] Python web framework. This is great if you want to outsource development, or get community help on an issue you're having. The pros over at #django on freenode.net [][6] (irc client required) are a very friendly and helpful bunch. Anybody that says community size/quality is over-rated hasn't run into enough difficult problems yet!

The framework itself fits it's motto "For perfectionists with deadlines." There is a huge library of community-built "apps" that you can easily toss into your application to extend its functionality. The code's flow is logical and simple, and keeps tight scopes on everything. An answer to the question "why" is almost never more than one jump away. Gone are the days of tracing function calls through 9 files to find a root cause. Development is fast and painless.

**Cons:** I question how well the system will scale if your site really explodes with growth, but honestly, you're not there yet, and if you do get there it's a damn good problem to have. I'd honestly rather have a better templating system such as Mako or Genshi. That's sort of the Achilles Heel of Django, but it's not a deal-breaker.

&nbsp;

### [Pylons][7]<span class="Apple-style-span" style="font-weight: normal; font-size: 12px; "><a href="http://pylonshq.com/"><img alt="Pylons logo" class="alignright size-full wp-image-57" height="37" src="/wp-content/uploads/2010/08/pylons.png" title="Pylons" width="150" /></a></span>

Pylons feels the up-and-comer that's aiming to do things right. It has nowhere near the community support that Django has, nor the library/"app" support. It's going to take you longer to develop an app using Pylons, but my feeling is that it is more of an "industrial-strength" framework for when you want to build an app that's rock-solid. The cost is that you'll be writing a lot more code yourself, but it's going to be built on top of a great foundation. The Pylons framework has a very dedicated core team that is constantly keeping the platform on the cutting edge. It's full-stack, and they unapologetically keep the components used current and relevant. I have no doubt that they will be the first to incorporate newer, better stack components as they stabilize and become production-ready (such as [Tornado][8] or [Twisted][9]). This is what I used to develop the back-end to [Socialgraph][10].

**Pros:** Cutting-edge, using the latest open-source components, philosophies, and techniques. It just hit v1.0 recently, and is a rock-solid choice for production development. If you have a big, mean, complicated web-app that you want control over, Pylons is the perfect foundation to build it on top of.

**Cons:** Prepare to write more code yourself. It has a lot less structure for plugins/apps and copy-paste than Django, so somebody else's solution may take a lot more to adapt to yours. After all, you're building the application-level framework yourself. If you're not afraid to get your hands messy with code and fix your own problems, I feel like Pylons is going to afford you a longer run-way than Django for really gnarly web-apps.

&nbsp;

### [Turbogears][11]<span class="Apple-style-span" style="font-weight: normal; font-size: 12px; "><a href="http://www.turbogears.org/"><img alt="Turbogears logo" class="alignright size-full wp-image-55" height="78" src="/wp-content/uploads/2010/08/g_gear.png" title="Turbogears" width="80" /></a></span>

Turbogears has the philosophy that they'll take the best of open web frameworks and components and stick them together. It's a similar philosophy to Pylons, but it feels a little less polished. On the other hand, they're not afraid to provide more functionality than Pylons, which is a plus and a minus. I feel like it's a solid attempt, but it's not really filling a market need. Need a ready-to-rock framework? Why would you pick Turbogears over Django? It's a false sense of accompishment. It's basically Pylons, with even more functionality, but no game-plan as to how to go any further. You're starting off at the same point as Django, but without any community support or pre-written apps. If you really needed the degree of customization offered by Pylons/Turbogears to begin with, why not just start with Pylons, and add in what you need. Turbogears has a lot of potential, but it's not there yet for production work.

**Pros:** Super-simple to get a basic web-app up and running. Clean MVC&nbsp;delineation.

**Cons:** Feels like a "me too" approach to Pylons, but with more stuff, and less production focus. It delivers on what it promises, but the question is "do you need what it delivers?" Probably not. If you want batteries included, go with Django. If you want a production-ready, easy-to-use stack, go with Pylons. Turbogears is still a niche framework, that I wouldn't really recommend for when you just want to take care of business needs.

&nbsp;

### [web.py][12]<span class="Apple-style-span" style="font-weight: normal; font-size: 12px; "><a href="http://webpy.org/"><img alt="web.py logo" class="alignright size-full wp-image-56" height="47" src="/wp-content/uploads/2010/08/webpy.gif" title="web.py" width="110" /></a></span>

web.py is the bare-bones of the web frameworks, and that's how it likes it. It doesn't waste your time with any cruft, or MVC, or telling you how to write your damn apps. In all reality, it's little more than simple hooks into a web-server that you can tie into your Python program. This framework is not for the faint of heart. If you don't know what you're doing, it will let you shoot yourself in the foot, and laugh in your face about it. On the other hand, not all web-apps fit nicely into the MVC paradigm. What if you're building a web-server that doesn't even have a presentation layer? web.py is great for web-enabling your own code, without fitting your square peg into the round hole of traditional web-app design. I used this heavily when I was working with [Oyster.com][13].

**Pros:** Fast, light-weight, and simple. You don't have to read a ton of documentation in order to understand how the whole system works. You can basically start writing your program your way, and every time you want some web or DB functionality, you can do a quick search in the web.py documentation for how to hook it in.

**Cons:** It will let you develop yourself a flaming pile of shit, and it certainly won't be web.py's fault. If you don't have software design experience, this is not the framework for you. Another note is that there are other frameworks out there that take a similar philosophy, that are a bit more modern, and higher performance (ie, [Tornado][14] or [Twisted][9]).

&nbsp;

## Overall recommendations?

Depends upon your size/ambition.

  * ***Quick up-and-running?*** Django. I'd recommend this to 80% of people out there. It will have you running in no time, and will allow you to scale out functionality quickly, and with minimal effort.
  * ***Serious web-app?*** Look into Pylons. It will grow with you better than Django, but you're going to have to put more effort into getting there. Still a well-designed system, and it makes doing a quality job easy.
  * ***Hardcore, mean and nasty platform?*** Need some serious firepower and your own architecture? Check out a low-touch framework like web.py, Tornado, or Twisted. Be prepared to roll up your sleeves and put some serious blood, sweat, and tears into your new project. I wouldn't recommend this for a part-time project unless you have a long development timeline in mind.

&nbsp;

A great list of a ton [more Python web frameworks][15] is kept up-to-date on the official Python website.

&nbsp;

<small>*note: No knock to Ruby and RoR there, they're just not my thing.</small>

 [1]: http://www.djangoproject.com/
 [2]: http://en.wikipedia.org/wiki/Model%E2%80%93View%E2%80%93Controller
 [3]: http://docs.djangoproject.com/en/dev/faq/general/#django-appears-to-be-a-mvc-framework-but-you-call-the-controller-the-view-and-the-view-the-template-how-come-you-don-t-use-the-standard-names
 [4]: http://www.peoplepatcher.com
 [5]: http://www.google.com/trends?q=django,+pylons,+turbogears,+zope,+grok&ctab=0&geo=all&date=all&sort=0
 [6]: irc://irc.freenode.net/django
 [7]: http://pylonshq.com/
 [8]: http://www.tornadoweb.org/
 [9]: http://twistedmatrix.com/trac/
 [10]: http://www.cleverkoala.com/projects/socialgraph/
 [11]: http://www.turbogears.org/
 [12]: http://webpy.org/
 [13]: http://www.oyster.com/
 [14]: http://www.tornadoweb.org/documentation#performance
 [15]: http://wiki.python.org/moin/WebFrameworks
