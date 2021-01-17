---

header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: Screenshot Anyday
permalink: /screenshot-anyday/
excerpt_separator: <!--more-->
layout: post
date: 2020-05-11 22:56:54
published: true
---

Day 17 of the #100DaysToOffload Series:

I find myself taking screenshots often. I think it's something individuals who work in computers will do much more often than those that don't, so it naturally there are a wide variety of tools out there to accomplish this task. My favorite is scrot.

<!--more-->

I'm not going to go through the whole man page for scrot to tell you how to use it, but I do want to highlight a few of the features I find handy.

No screenshot utility would be complete without the ability to, well, take a screenshot. Doing this with scrot is about as simple as it gets.

> mike$ scrot

Yup, that's it. Doesn't get much easier. Of course there are ways to make more useful. If you don't want a terminal on the screen when you take the shot, you may want to use a timer. For scrot, it would be the "delay" flag. I pretty much always use with the count down flag too, so I have some idea of how much time I have. 

> mike$ scrot -cd 5

This will give you a count down of five seconds to get the screen the way you want it before the screenshot is taken. Obviously changing the numeric value will change the length of the count down. 

But this is going to give you the whole screen. If you only want a window, you can do that too using the "select" feature. It's handy to use the freeze flag with this as that will stop all movement in windows until you take the shot.

> mike$ scrot -sf

It's important to keep in mind that any windows that are on top of the window you're selecting will be part of your shot. And for the record, don't use the freeze flag and the count down flag together. That's just dumb. You can use the select option with the count down if you choose.

> mike$ scrot -scd 10

This will allow you to select the window you want and then move everything out of the way before the shot is taken.

There are a ton of other options, but those are the ones that I use the most. You can also use -m for multiple displays, or -t to generate a thumbnail for your screenshot. -p will include the pointer, and there are ways to adjust the quality of the shot on the fly. I've found the default settings more than adequate though, so I don't really do that.

Like I said, I'm not going to do a play by play of the entire man page, but if you're someone who takes a lot of screenshots, I'd highly recommend giving it a go. It's quick, it's easy, and it works. 