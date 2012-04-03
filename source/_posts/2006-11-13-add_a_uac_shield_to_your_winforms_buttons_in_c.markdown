--- 
layout: post
title: Meet UAC - Add a UAC Shield to your Winforms buttons in C#
tags: 
- UAC
- Vista
comments: true
type: post
published: true
meta: 
  dsq_thread_id: "93354621"
---
One of the big, new features in Windows Vista is <a href="http://www.microsoft.com/technet/windowsvista/security/uacppr.mspx">User Account Control</a>, which is designed to...
  <blockquote>...reduce the exposure and attack surface of the operating system by requiring that all users run in standard user mode. This limitation minimizes the ability for users to make changes that could destabilize their computers or inadvertently expose the network to viruses through undetected malware that has infected their computer.</blockquote>
  There is a good deal of useful, interesting information available on the topic from the <a href="http://blogs.msdn.com/uac">UAC team's blog</a>, which I highly recommend reading through. For today, though, I want to dig into one topic for which I haven't seen any coverage yet. If you're writing a managed application, it's not immediately obvious how to add a shield to buttons in your application without manually copying a bitmap resource into your project...which kind of sucks. So, without further ado, here's one way (presented "as-is with no warranties expressed or implied") to handle this operation:

  <code>
  using System;
  using System.Collections.Generic;
  using System.Runtime.InteropServices;
  using System.Text;</code><code>namespace SecurityButtonTest
  {
    public class ShieldButton : System.Windows.Forms.Button
    {
      public ShieldButton() : base()
      {
        this.FlatStyle = System.Windows.Forms.FlatStyle.System;
        this.ShowShield = true;
      }

      private bool m_showShield;
      public bool ShowShield
      {
        get { return m_showShield; }
        set
        {
          m_showShield = value;
          SendMessage(new HandleRef(this, this.Handle), BCM_SETSHIELD, IntPtr.Zero, new IntPtr(m_showShield ? 1 : 0));
        }
      }

      const uint BCM_SETSHIELD = 0x0000160C;
      [DllImport("user32.dll", CharSet = CharSet.Unicode)]
      static extern IntPtr SendMessage(HandleRef hWnd, UInt32 Msg, IntPtr wParam, IntPtr lParam);
    }
  }

  </code>And here is the ShieldButton control in action:
  <img width="398" src="http://www.brethorsting.com/uidesign/2006/11/15/shieldbutton.png" alt="Shield Button" height="432" />
