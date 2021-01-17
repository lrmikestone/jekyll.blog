---

header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: An Amateur Mycroft Skill
permalink: /an-amateur-mycroft-skill/
excerpt_separator: <!--more-->
layout: post
date: 2020-11-13 17:20:34
published: true
---

One of my favorite things about #Mycroft is its open nature. It's not as advanced as Alexa, Google's Assistant, or even Siri and Cortana, but it's infinitely more private and just as infinitely more customizable. Today I thought I'd run through a really quick and basic skill creation.

<!--more-->

Creating a new skill for Mycroft is virtually childs play. The hardest part is getting SSH access if you've got a Mark I. If you're coming from a Linux system, or using a #Picroft, you'll have this part already.

From the command line, you're going to want to activate the virtual environment that was created for Mycroft during the installation. This is as easy as navigating to the installation location and typing the following command:

```
. venv-activate.sh
```

Once you've got the virtual environment activated, the hard part is already over. Next, type this into the command line:

```
bin/mycroft-msk create
```

This wizard will walk you through everything you need to do!

```
(.venv) [mike@localhost bin]$ ./mycroft-msk create
Enter a short unique skill name (ie. "siren alarm" or "pizza orderer"): HowManyLights 

Class name: HowmanylightsSkill
Repo name: howmanylights-skill

Looks good? (Y/n) Y
Enter some example phrases to trigger your skill:
- How many lights are there 
- How many lights do you see
- 
Enter what your skill should say to respond:
- There are four lights
- 
Enter a one line description for your skill (ie. Orders fresh pizzas from the store):
- Tells you how many lights there are
Enter a long description:
> Obeys the chain of command.    
> 
Enter author: Mike Stone
Go to Font Awesome (fontawesome.com/cheatsheet) and choose an icon.
Enter the name of the icon: lightbulb
Pick a color for your icon. Find a color that matches the color scheme at mycroft.ai/colors, or pick a color at: color-hex.com.
Enter the color hex code (including the #): #FEE255


Categories define where the skill will display in the Marketplace. It must be one of the following: 
Daily, Configuration, Entertainment, Information, IoT, Music & Audio, Media, Productivity, Transport. 
Enter the primary category for your skill: 
- Entertainment
Enter additional categories (optional):
- 
Enter tags to make it easier to search for your skill (optional):
- 
For uploading a skill a license is required.
Choose one of the licenses listed below or add one later.

1: Apache v2.0
2: GPL v3.0
3: MIT
Choose license above or press Enter to skip? 
Does this Skill depend on Python Packages (PyPI), System Packages (apt-get/others), or other skills?
This will create a manifest.yml file for you to define the dependencies for your Skill.
Check the Mycroft documentation at mycroft.ai/to/skill-dependencies to learn more about including dependencies, and the manifest.yml file, in Skills. (y/N) n
Would you like to create a GitHub repo for it? (Y/n) n
Created skill at: /opt/mycroft/skills/howmanylights-skill
(.venv) [mike@localhost bin]$
```

And that's it! You now have a very basic, working skill that will take in input and output a fixed response. Given, this skill isn't terribly useful, but what it does do is create the basic structure your skill requires to be loaded into Mycroft and used. 

It's handy if you want to create skills that will give predefined answers to questions, but it's also a base that can be used to create a more advanced skill later on. 


Day 96 of the #100DaysToOffload Series.