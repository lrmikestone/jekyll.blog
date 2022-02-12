---
header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: "Open Source Fitness"
permalink: /open-source-fitness/
excerpt_separator: <!--more-->
layout: post
date: "2022-01-10 09:05:00 -0700"
published: true
---

For Christmas, I bought myself a rowing machine. I've been wanting one for a while. Believe it or not, I actually do use it, it's not just a clothing rack. There is one thing that really bothers me about it though, and that's the fact that there are companies that are spying on me while I work out. We need an open source solution for fitness.

<!--more-->

The rowing machine that I have ties directly into [iFit](https://www.ifit.com). The "display" is really nothing more than a specialized Android tablet that goes directly to the company's portal with videos of fitness instructors using various pieces of equipment and "cheering you on". There are even live courses where they can watch you with the camera that's built into the display.

This is all well and good if you don't mind a company knowing every little detail about your fitness. But what about people who are more privacy conscious?

Well, there's really nothing like what I get on my rowing machine that doesn't involve some private company. Why is that?

Obviously there's the angle where they need to pay these instructors to provide their videos. But do they?

It really got me to thinking about what would be required to do this whole thing open source.

Videos could be hosted by [Peertube](https://joinpeertube.org). That would be easy enough. The metrics that a rowing machine keeps could easily be handled by a [Raspberry Pi](https://www.raspberrypi.org). They're not inherently complicated. Software wise, this thing is pretty much a no brainer.

When it comes down to it, the only thing that keeps fitness from being more open source is the hardware. You need sensors to monitor your pulse. You need sensors to see how fast you're rowing on your rowing machine, or how fast you're peddling on your exercise bike, or how fast you're running on your treadmill. We have an excellent start with the [PineTime SmartWatch](https://pine64.com/product/pinetime-smartwatch-sealed/). It's already got sensors for the basics. Step counters and heart rate monitors. It's inexpensive.

What we need is a portal of some kind that would gather up the data that you could host yourself. The PineTime syncs to that, and then all the subsequent equipment would also. It would know how fast you were peddling and how fast your heart rate was. It's not a complicated database.

I feel like the only reason this doesn't exist is because the fitness industry is downright hostile to the idea. They want to rope you into their walled garden and keep you there.

Maybe someday in the not too distant future, we'll have an open source option. I'd much rather host the data myself than have Google knowing how fast my heart beats and how much sleep I'm getting. 

Day 3 of the #100DaysToOffload 2022 Series.
