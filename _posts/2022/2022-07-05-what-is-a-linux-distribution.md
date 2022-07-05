---
layout: post
excerpt_separator: <!--more-->
title: What Is A Linux Distribution
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
permalink: what-is-a-linux-distribution
date: 2022-07-05T10:57:34.608Z
published: true
---

This is a response to a two episodes of the podcast [Linux Downtime](https://linuxdowntime.com), specifically episodes 49 and 50. These episodes discuss what it means to be a Linux Distribution. This is my thoughts on the matter.

<!--more-->

First of all, if you haven't listened to these episodes, now is a good time to do it. I'll wait. You can find them here:

[Episode 49](https://linuxdowntime.com/linux-downtime-episode-49/)

[Episode 50](https://linuxdowntime.com/linux-downtime-episode-50/)

OK, let's be clear here. I love these guys. I like [Joe](https://fosstodon.org/@JoeRess). I like [Wimpy](https://twitter.com/m_wimpress). They're all good guys, but they're massively overthinking this thing.

So, what _is_ a Linux Distribution.

Well, that's easy. It's in the stupid name. It needs two things. It needs Linux. And it needs to be distributed. _That's it_. Nothing more.

Almost immediately in episode 49 Martin Wimpress noted that it needs to be distributable, which is about where my agreement with what they were saying stopped. The guys dug into hypervisors and abstraction and blah blah blah. It makes for a good conversation, but they're missing the point.

Linux is a kernel. Is now and always has been. Anything that uses it and is distributed is a Linux Distribution. If tomorrow Microsoft swapped out the Windows kernel for the Linux kernel and kept literally everything else the same, Windows would then be a Linux Distribution. ChromeOS is a Linux Distribution. Android is a Linux Distribution.

The problem here is that most of what we're associating with "Linux" isn't _actually_ Linux. It's stuff that's gotten built on the Linux kernel. GNU or X or Gnome a random SDK or whatever. That stuff isn't Linux. Linux is the kernel. That's IT.

Take a Linux distro like [Ubuntu](https://ubuntu.com). Let's say that hypothetically in Ubuntu 26.04 Canonical has abstracted basically everything away from the Linux kernel. This is a hypothetical situation with a future release that isn't meant to be a prediction of any kind. It's just a hypothetical. Is this version of Ubuntu still a Linux distribution?

Yes. It's still a Linux distribution even though everything has been abstracted away from the kernel.

What if hypothetically Canonical releases an identical Ubuntu 26.04 with the Zircon kernel from [Fuchsia](https://en.wikipedia.org/wiki/Fuchsia_(operating_system)) instead of the Linux kernel. Is it still a Linux distribution.

No. No Linux. No Linux distribution. Even if literally everything else is the same and works the same and you can't tell the difference. It's still not a Linux distro.

People are always wanting to make Linux an OS. That's fine. It makes it easy to talk about, but not to go all rms on everybody but Linux is just the kernel.

OK, I'll stop now. Once more for posterity. Linux distribution = OS with a Linux kernel that's distributed. The end.

Day 10 of the #100DaysToOffload 2022 Series.
