--- 
layout: post
title: iRooster Status Update
tags: 
- iRooster
comments: true
type: post
published: true
meta: {}

---
<em>(Written at 35,000 feet somewhere between Minneapolis and Seattle)</em>

  I've been on vacation for most of this week, but I still found a few hours to work on iRooster. Typically, when I'll be gone from Seattle for more than a week I will bring my Apple iBook and my Sony Vaio with me as carry-on luggage (I'm sure TSA just looooves me). Since my trip to Minneapolis only lasted four days, and since I'm trying to be a little less geeky I brought just a single laptop with me: the Windows machine. Accordingly, there isn't much in the way of Mac updates, but I've been owrking quite dilligently on the Windows version.

  iRooster for Mac OS X
  There's really only one thing to report here. A friendly bloke in Romania has offered to localize iRooster into his native tongue, so expect more from this soon. I really am gearing up to release v2.1.1. I have a little more testing to do, and I need to fix a performance bug.

  Specifically, let's imagine that you're a college student who has thirty gigs of music in iTunes. As it turns out, the Alarm Editor loads really, really slowly under this sort of circumstance on first use, but should function normally later on. The reason for this is that iRooster reads in a file on disk called "iTunes Music Library.xml." On my iBook, which has a 12.5GB music library, this file is currently about 4.5 megabytes in size. The Alarm Editor works decently; I have no real complaints. However, increase it in size to 10+ megabytes, and I can imagine that the application will just crawl as it reads in this entire file.

  So, there's a pretty easy fix to this which shouldn't take more than a few extra lines of code.

  iRooster for Windows
  I've spent approximately ten hours working on iRooster for Windows over the past few days. I'm building it in the way that I wish I had first designed iRooster for Mac. The wake-up functionality is factored into an entirely separate application from the alarm editing functionality, which gives me quite a bit more flexibility over how everything works.

  Basic alarm editing functionality is working, repeating alarms don't exist yet.
  Snooze is working more-or-less correctly. There are a few minor-but-persistent bugs left for me to handle, and always more visual polishing to do.

  The one critical thing that has yet to happen is that iRooster for Windows still cannot wake me up from sleep yet. This should happen in the next week, and I'm anxious to start waking up with my Media Center machine. Hopefully, I'll have some more news here next Sunday.

  And with that, I think I should call this sufficient. We've hit some turbulence and the guy in front of me has decided that now is the ideal time to put his seat back, robbing me of my ability to type faster than 10 WPM.
