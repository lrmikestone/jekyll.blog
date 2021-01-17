---

header: Mike Stone
description: Mostly The Lonely Howls Of Mike Baying His Ideological Purity At The Moon
title: Mycroft v20.2.4 Released
permalink: /mycroft-v20-2-4-released/
excerpt_separator: <!--more-->
layout: post
date: 2020-05-30 00:20:48
published: true
---

Day 34 of the #100DaysToOffload Series:

Eighteen hours ago, Kris Gesling announced to the world the release of Mycroft Core version 20.2.4. This version has a couple interesting additions that we can go over quickly.

<!--more-->

First things first, the new release came with detailed release notes you can find [here](https://github.com/MycroftAI/mycroft-core/releases/tag/release%2Fv20.2.4). There are some updates to the Padatious Intent Parser and Voight Kampff, but the section on Polly interested me the most.

This version of Mycroft adds "real" support for Polly TTS. [Polly](https://aws.amazon.com/polly/) is a service offered through AWS. This is the description from the page.

>Amazon Polly is a service that turns text into lifelike speech, allowing you to create applications that talk, and build entirely new categories of speech-enabled products. Polly's Text-to-Speech (TTS) service uses advanced deep learning technologies to synthesize natural sounding human speech. With dozens of lifelike voices across a broad set of languages, you can build speech-enabled applications that work in many different countries.

I talked in an [earlier article](https://mikestone.me/voice-of-the-future) about Mycroft and it's annoying lack of voice options. Polly helps in that regard.

Mycroft can now be configured to use Amazon's voices. Amazon has a sizable list of voices that you can use with Mycroft. The catch is you're required to configure Mycroft with your own AWS account.

```
"tts": {
  "module": "polly",
  "polly": {
    "voice": "Matthew",
    "region": "us-east-1",
    "access_key_id": "YOUR_ACCESS_KEY_ID",
    "secret_access_key": "YOUR_SECRET_ACCESS_KEY"
  }
}
```

There's some privacy issues with this that I'm not a fan of. If I wanted Amazon to know everything I was asking my assistant, why not just use an Echo? Still, I like having the option despite the fact that I'll probably never use it.

There's a simple list of instructions on how to modify the user config provided in the documentation, but I'm not sure if the hub is offering a web based method for doing this. It's currently down at the time of this writing.

I'd hope they would as not everyone is comfortable negotiating the command line of a Linux system, even if they're running one. If you're using a Mark I, it's definitely problematic since the Mark I (and eventually the Mark II) are supposed to be plug and play hardware devices that don't require a great deal of technical expertise to get going.

I can't wait to spend more time with this release. I might even fire up the Polly TTS just for a test. I was playing some audio samples of the voices from the web page and it was pretty decent compared to Mycroft's own offerings. 

Hopefully the web hub will be back up and running soon and there's a web configuration for the Polly TTS service. It won't impact my own testing, but I'd much rather they thought ahead and made it easy for people to use.

Edit: After 24 hours and the hub being back up and running, there doesn't seem to be any methods for configuring Polly on the hub.