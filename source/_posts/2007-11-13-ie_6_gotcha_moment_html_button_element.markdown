--- 
layout: post
title: "IE 6 Gotcha Moment: HTML Button Element"
tags: 
- Web Design
status: publish
type: post
published: true
meta: 
  dsq_thread_id: "91764124"
---
So, for the past hour I've been trying to figure out why a website I'm working simply fails to render on IE 6. I finally traced it down to a rogue button element, which appeared to be well-constructed but was still making IE 6 barf spectacularly. In the off-chance this ever happens to anyone else, here's a tip: ensure that your button elements are constructed with a real closing tag as opposed to the short form (or whatever the real name for it is).

  i.e.: &lt;button&gt; &lt;/button&gt; instead of &lt;button /&gt;
