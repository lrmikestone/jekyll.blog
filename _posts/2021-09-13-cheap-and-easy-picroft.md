---
header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: "A Cheap And Easy Picroft"
permalink: /cheap-and-easy-picroft/
excerpt_separator: <!--more-->
layout: post
date: "2021-09-13 16:41:00 -0700"
published: true
---

I've been wanting to get more Mycroft units for my home. I really like having virtual assistants. I don't like having Google, Amazon, Apple, Microsoft, or whoever else listening to everything that's going on in my house. [Mycroft](https://mycroft.ai) has been my solution for a non-privacy-invading assistant for a while now.

But, there's a problem.

<!--more-->

The problem with [Mycroft](https://mycroft.ai) is that it's designed to be an appliance, but they don't sell an appliance. They had the [Mark I](https://mycroft.ai/product/mycroft-mark-1/), but they only sold it for a short time, and it was relatively expensive. They've been working on the [Mark II](https://mycroft.ai/product/reserve-your-mark-ii-with-a-small-deposit/) for years now, and keep promising it'll be shipping _any_ day now, but it still hasn't arrived. It runs great on a Linux computer, but I don't want to be buying computers and leaving them in each of the rooms of my house. So, what to do?

Since the Mark I and Mark II both run on an off the shelf [Raspberry Pi](https://www.raspberrypi.org) for it's SBC, it runs without effort on that hardware. I'd love to see a company like [Pine64](https://pine64.com) put something on the market (Pinecroft?), but so far that's been a pipe dream. The problem with the Raspberry Pi has always been the audio hardware. It doesn't have an onboard speaker or microphone, and attaching those to the Pi makes things bulky fast. When you're shooting for an "appliance" type of footprint, that's not great.

I _finally_ found a solution in the [MIC+](https://forum.raspiaudio.com/t/mic-installation-guide/17) from [raspiaudio](https://raspiaudio.com). I ended up buying mine on Amazon ([Link](https://www.amazon.com/RASPIAUDIO-COM-Speaker-MIC-Raspberry-Quality/dp/B07B3WYMN8)), but if you're looking for one and find a different way to get it, by all means. It's not an affiliate link, so where ever you can come by one.

![](/assets/images/picroft.png)

The MIC+ is a hat that fits on a Raspberry Pi. I used a Raspberry Pi 3 I had laying around and it worked just fine. I originally had a Pi 4 set aside just for this project, but when I tried to plug it in I ripped the USB-C port right off the board. I wasn't rough with it or anything, and I'm still pretty upset about that.

After you've got the hat installed, there are a couple commands you'll need to run. These are for Raspbian as I just installed a vanilla version of that OS to start from.

```
sudo wget -O - mic.raspiaudio.com | sudo bash
```

It'll ask you to reboot, and if you don't it doesn't work, so don't skip that step.

```
sudo wget -O - test.raspiaudio.com | sudo bash
```

After that, you can use the alsamixer to adjust your volume settings. For some reason, I had to do that second step several times before things worked. I haven't figured out why.

After that, I did the standard Mycroft installation from their Github [repo](https://github.com/MycroftAI/mycroft-core). I've done that so many times these days that I don't even look at the steps. Starting Mycroft and making sure all the updates were done, and shazam. A working Picroft that doesn't take up the space of a computer. The price point isn't bad either.

* Raspberry Pi - $35
* MIC+ Hat - $25
* Various shipping costs

Came to around $60-$70. Considering the Mark I originally sold for $150 a pop, that's not bad. True, it's not as cheap as a Google or Amazon assistant, but then it's not listening to my every word trying to gather as much information about me and my family as possible. That's worth the extra cost to me.

Day 30 of the #100DaysToOffload 2021 Series.
