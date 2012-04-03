--- 
layout: post
title: "Web Usability Pet Peeve #92: Overriding Common Accelerators"
tags: 
- Usability
status: publish
type: post
published: true
meta: 
  dsq_thread_id: "93899785"
---
I am a huge, huge, huge advocate of correctly supporting mnemonics and keyboard shortcuts throughout your application. It was, for this reason, that I was very excited when I first learned that you could do the exact same thing for web pages. Movable Type uses this, as do some other websites.

  What irritates me to no end, though, is when a website overrides a mnemonic or keyboard shortcut that I use on a regular basis. For example, I use the key combination Alt+D about 50 times a day (literally) to pop myself into the address bar in Internet Explorer. It's such a rote behavior for me, now, that I monkeyed around with one of Safari's .Nib files to switch its equivalent keyboard shortcut from Cmd-L to Cmd-D on my Mac.

  Movable Type used to (back in v3.2) override the default behavior of Alt+D to provide a shortcut for Delete Entry. This meant that I ran the risk of deleting the new entry every time I finished writing a blog post and flipped up to the address bar to verify the post on my website. Argh!

  <a href="http://www.sixapart.com/movabletype/docs/3.3/h_changelog/3_3.html">Movable Type 3.3 Changelog</a>:
  <blockquote>24907: Accesskey changes required because of conflicts
  BUG FIX: Made a system-wide change to the accesskeys for "delete" and focus on the "quick search" input box because of conflicts in certain browsers. The delete accesskey is now 'x' (think: expunge or crossing something out) and focus on the quicksearch input box is now 'q'.</blockquote>

  I am very excited to see that MT 3.3 has removed this behavior (it makes me ecstatic, seriously), but I still run into some websites that have this issue. For example, I just found <a href="http://tech.cybernetnews.com/2006/07/28/mozilla-thunderbird-20-alpha-1-released/">a mini-review of Mozilla Thunderbird 2.0 Alpha 1</a>. I read it, and then pressed Alt+D to flip to the address bar so that I could check Seattle's traffic briefly.

  Oh, but wait! IE moved back to the top of the page, but I got no focus in my address bar. Argh!
