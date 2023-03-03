---
layout: post
excerpt_separator: <!--more-->
title: Playing with the Front Matter Extension
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
permalink: playing-with-the-front-matter-extension
date: 2023-03-03T10:44:37.711Z
published: true
---
Based on the recommendation of [David Wynn](https://fosstodon.org/@FTWynn) over on [Fosstodon](https://fosstodon.org) to [Kev](https://fosstodon.org/@kev), I'm trying out the Front Matter "CMS".

<!--more-->

I've only been toying with this for a few minutes, so things are definitely still in the awkward phase. I've installed the extension in VSCodium, and everything seems to be working as expected.

There are some pretty cool "live" analytics that go on with with this extension. In the left hand panel (and this would be much better with an image), I can see that so far in my writing I've got three paragraphs and two external links.

I can also see on the left "Actions" where I can "Optimize Slug", "Start Server", or "Stop Server". The optimize slug option seems to just add a "slug: blah blah blah" thing to the front matter of the file, which I don't want, and the Start Server tries to execute the command "bundle exec jekyll serve --livereload", which fails because the term "bundle" isn't recognized. Since the server doesn't start, there's really no point for the stop button. I assume that the Start Server button is getting it's information from an above field which I haven't played with, and is currently populated with it's defaults. I'm going to look more into this in the future because I feel like this could be useful if I actually configure things correctly.

There's a couple things that are currently missing that I think would be super helpful. The first one, spell check because, ooof. My spelling *sucks*. A lot. Second one, out of the gate, I had to make some sizable changes to my front matter to get it to my traditional format. I'd like to be able to edit the defaults. There's an option in the left hand panel to create a template, which I'm going to play with in a few minutes which might answer this request (probably should have done that before I wrote this, but sometimes things just happen out of order).

I'm going to keep playing around with it because I do think this could be a viable solution for editing my blog. I've been using [Atom](https://github.com/atom/atom), but it's been basically EOLed at this point. It still works for the time being, but there aren't going to be any further updates and who knows how long I'll be able to say that. I've also been playing around with Code Spaces directly on GitHub. It's been fine, but some extra features wouldn't be unwelcome.

Oooo, eight paragraphs and three external links. Look at me go! Maybe next time I'll try an image!

Day 3 of the #100DaysToOffload Series.
