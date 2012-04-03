--- 
layout: post
title: Button Sizing
tags: 
- Apple
comments: true
type: post
published: true
meta: {}

---
Pop quiz: what was the correct size of an OK button back in Mac OS 8? If you answered "I have no idea," you would be in the same boat I was only a few minutes ago. It turns out that the correct size for your OK and Cancel buttons on Mac OS 8 was <a href="http://developer.apple.com/documentation/mac/HIGOS8Guide/thig-52.html">58px by 20px</a>. Unsurprisingly, the only way to figure out the answer to this question is to dig into Apple's HIG, assuming you think about this (admittedly) nitpicky issue.

  OK, next question: what's the correct size of an OK button on OS X? You might think to open up <a href="http://www.stoneschool.com/Work/NeXT_Team.html">everyone's</a> favorite UI design tool, <a href="http://developer.apple.com/tools/interfacebuilder.html">Interface Builder</a>. Alright, let's start by creating a new Cocoa window and dragging a button onto it. Change its title to "OK" and take a look at the size: ah, 70px by 20px. Case closed, right? Well, no actually, it isn't.

  Next step: Create a new Carbon window and drag a button onto it. Rename the button to "OK" and take a look at its size. Uh-oh, this button is 69px by 20px. Well, so what? What's one pixel between friends, after all?

  So here's the issue: Interface Builder for both Carbon and Cocoa disregards the Apple Human Interface Guidelines in this regard. <a href="http://developer.apple.com/documentation/UserExperience/Conceptual/OSXHIGuidelines/XHIGControls/chapter_18_section_2.html#//apple_ref/doc/uid/TP30000359-TPXREF186">Apple states that</a>:
  <blockquote>The standard width for OK and Cancel buttons is 68 pixels</blockquote>

  Oops. In contrast, this is one place where UI design tools for Windows get it right. Go take a look at the Windows Ux Guidelines. They specify that buttons should be 50x14 Dialog Units (DLUs) or 75x23px. Drag a button onto a Winform in Visual Studio. It's 75x23px. Drag a button onto a VC-generated RC file dialog: it's 50x14DLU.
