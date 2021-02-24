---

header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: I'm A Lazy Updater
permalink: /im-a-lazy-updater/
excerpt_separator: <!--more-->
layout: post
date: 2021-02-23 23:45:49
published: true
---

Confession time. When it comes to running updates, I'm super lazy about the whole thing. Super. I realize that keeping your system up to date is important, but I hate messing around and doing it. So, I do it the laziest way I can without not doing it.

<!--more-->

I'm not sure I'd recommend to others the way that I do my updates. Is it safe? Probably not. There have been cases where I started out with one thing and ended up with another without meaning to.

There's a particular case of converting UbuntuDDE to Kubuntu that's coming to mind, but that's another tale.

I also have more than one computer, and they don't all run the same distro.

So, how do I do this in the laziest way possible?

I alias the heck out of things.

See, almost all Linux distros these days have GUI tools that you can use to update your software with. The problem is, they don't all use the same one.

Almost all Linux distros also have a CLI tool to do updates, but the same problem exists there. They don't all use the same one.

To get around this, I've started aliasing "msupdate" to various command line tools. That's "Mike Stone", not "Microsoft" or something equally weird.

```
alias msupdate="yes|sudo pacman -Syu"
```

```
alias msupdate="sudo apt update;sudo apt upgrade -y;sudo apt dist-update;sudo apt autoremove"
```

```
alias msupdate="yes | sudo yum update"
```
You get the idea.

By using the yes tool, I'm basically just answering yes to any prompts that come up during the update process. Is this smart? Probably not, but I said I was lazy not smart.

By setting up these aliases, I'm creating a simple, one word command that I can enter on any of my computers that will update my computer to the latest and greatest without me having to think about whether I'm using Fedora, or Ubuntu, or Manjaro. It just gets the job done.

Most of the time. You know, when it doesn't blow up the whole thing.

Day 12 of the #100DaysToOffload 2021 Series.
