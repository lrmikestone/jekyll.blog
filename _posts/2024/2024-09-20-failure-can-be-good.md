---
layout: post
excerpt_separator: <!--more-->
title: Failure Can Be Good
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
permalink: 20240920-failure-can-be-good
date: 2024-09-20T10:36:37.711Z
published: true
---

I think most of us have it in our head that failure is a bad thing. It's understandable considering how we normally define failure. Failure is "not succeeding", but sometimes not succeeding is just as good as succeeding.

<!--more-->

Today I wrote a script. I was watching for a new game to show up in the Steam library, but so far all my searches came back with zero matches. Being the lazy cur I am, I decided to script the process. I grabbed the URL for the search used a wget and a grep with some strategically placed cuts to pull the 0 results found out of the HTML. Easy peasy. Then I stripped the 0 off the front and used that to power a while look with a sleep value of 10 minutes. 

**SHAZAAAAAAAM!!!!** Working script to tell me when the game I was looking for showed up.

Then I left and went to a football game. 

I came home and checked the script to find it crashed and burned and not running. In short, my attempt at automation had failed while I was gone. 

So this begs the question. Why did the script fail? Well, when I wrote it I didn't spend a whole lot of time looking at the "found" state. I assumed it would work exactly the same as the "not found" state, so that's what I coded for. It didn't work that way, so my code failed. But see here's the thing. In failing it still worked. It told me the game I was looking for was now available to add to my wishlist in the Steam store. So, how is this failure different than succeeding? The message on the screen wasn't as pretty? 

Today I wrote a script that completely failed, and it worked great.

Day 24 of the #100DaysToOffload Series.