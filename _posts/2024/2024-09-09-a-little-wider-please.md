---
layout: post
excerpt_separator: <!--more-->
title: A Little Wider Please
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
permalink: a-little-wider-please
date: 2024-09-09T10:36:37.711Z
published: true
---

This will come as no surprise to people who know me, but I spend a _lot_ of time on [Fosstodon](https://fosstodon.org). It's virtually a second job for me. As one of the two founders of the instance (along with [Kev](https://fosstodon.org/@kev)), that's probably expected. Because I spend so much time there and I keep an eye on so much stuff, I don't like to hop around between screens. I want to have a lot of stuff on the screen at the same time. To accomplish that, I use [Mastodon's](https://joinmastodon.org) advanced web interface. It allows me to put many different feeds on the screen at the same time, similar to how TweetDeck used to work in the old days. My only real day to day complaint is the columns aren't wide enough. I want a lot of information on my screen, but I would prefer my columns to be just a little wider please.

<!--more-->

So, that's the problem to solve. My columns are too narrow for my personal tastes. 

As an admin on the instance, I can make changes to our layout. The problem there is any changes I make impact the whole instance. It feels like kind of a jerk move to put a personal preference change in that would then impact the more than 11,000 people using the instance on a day to day basis, so that option is out.

There are personal preferences in Mastodon that allow you to change some of the aspects of the view you're looking at, but the width of the columns isn't one of them, so that's out too.

So, I hit Ctrl-Shift-I on my keyboard to open the developer tools, and I found the CSS class that defined the columns.

<code>
.column {
    box-sizing: border-box;
    display: flex;
    flex-direction: column;
    position: relative;
    width: 350px;
}
</code>

The column width is right there, plain as day. I simply switch 350px to 500px and like magic, my columns are wider. 

Now the problem is, I can never leave this page without losing that setting. I can easily go back in and do it again, but that's a pain in the neck and I don't want to do that. So, how do I make this change a little bit more permanent without messing with 11,000 people?

I installed an addon called [Stylus](https://addons.mozilla.org/en-US/firefox/addon/styl-us/). Stylus lets you change style sheets for yourself without making changes to the source site. You can style any site, anywhere on the Internet to your personal preferences if you are willing to expend the effort. 

I created a new Style for Fosstodon that replaces the predefined column class with my own version, bumping the width up to 500px instead of 350px. I save, and now my personal style sheet changes are automatically applied to Fosstodon every time I'm on the instance, making my columns just a little wider. Until such a time as developers of Mastodon give us some more configuration options, this will work. It's seamless and lets me apply anything from the simplistic expanding of columns to something more complex like [Tangerine UI](https://github.com/nileane/TangerineUI-for-Mastodon). 

Day 18 of the #100DaysToOffload Series.
