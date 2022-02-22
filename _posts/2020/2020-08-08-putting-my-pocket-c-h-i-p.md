---


description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: Putting My Pocket C.H.I.P. To Use
permalink: /putting-my-pocket-c-h-i-p/
excerpt_separator: <!--more-->
layout: post
date: 2020-08-08 15:14:03
published: true
---

A couple years ago, I bought a Pocket C.H.I.P. to tinker around with. It was a cool little device that I didn't use to nearly it's potential. And then it went into a drawer. Recently, I've dug it back out again, and I'm seeing if there's something I can do with it.

<!--more-->

For those of you that aren't familiar with the Pocket C.H.I.P., this is what it looks like:

![](/assets/images/jNN4Fl1.jpg)

The device has the simplest form of built in keyboard, and a touch screen. While it was a neat little idea, I found both to be mostly useless. The keyboard was difficult to use, and I only used it when no other options were available. 

I quickly swapped out the GUI the device defaulted to with I3, which worked great with an external keyboard. 

Then [the company that made the Pocket C.H.I.P. went bankrupt](https://en.wikipedia.org/wiki/CHIP_(computer)#Next_Thing_Co._Insolvency).

I continued to tinker a little bit with it, but it quickly went into a drawer and didn't come back out.

Recently, digging through my random tech junk, I ran across it again. It seemed a shame to have a perfectly working device sitting in drawer doing nothing, so I fired it back up again. 

I quickly remembered how useless that keyboard was, so I plugged it in to a USB power source and made sure SSH was enabled, and used my normal computer to access it. 

Poking around to re-familiarize myself with the device, I noticed that this device used a pretty standard installation of Debian with a single repo for the stuff that was Pocket C.H.I.P. specific. Since the company that made the Pocket C.H.I.P. was bankrupt, that server was no longer online, so I removed it and ran updates.

Everything went through completely painlessly. No issues, and I was up to date with the latest [Jessie](https://wiki.debian.org/DebianJessie) packages. Then I upgraded to [Stretch](https://wiki.debian.org/DebianStretch) with the same results. No issues at all.

I ran into a few glitches when I moved it up to [Buster](https://wiki.debian.org/DebianBuster), which I meticulously documented and then immediately lost somehow, but it was really just a couple packages that needed to be removed and some minor reconfiguration.

Today, I'm running the latest version of Buster on a Pocket C.H.I.P. built by a company that's been out of business for two years. 

![](/assets/images/bn6c4OO.png)

I'm still no sure what I'm going to do with it. It's plugged into USB power and sitting next to my wireless router, so it should run virtually forever. It's not speedy by an stretch of the imagination, but it's passable. 

If you've got some ideas on what I can use this interesting little device for, reply to me over on [Fosstodon](https://fosstodon.org/@mike/).

Day 78 of the #100DaysToOffload Series.
