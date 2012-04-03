--- 
layout: post
title: Cocoa Controls
tags: 
- Mac OS X
status: publish
type: post
published: true
meta: 
  dsq_thread_id: "91763154"
---
I've been a fence-sitter for years. I started out with Mac OS 7.5 (really, System 7.5) back in the early 1990s on a Power Mac 6100. I was totally a Mac zealot: "PCs suck, blah blah blah." At the age of 17 I started working for the Geek Squad, where I became a PC user by default. I was fixing Windows machines by and large, and then fixing the occasional Mac that came in. By this time, I had built myself a Windows machine, and started running Windows 98 full-time. By the time I started in college, I had abandoned Mac OS completely.

  September 13 2000. Apple released Mac OS X Public Beta. After several false starts, the single most dull Macworld Expo speech ever, and the return of Steve Jobs Apple had finally flung itself into the future. I started reading more about OS X and got more and more excited. The University of Minnesota was a UNIX school, and I needed an easier way of writing my little C and C++ apps than I was afforded through an SSH terminal. I needed a friggin' shell on my computer. So, I bought an iBook and spent the extra $30 for the Public Beta.

  Holy cow, did it ever suck.

  OS X Public Beta is quite possibly the single slowest operating system I have ever used in my entire life. It was slow, it was incomplete, it gave me the spinning pizza of death for minutes straight. And I kept using it anyway. This is, of course, because it was still the coolest piece of software I had ever seen in my entire life.

  It took me a while to get the hang of the Cocoa API, but <a href="http://www.sixdollarchimp.com/irooster.aspx">I eventually figured it out</a>. The thing that has always killed me about Mac OS X and Cocoa, though, is the lack of third-party control libraries.

  Windows Forms applications (Windows GUI apps written using the .Net Framework) are really easy to write too. In some respects, it's easier to write a WinForms app. In others, Cocoa is easier. It just depends on what you're trying to do.

  One thing that is far easier to do with WinForms is locating and using free, third-party controls. You can find controls that give your application a Windows XP look and feel, an Office 2003 look and feel, and so forth.

  At this point, there is no easy way to build an application that resembles the OS X Finder. Where's the location switcher control from Apple? (the little thingy you click on on the left hand side of each Finder window in order to easily switch between different folders on disk) Where's the switcher control from third parties? Hell, I can't even spend money to get something like that. Where are all of the controls out there to help me emulate the appearance and behavior of iCal?

  I can only assume that this has a lot to do with the sheer differences in the numbers of developers writing Cocoa apps (and third party controls) and writing .Net apps (and third party controls).

  One of the best things that Apple could do right now, I think, is if more high-quality control samples were released. Cocoa developers really need more information on how Apple does things like make the little, funky modal dialogs in iCal that let you choose repeating calendar events. One of the best-attended sessions at WWDC last year was a talk on how Apple does certain little bits of UI mojo. They need to do more, and all year-round.
