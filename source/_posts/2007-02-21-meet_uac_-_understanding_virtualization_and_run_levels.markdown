--- 
layout: post
title: Meet UAC - Understanding Virtualization and Run Levels
tags: 
- UAC
- Vista
status: publish
type: post
published: true
meta: 
  dsq_thread_id: "92385086"
---
You've probably heard a lot about User Account Control (UAC) on Windows Vista already. Contrary to popular perception, it's really not that bad, as long as the developers creating the software you use do the right thing by not trying to write or access stuff where they shouldn't. Ensuring that your software correctly supports UAC is critical to providing your users with a great experience on Vista.

  On 32-bit versions of Windows Vista, a system called virtualization is used to improve compatibility with apps that still <strong>do the wrong thing</strong> in terms of irresponsibly writing data to protected locations, such as the Windows directory, Program Files, or HKLM. Basically, virtualization silently redirects non-privileged writes to these locations to a location where the user who launched the process <em>can</em> write. You can see right now which of your applications are virtualized by opening Task Manager and choosing Select Columns from the View menu.

  <img src="http://brethorsting.com/blog/wp-content/uploads/2007/02/virtualization.png" alt="Virtualiztion in Task Manager" />

  Virtualization is something that your software is automatically opted into on 32-bit Windows. To specifically exclude your application from being virtualized, you must include an XML manifest with your app that specifies its UAC runlevel. A runlevel consists of one of three values:
  <ul>
  	<li>asInvoker - Run this process with the account and privileges of the person who launched it. You should default to choosing asInvoker, and only deviate if absolutely necessary.</li>
  	<li>highestAvailable - This one is kind of an odd duck. Basically, it says that this application should be run with the highest privileges available to the account that launched it. For example, let's say you're logged into your computer with an account that is a member of the Backup Operators group. Windows sees this, and requests that you authorize this application to be run at that privilege level. From the Ux perspective: if this app is launched by a standard user, it just runs. If the app is launched by anyone else (Administrator, Backup Operator, etc.) they will get a UAC prompt. Regedit uses highestAvailable. You shouldn't. End of story.</li>
  	<li>requireAdministrator - Just like it sounds. This app is only available to people with administrative privileges. If your account has admin privs, you're presented with a UAC consent dialog. If you don't, then you get a UAC credentials dialog. The UAC credentials dialog requires an administrator to come along and enter their password "over the shoulder" of the person operating the computer. Here's the funky bit: if an administrator <em>does</em> launch a process that is marked as requireAdministrator, that process runs as that administrator. If an application has the ability to launch other apps from within it, those will also be run with the administrator's privilege set (likes beget likes is the rule of thumb). Be cautious, in any case. Some apps, like MMC, require administrative privileges to launch.</li>
  </ul>
  Whew, that was a mouthful. I still have a lot more to talk about: creating your manifest, specifying the runlevel, embedding it into your managed application with VS 2005. I'll be along with a follow-up soon to answer all of these questions.

  In the mean time, I highly recommend reading the old posts on <a href="http://blogs.msdn.com/uac/">the UAC team's blog</a>. They have a wealth of information available, there.
