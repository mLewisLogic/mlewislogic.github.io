---
title: How to change keyboard layout in OS X from the shell
author: Mike
layout: post
permalink: /2012/12/how-to-change-keyboard-layout-in-os-x-from-the-shell/
dsq_thread_id:
  - 956993242
categories:
  - Ergonomics
  - Programming
---
Easy solution is Applescript:


{% highlight applescript %}
on run argv
  set layoutName to item 1 of argv
  tell application "System Events" to tell process "SystemUIServer"
    tell (1st menu bar item of menu bar 1 whose description is "text input") to {click, click (menu 1's menu item layoutName)}
  end tell
end run
{% endhighlight %}


save it as 'change_input.scpt' wherever you like. Now run it using:

{% highlight applescript %}
osascript change_input.scpt "U.S."
{% endhighlight %}

or

{% highlight applescript %}
osascript change_input.scpt "Dvorak"
{% endhighlight %}

or whatever layout you need.

Note, you need the inputs enabled and the input menu enabled for the menu bar.
