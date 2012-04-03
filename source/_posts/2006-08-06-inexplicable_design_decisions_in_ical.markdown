--- 
layout: post
title: Inexplicable Design Decisions in iCal
tags: 
- Apple
comments: true
type: post
published: true
meta: {}

---
Since Tiger shipped in early 2005, Mail.app has gone from being one of my favorite mail clients around, to being my absolute least favorite mail client. It frequently displays unintelligible warnings like "<a href="http://www.inertramblings.com/2006/03/09/mailapp-and-courier-imap-the-message-could-not-be-saved/">The message could not be saved</a>," or it simply hangs at shutdown.

  <a href="http://www.halfamonkey.net/archives/2006/08/failure_to_just.php">According to Brendan at halfamonkey</a>, iCal's interactions with Mail.app are even stranger than the problems I've run into in the past with Mail. Apparently, iCal uses two different, inelegantly selected email addresses for determining how to send an invitation, and what reply-to address should be marked on it.

  For the first,
  <blockquote>the account used for sending the invitation is determined by whichever account is currently selected in Mail.app.</blockquote>

  The second adddress, used to mark the reply-to address on your email invitations is selected in a truly byzantine fashion:
  <blockquote>This address is obtained from Address Book.app by selecting the first address listed on the card you've marked as your own...[where the] order of items in an address book card is not user-controllable. In fact, it's not even visible to the user.</blockquote>

  Brendan mentions that "I'm not sure even Microsoft could come up with something that convoluted (though I'm sure they'd take the challenge)," but I'm an Outlook+Exchange user at work; I send and receive hundreds of email and meeting requests every day (emails take up the lion's share, of course), and we never run into the issues that Brendan describes. That said, we have had plenty of other weirdo issues in the past, like <a href="http://msexchangeteam.com/archive/2004/04/08/109626.aspx">Bedlam DL3</a>.
