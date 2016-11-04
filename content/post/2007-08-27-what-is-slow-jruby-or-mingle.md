---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2007/08/what-is-slow-jruby-or-mingle.html
categories:
- Uncategorized
date: 2007-08-27T15:00:00Z
dsq_thread_id:
- "204692731"
guid: /2007/08/what-is-slow-jruby-or-mingle/
id: 51
tags:
- java
- management
- ruby
title: What is slow? JRuby or Mingle?
url: /2007/08/27/what-is-slow-jruby-or-mingle/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="java,management,ruby" data-count="vertical" data-url="/2007/08/27/what-is-slow-jruby-or-mingle/">Tweet</a>
</div>

I have been testing [Mingle](http://studios.thoughtworks.com/mingle-project-intelligence), the new tool from [<span class="blsp-spelling-error" id="SPELLING_ERROR_0">Thoughtworks</span>](http://studios.thoughtworks.com/) to manage Agile developments. The application really looks promising, and have a lot of new features that I&#8217;m discovering, but it&#8217;s taking me more time than I expected because it&#8217;s slow, very slow.

The guys from <span class="blsp-spelling-error" id="SPELLING_ERROR_1">Thoughtworks</span> claim they have built the first <span class="blsp-spelling-error" id="SPELLING_ERROR_2">JRuby</span> commercial application. Probably true, but the price they have paid is high. The application is slow, and it&#8217;s slow even on a 2.8<span class="blsp-spelling-error" id="SPELLING_ERROR_3">Ghz</span> 2<span class="blsp-spelling-error" id="SPELLING_ERROR_4">Gb</span> Server. I have checked the default <span class="blsp-spelling-corrected" id="SPELLING_ERROR_5">configuration</span> and heap size is set by default to 1 gig. Not too bad for an application being use by a single user&#8230;

I hope they make some changes to improve the overall performance of the application. It&#8217;s not very &#8216;Agile&#8217;.
