---
layout: post
title:  "Brightness Shortcut in Ubuntu"
date:   2015-05-20 23:10:00 -0400
categories: ubuntu
---

**Note:** This is not a perfect solution, this is an easy work around for the brightness key binding issue in Ubuntu.

**Install xbacklight:**

`sudo apt-get install xbacklight`

**Add Custom Shortcut:**

Then open the dash and type "keyboard" and launch the app, then switch to the "Shortcuts" tab and add two new shortcuts (+ button at the bottom):

Called "Backlight +" and running the command `xbacklight -inc 10`
Called "Backlight -" and running the command `xbacklight -dec 10`

Then map these commands to whatever key combo you want (I use **Super+F5** and **Super+F6**).

Still it won't show the slider as in volume change. But it works!


**Credits:**
[clappboard](http://askubuntu.com/a/253315/385828)