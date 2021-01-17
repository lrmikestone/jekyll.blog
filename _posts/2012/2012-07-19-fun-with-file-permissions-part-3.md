---

header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: Fun with File Permissions – Part 3
permalink: /fun-with-file-permissions-part-3/
excerpt_separator: <!--more-->
layout: post
date: 2012-07-19 08:24:57
published: true
---


Welcome to back to Mike's 4 Days of Extreme Geekery (yes, Geekery is a word I just made up)! On [Day 1](https://mikestone.me/fun-with-file-permissions-part-1 "Fun with File Permissions – Part 1") we talked about traditional Unix file permissions. On [Day 2](https://mikestone.me/fun-with-file-permissions-part-2 "Fun with File Permissions – Part 2") we talked about setfacl and getfacl. Today, I want to go over chattr and lsattr!

<!--more-->

What these two commands do is pretty self explanitory. lsattr shows you the attributes currently on a file or directory, and chattr changes those attributes. You use either + or - to add or subtract attributes.

>  mike@PreciseApex:~/mike/test$ lsattr mike
>  -------------e- mike
>  mike@PreciseApex:~/mike/test$ sudo chattr +i mike
>  mike@PreciseApex:~/mike/test$ lsattr mike
>  ----i--------e- mike
>  mike@PreciseApex:~/mike/test$

The first time I found about the file attributes in Linux, I thought right away, "Hey, this is kinda like DOS!" I know what you're thinking, and trust me if I could kick my own ass for saying that, I would. It turns out that the file attributes in DOS/Windows suck compared to the Linux version (like most things in DOS/Windows when compared to their Linux counterparts). Quick comparison will show you that DOS/Windows has 5 attributes. They are:

>  R: Read Only
>  A: Archive
>  S: System
>  H: Hidden
>  I: Index

What each of these attributes does is, well, who cares. We're not talking about DOS/Windows. The Linux version of file attributes is significantly more advanced. Available file attributes are:

>  A: The date of last access is not updated (only useful for reducing disk access on laptops)
>  S: The file is synchronous, the records in the file are made immediately on the disc.
>  a: The file can be opened in addition to writing
>  c: The file is automatically compressed before writing to disk, and unpacked before playback.
>  D: The case is synchronous (see:S)
>  d: The file will not be saved by the dump
>  I: Can not be fixed by chattr only listed by lsattr
>  i: The file / directory can not be amended, deleted, renamed or linked symbolically, not even by root.
>  j: Mount file system with "data=ordered" or "data=writeback", and files are written to the log before the file.
>  s: When the file is destroyed, all data blocks are being released to zero.
>  T: Usable from version 2.5.46 kernel.
>  u: If the file is deleted, its content is saved, it allows the user to seek its restoration.
>  E: Experimental, can detect an error of compression can not be fixed by chattr, but can be listed by lsattr
>  X: Experimental shows that the raw data to a compressed file can be accessed directly.
>  Z: Experimental, provides information on the status of a compressed file.

As you can see, there are quite a few more file attributes that do significantly more. Some of these are more interesting than others. I'm only going to touch on a few of them that I find interesting. Of course, consult your man page for more information on the others.

The +A attribute basically locks that last accessed time to what it's currently set at. Set this attribute, and you're fill will be frozen in time. No more accesses will be recorded.

A really interesting one is the +c. This is an on the fly compression. If you add the +c attribute to an empty directory, everything you write to that directory will be compressed as if you stuck it in a file using gzip9 compression. One odd thing about it is that ls -l doesn't show a darn thing. You can't see the compression. I've heard that you can see it with a du, but when I was playing around with it, I didn't see that.

I have to say that my favorite is the +i. I'm not sure what the i stands for, but I'm going with "Immortal".

> mike@PreciseApex:~/mike/test$ lsattr mike
> ----i--------e- mike
> mike@PreciseApex:~/mike/test$ rm mike
> rm: remove write-protected regular empty file \`mike'? y
> rm: cannot remove \`mike': Operation not permitted
> mike@PreciseApex:~/mike/test$ sudo rm mike
> rm: cannot remove \`mike': Operation not permitted
> mike@PreciseApex:~/mike/test$ sudo rm -f mike
> rm: cannot remove \`mike': Operation not permitted

With the +i attribute set, this file can not be deleted. Not by the owner, not by root, not by anybody. You have to be root (or equivalent) to set this attribute, so no messing with your admins on servers you don't own, but still fun.

The last two kind of have to be taken together. +s and +u. If a file with the s attribute is deleted, the blocks where it lived are zeroed out and written to the disk. Bye bye file. Good luck retrieving that one. In contrast, the +u makes sure that the files information is saved just in case you want to undelete it later. +s and +u are opposites. Oddly, you can set both flags on a single file. Not sure what that would do. If you know, throw it into the comments.

That's an extremely high level view of the file attributes in Linux. I could probably spend weeks on these two commands going over what they do, but I have the feeling that I'd probably lose most of you in that amount of time. Tomorrow, I'm going to take a look at sticky bits! Bound to be fun!
