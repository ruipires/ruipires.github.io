---
layout: post
navigation: True
class: post-template
subclass: 'post'
status: publish
published: true
title: Gang of Four interviewed 20 years later
author: rui
author_email: rui@sennin.pt
author_url: http://www.sennin.pt
excerpt: "<p>The <a href=\"http://www.se-radio.net\">software engineering radio
  podcast</a> has a very interesting <a href=\"http://www.se-radio.net/2014/11/episode-215-gang-of-four-20-years-later/\">interview</a>
  with the <a href=\"http://en.wikipedia.org/wiki/Design_Patterns\">Gang
  of Four members, from \"Software Design Patterns\" fame</a>. It is roughly 75
  minutes, but it is really nice seeing them comment on their book 20 years later.</p><p>Here
  is a transcript I did of a portion of the podcast that I found extremely&nbsp;interesting
  (validating of my point of view, actually), that I just had to write down and keep,
  so I could quickly use it as a way to avoid discussions about the recurring Singleton-as-global
  (anti?) pattern.</p>"
wordpress_id: 536
wordpress_url: http://www.sennin.pt/?p=536
date: '2015-01-23 01:20:46 +0000'
date_gmt: '2015-01-23 01:20:46 +0000'
categories:
- books
- interview
- c++
tags: [books, interviews, c++]
banner: '/assets/2015/azulejos-de-lisboa.png'
cover: '/assets/2015/cover/azulejos.jpg'
cover_url: "https://www.flickr.com/photos/silviabes/10522661346/"
cover_author_name: Silvia Benedet
cover_author_url: "https://www.flickr.com/photos/silviabes/"
cover_license_url: "https://creativecommons.org/licenses/by-nc/2.0/"
cover_license: CC BY-NC 2.0
comments:
- id: 5709
  author: Arne Mertz
  author_email: blogadmin@arne-mertz.de
  author_url: http://arne-mertz.de
  date: '2015-03-30 16:29:47 +0000'
  date_gmt: '2015-03-30 16:29:47 +0000'
  content: Great! Singleton on the backlog for my blog, and this is the missing piece
    for my argumentation. May I link to your transcript?
- id: 5710
  author: Rui Pires
  author_email: rui@sennin.pt
  author_url: ''
  date: '2015-03-30 17:47:45 +0000'
  date_gmt: '2015-03-30 17:47:45 +0000'
  content: Sure you can, It would be an honor.
- id: 5715
  author: Singletons &#8211; What&#8217;s the Deal? | Simplify C++!
  author_email: ''
  author_url: http://arne-mertz.de/2015/04/singletons-whats-the-deal/
  date: '2015-04-12 16:00:34 +0000'
  date_gmt: '2015-04-12 16:00:34 +0000'
  content: "[&#8230;] There is an episode of the &#8220;SE-Radio&#8221; Podcast&nbsp;where&nbsp;Johannes
    Th&ouml;nes interviews three of the GoF members about their book and the evolution
    of design patterns.&nbsp;Towards the end they also talk specifically about Singleton.
    You can see a transcript of that section here. [&#8230;]"
---

<img src="{{ site.baseurl }}/assets/2015/azulejos-de-lisboa.png">
<p>The <a href="http://www.se-radio.net">software engineering radio podcast</a> has a very interesting <a href="http://www.se-radio.net/2014/11/episode-215-gang-of-four-20-years-later/">interview</a> with the <a href="http://en.wikipedia.org/wiki/Design_Patterns">Gang of Four members, from "Software Design Patterns" fame</a>. It is roughly 75 minutes, but it is really nice seeing them comment on their book 20 years later.</p>
<p>Here is a transcript I did of a portion of the podcast that I found extremely&nbsp;interesting (validating of my point of view, actually), that I just had to write down and keep, so I could quickly use it as a way to avoid discussions about the recurring Singleton-as-global (anti?) pattern.</p>
<p><a id="more"></a><a id="more-536"></a></p>
<p>This took place at around minute 56 onward, when they were commenting on how the patterns in their book stood the test of time.</p>
<blockquote>
<p>Ralph Johnson: (...) I would say that creational patterns, we have been making comments about Singleton, but in fact all the creational patterns are not used as much as they were back when we wrote the book because dependency injection is sort of an alternative pattern that ...</p>
<p>Erich Gamma: Decouples things</p>
<p>Ralph Johnson: is sort of a better way of doing things. There are still cases where the other patterns make sense, but they just make sense a lot less frequently because dependency injection is often a better way of doing things.</p>
<p>Johannes: So you mentioned in the beginning, so I'm just saying the word of the pattern: Singleton.</p>
<p>Erich Gamma: So we added it, and it was an example everybody understood. In C++ how you do Singleton, have a static member and whatever, right? Everybody got that immediately, I think. That&nbsp;was a great way to tell someone what you talk about, but if you think about it doesn't have a lot of coolness, Singleton, right? You something global which is kind of against objects, which are more about distributing things and not having a centralised thing which will at some point hurt you because you want to have multiple of these things, or whatever, right? Its often a design shortcut. To me Singleton is often a design shortcut. You have a well known place to get to another object, rather than reach into objects to get to this space, so thats why it often hurts [unintelligible] so that why its not on my top list of favorite patterns, right? To me its a list of the things that will be listed off of the island: Singleton.</p>
<p>Ralph Johnson: In Smalltalk Singleton has not been the problem that it is in C++. What people have used it for in Smalltalk is: you try to eliminate global state when you can, when you just can't get rid of it, then you manage it, and that's a good way of managing it. But the problem is, I think in C++ is a lot of people instead of using it as a way to manage global state you can't get rid of, they instead use it as an excuse, or something that will make it ok, to have global state.</p>
<p>Erich Gamma: thats a justification for having global state.</p>
<p>Ralph Johnson: It's a justification for having global state. "Its a pattern! Its ok because it is a pattern!" And global state is bad, you want to get rid of it as much as you can.</p>
<p>Erich Gamma: And my rule is it is very easy to add global state, but it is very hard to take it out.</p>
<p>Johannes&nbsp;Th&ouml;nes: So you think in retrospect you shouldn't have put it into the book ?</p>
<p>Erich Gamma: You see, I love all the patterns that we have in the book. So that is something ... I made peace with them.</p>
<p>Ralph Johnson: So I've got a version of Singleton that I've rewritten. I wrote it in a way to make it really clear that global state is bad and this is only what you do when you can't get rid of it. So we could have written it in a way that would have made that more clear. Its just that we didn't realize how people were going to interpret it. We didn't realize that people would have taken it as a justification for global state. You just put the book out there and see what people do with it.</p>
</blockquote>
