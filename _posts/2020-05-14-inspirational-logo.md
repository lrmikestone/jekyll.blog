---
title: Mike Stone
header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
post_title: Inspirational Logo
permalink: /inspirational-logo/
excerpt_separator: <!--more-->
layout: post
date: 2020-05-14 11:35:41
published: true
---

Day 20 of the #100DaysToOffload Series:

It's interesting when you're an adult being able to look back on things from your childhood and see how those things really had an impact on you and where you are now. For me, one of those was a programming language called [Logo](https://en.wikipedia.org/wiki/Logo_\(programming_language\)).

<!--more-->

When I was a kid, I didn't have a computer. In fact, I didn't get my first computer until I was 17 and I'd saved up enough money to buy my own. In those days, you couldn't get a computer for a couple hundred dollars like you can now, and there was almost no market for a used computer. Because of that my first real computer experience was in school.

Don't get me wrong, I'd occasionally see a computer at the the [KMart](https://www.kmart.com) when my parents would drive to the closest "city" to pick up supplies, but I never spent any real time on one.

It was probably around 1986 when I first got to use one for more than a couple minutes at a time, and one of the things my teacher introduced to us in class was Logo.

I'd be surprised if most people had even heard of Logo. When I've brought it up with coworkers or friends over the years, they all seem to give me that "What?" look that says they've never heard of it.

Stealing this directly from Wikipedia:

>Logo is an educational programming language, designed in 1967 by Wally Feurzeig, Seymour Papert, and Cynthia Solomon. Logo is not an acronym: the name was coined by Feurzeig while he was at Bolt, Beranek and Newman, and derives from the Greek logos, meaning word or thought.
>
>A general-purpose language, Logo is widely known for its use of turtle graphics, in which commands for movement and drawing produced line or vector graphics, either on screen or with a small robot termed a turtle. The language was conceived to teach concepts of programming related to Lisp and only later to enable what Papert called "body-syntonic reasoning", where students could understand, predict, and reason about the turtle's motion by imagining what they would do if they were the turtle. There are substantial differences among the many dialects of Logo, and the situation is confused by the regular appearance of turtle graphics programs that are named Logo.

As programming languages go, it's pretty limited. It's not something you write an operating system in. What it did for me is show me how I could enter commands on a computer keyboard and watch the computer execute those commands on the screen.

![](/assets/images/pz5H6cD.png)

While this is pretty basic, it allows for some pretty complex things once you start to grasp the syntax. I haven't played around with it much since the 80s, but a few minutes allowed me to cobble together some fun things.

```
to pick_color
output pick [ 1 2 3 4 5 6 7 8 9 10 11 12 13 14 15 ]
end

to ms_square :size
if :size = 1 [stop]
setpencolor pick_color
forward :size
right 90
forward :size
right 90
forward :size
right 90
forward :size
ms_square :size - 1
end

to ms_rotate :angle
if :angle = 91 [stop]
ms_square 200
left 1
ms_rotate :angle + 1
end
```

This was built off of some random memories and [some code I pilfered from the Internet](https://linuxgazette.net/167/silva.html). It's nothing fancy, but when you run "ms_rotate 1", the output looks like this.

![](/assets/images/bbCUBT5.png)

I'd really recommend giving it a look. As I said, this is not a programming language you're going to do any serious work in. You're not going to crunch the corporate database or write the newest operating system, but it's a fun language to play in, and it's a great start for kids. Who knows, it might just inspire someone.
