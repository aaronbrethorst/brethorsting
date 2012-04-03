--- 
layout: post
title: "Meet UAC - Why you must factor out your apps\xE2\x80\x99 admin components"
tags: 
- UAC
- Vista
comments: true
type: post
published: true
meta: 
  dsq_thread_id: "91763948"
---
Let's say you have a shareware application that can do exciting things like self-registration and updating on the fly. Back in the Windows XP days, supporting scenarios like these would be a cakewalk; you could simply write a serial number to HKLM, or run an MSI downloaded off the Internet. Too bad if a user didn't have administrative privileges on their XP machine; that wasn't really a normal scenario anyway.

  Windows Vista throws an interesting kink into the mix with UAC. Now, an application cannot write data to protected locations like Program Files or HKEY_LOCAL_MACHINE unless it has administrative privileges. Just to make matters worse, your app cannot be granted new privileges once it's running. Let me state this again, just because I've found this is the part of the message that gets missed most often.

  Once your process is started, it <strong>cannot</strong> be granted new privileges. It also cannot shed permissions.

  This is true if you're running as a standard user or as an administrator. It doesn't matter. A user whose account belongs to the Administrators group still must deal with UAC just like a standard user. The two key differences are:
  <ol>
  	<li>Administrators receive a consent dialog ("are you sure you want to do this?") as opposed to the credentials dialog standard users see ("please enter the user name and password for an account with privileges to accomplish this task").</li>
  	<li>Processes launched by an administrator with administrative privileges (i.e. launched through a UAC consent dialog) run as the same user who launched them. Administrative processes launched on behalf of a standard user (i.e. with a UAC credentials dialog in the so-called "over the shoulder" scenario) run as the administrator who launched them. This is a extremely critical point. I have mentioned it before, and will do so again, because it is REALLY IMPORTANT.</li>
  </ol>
  Let's say <a href="http://blogs.msdn.com/uac/archive/2006/04/06/570560.aspx">Abby</a> just bought a brand-new machine with Windows Vista on it. She brings it home, sets it up, transfers her data off the family's old Windows XP machine. Abby creates an account for herself (creatively named Abby) with administrative privileges. Abby also creates an account for her teenage son, Toby. Toby gets standard user privileges and some locked-down functionality courtesy of the new parental controls in Vista. For example, Toby is not allowed to play games rated <em>M</em>.

  Not surprisingly, Toby doesn't like this arrangement. He really wants to play Prey, Crysis, and Halo 2. <strong>Really bad</strong>. So, being the devilishly smart cookie that he is, he convinces his mom that he <em>really </em>needs to have Word or Notepad, or whatever, launched for him with administrative privileges. Toby goes to the File.Open dialog, navigates to the system32 directory, right clicks on MMC, chooses Open, selects the Users and Groups snap-in, and adds his account to the administrators group. Damn, mom just got <em>pwned</em>.

  The bottom line is that requiring a piece of software to be run with administrative privileges in such a way that a standard user can interact with it can lead to very unexpected, very deleterious effects. This is why when you write software for Vista you should make absolutely certain that only the barest minimum chunks of code run with administrative privileges. For the 95% case, your app should never require administrative privileges to perform a task. For the other 5%, stay tuned: I'll be writing about how to factor these pieces of administrative functionality into a separate application. 
