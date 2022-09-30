---
layout: post
excerpt_separator: <!--more-->
title: Tell Me A Story
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
permalink: tell-me-a-story
date: 2022-09-29T05:26:34.608Z
published: true
---

I've never been much of a podcast person. I'm not sure what it is about them, but they've just never been a thing for me. I do read a lot of stuff on the Internet, but lately even that has been harder to do just because I'm busy with other things. Today [Joel](https://fosstodon.org/@joel) published on [Fosstodon](https://fosstodon.org) something that I feel like I should have been aware of but wasn't. So, I've decided to try a _different_ solution.

<!--more-->

I'm not sure this is going to work. Well, it works, but I'm not sure I'm going to keep doing it because it's kind of a pain. Parts of it anyway.

I mentioned earlier that I'm not much of a podcast person. About the only podcasts I listen to are [Joe Ressington's](https://joeress.com). The problem with so many podcasts is that they're too long. I always get interrupted and then I have to try to rejoin the conversation later and that just annoys the hell out of me. I think that's why I've been able to stick with the collection of podcasts that Joe Ressington does. He keeps things interesting and on the shorter end of things. That might sound like a backhanded compliment, but too often podcasts ramble about useless garbage to try to fill time and to me, that's just a waste.

What does my distain for overly windy podcasts have to do with anything you ask?

I still spend time that I could be listening to podcasts. Working out. Walking. Cleaning my garage. That kind of thing. I usually don't listen to podcasts because (again), they're too long and I don't get that much time to listen.

I've run into the same problem with written material lately too. I have a whole lot of news that I'd really like to read, but can't because I'm occupied with other things.

Today, I roughed up what I hope will be a compromise. I was trying to get through an article for the third or fourth time when I was interrupted again. I thought to myself, "I just want someone to read this to me while I'm working on this other thing." There are tools to do that, but the browser based ones that I've found are kind of garbage. Plus, they tend to use TTS engines from Amazon or Google, which creeps me out from a privacy perspective. 

I've made no secret of the fact that I'm a huge fan of [Mycroft](https://mycroft.ai). Well, the people at Mycroft created their own TTS engine called Mimic (it's on version 3 now). Mimic installs locally with a deb and you can just dump whatever text you want to it at any time. It took about a minute to rough this up.

```
#!/usr/bin/bash

for x in *.txt
do
  RAWFILE=`echo "$x"|cut -d. -f1`
  echo Processing file "${x}"...
  {
    cat "${x}" | mimic3 > "${RAWFILE}".wav
  } &> /dev/null
  ffmpeg -i "${RAWFILE}".wav -acodec mp3 "${RAWFILE}".mp3 &> /dev/null
  rm "${RAWFILE}".wav
done
```
What this does is takes the text from a file and sends it to Mimic3. Mimic3 generates a wav file, and then I use ffmpeg to convert that wav to an mp3. I haven't found a way to go directly to mp3. If I figure something out, I'll update this article. Once I have the mp3 files I can drop those on my cell phone and then I have a series of news articles that are less than 10 minutes to "read".

I'm hoping this is going to let me get more "reading" done, but right now my biggest obstacle is getting the articles into the text format. Too many pages insert stupid ads or links to other articles right in the middle of everything. If you don't want that stuff read out to you, you have to go through and pull that out manually (at least at this point). This could be the thing that is the deal breaker with this process. The point is I don't want to spend a lot of time on it, and if I have to spend a lot of time parsing through the articles _before_ I read them, that's voiding the whole point. We'll just have to wait and see if this is going to work.

If anybody has any bright ideas on how to get the raw text out of these articles without a ton of overhead, I'm all ears. I just wish more people put the full text of articles into the RSS feeds. That seems like an obvious solution, but then they miss out on all that ad revenue.

Day 19 of the #100DaysToOffload 2022 Series.
