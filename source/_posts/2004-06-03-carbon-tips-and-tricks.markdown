--- 
layout: post
title: Carbon Tips and Tricks
tags: 
- Mac OS X
comments: true
type: post
published: true
meta: 
  dsq_thread_id: "92176651"
---
How do I bring all my windows to the front?

  Mac OS X introduced a new paradigm of window layering which allows windows of different applications to be interwoven with one another. This paradigm makes dragging from one applications window to another much easier but there are also time in which you may want to force all your applications windows to the foreground. There are two ways of doing this. Mac OS X 10.1 introduced a new HI command, kHICommandBringAllToFront. By sending this command to yourself, and letting the default handlers process the event your application windows will be brought to the front. Another choice which works on all versions of the OS is to force your applications process to the front with the Process Manager.

  void MakeMeTheFrontProcess()
  {
      ProcessSerialNumber psn;
      OSErr err;

      err = GetCurrentProcess( &psn );
      if ( err == noErr )
          (void) SetFrontProcess( &psn );
  }

  <i>From <a href="http://developer.apple.com/carbon/tipsandtricks.html">Apple's Carbon Tips and Tricks</a> webpage</i>. Placed here for my future edification (i.e. so I know where to find this when I get around to needing it in iRooster ;-) ).
