---
title: Mike Stone
header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
post_title: A Match Made In Heaven
permalink: /a-match-made-in-heaven/
excerpt_separator: <!--more-->
layout: post
date: 2020-10-22 14:29:32
published: true
---


We’ve been using our phones to ask for information for almost as long as there have been phones. Modern phones have taken this to a new level by having automated assistants answer our questions and even anticipate our needs. The problem so far has been that these assistants don’t necessarily respect our privacy when they’re telling us the weather. 

<!--more--> 

Phones have always been a logical source of information for their users. If you don’t know something, you ask someone else. If they don’t know, you ask someone else. Your phone is an obvious way to extend the reach of the circle of people you can ask questions. People will ask questions ranging from the mundane like what a person’s phone number is, to the more complicated. I remember calling Information when I was in college to get the volume of our campus Field House. I didn’t expect an answer, but was pretty surprised when they only wanted to know if I wanted it in cubic feet or meters. Meters of course. I’m an American but I’m not a savage.

When smart phones arrived, it made obvious sense to even go beyond asking people on the phone to asking the phone itself. After all, the phone had access to the Internet, and the Internet has access to almost everything. 

Apple made a lot of noise after it purchased Siri in 2010 and integrated it with iOS. Of course, Apple wasn’t the first to do this, but they probably took it further than other companies at the time had. Google wasn’t far behind, and soon there were offerings from other companies, like Samsung and Microsoft.

Privacy has always been a concern with these assistants though. To make them respond to a keyword, they need to be listening to their surroundings all the time.  The companies that are making them do not have your best interests at heart when it comes to your privacy. Google and Amazon barely pretend, and while Apple makes a good show, I have no belief that they wouldn’t sell their customers down the river if it would make them a few extra bucks.

So, what are our options?

![](https://i.snap.as/JSJwX4X.png)

Admittedly, at this point they’re very limited. I’ve written about [Mycroft](https://mycroft.ai) quite a lot, and I’m a huge fan. Up until now, it’s been limited to computers and the [Mark 1](https://mycroft.ai/mark1/), but now seems like a perfect time to get into the mobile space.

The new Mycroft GUI designed around the [Mark 2](https://www.indiegogo.com/projects/mycroft-mark-ii-the-open-voice-assistant#/) is coming out, and it was brought up by [daver98](https://fosstodon.org/@daver98) the other day on [Fosstodon](https://fosstodon.org), wondering if it could be used on the PinePhone. I don’t have the phone right now, but it is on order and I’m looking forward to getting it. [Pine64](https://pine64.org) also has a Linux based tablet and computer. They’re inexpensive and privacy respecting. I recently received my [PineTab](pine64.com/product/pinetab-10-1-linux-tablet-with-detached-backlit-keyboard/), and I’ve been enjoying playing with it. It’s obviously a first offering, but it’s still pretty decent for the $120 American. 

[daver98](https://fosstodon.org/@daver98)’s question inspired me to give Mycroft a try on my PineTab, and it actually works, no modifications, from the defaults Linux instructions on the Mycroft site. I’m using [Mobian](https://wiki.mobian-project.org/doku.php?id=install) as the OS on the device, which is a Debian based OS with a mobile focus, and it uses the [Phosh](https://source.puri.sm/Librem5/phosh) shell from [Purism](https://puri.sm). Because of it’s Debian roots the installation of Mycroft was pretty simple. I followed the instructions from the site.

```bash
git clone https://github.com/MycroftAI/mycroft-core.git
cd mycroft-core
bash dev_setup.sh
```

I declined doing the local Mimic build after it failed on me a couple times. No errors, but locked up during a compile. Mycroft will work without a local copy of Mimic, but having it would be better for a tablet. 

The GUI is a bit of a different story. Mobian worked great for the installation of Mycroft Core, but the GUI is based on QT. Phosh and Mobian in general is not. I tried the installation anyway, and there was just a ton of stuff that needed to be installed. The installation of the GUI is very similar to the Mycroft Core installation:

```bash
git clone https://github.com/mycroftai/mycroft-gui
cd mycroft-gui
bash dev_setup.sh
```

That’s fine if you’re on a desktop, and really fine if you’re using KDE, but after the dev_setup.sh started, I experienced hours of downloads and compiles and crashes. I’m still not 100% confident it won’t work, but as of now it’s _not_ working.

I feel like this is _so_ close to being a workable solution. I would _love_ to see Pine64 and Mycroft work together to create a privacy respecting mobile personal assistant. Maybe moving from Phosh to [Plasma Mobile](https://www.plasma-mobile.org) would ease some of the library overload and make things work a little more smoothly. Some improved hardware would be a real benefit too. There’s just not enough oomph in this version of the PineTab to drive its apps and all the components that Mycroft needs to work efficiently. 

If you’ve got a Pinephone and you’re willing to give this a shot, I’d love to hear from you about how your experience went. Hopefully, Mycroft and Pine64 can get something going together in the near future. To me, they seem like a match made in Heaven.

Day 91 of the #100DaysToOffload Series.

