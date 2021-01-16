---
title: Mike Stone
header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
post_title: Fun with File Permissions – Part 2
permalink: /fun-with-file-permissions-part-2/
excerpt_separator: <!--more-->
layout: post
date: 2012-07-18 08:21:39
published: true
---


Now, where were we? Oh yea, so the day before yesterday (I know I said I was going to do this daily, but the series finale of Eureka was on!) we covered what's commonly thought of as the traditional Unix file permission. Permissions are applied using chmod, and can be seen as a -rwxrwxrwx at the front of the line after doing an ls -l.

<!--more-->

OK, that's all well, and good, but what do you do if you want to grant permissions to just a single person, or add different permissions to multiple groups? That's where the crazy combo of setfacl and getfacl come in. I have a test file called "test". If I do an ls -l on the file, I see these permissions:

> \-rw-r----- 1 mike users 0 Jul 15 22:35 test

So, this tells us that I'm the owner, and users is the group the file is assigned to (my group being the default). So, with these permissions, I can read and write to the file, anybody in the group users can read the file, and no one else can do anything with the file. Standard 640.

At this point, if I use one of our commands, the getfacl, I'll see a little bit different information, but still basically the same:

> \# file: test
> # owner: mike
> # group: users
> user::rw-
> group::r--
> other::---

But what if I want to give my wife permissions to that file, but no one else in the group users. One possibility is that I could create a separate group with just my wife and I in it and assign that group rights, but then the users group loses rights to the file. The simple solution is to just add my wife using this command:

> setfacl -m u:amy:rx test

If I do an ls -l after this command, there's only one slight change to tell us that we've done anything.

> \-rw-r-----+ 1 mike users 0 Jul 15 22:35 test

You can see now that there's a + after the standard -rwxrwxrwx. This is a good sign. It means that our command was successful. If you were to do the getfacl now, you'd see this:

> \# file: test
> # owner: mike
> # group: users
> user::rw-
> user:amy:r-x
> group::r--
> mask::r-x
> other::---

You can see now that the user "amy" has been added to the permissions of the file. If you were to do an ls -l command, you'd see that the group permissions would be replaced with the value in the "mask" field. This value reflects the last permissions applied to the file. A similar command can be used to add groups:

> setfacl -m g:plex:rwx test

This gave full permissions to any users in the "plex" group. Now my getfacl looks like this:

> \# file: test
> # owner: mike
> # group: users
> user::rw-
> user:amy:r-x
> group::r--
> group:plex:rwx
> mask::rwx
> other::---

Through all of this, if I were to do an ls -l, the mask on that line would now show the permissions of the "plex" group, not the user "amy".

> \-rw-rwx---+ 1 mike users 0 Jul 17 21:23 test

And if in the end, you decide that you would rather return to the standard -rwxrwxrwx Unix type permissions, it's as easy as this:

> setfacl -b file

After that command, the + is gone, and the getfacl returns to it's defaults.

>  -rw-r-----  1 mike users  0 Jul 17 21:23 test
> 
> \# file: test
> # owner: mike
> # group: users
> user::rw-
> group::r--
> other::---

Really, this is just scratching the surface. There is so much more that you can do with this, but again, I've gone on too long. Tomorrow (probably), I'm going to cover lsattr and chattr, and the day after I want to take a look at sticky bits!
