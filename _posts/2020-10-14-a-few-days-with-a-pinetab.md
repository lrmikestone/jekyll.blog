---
title: Mike Stone
header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
post_title: A Few Days With A PineTab
permalink: /a-few-days-with-a-pinetab/
excerpt_separator: <!--more-->
layout: post
date: 2020-10-14 00:41:36
published: true
---

In June, I ordered myself a brand new [PineTab](https://pine64.com/product/pinetab-10-1-linux-tablet-with-detached-backlit-keyboard/) from [Pine64](https://pine64.org). Tablets are interesting devices, and really the only one that's been moderately successful over the years has been the iPad. I've been using my trusty old [Pixel C](https://en.wikipedia.org/wiki/Pixel_C)for the last four years. Can the PineTab replace it?

<!--more--> 

Let's answer that question right out of the gate. 

No, it can't.

Not even close.

At least, it can't for me. Maybe it can for you.

I use my Pixel C mostly for consumption of media. Watching videos. Reading books. That kind of thing. The screen on the Pixel C is _far_ superior to the screen on the PineTab. Honestly, that's to be expected considering the chasm of difference in price. I don't remember exactly how much I spent on it, but I'm guessing it was around $800 American. The PineTab _with the keyboard_ runs $120 American. For my use case, the quality of the screen is super important, so I'm just not going to be able to use the PineTab for that.

So, how is the PineTab overall?

The hardware of the PineTab is obviously inexpensive. It feels almost hollow to me when I'm holding the tablet. The screen feels light and is easy to hold. The  bezel is a little large for today's devices, but I actually don't mind a little bezel for ease of holding the device.

It's got all the ports that I would expect on a device, including USB and HDMI. There's a SDCard slot for quick booting of new OSs.

The keyboard doesn't feel like it's going to take much abuse. I tend to come down pretty hard on the keys, so I'm a little worried about how long it's going to last. The keyboard is actually one of the features I like more about the PineTab than the Pixel C. The Pixel didn't include a full keyboard, and it's missing some keys that I use that are not common for the everyday user. A perfect example is the Escape key which I, as a vim user, use almost constantly.

What about the software?

The PineTab came with a version of UBPorts preinstalled. I hadn't tried UBPorts before, so I was pretty excited about this prospect. I confess I was disappointed.

The UI is basically the Unity type interface, and I actually don't mind this for the tablet. The problem I ran into almost immediately is that when you put the tablet on the keyboard, the mouse would get "stuck" in portrait mode even though the screen was in landscape. This limited my mouse movement to the center of the screen, and I couldn't reach the application launcher on the left side of the screen.

Another thing, and maybe I missed something super important here, but when I dropped to a terminal and tried to use apt, it told me that this functionality was locked out in favor of the GUI. This annoyed me _greatly_. 

It didn't take long for me to move over to Mobian.

Mobian uses the Phosh interface from Purism, so it's designed for mobile devices. It kind of gives the tablet a little bit more of a phone feel than I'd like, but it's much farther along with it's development than UBPorts. The camera even works! Ish.

With Mobian, I was able to use the keyboard and the touchpad without any issues. The OS shifted from touch to keyboard/mouse mode flawlessly. Even allowed me to install the latest version of LibreOffice with apt. The only issue I've run into in that regard is that some applications don't recognize that there's a bar at the top (with wireless signal, clock, etc type stuff) of the screen, so it draws parts of the application under that bar. This effectively makes those elements inaccessible, which can be a pain to the user.

I'm also able to use Firefox ESR instead of the Morph browser, which provides a better experience for me. I'd rather have [Vivadi](https://vivaldi.com), but beggars can't be choosers.

All in all, my experience with the PineTab is still in it's early stages. I feel like there's a lot that I'm going to be able to do with it. Unfortunately, while I think the software for it is going to get better and better over time, no amount of time is going to make that screen any better. Because of that, the things I use the PineTab for are going to more closely resemble what I use my Pinebook Pro for, and not what I'm using my Pixel C for. 

Now, I've got a PinePhone coming, and I'm super excited to give it a try.

Day 89 of the #100DaysToOffload Series.