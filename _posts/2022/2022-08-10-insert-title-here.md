---
layout: post
excerpt_separator: <!--more-->
title: Playing With WSL2
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
permalink: playing-with-wsl2
date: 2022-08-10T10:57:34.608Z
published: false
---

I played with WSL a while back, and I suppose I technically use it daily on my work PC. I say "technically" because the way I use it is more of just a terminal window that automatically connects SSH to a remote server where my screen session is running. It doesn't _really_ do anything locally. I was listening to [episode 52 of Linux Downtime](https://linuxdowntime.com/linux-downtime-episode-52/), where [Hayden](https://twitter.com/unixterminal) was discussing his daily use of WSL, and I realized that I haven't really done much with it lately. Supposedly WSL now supports GUI applications and everything. Now is a good time to give it another shot.

<!--more-->

My first instinct was to run this on my work computer, which was followed almost immediately with the realization that this was a stupid instinct.

My second instinct was to run this on the gaming PC in my home. It's a Windows 11 machine, and while it's not _super_ beefy, it's more than capable of running the games I and my kids play. Seemed like a good choice. An additional benefit was that WSL was already installed from me plinking around with it previously.

How hard would it be to get it up to date? Shouldn't be bad, right?

I suppose those are famous last words for a reason. People say them right before things go pear shaped.

I found a guide that claimed it could get me up and running with the new WSL2 and GUI applications on a Windows 11 system. The directions seemed pretty straight forward. Update your graphics driver to version whatever at least.

1. Update WSL using wsl --update.
2. Restart it with wsl --shutdown.
3. Make sure you've got the latest updates in your installed Linux using apt update;apt upgrade -y.
4. Run GUI applications.

Even I could screw instructions that simple up.

So, I updated WSL, I restarted WSL. I ran updates on the system. I installed gedit with apt.

Now, I'm not the fastest typist in the world. I can do over 100WPM, but I'm not setting any records compared even with some of the people I know. As I stated before, the computer I was on was pretty beefy, but not _super_ so. But let me tell you, I can type "gedit" in less than a second, and that computer was more than beefy enough to show that BSOD in record time. That computer went down like I was playing [Jenga](https://www.jenga.com) with a [wrecking ball](https://yewtu.be/watch?v=D7sj7L1uLiw&t=457).

It's been a while since I've had a full BSOD. My experience with Windows is I have a lot more crashes than I do on my Linux systems, but even I'll credit Microsoft in that they're _usually_ application crashes, not the whole stupid thing. It made me a little paranoid with everything I did after that to be honest.

I made some changes, and tried again. I typed in gedit and closed my eyes before pushing Enter. This time it didn't blow the whole thing up, just failed because it couldn't connect to the display. More changes, more tries. More [DDG](https://duckduckgo.com).

Honestly, I was about to give this whole thing up as a failed experiment and get back to my life. I probably wasn't going to use it much anyway. As a last ditch, I went to the Microsoft App Store and just selected the [Ubuntu](https://ubuntu.com) 22.04 WSL installation from [Canonical](https://canonical.com). Full install of a new version of Ubuntu into WSL. I still held my breath when I hit enter on gedit, but miracle of miracles, it worked!!

So, I have a working install of WSL running GUI applications. Time to play around a little bit.

First things first, gedit ran fine. I'm typing this blog post in it right now on a Windows 11 computer. The only problem I see (or don't as the case may be) is that this is a 4K screen, gedit looks super tiny, and I'm _old_.

Second thing I tried was a web browser. I installed my go-to, Vivaldi, and fired it up. It worked too. Ish. The browser felt a little sluggish. OK, let's be honest. It felt a lot sluggish. I browsed some sites and watched a video or two. Frame rate on the video was garbage. If it was 10fps I'd be shocked. Even scrolling on this site felt delayed, and the front page is in the 20k range.

That was my impression of all the GUI apps I ran through WSL. They work fine, but they're slow compared to the Windows apps on the same computer, and they're even slow compared to the same version of the app running in Linux on slower and older hardware.

Maybe there's something here that I'm still missing, but I've spent much more time than I'd like already getting these things working. Maybe I'll keep using gedit to write my blog posts since I'm currently using [Atom](https://atom.io), which is [being sunsetted as of December 15th this year](https://github.blog/2022-06-08-sunsetting-atom/). Probably not though. It would be faster just to write in [vim](https://github.com/vim/vim).

I guess if you're stuck in Windows and you need a Linux specific tool, this is a workable middle ground. It's not something I'd day to day like Hayden is doing for anything other than regular old CLI type applications. And ssh. It's great for ssh.

Day 13 of the #100DaysToOffload 2022 Series.
