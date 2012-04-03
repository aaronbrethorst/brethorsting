--- 
layout: post
title: "Sprinkle on a Little Ribbon and You\xE2\x80\x99re Good to\xE2\x80\xA6Oh Wait"
tags: 
- Windows
comments: true
type: post
published: true
meta: {}

---
<a href="http://blogs.msdn.com/jensenh/archive/category/11716.aspx">The Ribbon</a> is the biggest new feature in Office 2007, and probably the biggest new feature for the past few releases of the product. It's an incredibly cool new feature, and makes Office 2007 significantly easier to use, in my opinion.

  I've seen a number of .NET control vendors release <a href="http://www.devcomponents.com/dotnetbar/nextgen.html">look-and-feel-alikes of the Ribbon</a>, which is very cool from the perspective that Windows ISVs will be able to mirror the look-and-feel of Office if they choose. I am very much in favor of seeing Windows applications that feel as new, fresh, and interesting as the Office 2007 suite.

  For the general case, though, it is not a silver bullet, nor will it ever be. From reading <a href="http://blogs.msdn.com/jensenh">Jensen Harris's weblog</a>, it's pretty clear that a dedicated team in Office literally spent years coming up with the right placement and sizing of commands for the Ribbon. This isn't a trivial task that you can accomplish in a day or two. Correctly supporting the Ribbon in your (non-trivial) application is a challenging, time-consuming task.

  The Ribbon is not necessarily something that can be consumed as-is by every application out there, either. I've spent a lot of time thinking about how it could best be supported in Visual Studio, and it's not easy. Some applications, like <a href="http://www.adobe.com/products/photoshop/">Photoshop</a>, lend themselves well to the notion of the Ribbon. Others, like Visual Studio or EMACS, don't make nearly so much sense in that model.

  I'm not saying it's impossible for every application out there to adopt it; it's just that it's a trickier problem than you might think.
