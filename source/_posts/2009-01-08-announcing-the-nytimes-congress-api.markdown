--- 
layout: post
title: Announcing the NYTimes Congress API
tags: 
- Technology
- Zoon Politikon
comments: true
type: post
published: true
meta: {}

---
<blockquote>The initial release exposes four types of data: a list of members for a given Congress and chamber, details of a specific roll-call vote, biographical and role information about a specific member of Congress, and a member’s most recent positions on roll-call votes.</blockquote>
The NYTimes just announced their Congress data API. Data is served up via a Rails app that uses _why's Hpricot gem to parse XML from the House website and HTML from the Senate website.

I've been waiting for something like this for a long time, and I'm excited to see it built and maintained by the New York Times. They've been on quite a tear lately in producing web services, and I can't wait to see what's next.

via <a href="http://open.blogs.nytimes.com/2009/01/08/introducing-the-congress-api/">Announcing the Congress API - Open Blog - NYTimes.com</a>.
