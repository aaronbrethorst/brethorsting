--- 
layout: post
title: Web development tools every Windows developer must have
tags: 
- Ajax
comments: true
type: post
published: true
meta: 
  dsq_thread_id: "91763841"
---
No respectable Windows developer would try debugging their application with printf()'s or Console.WriteLine()'s, so why would you try doing the same thing with Javascript? Yeesh. I've been hacking a fair amount of Javascript and Ajaxy things lately, and I've put together a respectably little toolkit with which I can work it over. If you're doing any web development on Windows, you should add all of these tools to your repository immediately!

  First off, the IE Developer Toolbar is super-handy for DOM inspection. You can download it from the <a href="http://www.microsoft.com/downloads/details.aspx?familyid=e59c3964-672d-4511-bb3e-2d5e1db91038&displaylang=en">Microsoft Download Center</a>.

  Next, <a href="http://www.fiddlertool.com/">Fiddler</a> is a cool tool for doing inspection and manipulation at the HTTP transmission level. It even provides debugging capabilities.

  And, for the coup de grace, did you know that you can debug friggin Javascript code in Visual Studio 2005? The steps are pretty straightforward:
  1. Open your website in VS 2005.
  2. Hit F5.
  3. Go to the Attach to Process window (Tools.Attach to Process).
  4. Make sure that 'Attach to' is set to Automatic or Script.
  5. Scroll through the list of Available Processes and select the iexplore.exe window with the name of the page you're attempting to debug.
  6. Hit the Attach button.

  I've verified that this even works on Windows Vista RTM with IE 7 and VS 2005 RTM. Awesome stuff, and it makes life <em>so</em> much easier.
