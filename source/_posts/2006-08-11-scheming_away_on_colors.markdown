--- 
layout: post
title: Scheming Away on Colors
tags: 
- Windows
comments: true
type: post
published: true
meta: 
  dsq_thread_id: "116148894"
---
<em>(yeah ok, I haven't quite figured out what innovation means to me yet. I'm still thinking about it.)</em>

  <a href="http://blogs.msdn.com/jensenh/archive/2006/08/10/694577.aspx">Jensen Harris had an interesting post on his blog yesterday</a> about what it took in Office 2003 to maintain the color schemes presented on Windows XP. Interestingly, in Visual Studio we use approximately the same scheme that you can see if Office 2003. We key off a set of known color schemes and proffer up a default color palette based upon that theme. In the case of VS, I believe we use a palette of about 250 colors.

  You'll notice that the 2007 Office System offers three themes: Black, Silver, and Blue. In Visual Studio 2005, we had the following predefined palettes:
  <ul>
  <li>Luna Blue (aka NormalColor)</li>
  <li>Luna Silver (aka Metallic)</li>
  <li>Luna Olive (aka HomeStead)</li>
  <li>Royale (which has a story behind it)</li>
  <li>Unknown Theme</li>
  <li>Windows Classic</li>
  <li>High Contrast</li>
  <li>Debug (<a href="http://www.skittles.com">taste the rainbow</a>)</li>
  </ul>

  So, a couple comments: apparently, there was a brief period of time (before I started at Microsoft) where Whidbey had a blue color scheme nearly identical to Office 2003. We decided to change this to the tan or putty-colored palette that you see by default in VS 2005 today (which was for the best, I think).

  When Visual Studio runs on a version of Windows with a theme it doesn't recognize, it will generate a "best-fit" palette keyed off Windows's system colors. Back in Whidbey Beta 1, this applied to the new Royale visual style, which was introduced in Tablet PC 2005 and Media Center 2005.

  Back in January 2005, I purchased a PC running Media Center 2005 to replace the decrepit, old PC that had served me all the way through college. I loved every bit of the MCE experience, except that the color scheme Visual Studio generated for Royale was less than optimal. I took it upon myself to create a new VS theme to support Royale over the course of a weekend and checked it in just before we locked down for release. I think the first place the new color scheme was ever seen was on my <a href="http://blogs.msdn.com/aaronbrethorst">MSDN blog</a> shortly thereafter.

  <a href="http://www.brethorsting.com/msdnblog/newtabs.png"><img src="http://www.brethorsting.com/msdnblog/newtabs.png" height="374" width="298" alt="Visual Studio 2005 running under Media Center 2005" /></a>

  For Orcas, we're planning on maintaining our existing color palette selection system and extending it to include a palette for Windows Vista's Aero. I don't expect that we will move to a scheme like Office 2007's, but it's always interesting to understand why other groups in Microsoft make the decisions they do.

  Also, in case you maintain a Windows application that proffers up a custom color palette based upon the current theme, make absolutely sure that your theme detection code checks for more than the theme name. "NormalColor" is not unique to Luna Blue. Performing a simplistic theme-check also pick up Royale (and possibly Aero, though I haven't checked yet). Make sure you use two separate pieces of data to validate which theme you're using.
