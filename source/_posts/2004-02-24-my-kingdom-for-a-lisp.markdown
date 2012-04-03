--- 
layout: post
title: My Kingdom for a LISP
tags: 
- Technology
comments: true
type: post
published: true
meta: {}

---
I'm working on a project right now that requires me to parse a humongous tree of data (folders and html files), and then build all sorts of interesting visual structures out of this information. It's being done in C#, since it's an ASP.Net web application. I would kill to be able to do some of this work in Scheme or Lisp. For example, Scheme gives you the handy-dandy ability to append data onto a list through recursive function calls. In order to kludge this sort of behavior out of C#, I am having to go through any number of contortions. I'm sure there's an easier solution than what I'm doing, but I wanted to use a Scheme-type solution, dammit!

  (((((Multiple) Nested) Parentheses) Are Our) Friends).
