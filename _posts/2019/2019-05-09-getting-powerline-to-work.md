---

header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: Getting Powerline to Work
permalink: /getting-powerline-to-work/
excerpt_separator: <!--more-->
layout: post
date: 2019-05-09 09:21:30
published: true
---

I’ve been testing out Ubuntu 19.04 lately, but the shell has been feeling a little naked. In the past I’ve really liked the way powerline updates the looks of things so I thought that I’d install that to improve the asthetic. I had a few problems finding instructions that work in the newest version of Ubuntu, so I thought I’d post my results here.

<!--more-->

```
sudo apt-get install python-pip
git clone https://github.com/powerline/fonts.git && cd fonts && sh ./install.sh
```
Once that’s done, you need to add this stuff to respective files.

__.vimrc__

```
set rtp+=/usr/local/lib/python2.7/dist-packages/powerline/bindings/vim/
set laststatus=2
set t_Co=256
```

__.bashrc__

```
if [ -f /usr/local/lib/python2.7/dist-packages/powerline/bindings/bash/powerline.sh ]; then
source /usr/local/lib/python2.7/dist-packages/powerline/bindings/bash/powerline.sh
fi
```

This seemed to get everything up and running fine.