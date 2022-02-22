---


description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: A Different Kind Of Shell
permalink: /a-different-kind-of-shell/
excerpt_separator: <!--more-->
layout: post
date: 2020-05-01 13:21:16
published: true
---

Day 7 of the #100DaysToOffload Series:

People can be passionate about their tools, myself included. I have two, maybe three tools that are absolutely essential to my day. My browser, and my shell (and if forced, my work email client). For years I used bash simply because it was the default and it did everything I needed it to do. Then, I switched to [xonsh](https://xon.sh).

<!--more-->

I guess the main reason I was even interested in switching was a moderately recent decision to learn Python. It’s been on my “To Do” list for a while, and it just never seemed to get done. Finally, I managed to scrape up the motivation to start.

My biggest problem is I don’t have a lot of free time on my hands, and I wasn’t using Python on a day to day basis, so even when I learned something, it would fade quickly and I’d be back at the beginning. I needed to find a way to force myself to use it daily. 

## xonsh

I ran across an article on [opensource.com](https://opensource.com) titled [Why I Love Xonsh](https://opensource.com/article/18/9/xonsh-bash-alternative). It was written by [Moshe Zadka](https://opensource.com/users/moshez), and it showed me a different kind of shell. It looked and worked a lot like other shells I was more familiar with, but it was based on Python. It can use Python specific syntax like this:

>$ print("Mike Was Here")
>Mike Was Here

_Or_ it can use bash style sytanx:

> $ echo "Mike Was Here Too"
> Mike Was Here Too

It can even use them together!!

>$ for i in range(3):
>  echo "Mike Was Here"
>
>Mike Was Here
>Mike Was Here
>Mike Was Here

## xontribs

There are also xonsh contributions (called [xontribs](https://xon.sh/xontribs.html)), which means I can install powerline with a simple command.

> xpip install xontrib-powerline

There are a wide variety of xontribs for you to use, and installing them is just as easy. 

## Annoyances

There are some things about it that still get me. One of my personal habits is I like to look at “ls” output on a clean screen. My fingers have gotten used to the “clear;ls -al” over the years I use it so much. This command does _not_ work in xonsh. I had to create a function that accepted parameters to emulate this functionality. So now I type “mls” or “mls -al” and it clears the screen prior to output.

## Not Unique

Most of the functionality in xonsh can be emulated or replicated in bash or ksh. Other than the tight integration of Python, xonsh’s features can be replicated with scripts or additional apps. Still, I’ve really enjoyed using it. If you’re open to looking into new shells or even if you’re just not super tied to the one you’re using, I’d recommend giving it a try. 