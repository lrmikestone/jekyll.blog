---
title: Mike Stone
header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
post_title: Fun with File Permissions - Part 1
permalink: /fun-with-file-permissions-part-1/
excerpt_separator: <!--more-->
layout: post
date: 2012-07-16 08:20:55
published: true
---


First, a little side story. I like messing around with my Linux computer. I have fun just seeing what the operating system can do. I like to talk about what I find, probably because learning new things excites me. I get giddy when I find out something new about something that's familiar. Unfortunately, in my house, no one cares but me. I sometimes try telling my wife about it, but to say she doesn't care is an understatement. She doesn't even pretend to pay attention when I'm talking any more.

<!--more-->

I was playing around with Linux file permissions the other day. I've been using Linux on my personal desktop for over a decade, and I use it at work as a developer. I've never spent a lot of time where I was the one who administered a multi-user environment, so file permissions were always the basics for me. In my playing the other day, I found a whole bunch of new things that I never even knew existed, and since my wife would rather watch paint dry than hear me talk about file permissions in Linux, I'm turning to you.

I'm sure most people reading this post are familiar (at least superficially) with Linux file permissions. Simply doing an "ls -l" will show you the long listing format of the current directory. The very front of the line will show you the permissions of each file in the list. An example:

> \-rwx--x--x
> drw-------

The top entry is a file, the second is a directory. Whether that file is a directory, link, or regular file is represented by the first character. - means that it's a file, d that it's a directory. Extremely simple. The next nine characters are broken down into three characters each representing the file's permissions.

The first three characters are the owner's rights, the second group of three is the Group's rights, and the last group of three is the rights of everybody else.

What the example above shows us is that the owner of the file can read, write, and execute the file, the Group and the average user on the system only show execute rights. For the directory, the owner can read and write, but no one else can do anything at all.

These rights can be changed using the chmod command at the Linux command line. There's a GUI to do this too, but I'm not going to deal with it right now because I really don't feel like it. chmod uses a numeric combination to determine what rights to set. An example:

> chmod 755 filename

This command give the file these rights:

> \-rwxr-xr-x

Basically, it gives the owner full rights to read, write, and execute. Everybody else can read and execute, but no writing.

Maybe I should be embarrassed by this, but for years I didn't understand what the 7s or 5s or whatever represented. It seemed like arbitrarily assigned values. I was wrong about that, and the way that those values are arrived at is really ingenious in it's simplicity. Let's count a little bit in Binary:

> 1 = 001 = --x
> 2 = 010 = -w-
> 3 = 011 = -wx
> 4 = 100 = r--
> 5 = 101 = r-x
> 6 = 110 = rw-
> 7 = 111 = rwx

See what I mean? Brilliant in its simplicity.

There's so much more to go into, but I've already gotten fairly long winded about this tonight. There will be at least two more parts to this little adventure I'm on. Tomorrow I want to cover getfacl and setfacl, and the day after lsattr and chattr.

If there are any more subjects on file permissions that you'd like to see covered, please let me know in comments and we can add more days.
