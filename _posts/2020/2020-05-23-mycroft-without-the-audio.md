---


description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: Mycroft Without The Audio
permalink: /mycroft-without-the-audio/
excerpt_separator: <!--more-->
layout: post
date: 2020-05-23 23:54:23
published: true
---

Day 29 of the #100DaysToOffload Series:

I talk about #Mycroft often. I think people have probably realized that I'm a Mycroft fan. One of the responses I've gotten is that the individual would love to try it, but doesn't have the hardware to make it go. That's actually not true.

<!--more-->

Mycroft has very few hardware requirements. The [Mycroft Mark I](https://mycroft.ai/mark1/) was based on a Raspberry Pi. If you've got a computer (or a virtual machine) that runs a modern version of Linux, you can run Mycroft.

Hey Mike, what about the audio?

Well, I'm glad I asked myself that question!

What if you're running Mycroft on a computer that doesn't have audio output or a microphone to speak to it with? Mycroft has a built in command, "mycroft-cli-client".

The CLI client has made an appearance in several of my #ScreenShotSunday posts because I probably use the CLI of Mycroft more often than I talk to it.

![](/assets/images/r6MaBat.png)

When you run the Mycroft CLI client, you get the log output, the history, and the legend. you can also see the Mic level. I expect that the CLI client was originally intended for troubleshooting skill issues. Since I usually have my mic muted, that doesn't usually show anything.

At the "Input" line, you just enter text exactly like you'd speak it. It interprets what you typed as if it was spoke, and returns a result both in text on the screen in the History, and using the speech output. If you've got the audio on your computer muted or you don't have speakers or sound output, no big deal. 

If you're interested in an open source personal assistant to compete with Google and Amazon, I suggest giving it a try. You can get it [here](https://mycroft.ai/get-started). Installation is really straight forward and the requirements are extremely minimal. 
