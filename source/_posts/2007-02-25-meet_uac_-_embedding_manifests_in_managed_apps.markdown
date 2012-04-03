--- 
layout: post
title: Meet UAC - Embedding Manifests in Managed Apps
tags: 
- UAC
- Vista
comments: true
type: post
published: true
meta: 
  dsq_thread_id: "91763937"
---
Over the past few blog posts, we've looked into <a href="http://www.brethorsting.com/uidesign/2007/02/meet_uac_-_understanding_virtualization_and_run_levels.html">what Virtualization and run levels are all about</a>, and learned <a href="http://www.brethorsting.com/uidesign/2007/02/meet_uac_-_creating_a_uac_manifest.html">how to create a Fusion manifest</a> that is appropriate for inclusion on Windows Vista. When we created that Fusion manifest for Windows Vista, we never solved the problem of how to include it in your application. I gave you a hand-wavy answer about including the manifest file side-by-side with your app. This is an okay solution, but certainly not a great one. Ideally, we'd be able to embed our manifest directly into our managed exe, just like the big dogs do with their fancy native apps.

  Today, we're going to do just that. It's actually surprisingly easy to accomplish this with Visual Studio 2005, due to the awesomeness of the managed Project system and MSBuild (<em>not that I'm biased or anything</em> ;-) ).

  Step 1: Locate the Project in Solution Explorer that builds your executable.

  Step 2: Double-click on the Properties node in Solution Explorer.

  Step 3: Click on the Build Events tab in the App Designer (or Project Designer, or whatever it's called).

  Step 4: Add the following text to the Post-Build Steps:

  <em>"C:\Program Files\Microsoft Visual Studio 8\Common7\Tools\Bin\mt.exe" -manifest "$(ProjectDir)Borealis.exe.manifest" -outputresource:$(TargetDir)Borealis.exe;#1</em>

  Clearly, you should make sure that the path to mt.exe jives with the installation location on your machine, and you should name the manifest and output executable files according to what they're actually called for your project (<em>hey, what's Borealis?</em>). But yeah, otherwise you're done. That was pretty easy, no? Check out the screenshot below.

  <img src="http://www.brethorsting.com/uidesign/wp-content/uploads/2007/02/virtualization-disabled.PNG" alt="Virtualization Disabled" /><a rel="attachment wp-att-608" href="http://www.brethorsting.com/uidesign/?attachment_id=608" title="Virtualization Disabled"></a>
