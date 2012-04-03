--- 
layout: post
title: "Meet Popfly \xE2\x80\x93 Mashups for the rest of us"
tags: 
- Popfly
comments: true
type: post
published: true
meta: 
  enclosure: |-
    http://download.microsoft.com/download/7/7/9/77984ab1-5438-4330-9430-90553f3555be/PopflyIn15Minutes.mov
      68454701
      video/quicktime
  _edit_last: "2"
  dsq_thread_id: "91763994"
---
For the past few months, I’ve been toiling away in secret with a small team (only about 15 people, which is tiny by Microsoft standards) on a new project that we’re finally ready to unveil. I’m very excited to introduce you to <a href="http://www.popfly.com">Microsoft Popfly</a>, a fantastically innovative new web application that allows you to easily create rich, compelling mashups without writing a single line of code. Ever seen Twittervision? You can build it in Popfly in 45 seconds by dragging and dropping web services onto a Silverlight-based designer. Popfly even has Intellisense!<img src="http://www.popfly.ms/Overview/images/overview/thumb_designersurface.gif" />

  A while ago, I was giving a talk on the user experience enhancements that I was driving for the Visual Studio “Orcas” release here in Microsoft’s Developer Division. We’d run into some technical difficulties with projecting, and so I had a few minutes to kill. I ended up chatting with the next speaker—a guy named John Montgomery from the Non-Professional Tools team—about the work he was doing in the web space. It sounded interesting, and I scheduled some time to meet with him and get a demo of the application. It only took about 30 seconds before I asked him for a job.

  I’ve been on the team for about four months, now, but I’m still blown away by what you can do with Popfly with basically zero effort. Don’t take my word for it, though, instead you should go watch our screencast (<a href="http://go.microsoft.com/fwlink/?LinkID=91175">WMV version</a> | <a href="http://download.microsoft.com/download/7/7/9/77984ab1-5438-4330-9430-90553f3555be/PopflyIn15Minutes.mov">Quicktime version</a>). It provides a great 15 minute overview of the capabilities of the site.

  The ease of creating mashups using Popfly is really something to see. In addition to the Twitter map app I referred to above, there are a ton of other things you can do today, too: Want to create a Vista sidebar gadget that shows off pictures from Flickr? 30 seconds, worst case. Need to relieve some stress? We have a whack-a-mole game that you can customize, too.

  In the event that we don’t have a web service wrapper (called a “block” in Popfly parlance) that you’re looking for, we also offer an extensibility model for you to create your own blocks. This is one of my favorite features in the site, given that <a href="http://www.programmableweb.com/">Programmable Web</a> currently lists 436 separate APIs.

  Blocks are a composite of a Javascript object, maybe some XAML, and an XML descriptor. Typically, they provide one-stop access to a web service, but others may perform data transformation, or they may display a Silverlight or DHTML-based UI. Each web service block exposes a handful of methods that encapsulate common scenarios for that service. For example, our Flickr block exposes a method to snag n geotagged photos that match a set of search terms. You can, for example, search for geotagged photos with the term “Ichiro Suzuki” and plug the data into a Virtual Earth map, which will give you back a VE map showing photos of Ichiro doing his thing at Qwest Field here in Seattle.

  Popfly gives everyone the ability to easily create rich web mashups without writing a single line of Javascript. It’s a fantastic tool, and I hope you have the opportunity to try it out soon. If you <a href="http://www.popfly.com">visit the site</a>, you can sign up for an invitation and browse through tons more information about us and what we’re building. Feel free to ask me questions, if you’d like. I look forward to your feedback!
