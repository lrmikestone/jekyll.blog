---


description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: Watching In Linux
permalink: /watching-in-linux/
excerpt_separator: <!--more-->
layout: post
date: 2020-05-28 23:23:42
published: true
---

Day 33 of the #100DaysToOffload Series:

A few days ago, a comment went by in my timeline saying something to the effect of, "How have I not known about watch for this long?" That's not an exactly quote, but I didn't write it down at the time. Just in case there are other people out there who haven't heard of watch, let's look at it quickly.

<!--more-->

Here's the description from the man page for watch:

> watch  runs  command  repeatedly, displaying its output and errors (the first screenfull).  This allows you to watch the program output  change over  time.   By default, command is run every 2 seconds and watch will run until interrupted.

This little app has come in so handy for me over the years. I use it at work all the time. Why? Because I'm lazy that's why.

There are a couple different things that you can do with watch that make it super handy. Here are the flags that I use the most, and what they do.

-d: This highlights the differences between the runs of the specified command. For example, if you're doing an ls and a file gets added to the directory, the new file will light up. 

-n: This lets you update the interval you're running the command. The default is two seconds, but if you're not needing to do it that often to accomplish your goal, or if you need to do it more often, you can specify the interval with the -n flag. I use this the least of the flags I'm going to mention because two seconds seems pretty much perfect for me.

-b: If something changes in the output of the command, your computer beeps. This is good for if you're at your computer, but maybe looking at something else. I've used this waiting for clients to send me files. They say they're going to do it right away, but "right away" can sometimes take longer than you'd think.

-g: This exits your watch if the output changes. I've also used this one quite a bit for work because sometimes "right away" could be hours later. This one works really well for doing something inline. I have a script at work that sends a notification to my phone, and using watch -g \<command\>;notify_mike.ksh has saved me hours of staring at a screen. I can run that short command and go have lunch knowing I won't be surprised.

watch is a really simple little app that really saves me time and boredom. Hopefully this brief little summary of the app with a few tiny examples will give you some idea of how you can use it to help you.