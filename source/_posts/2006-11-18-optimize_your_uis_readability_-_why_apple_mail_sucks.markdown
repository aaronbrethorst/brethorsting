--- 
layout: post
title: "Optimize your UI' readability - why Apple Mail sucks"
tags: 
- Usability
comments: true
type: post
published: true
meta: 
  dsq_thread_id: "91763825"
---
One of my least-favorite pieces of software ever is Mail 2.x, included in Mac OS X 10.4 Tiger. What was a stable, reasonably performant, sensible, and usable mail client in previous iterations has become <a href="http://arstechnica.com/reviews/os/macosx-10.4.ars/3">&quot;hideously ugly,&quot; and &quot;inflexible, inconsistent, and again, a little strange.&quot;</a> You can find a ton of usability nitpicks of Mail scattered across the web from any Mac pundit with a pulse.

  My greatest pet peeve in Mail 2 is its insistence upon forcing users to read their mail in a horizontal orientation reminiscent of the worst aspects of Microsoft Outlook Express.

  <a href="http://www.brethorsting.com/uidesign/2006/11/18/mail2.png"><img alt="Mail 2 in Tiger" src="http://www.brethorsting.com/uidesign/2006/11/18/mail2-thumb.png" width="269" height="184" /></a>

  Mail's UI layout has two major deficiencies. First, according to <a href="http://psychology.wichita.edu/surl/usabilitynews/42/text_length.htm">a 2002 usability study</a>:
  <blockquote>[I]t is suggested that full-screen line length should be avoided for online documents, especially if a large amount of text is presented. For adults, it is suggested that medium line lengths should be presented (approximately 65 to 75 CPL [characters per line]).</blockquote>

  On my Apple iBook G4 (with a 12" screen at 1024x768px), I find that Mail can display approximately 120 characters per line in a maximized state, which is well outside of the line length threshold established in the aforementioned article.

  Second, I have many more emails in my Inbox than can be shown in Mail's email header table at any given time: I can see the header information for 15 emails out of 45 messages in my Inbox. This isn't so bad, but if my personal Inbox looked like my work Inbox where I typically have 1000 emails, this would be a nightmare for management!

  If Mail provided a vertical layout I would be able to see many more email headers than I can now, and provide myself with a more enjoyable reading experience. For an example of how this might turn out, see the mockup I created below. Unfortunately, creating a &quot;widescreen&quot; version of Mail doesn't work quite as well as you might like on a screen with a 1024x768px resolution (perhaps the reason why Apple chose not to provide this option), but it can be made to work quite well with a few modifications to Mail's overdesigned UI:
  <ol>
  <li>There is no reason why the folder list on the left has to use 32x32px icons by default. Change the default to 16x16px.</li>
  <li>We are sacrificing 22 horizontal pixels to the iChat availability icon in the mail header table. Let's push these icons into the 'From' column on the left-hand side.</li>
  <li>The splitter is ridiculously oversized. We can easily shave two pixels off its width.</li>
  <li>Let's clean up the folder area's buttons on the bottom and shave off a few more pixels from them.</li>
  </ol>

  You can see the fruit of our labor below (click it for a full sized image). Now, we can see about three times as many email headers as we could before, quite a bit more of our individual emails, and the width of an opened email is displayed to us in a far more pleasant to read size. I hope Apple fixes this serious UI issue in Leopard, the next version of OS X, but <a href="http://www.apple.com/macosx/leopard/mail.html">from the look of things</a> it appears that I will be sorely disappointed.

  <a href="http://www.brethorsting.com/uidesign/2006/11/18/Mail-mockup.png"><img alt="Mail Mockup" src="http://www.brethorsting.com/uidesign/2006/11/18/Mail-mockup-thumb.png" width="337" height="253" /></a>
