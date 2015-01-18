---
title: github mute
author: Mike
layout: post
permalink: /2013/09/github-mute/
dsq_thread_id:
  - 1809648337
categories:
  - Programming
---
If a particular Github account is cluttering up a pull request you&#8217;re trying to review (a robot perhaps), you can mute their comments out with a quick bookmarklet. Note: this is hacky and will probably break at any momment.

 

{% highlight javascript %}
javascript:(function() { var username=prompt("Hide comment blocks including user:"); if (username!=null && username!="") { $(".comment-header-author:contains("+username+")").parents("tr.inline-comments").hide(); } })();
{% endhighlight %}
