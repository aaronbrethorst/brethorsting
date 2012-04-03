--- 
layout: post
title: "iRooster and Murphy' Law"
tags: 
- Apple
comments: true
type: post
published: true
meta: 
  dsq_thread_id: "93585246"
---
Even though it may not seem like it, I've been working feverishly on <a href="http://chimpsoftware.com">iRooster</a> here in Chimp Software Headquarters (aka the Starbucks down the street, my couch, and Helen's couch) ever since I released v2.4 back in January.

  <strong>The Sad story of 2.4.3 - unintended consequences and all that</strong>

  Last week started off with a trickle and then a flood of complaints about how iRooster was no longer working. It took me a while to figure out what was going on; <a href="http://www.codinghorror.com/blog/archives/000818.html">everything was working just fine on my development machine</a>. Finally, it dawned on me: a teeny-tiny update had been published for iTunes. Version 7.1.1, to be exact. This update, it turns out, had hosed every single user of iRooster who woke up to their Library. <a href="http://bbs.applescript.net/viewtopic.php?id=20634&amp;action=new">I wasn't the only developer affected by this obnoxious issue</a>. It's a pity that app compat testing in Apple's iTunes product group didn't catch this, or that an errata wasn't published somewhere really obvious to alert us to this sort of thing. Anyway, I promptly released iRooster 2.4.3 to compensate for this issue, and relaxed a bit.

  <strong>Wham! </strong>Friday morning greeted me with a whole slew of crash reports for iRooster...Actually I was greeted by a host of crash reports for <em>(null)</em>. Welcome to the land of unintended consequences, population: me. It didn't take me very long to figure out what happened, but I never anticipated the issue that cropped up. This issue affected every user of iRooster, including those who were still using Panther.

  I made a decision with the release of iRooster 2.4.1 at the beginning of March to EOL support for Panther, Apple's 4+ year old OS. I support the current version of the OS and the one just past, and Leopard should be out any day now (I hope). Furthermore, some of the new features I'm working on absolutely require OS X 10.4 or above, I didn't have a machine to test iRooster on Panther, and cutting support for 10.3 gave me the ability to use other handy-dandy bits of functionality, like NSDatePicker, whose introduction let me cut 2000 lines of code from my product (less code == less bugs and more time to make cool features).

  Of course, it seems like really bad form to suddenly say to every user of iRooster still on Panther that "you're gonna have to go buy a new OS in order to keep using your shiny $10 alarm clock." Yeah, that'd fly. So, I did the only thing I could: I backported all of the bug fixes I made for 2.4.2 to 2.4.1, fixed the iTunes issues in both codebases, checked them into my source control tree as 2.4.3-Panther and 2.4.3-Tiger and released both as a single Apple Disk Image file (DMG). This DMG even had a snazzy-looking background and stuff. It's pretty fancy.

  I published the update to my website and updated my appcast file, so that my awesome Sparkle auto-updater framework (created by Andy Matuschak) would inform all of my users that a fix is available for their problem. Of course, Sparkle wasn't quite sure what to do when it encountered an archive with <em>two</em> applications in it, so it crashed. This resulted in a flurry of crash reports for my application, <em>(null)</em>. Good times.

  After mulling over a number of solutions, I finally decided to repackage the Panther version of 2.4.3 as a zip file and publish it through my appcast mechanism. There's no easy way for me to get any sort of differentiation between OSs to work, which means that I couldn't selectively tell Tiger-hosted versions of iRooster to download one version, while asking Panther-hosted versions to download a different one. :( I investigated a few alternatives, such as detecting which version of the CFNetwork class was hitting the appcast.xml file, except that Apple doesn't seem to publish the version numbers of these things anywhere, so I have no clue which version of CFNetwork corresponds to which version of the OS.

  <strong>Version 3.0 - Featuring 25% more shiny stuff</strong>

  Anyway, so that was Thursday and Friday of last week. Busy busy busy. I've also been hard at work on iRooster 3.0. I believe I've finally settled on a final list of features for the release. Some of them are obvious things that everyone using iRooster is clamoring for (<a href="http://www.chimpsoftware.com/forum">see the forums for more on that</a>), and some are features that you've never seen on any alarm clock before. I'll give you a hint, though. iRooster is all about web services and flashy stuff introduced in 10.4. What kind of web services? I'm not going to say yet, but I think you'll be pretty excited :) I sure am!

  Here are the two features I'm willing to reveal:
  <ul>
  	<li>Streamlined alarm editor - the old one has been around in pretty much the same state since version 1.0 shipped in 2003. Kinda lame. A reimagining of this UI is long overdue.</li>
  	<li>A resizable clock, and the removal of the mini window (or as they'd say in a bad 80s movie: two clocks enter, one clock leaves!)</li>
  </ul>
  Here are the features I'm not willing to reveal yet:
  <ul>
  	<li>Cool thing involving a web service</li>
  	<li>Another cool thing involving a web service</li>
  	<li>Cool thing not involving a web service</li>
  </ul>
  ;-)

  I'm not really prepared to discuss the timeline for iRooster 3.0, yet, but I can assure you it won't take nearly as long as 2.2 did. I've been working on v3.0 since February in fits and spurts, and it's getting pretty close to Beta quality. I will certainly release a Beta version as soon as I believe it's ready. I hope to publish the final release before the end of the month, but I have a lot of work in my day job that has to take precedence over iRooster (on a related note: let me know if you'll be in Vegas for <a href="http://www.visitmix.com">Mix'07</a> at the end of the month).
