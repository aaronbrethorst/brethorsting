--- 
layout: post
title: Rocking 3D Graphics with WPF
tags: 
- WPF
status: publish
type: post
published: true
meta: 
  dsq_thread_id: "91809637"
---
Eric Sink, blogger extraordinaire and founder of SourceGear, experimented with Windows Presentation Foundation (formerly known as Avalon) last month, with great success. He built an application that enumerates woodworking steps along with little 3D previews, <a href="http://software.ericsink.com/entries/WPF_14July2006.html">and had this to say about the experience</a>:
  <em>WPF 3D is far simpler to use than Managed DirectX.  That's kind of a remarkable thing to say when you consider that Managed DirectX is far simpler than using DirectX from unmanaged code.  I was able to get excellent results from the 3D features of WPF in very little time.</em>

  <a href="http://software.ericsink.com/entries/WPF_3D_Printing.html">A follow-up blog entry from Eric dicusses printing support in WPF</a>:
  <blockquote>Recently I switched everything over to WPF.  Here is my printing code:
  <pre>
  PrintDialog dlg = new PrintDialog();
  if ((bool)dlg.ShowDialog().GetValueOrDefault())
  {
      dlg.PrintVisual(myViewport, "sawdust");
  }
  </pre>
  Five lines.  Were it not for my pathological need to use braces on every if statement, it would be three lines.</blockquote>

  I've seen some demos of WPF that really just knocked me onto my ass, and stories like Eric's reconfirm my excitement in the framework, but I haven't had the time or patience to really get in and learn WPF, yet. In the parlance of the Developer Division's Usability group, <a href="http://wesnerm.blogs.com/net_undocumented/2003/09/who_are_you_mor.html">I'm probably an Elvis, compared to Eric Sink's Einstein</a>, and I generally lack the patience to dig into new frameworks and technologies until the tooling catches up.

  That said, I still write HTML and CSS by hand, so maybe I'm just being lazy :-).
