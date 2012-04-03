--- 
layout: post
title: dom:loaded makes me happy
tags: 
- Web Design
comments: true
type: post
published: true
meta: 
  dsq_thread_id: "91764141"
---
I've been using MooTools for the past month on a personal project, and I couldn't be happier. In my new job, I've been boning up on my Prototype skillz. I certainly don't mind Prototype, although I do find it to be a little heavy. The one thing that has been bugging me was the apparent lack of an equivalent to MooTools' <a href="http://demos.mootools.net/DomReadyVS.Load">domready</a> event.

  Here's what domready does for you. Let's say you're loading up a page that is heavily dependent on Javascript for user interaction. The page contains 400KB of pictures. If you wait around for the page load event to fire, the user will experience what seems like terribly broken behavior. domready, instead, gets fired as soon as you can start monkeying with the document's object model, enabling you to get your Javascripty meathooks into just about anything.

  As it works out, though, this is actually in Prototype v1.6, and I am <em>ecstatic</em>. It's called dom:loaded and you can learn all about it from <a href="http://solutoire.com/2007/11/08/firing-custom-events-with-the-prototype-javascript-framework/">this linked blog entry</a>.
