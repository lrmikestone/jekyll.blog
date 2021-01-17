---

header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: Fun with File Permissions – Part 4
permalink: /fun-with-file-permissions-part-4/
excerpt_separator: <!--more-->
layout: post
date: 2012-07-21 08:26:34
published: true
---


And we're back for Day 4 of the Fun with File Permissions Nerdathon! On [Day 1](https://mikestone.me/fun-with-file-permissions-part-1 "Fun with File Permissions – Part 1") we covered our standard DAC permissions. On [Day 2]( https://mikestone.me/fun-with-file-permissions-part-2 "Fun with File Permissions – Part 2") we covered getfacl and setfacl, and on [Day 3](https://mikestone.me/fun-with-file-permissions-part-3 "Fun with File Permissions – Part 3") we covered lsattr and chattr. Today we're going to close out our run by taking a quick look at the sticky bit!

<!--more-->

I'll admit right out of the gate that I know the least about the sticky bit than any of the other day's topics. If you see something I get wrong, don't hesitate to correct me in the comments. I'll update the post with the correct information.

So stick bits really started out in Unix in the 70s. You can still find pictures of it with big hair and bell bottoms. The original idea was that it was meant to be used on executable files. When the bit was flipped, the executable file would stay resident in memory so that it could be quickly loaded again. There were issues with it, like when you had to update those executables, you had to remove the bit, upgrade the file, and then replace the bit.

The functionality evolved. Linux has never supported this implementation of sticky bits.

Today, sticky bits are used to protect files from being removed when you give another user full rights to the file. So, how does this thing work?

Setting the sticky bit is easy. You just use the chmod command just like you did back on Day 1:

> chmod +t test

This will set the sticky bit on a file, or in my case directory. Doing an ls -al from inside the test directory you'll see this:

> mike@PreciseApex:~/test$ ls -al
> total 28
> drwxrwxr-t 2 mike mike 4096 Jul 20 20:15 .
> drwxr--r-- 56 mike mike 16384 Jul 20 19:20 ..
> -rwxrwxrwx 1 mike mike 0 Jul 20 20:15 file

In that directory, I've created a file called (originally), file. You can see that file has full read write execute privileges. You can also see the permissions on the . directory above oddly end with a "t" instead of an x or a - like you'd expect. That tells us that the sticky bit is active. If you were using the sticky bit on a file, a lowercase t would indicate that it's not executable, and an uppercase T would indicate that it is.

So, let's try to kill this file.

I login with my wife's account (shhhhhhhh), and do an ls -al in the same directory:

> amy@PreciseApex:/home/mike/test$ ls -al
> total 28
> drwxrwxr-t 2 mike mike 4096 Jul 20 20:15 .
> drwxr--r-- 56 mike mike 16384 Jul 20 19:20 ..
> -rwxrwxrwx 1 mike mike 0 Jul 20 20:15 file

Things look pretty much the same in this account. You can see the lowercase t on the end of the directory permissions, but other than that, it looks like I've got full rights to file. I can open that file, modify that file, and save that file. No problems, even from my wifes account. Where the sticky bit comes into play is when I try to delete the file. An rm -f results in:

> amy@PreciseApex:/home/mike/test$ rm -f file 
> rm: cannot remove \`file': Permission denied

Dun dun dun. Permission denied. If I do the same command from my user?

> mike@PreciseApex:~/test$ rm -f file 
> mike@PreciseApex:~/test$

No errors. The sticky bit will allow the owner of a file, and root (or a user with equivalent rights) to remove the file. If you want to remove the sticky bit from a file, it's as easy as:

> chmod -t file

And so our four days of Fun with File Permissions come to an end. I had a great time writing about this. It seems on the surface like it would be such a dry subject, but there are so many fun intricacies that it's so exciting to experiment with. Please, if I didn't cover something that you could have liked to see me cover, please mention it in the comments.
