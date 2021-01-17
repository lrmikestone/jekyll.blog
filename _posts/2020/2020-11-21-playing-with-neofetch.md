---

header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: Playing With neofetch
permalink: /playing-with-neofetch/
excerpt_separator: <!--more-->
layout: post
date: 2020-11-21 00:18:39
published: true
---

A couple days ago, a friend of mine asked me about a screenshot she saw displaying the desktop of a Raspberry Pi 400. In the shot was a window displaying neofetch showing a Raspberry logo, and she was curious.

<!--more-->

![](/assets/images/WA5kZzH.png)

It's been a while since I've done much with neofetch other than run it with defaults, so I had to fire up the man page to figure out how to get the raspberry logo.

```
neofetch --ascii_distro Raspbian
```

In digging up this detail, I ran across some other interesting stuff, and of course fell down the rabbit hole for a couple hours.

One of the more interesting things I found is that neofetch can take ascii input from other processes using the --ascii flag.

```
neofetch --ascii file.txt
```

This will display the contents of the text file on the left hand side of the neofetch output instead of the distro logo. That's fun, and I'm going to get back to this later. 

Another thing that you can do is use the output from a command.

```
neofetch --ascii "$(fortune|cowsay)"
```

This has to be one of my favorites. 

![](/assets/images/SlfXePqH.png)

Things got a little weird from here. I thought it would be cool to pipe the fortune|cowsay through lolcat to get some fun colors. Turns out that doesn't work, which was a little bit disappointing. 

While I was researching if colors worked that way, I ran across a method to do it in a static text file, but not straight from the command line. It turns out there does seem to be a way to do that, but I never got it to work correctly.

I found that using jp2a, you can convert a JPEG to an ANSI file. This works great in cat or bat, but when running it through the neofetch command, the information on the right hand side didn't show up after that. I still haven't figured out what the heck was going on there. 

I tried converting a JPEG to a ANSI text file, which didn't work. I tried running neofetch with the --jp2a flag, which did the exact same thing, but took about 20 times longer than just dumping jp2a to a file and using that with the --ascii flag. 

I spent more time than is healthy trying to get this to work, and never really did get results that I liked. Finally, I converted a JPEG using jp2a without the color flag, which just gave me non-colored text. Then you can add values to the text ${c0}, ${c1}, etc, to change the colors on the fly. For fun, I created this file.

```
${c1}

cccccccc:;,'${c2}................${c1}',;ccccccccc
ccclc;'${c2}..........................${c1}':clccc
clc;${c2}................................${c1};ccl
cc'${c2}..................................${c1}'cc
l;${c2}....................................${c1};l
l${c2}..${c1}';;;;;;,${c2}.${c1}',;;,,${c2}...${c1},,;;,,${c2}..${c1}',;;;,${c2}...${c1}'c
l${c2}..${c1}';;;'''';;;'';;;';;;,';;,,;;;';;;${c2}..${c1}'l
l${c2}..${c1}';;;;;;;;;,${c2}..${c1}';;,${c2}.${c1},;;;;,${c2}..${c1},;;;;,${c2}...${c1}'l
l${c2}..${c1}';;;${c2}...${c1}';;;${c2}..${c1},;;,;;,',;;;,;;'';;;${c2}..${c1}'l
l${c2}..${c1}';;,${c2}.....${c1},;;;;;'${c2}.${c1}';;;;;;${c2}..${c1},;;;;;,${c2}..${c1}'l
l${c2}.....................................${c1},l
l${c2}.....................................${c1};l
c'${c2}...................................${c1}':l
c;${c2}.................................${c1}';;:l
cc${c2}.............................${c1}',;;;;;:l
cl:${c2}.........${c1};;;;;;;;;;;;;;;;;;;;;;;;;;:l
ccl;${c2}.........${c1};;;;;;;;;;;;;;;;;;;;;;;;;:l
ccll:'${c2}..........${c1}'''''''''..;;;;;;;;;;;:l
ccccclc;'${c2}..................${c1};;;;;;;;;;;:l
ccccccllc:;,'${c2}..........${c1}',;;;;;;;;;;;;;:l
```

I saved this off to a txt file in my Documents directory, and then added a simple alias to my .bash_aliases.

```
alias neofetch="/usr/bin/neofetch --ascii /home/mike/Documents/fosstodon.txt"
```

Now, every time I run neofetch, this is how my results come back. 

![](/assets/images/Tk8f1Nv7.png)

This isn't really useful for anything in the grand scheme of things, but it's kinda fun. 

A word of caution though. I'm currently using Fedora, but I noticed that when I used the --ascii\_distro flag and selected a distro that _wasn't_ Fedora, it messed with the colors. If you're using a non-Fedora distro, you may have to use the "--ascii\_distro Fedora" to make it come out with the proper color scheme.

Day 97 of the #100DaysToOffload Series.
