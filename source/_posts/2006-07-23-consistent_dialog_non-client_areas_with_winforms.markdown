--- 
layout: post
title: Consistent Dialog Non-Client Areas with Winforms
tags: 
- Windows
status: publish
type: post
published: true
meta: 
  dsq_thread_id: "95463084"
---
Even though it receives far less attention than it's more-malleable sibling, the non-client area of a dialog (the window frame, etc.) is highly configurable with Winforms 2.0. There are several guidelines that you should follow when creating new dialogs in order to ensure that your application's non-client area meets the Windows Ux Guidelines.

  By default, you should use the following settings for your window’s frame:
  <ol>
  <li>MaximizeBox = false</li>
  <li>MinimizeBox = false</li>
  <li>ShowIcon = false – Dialog boxes must never have an icon in their top-left corner.</li>
  <li>ShowInTaskbar = false – Dialog boxes must never be shown in the task bar.</li>
  <li>FormBorderStyle = Sizable or FixedDialog – Make sure that dialog resizing works as expected when enabling this.</li>
  <li>SizeGripStyle = Show or Hide – Make sure that the resize handle is always visible when the FormBorderStyle is set to Sizable, or never shown when set to FixedDialog.</li>
  </ol>

  When naming your dialog, there are a few simple guidelines to follow:
  <ol>
  <li>Dialog title is concise; describes intent succinctly.</li>
  <li>First letter of each word is capitalized.</li>
  <li>Never use periods, colons, semicolons, commas or other punctuation in a dialog title, except for proper names.</li>
  </ol>

  Examples:
  <ol>
  <li>“Options”</li>
  <li>“About MyCompany Software”</li>
  <li>“Select Resource”</li>
  </ol>

  Anti-Examples:
  <ol>
  <li>“Choose a file to open:” – Lacks proper capitalization, too wordy, and includes a colon.</li>
  <li>“OPEN FILE…” – Lacks proper capitalization, and includes three periods.</li>

  <img alt="A proper titlebar" src="http://www.brethorsting.com/uidesign/Titlebar.png" width="318" height="65" />
