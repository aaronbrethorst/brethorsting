--- 
layout: post
title: Tabs, Tabs, Everywhere!
tags: 
- Usability
comments: true
type: post
published: true
meta: {}

---
The tab control is a fantastic tool for grouping large numbers of related UI elements into a limited amount of space. Jennifer Tidwell, author of <a href="http://www.brethorsting.com/uidesign/2006/07/designing_interfaces.html">Designing Interfaces</a>, provides a set of reasons, use cases and common designs for correctly applying this UI design pattern to your application:
  <blockquote>The labeled "cards" structure the content into easily-digestible chunks, each of which is now understandable at a glance. Also, tabs, the most common form of Card Stack, are very familiar to users.</blockquote>

  Of course, it's very easy to go overboard on creating tabbed UIs, <a href="http://homepage.mac.com/bradster/iarchitect/tabs.htm">as the Interface Hall of Shame points out in excruciating detail</a>:
  <blockquote>The sheer number of tabs, combined with the use of iconic labels and the gratuitous use of graphics on the tabs themselves results in a veritable visual assault.</blockquote>

  Interestingly, if you examine the Interface Hall of Shame's write-up on Multi-Edit 8.0, they describe how this application can improve its Options dialog (or Preferences, for a Mac user). The Interface Hall of Shame's recommendation is to remove the multiple rows of tabs, and turn them into a listview on the left hand side of the Options dialog. The solution presented here is typically effective, but breaks down for the case where an application uses tabs embedded inside tabs. Employing tabs within tabs is almost always a no-no, in my book, as it requires the user to manipulate two separate navigational mechiansms.

  The solution to this second problem is one that you can find in Visual Studio, today. VS makes use of a treeview control for its Options dialog, instead of a listview. By using a treeview, many related property pages can be grouped together in a logical fashion, while still maintaining a single navigational mechanism.

  <img alt="Visual Studio Tools Options dialog" src="http://www.brethorsting.com/uidesign/dir_vs8_standard_x86.png" width="425" height="252" />
