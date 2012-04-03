--- 
layout: post
title: Android in 5 Minutes (or your money back!)
tags: 
- Android
- Mobile
comments: true
type: post
published: true
meta: 
  _edit_last: "2"
  dsq_thread_id: "199722277"
  _wp_old_slug: ""
---
In response to a request for help on how to get the Android SDK up and running on a Mac, I thought it might be worthwhile to go back through the process and see how simple and fast I could make it. As it works out, I was able to get the Android emulator running on my Mac in about 5 minutes.

Here's what this (abbreviated) guide covers: getting the Android emulator running with Gingerbread.

Here's what it doesn't cover: everything else, including Eclipse installation, because—quite frankly—Eclipse is a hairy, scary beast.

<strong>Step 1: Download the Android SDK</strong>

<a href="http://developer.android.com/sdk">Go to the Android Developers website</a>, and choose the appropriate package for your platform. In my case, it was the zip file entitled android-sdk_r08-mac_86.zip. Download the file. The package is about 28MB in size.

<strong>Step 2: Stick it Somewhere Memorable</strong>

I dragged the Android SDK folder into my /Applications folder, but you can put it wherever you want to.

<strong>Step 3: Launch the AVD Manager</strong>

Navigate into the Android SDK's tools folder, and double click on the Unix executable called <em>android</em>. A window entitled <em>Android SDK and AVD Manager</em> will appear.

<strong>Step 4: Install the Gingerbread SDK</strong>

For whatever reason, Google decided to designate the components of each Android OS with three separate names. Gingerbread = 2.3 = API 9 (don't ask, I have no idea). We're going to install Gingerbread: choose <em>Available Packages</em> from the table on the left and click the disclosure triangle next to <em>Android Repository</em>.

You'll see an item right near the top called "SDK Platform Android 2.3, API 9, revision 1". Check the checkbox next to it and then click the <em>Install Selected</em> button in the lower right corner of the window.

A window entitled <em>Choose Packages to Install</em> will appear. Click the <em>Accept All</em> radio button button and then press the <em>Install</em> button. The Gingerbread SDK will now begin downloading.

Once complete, you can click the <em>Close</em> button (formerly labeled <em>Cancel</em>) on the <em>Installing Archives</em> window. Make sure you watch carefully as the dialog doesn't provide any other meaningful feedback.

<strong>Step 5: Create an AVD</strong>

I think AVD stands for Android Virtual Device, but I could be horribly mistaken. Long story short, it's the virtual hardware/software combination that the emulator will run to let you play with Android. Select <em>Virtual devices</em> from the left-hand table and click the <em>New</em> button.

Give your AVD a name; I called mine "Gingerbread." Next, choose a target: the only option available will be <em>Android 2.3 - API Level 9</em>. Finally, click <em>Create AVD</em>.

<strong>Step 6: Fire it Up!</strong>

Select your new AVD in the Virtual devices list, and click the <em>Start...</em> button on the right hand side. A <em>Launch Options</em> dialog will appear. Ignore it, and click the <em>Launch</em> button. The Android emulator will appear and launch. Note that it takes a couple minutes for the emulator to boot. Congratulations! You're all set!
