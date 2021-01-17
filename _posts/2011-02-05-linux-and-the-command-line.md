---

header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: Linux and the Command Line
permalink: /linux-and-the-command-line/
excerpt_separator: <!--more-->
layout: post
date: 2011-02-05 08:29:41
published: true
---


In this day and age, pretty much anything in Linux can be done from the GUI. That being said, the command line holds such tremendous power that it really shouldn't be ignored. If you're not familiar with the Linux command line, and you have a Linux box that you can use, I'd highly recommend familiarizing yourself with it. Here's some basic commands that I use almost every day. Keep in mind, some of the syntax may vary depending on distribution.

**ls:** ls is one of the most basic and important commands. It can give you a list of files in a specified directory, or the current one if you don't specify. More or less information can be requested using flags. For example, I use "ls -alrt" almost constantly. This command and flags will show you all the files in a directory (even the hidden ones) in long listing format. Not only that, but it puts them in reverse order by modification time. In short, it puts the most recently modified files at the bottom. Very handy.

**cd:** cd is another of the most basic commands you'll run at the Linux command line. It will change the current working directory to a specified directory, or if no directory is specified, take you to your home folder. Adding a dash to the end (cd -) will take you to your previous location, which can come in very handy if you're moving around a lot, or if the path to that location is extremely long. It can also be used in conjunction with another command, which can be endlessly useful. For example, "cd /home/mike && runcommand.t", which will take you to the directory /home/mike and execute the "runcommand.t" file, and then return you to the previous location.

**cat:** cat is useful in and of itself, but it doesn't start to really shine until you add it to other commands. cat dumps the contents of a specified file out to standard out (your terminal) for your viewing. If the file is to large, then things can be a little overwhelming, but that's really where other commands can come into play. grep and awk (which we're getting to) are two of the more useful, but others that you'd never expect can be valuable. For example, using the command "time cat", will start a stopwatch that will stop when ctrl-d is pressed.

**find:** This command does pretty much what you'd expect it to do. If you're looking for a file, type of file, or basically anything in the file system, find can find it for you. This command is one that I've seen vary a lot over time and distribution, but it's usefulness is hard to question. The one problem that I have with this command is that it searches the entire file tree you specify, so if you give it /, it will search any and every path you have permissions to, which can take a great deal of time. That is where locate really shines, so it may be a better choice if you're not sure at least on a general location. I'm not going to go into examples for find, just because it's such a powerful command, I couldn't do it justice in a single paragraph.

**locate:** Searches a database of files on your computer to make finding files quicker. locate can be very handy, but it's not always installed on a system, so it's not as universal as the actual "find" command. A command (updatedb) has to be run to update the file location database, so files that are new to the system won't be found until if you run the locate command without the updatedb command.

**grep:** If you're looking for a pattern of some kind in a file, grep is the tool for the job. It can be used on it's own to find a pattern in a single or multiple files, or it can be an amazingly handy tool to pipe output from other commands to. Using the grep command by itself, you can get things like "grep -n mike \*", which would go through all the files in the current directory and find the name mike in all of them. It will print out on the page every time it finds a match, and the file name, and the line number. Very handy. Also, the command can be used like "ls -alrt|grep mike", which will give you a list of all the files in the current directory that have "mike" anywhere in their information (which could be in more places than just the file name).

**awk:** awk is kind of an interesting command, and one that's hard to really get to know. It, like grep, is an excellent pattern matching command, but I've never used awk straight from the command line like I do with grep. awk can be used to find multiple different patterns in a single command. One example would be "awk '/string1/ || /string2/' filename". This would find any lines that contained either string1, or string2 in the file filename. Very cool if you spend a lot of time parsing information from text files.

**wget:** wget is a command that I use endlessly. I'm not sure it should be included here as a "command" in Linux since it's really a stand-alone application, but it's usefulness is so great that I feel like I have to include it. wget can be used to grab files from the Internet or Intranet in almost any way you want to do it. If there's not a book on all the ways that wget can be used, there should be. My usual use is updating Wordpress themes or plugins since I've never set it up to do automatic updates, but it can be used for downloading pretty much any kind of file as long as you've got the path to that file.

There really is so many more useful commands that I haven't even touched on, I feel like I'm not giving the command line it's due. I know that I could literally type for hours here going over the multitude of possibilities and uses for all these command line tools, so I'm not feeling super super guilty. Some I didn't even touch on also so much functionality, it's really kind of embarrassing to not mention them. sed, sort, touch, etc. This doesn't even mention other applications, like ssh or ftp, which can be used to further extend the functionality of the command line.

If you've always been afraid of the command line, or you've never even tried to use it, now's your chance. Fire it up and give it a shot. You'll be glad you did.
