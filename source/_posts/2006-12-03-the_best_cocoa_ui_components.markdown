--- 
layout: post
title: The best Cocoa UI components
tags: 
- Cocoa
comments: true
type: post
published: true
meta: 
  dsq_thread_id: "91763859"
  _edit_last: "2"
---
Update: I just launched a new website that tracks <a href="http://cocoacontrols.com/">the best custom Cocoa controls for iOS and OS X</a>. It doesn't have a ton on it yet, but I'm stocking it up with my favorite items. Also, feel free to submit your own!

<a href="http://chimpsoftware.com">As a Cocoa developer on Mac OS X</a>, I feel a certain obligation to provide a kickass user experience for my customers. Unfortunately, relying entirely on Apple's built-in set of controls leaves the experience a little...lacking. Things just seem a little too plain-vanilla and drab if you stay to the well-defined path. Apple seems to feel this way, too, and has gone out of their way to reinvent the wheel with a wide variety of window styles, new button types, date and time controls, icon badges and a whole host of other things that you simply cannot obtain <a href="http://www.brethorsting.com/uidesign/2006/07/the_goldstandard_for_ui_guidel.html">if you hew entirely to the Apple HIG</a>.

This is nothing unique to Apple; you tend to have the same experience when you resort to nothing but built-in controls on Windows, as well. As a result of this, a veritable industry has sprung up on Windows to provide supplemental controls for WPF, Winforms, and Win32. You can even find <a href="http://www.infragistics.com/">drop-in Office 2007 UI systems</a>.

Anyway, the following list documents my favorite Cocoa controls on the Mac. These are all consumable by Cocoa applications, and will make your application look and feel far better than it would if you kept to the stock set of controls. Some of these controls are available in newer iterations of OS X, like the calendar control. Unfortunately, some of us happen to still support older (cough) versions of OS X, like Panther, which came out only a bit over three years ago. C'est la vie.

<a href="http://cocoadev.com/index.pl?FlowLayoutView">ZFlowLayout</a> - Need a flowing layout view, like the one built into Winforms 2.0? Step right up; the source code's available, too.

<a href="http://andymatuschak.org/pages/sparkle">Sparkle</a> - An update manager that works with almost no developer-intervention. I think it took me all of 20 minutes to wire this into iRooster and get the web components working properly, including a custom release notes system. I may have made coffee in the middle of that, too. Very cool.

<a href="http://blog.oofn.net/2006/01/15/gradients-in-cocoa/">CTGradient</a> - This is a simple class that wraps all the nasty bits of creating gorgeous gradients on OS X. It also appears to be the new hotness in that I've seen a ton of projects incorporating this over the past few months. I am definitely looking forward to including this in iRooster once I drop support for Panther.

<a href="http://www.positivespinmedia.com/dev/PSMTabBarControl.html">PSMTabBarControl</a> - This control is used in Postive Spin Media's Pandora web content grabber. It duplicates the look-and-feel of the tab bar control used in Safari. Very hot.

<a href="http://s.sudre.free.fr/Software/DevPotPourri.html">WBTimeControl</a> - Stephane Sudre's open source implementation of Apple's date time control. I use this in iRooster and am far happier for it.

<a href="http://cocoadev.com/index.pl?OmniAppKit">Omni AppKit</a> - Although it has virtually no documentation, this large collection of AppKit-esque features is phenomenally valuable. The other big downside is that you can't compile this without OmniBase and OmniFoundation, which can add some serious bloat to your app. It should be entirely possible to rip out specific pieces of functionality, as most of OmniAppKit's controls aren't actually dependent on features found in OmniBase or OmniFoundation.

<a href="http://www.seanpatrickobrien.com/2006/09/24/a-new-blog-for-a-new-mac-developer/">iLifeControls</a> - Although I haven't actually had an opportunity to use Sean Patrick O'Brien's iLifeControls suite, I must say that it looks awesome. iLifeControls duplicates a nice chunk of the basic look-and-feel you'd expect from an iLife-like application.
