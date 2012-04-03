--- 
layout: post
title: Meet UAC - Creating a UAC Manifest
tags: 
- UAC
- Vista
comments: true
type: post
published: true
meta: 
  dsq_thread_id: "91763926"
---
<a href="http://www.brethorsting.com/uidesign/2007/02/meet_uac_understanding_virtual.html">Last time</a>, we took a dive into what virtualization on Windows Vista is all about, and examined the different run levels available to your application. Like I mentioned before, <strong>unless you know for a fact</strong> that your app should run with higher privileges, you should always make your application run under asInvoker.

  Today, we're going to look at how to create a UAC-aware Fusion manifest, in order to deliver the best User Experience possible to your customers on Windows Vista.

  The manifest file itself is relatively simple: it's a blob of XML that sits either side-by-side or embedded within your executable. Back in the Windows XP timeframe, there were two ways to give your application Windows XP visual styles. The first was to call the method EnableVisualStyles() on the Application() class in your Main() method. The second was to <a href="http://www.developer.com/net/asp/article.php/3101831">create a Fusion manifest</a>:
  <pre>
  &lt;?xml version="1.0" encoding="UTF-8" standalone="yes"?&gt;
  &lt;assembly xmlns="urn:schemas-microsoft-com:asm.v1"
            manifestVersion="1.0"&gt;
  &lt;assemblyIdentity
      version="Insert Your Exact Version Number Here"
      processorArchitecture="X86"
      name="Name of Application"
      type="win32"
  /&gt;
  &lt;description&gt;Description of Application&lt;/description&gt;
  &lt;dependency&gt;
      &lt;dependentAssembly&gt;
          &lt;assemblyIdentity
              type="win32"
              name="Microsoft.Windows.Common-Controls"
              version="6.0.0.0"
              processorArchitecture="X86"
              publicKeyToken="6595b64144ccf1df"
              language="*"
          /&gt;
      &lt;/dependentAssembly&gt;
  &lt;/dependency&gt;
  &lt;/assembly&gt;</pre>
  When Windows Vista came along, the simplest way for the UAC team to correctly support various runlevels was by overloading the functionality provided by a Fusion manifest to provide this extra information. You can specify the desired runlevel for your application by adding an extra bit of goop to your application's manifest. If your app doesn't have one yet, don't fret! We'll handle that, too.

  UAC information specified within a Fusion manifest looks like the following:
  <pre>
    &lt;!-- Identify the application security requirements. --&gt;
    &lt;trustInfo xmlns="urn:schemas-microsoft-com:asm.v3"&gt;
      &lt;security&gt;
        &lt;requestedPrivileges&gt;
          &lt;requestedExecutionLevel
            level="asInvoker"
            uiAccess="false"/&gt;
        &lt;/requestedPrivileges&gt;
      &lt;/security&gt;
    &lt;/trustInfo&gt;
  &lt;/assembly&gt;</pre>
  There are two key elements specified within the requestedExecutionLevel:
  <ul>
  	<li><strong>level</strong> - This is the runlevel we explored last time. Unless you have a very good reason not to, you should always specify asInvoker here.</li>
  	<li><strong>uiAccess</strong> - Set this to "false" unless you know exactly why you require UI access. Essentially, this parameter specifies whether or not your application requires the ability to drive UI input into other apps. Examples of apps in this class would include assistive technologies like screen readers or automated UI testing frameworks.</li>
  </ul>
  The full Fusion manifest updated for Vista will look like this:
  <pre>
  &lt;?xml version="1.0" encoding="UTF-8" standalone="yes"?&gt;
  &lt;assembly xmlns="urn:schemas-microsoft-com:asm.v1" manifestVersion="1.0"&gt;
    &lt;assemblyIdentity
        version="1.0.0.0"
        processorArchitecture="X86"
        name="ChimpSoftware.Borealis"
        type="win32"
      /&gt;
    &lt;description&gt;Chimp Software Borealis&lt;/description&gt;
    &lt;dependency&gt;
      &lt;dependentAssembly&gt;
        &lt;assemblyIdentity
            type="win32"
            name="Microsoft.Windows.Common-Controls"
            version="6.0.0.0"
            processorArchitecture="*"
            publicKeyToken="6595b64144ccf1df"
            language="*"
          /&gt;
      &lt;/dependentAssembly&gt;
    &lt;/dependency&gt;

    &lt;!-- Identify the application security requirements. --&gt;
    &lt;trustInfo xmlns="urn:schemas-microsoft-com:asm.v3"&gt;
      &lt;security&gt;
        &lt;requestedPrivileges&gt;
          &lt;requestedExecutionLevel
            level="asInvoker"
            uiAccess="false"/&gt;
        &lt;/requestedPrivileges&gt;
      &lt;/security&gt;
    &lt;/trustInfo&gt;
  &lt;/assembly&gt;</pre>
  Drop this text into a file named MyApplication.exe.manifest, and place it next to your executable. Clearly, MyApplication should be the name of your app. You should also replace the references to Chimp Software Borealis with references to the name of your app (gee, what's Borealis?). Now, launch your app and then Task Manager. You should see that your application is no longer being virtualized. If you do bad things, like writing to Program Files or the Windows directory, these calls will now promptly fail. This is good, because those are bugs in your app. Go fix 'em!

  Clearly, you still need a way to bundle the manifest with your application. You could simply add the manifest to your setup application, but you'd be better off embedding the manifest directly into your application. Directions for doing this are pretty straightforward for native applications, and instructions already exist on how to do this. Trying to do this for a managed application with VS 2005 is trickier. Next time, I'll show you how to solve this problem.
