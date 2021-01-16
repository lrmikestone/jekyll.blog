---
title: Mike Stone
header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
post_title: Migrating from Wordpress to write.as
permalink: /migrating-from-wordpress-to-write-as/
excerpt_separator: <!--more-->
layout: post
date: 2020-03-08 19:07:06
published: true
---

It's been literal years since I've faithfully updated my blog. The old content has been sitting idly on [Wordpress.com](https://wordpress.com) in a free account since I canceled the server I had [GoDaddy](https://www.godaddy.com) hosting for me. I planned to self host, but having a pseudo-large family and a job that doesn't understand boundaries made the idea of hosting infrastructure in my home less and less appealing. So, things basically stagnated. 

Lately I've been feeling the urge to write again, so I started looking at my options. I still didn't want to host in my home. I considered Wordpress since my posts were already there, but it just seemed like more than I needed or wanted. Most of the posts I'd put up before were basic syntactically. To make a long story short, I settled on [write.as](https://write.as).

<!--more-->

write.as was an obvious choice for me because of its integration with the Fediverse. My friend Kev and I founded [Fosstodon](https://fosstodon.org) two and a half years ago, and it's grown to almost 8500 users as of this writing. I interact with some really great people there on a day to day basis, and having a blog connected directly to the Fediverse seemed like a really great option. 

The next big challenge was I didn't want to lose my old content. Not all of it at least. Previously I'd used my blog for some pretty frivolous things, and I didn't want to pull all of that over, but there were several things I did want to keep. How do I get content from [Wordpress](https://wordpress.com) to [write.as](htts://write.as)?

Kev came through for me on this one, and [wrote an article on his blog](https://kevq.uk/how-to-convert-wordpress-to-markdown/) detailing how to export the content from [Wordpress](https://wordpress.com) to markdown, which is what [write.as](https://write.as) uses for its formatting. The [Wordpress](https://wordpress.com) posts are exported to individual directories containing a file called index.md and a directory with any images that were embedded into the post. The vast majority of the images I'd used were decorative, and not really relevant to the article, so for the most part I didn't need them.

So, how to get the index.md files into [write.as](https://write.as), _and_ maintain the original dates. Turns out that last part was a little bit of a sticking point. There were cli tools for [write.as](https://write.as), but they didn't let you change the date a post was being made. I couldn't find a way to do it through the web interface either. I couldn't find any way to do that other than the through the API.

Now, I went to college for Computer Science, but I haven't done serious development for a very long while. When I do write something, it's usually very basic to automate a process at work or simplify something at home. I've been learning Python lately, and this seemed like a good opportunity to give myself a homework assignment.

### File format

Using the [write.as](https://write.as) API and Python, I wrote myself a little script that can post the files retrieved using Kev's method and still retain the original post dates. This is how those files were arranged.

```
---
title: "Title of the Post"
date: "2020-03-08"
---

And here's the body of the post. This part is written in traditional markdown.
```

So, the script just had to pull the title, the date, and the body into memory and send it out to [write.as](https://write.as) in a way that would be understood and placed into my new blog.

### The Code

Here's the code that I came up with. Please keep in mind, I'm a Python beginner. I put off making this post for quite a while planning on cleaning this up so people wouldn't think I'm a massive idiot after looking at this code, but I'm finally just doing it and hoping anybody who reads this will have mercy on me.

```
import requests
import json
import time

blogPostBody = ""
msPassword = "thisIsNotMyRealPassword"

msFile  = open("index.md", "r")
msFileAll = msFile.readlines()
msFileLines = len(msFileAll)

print ("Read " + str(msFileLines) + " lines from index.md.")
msTitle = str(msFileAll[1])[8:-2]
msPostYear = str(msFileAll[2])[7:11]
msPostMonth = str(msFileAll[2])[12:14]
msPostDay = str(msFileAll[2])[15:17]
print ("Extracted Information: ")
print ("  Title: \"" + str(msTitle) + "\".")
print ("  Date: \"" + msPostYear + "-" + msPostMonth + "-" + msPostDay + "\"")

currentTime = msPostYear + "-" + msPostMonth + "-" + msPostDay + "T" + time.strftime("%H:%M:%S") + "Z"

for i in range(5, msFileLines):
   blogPostBody += str(msFileAll[i])

r = requests.post("https://write.as/api/auth/login", json={"alias": "mikestone", "pass": msPassword})

if r.status_code is 200:
  print ("Authorization granted")
else:
  print ("Something went sideways with your access.")
  exit()

tokenToSend = "Token " + r.json().get("data").get("access_token")
msHeaders = {"Content-Type": "application/json","Authorization": tokenToSend}
msBody = {"created": currentTime, "body": blogPostBody, "title": msTitle}

t = requests.post("https://write.as/api/collections/mikestone/posts", headers=msHeaders, json=msBody)

if t.status_code is 201:
  print ("Your post was made successfully.")
else:
  print ("Yea, that didn't work. You need to figure out why.")

d = requests.delete("https://write.as/api/auth/me", headers={"Content-Type": "application/json","Authorization": tokenToSend})

```

I know it's not pretty, but it works. After it was done, I went through my old posts and used my script to post them to the new blog. This entry is my first official post on this blog.

As I said before, I've been wanting to write again, and now that I've migrated over to [write.as](https://write.as), things should be easier to maintain. Hopefully I can get more content pushed out to the blog on a more regular basis.