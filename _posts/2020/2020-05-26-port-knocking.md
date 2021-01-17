---

header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: Port Knocking
permalink: /port-knocking/
excerpt_separator: <!--more-->
layout: post
date: 2020-05-26 23:48:21
published: true
---

Day 32 of the #100DaysToOffload Series:

Once upon a time, a long time ago, I read something somewhere about "port knocking". I thought to myself, that's going to be something that's just everywhere in a few years. Turns out I was wrong about that, but I really wish I wasn't just because it's such a cool idea.

<!--more-->

Stealing from [Wikipedia](https://en.wikipedia.org/wiki/Port_knocking):

>Port knocking is a method of externally opening ports on a firewall by generating a connection attempt on a set of prespecified closed ports. Once a correct sequence of connection attempts is received, the firewall rules are dynamically modified to allow the host which sent the connection attempts to connect over specific port(s).

So, what this means for the end user is when you look at a server, it may have no visible ports open on the network. That network can be the local intranet or the Internet at large. 

Like a secret knock, you send some kind of information to a specific set of ports in a specific order. Those ports are closed, so you're not going to see anything visibly regarding whether you're right or wrong about a sequence.

A sequence can be any length, and for automated connection attempts, you could use an obscenely long sequence of ports and reduce the possibility of an accidental or brute force connection.

Once the sequence is _correctly_ entered (remember, by hitting certain ports in a certain order), then a port opens up for a specific protocol to the IP that's been knocking.

What this means is, even if you correctly enter the sequence, all the traditional means of access control are still there. You still need a username and you still need a password.

There's so much cool here I just can't imagine that this didn't take off. You can have any number of sequences configure. Hit one sequence of ports, and you can open port 22 to establish an SSH session. A different sequence of ports might open up 443 for a secure web connection. 

The possibilities aren't _literally_ endless, but close enough we could make that claim with a straight face. 

Sadly, I've never seen a service require port knocking, and most people don't seem to know what it is. I really thought that this would be commonplace long ago. Unfortunately that's just not the case. Maybe it'll still happen but I doubt it at this time.