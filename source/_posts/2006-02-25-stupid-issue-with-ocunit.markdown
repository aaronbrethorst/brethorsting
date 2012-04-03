--- 
layout: post
title: Stupid Issue with OCUnit
tags: 
- Developer Tools
comments: true
type: post
published: true
meta: 
  dsq_thread_id: "91763369"
---
I hit an issue with OCUnit the other day when I was trying to get a project of mine working correctly with it. The issue was that using the macro STAssertEqualObjects anywhere would cause the following build error:

  <em>error: parse error before 'typeof'</em>

  After a whole lot of digging, I finally figured out what was causing this issue. I reprint it here because no-one else appears to have this documented. If you are running into this problem, go check that the selected C Language Dialect is anything besides ANSI C or some variant thereof. This includes C89 and C99. C99 does not include support for the typeof keyword, which is what is causing this error message.

  My whole iRooster project was originally set to use C99 mode because it drives me nuts to not be able to declare ints inside of a for loop (like in the following syntax: for (int i=0; i<[foo length]; i++) { /* */ }.

  Setting the C Language Dialect to GNU99, on the other hand, will give you the the for loop declaration ability, along with support for typeof, thereby neatly solving the problem.

  Good luck!
