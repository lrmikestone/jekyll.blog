---

header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: Migrating Posts To Jekyll
permalink: /migrating-posts-to-jekyll/
excerpt_separator: <!--more-->
layout: post
date: 2021-01-18 19:30:49
published: true
---

I wrote in my last post about moving from [write.as](https://write.as) to Jekyll. [Kev](https://fosstodon.org/@kev) wrote an extensive [guide](https://kevq.uk/how-to-build-jekyll-site-simple-css/) on how to create a Jekyll site using [Simple.css](https://kevq.uk/simple-css-framework/), the hardest part about this process (other than customizing the new blog to my personal tastes, which I'm still working on) was moving my old content over to the new blog. Here's how I did it.

<!--more-->

The first thing to do is somehow get the content from write.as. Fortunately, they've been nice enough to include an export option in the menu.

![](/assets/images/2021-01-18-19-22-38-export-menu.png)

After that, you're given a few different choices.

![](2021-01-18-19-39-00-export-options.png)

This is where things kind of went off the rails for me at first. I downloaded them all because I didn't know which would be the easiest to work with.

It turns out that csv is the worst option. It gives you the contents of the your posts, so if that's all you're interested in, you're probably going to be fine. What it didn't give me that I wanted was a way to preserve the date that the post was made.

I've been dragging around many of my old posts, and [my oldest](https://mikestone.me/why-linux/) dates back to 2002. Honestly, that wasn't even originally a blog post, it was a stand alone page on my website. I'm getting off into the weeds here though.

I didn't want all my posts to have a new published date in 2021, so I started looking at other options. I next chose the prettified json. There was no real difference between it and the other json version, and this one was prettier.

I spent some time digging through the json, and even wrote some really basic Python to try to export what I needed from there, but I just don't have the skills with Python to make that work. After spending an hour or more beating my head against the wall trying to make that work, I took a closer look at the text option.

I initially dismissed the text option because it basically just exported the markdown files as text in a big zip document. The markdown as pretty much exactly as I'd entered into the page, with no further information.

This is where muscle memory saved me.

![](2021-01-18-19-45-55-terminal-with-files.png)

I just randomly typed in "ls -alrt" in my terminal, which displays all the files in chronological order. I noticed that the text files were dated as being last modified on the date they were created on the site.

The files had the published date!

From there, things were really pretty simple. I had almost 180 posts that I wanted to move over, so I didn't wan to do this manually, but a script was a pretty simple option since all the information I needed was there and available.

```
#!/usr/bin/bash

for x in *.txt
do
  FILE_NAME=`echo ${x}|cut -d_ -f1`
  FILE_DATE=`stat ${x}|grep Modify|cut -d" " -f2`
  FILE_TIME=`stat ${x}|grep Modify|cut -d" " -f 3|cut -d. -f1`
  FILE_NAME_NEW="${FILE_DATE}-${FILE_NAME}.md"
  POST_TITLE=`head -1 ${x}|sed s/"# "//`
  TAIL_VALUE=`cat ${x}|wc -l`
  TAIL_VALUE=$((${TAIL_VALUE}-1))

  echo Converting ${x} to ${FILE_NAME_NEW}

  echo --- >> ${FILE_NAME_NEW}
  echo title: ${POST_TITLE} >> ${FILE_NAME_NEW}
  echo header: Mike Stone >> ${FILE_NAME_NEW}
  echo description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon >> ${FILE_NAME_NEW}
  echo permalink: /${FILE_NAME}/ >> ${FILE_NAME_NEW}
  echo 'excerpt_separator: <!--more-->' >> ${FILE_NAME_NEW}
  echo layout: post >> ${FILE_NAME_NEW}
  echo date: ${FILE_DATE} ${FILE_TIME} >> ${FILE_NAME_NEW}
  echo published: true >> ${FILE_NAME_NEW}
  echo --- >> ${FILE_NAME_NEW}
  echo >> ${FILE_NAME_NEW}
  tail -${TAIL_VALUE} ${x} >> ${FILE_NAME_NEW}

done
```   
The script above was able to extract the information from the text files and place it where it belonged in the front matter of the new markdown files for Jekyll. From there it was a simple matter of dropping them into the proper directory and publishing the page with all my old content.

Day 4 of the #100DaysToOffload 2021 Series.
