---
layout: post
excerpt_separator: <!--more-->
title: More On The Mycroft Mark II
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
permalink: more-on-the-mycroft-mark2
date: 2022-11-27T05:26:34.608Z
published: true
---

Not long ago, I published my [initial impressions](https://mikestone.me/mycroft-mark2-has-arrived) of the [Mycroft](https://mycroft.ai) [Mark II](https://mycroft.ai/product/mark-ii/) after I did a quick setup in a hotel room. Quick warning, I'm probably going to have several more posts as I discover new things about this device and new features become available.

<!--more-->

We got home from our quick vacation yesterday evening and the Mycroft has found it's new home on my network. The people at Mycroft have greatly streamlined the process of changing Wi-Fi networks. This is something that I've noted is even problematic for devices from Google and Amazon. When we got home and I plugged everything in, Mycroft immediately noted that it was no longer connected to a network and kicked off the setup wizard again. The process was identical to what I'd done in the hotel, but this time around I didn't have to connect the device to the Mycroft service. It automatically realized that I'd already paired the device and used the previous configuration. This is fairly new, and my Mycroft device list is littered with broken Mycroft configurations.

![Broken Mycroft Configurations](/assets/images/broken_mycrofts.png "Broken Mycrofts")

I expected the pairing to break, so I opened the portal right away during the initial setup. After I found out I didn't need to and the Mycroft just reconnected without error, I looked around a little bit. The people at Mycroft AI have been updating their portal, and there's rumor they're working on the ability to setup a Mycroft device completely offline.  

![Mycroft Settings](/assets/images/mycroft_settings.png "Mycroft Settings")

There's some good and some bad in the Mycroft settings. In the good category, there's now an option in the portal to choose which software releases you want to go with. You could do this previously, but only through a voice command or configuration on the device through SSH. Now there's an easy button to push, so I like that. There's a new toggle to do automatic updates or not, and the biggest new feature in my mind is a field to add your SSH key to for easy command line access to your device. This should be much more secure and easy compared to passing around default usernames and passwords.

In the negative category, they've taken out the voice settings. What was there before was pretty meager. They had the default AP voice which has been around since the initial release of Mycroft, and they had a newer "American" voice. At one point they had a third option, but it was removed for reasons I don't know. Those two options are now gone. I hope this is a temporary thing since the Mark 2 uses Mimic3 for it's TTS, and Mimic3 has literally hundreds of really great voice options out of the box. It's a shame to not have easy access to them. Also, they've removed the ability to easily change the wake word. Previously there were a couple different options like "Computer" or "Jarvis", but that's also now gone. I'd like to see that brought back, and maybe even an option to train up your own wake words directly in the portal. Mycroft AI has the software for that, and publishes the code so you _can_ do it, but now your options are limited.

I'm still exploring so many things about this device. There are things I love like the hardware switches on both the microphone and the camera. There are things that I'm less fond of, like the device not tracking light levels so it's not something your'e going to want in your bedroom if you actually plan on sleeping in it. I can't wait to see what I find next.

Day 22 of the #100DaysToOffload Series.
