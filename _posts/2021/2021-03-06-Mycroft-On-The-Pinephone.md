---


description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: Mycroft On The Pinephone
permalink: /mycroft-on-the-pinephone/
excerpt_separator: <!--more-->
layout: post
date: 2021-03-06 02:31:49
published: true
---

Mycroft AI recently announced the [Mycroft Mark II Dev Kits are shipping](https://mycroft.ai/blog/mark-ii-dev-kits-are-shipping-%F0%9F%9A%A2/). Finally. They were expected to ship in the first part of 2018 or the end of 2017. They are decidedly late. I have been anxiously waiting for the Mark II now for years, and lately I've gotten impatient so I've been trying Mycroft on just about any new hardware I get.

<!--more-->

Recently I was talking with [GreyLinux](https://fosstodon.org/@greylinux) about what I have described as the Pinecroft. While Mycroft has finally gotten around to shipping their Mark II Dev Kits, the production version of the device has yet to ship. Originally, this was supposed to arrive in March of 2018. It's my personal opinion that Mycroft has just bitten off more than they can chew when it comes to hardware.

What Mycroft needs is a company that's adept at making hardware that can step in and do the heavy lifting. I think Pine64 is the perfect choice.

But how close to having a working device are they really?

That's a good question. Pine64 makes a variety of devices, from watches to laptops. How much work would it take to put Mycroft on a device Pine64 already makes?

I already have quite a lot of their hardware, and I've been working my way through the list seeing how Mycroft runs on each. Weirdly, the worst experience I had was with the PineTab. It worked, but barely.

Today, I was sitting in my office in a meeting I was mostly paying attention to (I promise!), eyeing the Pinephone on my desk. A Pinephone is an interesting device for Mycroft because it's meant to be portable and small. The price is around $150 American, so it's already competitive with Mycroft devices that have been promoted through Kickstarter.

Being the lazy git that I am, I plugged the Pinephone into power and sshed in from my laptop in the next room. I don't have mobile service on the phone, and when the phone sleeps it disconnects the WiFi (for obvious reasons) unless it's plugged in.

A quick note here. The version of the phone I have is a Manjaro distro running Phosh as the interface. Pine64 recently announced that they're actually going to be standardizing on Manjaro for their phone, but they're going to be using KDE Plasma Mobile instead of Phosh. I haven't tried it yet, but I really want to get around to it here soon. It would be really interesting for Mycroft too since their default GUI is written for KDE. Because I'm not running KDE Plasma Mobile, I didn't attempt the Mycroft GUI, and settled for the command line and voice activated interfaces.

So, back to the installation. I followed the default installation instructions for a Linux based device. I went through the normal routines, and everything worked without a hitch. I registered on the Mycroft portal, and started up the services.

The moment of truth.

With the SSH session I fired up the CLI interface and asked it how the weather was.

> It's currently clear sky and 62 degrees. Today's forecast is for a high of 82 and a low of 62.

Perfect response. While I was doing this, I noticed that there was data coming in on the mic. It _looked_ like it could hear things in the room (which I wasn't in), so I went and got the phone and took it away from all my other Mycroft devices. Holding it in my hand, I asked it what time it was (standard boring question to test if the mic is working). It answered me almost immediately.

Mycroft on the Pinephone works perfectly out of the gate. "Adjusting" the device to be an in home assistant would be trivial. The microphone could be upgraded and the speakers improved. The screen kept or ditched works either way. Ditched makes for a cheaper and less complicated device. The price point is already competitive, and the real kicker for me was that it's already more responsive than the Mark I that sits on my desk.

I think it's pretty obvious that Pine64 could easily step in and create a reasonable Mycroft device with minimal effort. I really would like to see them give it a spin. 

Day 14 of the #100DaysToOffload 2021 Series.
