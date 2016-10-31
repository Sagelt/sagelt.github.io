---
layout: post
title: "Black Stars Rise on Github"
date: 2013-10-23
categories:
  - Games
image: /images/stars.jpg
image-sm: /images/stars.jpg
---
Between revisions on the Dungeon World supplement, I keep getting drawn back to Black Stars Rise. As this thing gains momentum, I decided it was time to start my development flow: xml to InDesign and HTML [on github](https://github.com/Sagelt/black-stars-rise).

This time, though, I've learned a few lessons. For DW, the XML was mainly for InDesign, and the git repo didn't really do anything. The eventual fan HTML projects required way too much work.

So this time around I've developed some infrastructure first. With an eye towards single-sourcing and remixing, Black Stars Rise is written in logical XML units (sections, moves, careers, setups, breaks) that can be grouped into chapters by a python configuration file. This configuration file feeds both the web interface and a build script for InDesign.

The end effect is that one XML change can be pushed to both InDesign and web with very little effort. I still haven't completely freed it from InDesign's requirements—you still have to be careful enough with whitespace that proper indenting isn't an option—but it's way better than DW ever was. Even better, the website and PDF are one united project, instead of two distinct formats.

I'm also happy to have BSR on git earlier than DW. Hopefully this will make some of github's features (bug tracking, releases, pull requests) more useful.

Having a simple web interface also makes BSR more forkable than DW. To make a fork of DW you'd basically have to reinvent the presentation. Making your own version of BSR is simply setting up an AppEngine project and deploying to it (I use git push to deploy, to make it even easier).

This isn't for everyone, obviously. (What is for everyone, anyway?) Most people will just want [the PDF](http://goo.gl/NJrjlJ) and never care about what's behind the scenes. But for the folks who do care—the hackers and tinkerers—I'm hoping this proves even better than DW.