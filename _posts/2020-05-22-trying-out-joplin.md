---
title: Mike Stone
header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
post_title: Trying Out Joplin
permalink: /trying-out-joplin/
excerpt_separator: <!--more-->
layout: post
date: 2020-05-22 23:17:44
published: true
---

Day 28 of the #100DaysToOffload Series:

Throughout the course of my day I read a lot of things. Articles, emails, books, web pages, toots, etc. Often times I find myself wanting to revisit material because I can't devote the attention to it I want to at the time I've found it. More often than not, I just [leave the browser tab open](https://mikestone.me/my-problem-with-tabs) until i can come back to it. Sometimes I use a note taking app to keep track of details for later.

<!--more-->

I started using an app called [Journal](https://usejournal.com) to keep track of miscellaneous, random thought strings that I hadn't found the end of. It let me organize links and text and images and stuff from various apps all in one place. I really liked that idea.

Unfortunately, the implementation wasn't the best for me personally. The developers were more focused on the "iMarket" than anything else, so the majority of the places it worked didn't work for me.

![](https://i.snap.as/623B1ap.jpg)

After [Kev](https://fosstodon.org/@kev) conned me into firing my blog back up again, I started using [markdown](https://mikestone.me/struggles-with-syntax-highlighting) for publishing my blog on [write.as](https://write.as). As I became more familiar with the syntax, I thought it would be a good way to do more than just blogging, and one of those things was notes.

Up until yesterday, I just had a file in my Documents directory called "RandomNotes.md". In that file I was keeping (you guessed it) random notes. Yesterday when I published my [Struggles With Syntax Highlighting](https://mikestone.me/struggles-with-syntax-highlighting) article, I got a reply back from [@vikingkong@fosstodon.org](https://fosstodon.org/@VikingKong) regarding [Joplin](https://joplinapp.org).

>Joplin https://joplinapp.org/ note taking app is heavily based on markdown and has quite a good in-built markdown editor with syntax highlighting and live preview. I use it on daily basis.
>
But actually, in most cases Vim with a couple of plugins is totally enough for me, moreover I find syntax highlighting even distractive, especially in coding.

This inspired me to try it.

Download was super easy as it's just an AppImage. Nothing to do other than find a place to plop it down. Throw a +x onto the chmod and we're in business.

![](https://i.snap.as/KvnBj6e.png)

I've been using this for all of twenty-four hours now, and so let me give you my super experienced opinion on the software, specifically compared to Journal which I've been using.

Joplin starts out with a single Notebook that has some reading material in it on how to use the application. It seems pretty comprehensive, but I've noticed some of the information in the "HowTo" doesn't seem to match the application. That's not a huge deal as the app seem pretty easy to use. Most of the features are pretty self explanatory. I only really looked at the documentation when something didn't quite work the way I expected, and it was enough to give me a hint as to how it worked to figure it out for real.

Notes can be organized by Notebooks or by Tags. Notes from different Notebooks can be in the same tag. My initial impression after twenty-four hours of use is that this is a cool way to do this. 

The syntax seems pretty standard. There are way more capabilities in the syntax than I'm going to use. Such as this:

```
$$
f(x) = \int_{-\infty}^\infty
    \hat f(\xi)\,e^{2 \pi i \xi x}
    \,d\xi
$$
```

This translates into this in Joplin:

![](https://i.snap.as/rtQ9i4o.png)

I'm never going to use this, but it's cool that it's there.

It also allows for synchronization with multiple different services, like Dropbox and Nextcloud. Unfortunately Synology isn't one of them, but I can work around that with a mounted drive for the most part. I'm not sure how I'm going to make that work with my phone yet.

For the security conscious, the notes can be encrypted. I haven't played around with this one that much, but since I've got it configured to start Joplin to the tray on startup that would probably only ask for a password on the first use. 

It's also got a web plugin that, for me, matches the functionality I did have with Journal. When you add in the encryption, working apps on platforms not created by Steve Jobs, and a more open nature, it's really a no brainer. 

Oh, and it let me import my "RandomNotes.md" file straight into a notebook, so I didn't even have to copy and paste it. Bonus.