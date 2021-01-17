---

header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: Making UbuntuDDE More Usable
permalink: /making-ubuntudde-more-usable/
excerpt_separator: <!--more-->
layout: post
date: 2020-08-14 16:03:01
published: true
---

Ever notice how sometimes it's the tiny features that you use so much you don't even notice they're there that really make a UI usable? Recently I switched to UbuntuDDE from Ubuntu Mate, and one of those features was missing, and it's been driving me crazy!

<!--more-->

I like UbuntuDDE. It's got a really cool interface, and the Ubuntu back end makes things super simple to use. 

Still, there was one super tiny feature that was missing that has been driving me bonkers. Horizontal scroll with the touchpad just flat out didn't work. 

Yep, that's it. Super simple feature, but it wasn't there, and there are no integrated tools in UbuntuDDE to add it. 

Finally, I couldn't take it anymore, and I had to fix this. As easy as it was to fix, it was stupid of me to let this go on as long as it did. If you've got the same problem, here are the steps.

> sudo apt install dconf-editor

Once that's done, just run the dconf-editor and go to com>deepin>dde>touchpad. Flip the switch that says "horiz-scroll-enabled", and that's it. You're done. It works.

That super simple change managed to fix something that's been eating at me for at least a couple weeks, and it took less than five minutes. 

Day 81 of the #100DaysToOffload Series.