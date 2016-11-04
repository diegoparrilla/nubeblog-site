---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2007/12/google-chart-api-or-how-google-gives.html
categories:
- Uncategorized
date: 2007-12-07T11:40:00Z
dsq_thread_id:
- "204894730"
guid: /2007/12/google-chart-api-or-how-google-gives-raw-performance-for-free/
id: 1218
tags:
- api
- architecture
- google
title: Google Chart API or how Google gives raw performance for free
url: /2007/12/07/google-chart-api-or-how-google-gives-raw-performance-for-free/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="api,architecture,google" data-count="vertical" data-url="/2007/12/07/google-chart-api-or-how-google-gives-raw-performance-for-free/">Tweet</a>
</div>

<div xmlns="http://www.w3.org/1999/xhtml">
  If you dont&#8217; understand why <a href="http://code.google.com/apis/chart">Google is giving for free this API</a>, where is the value of this action, then you probably have never tried to render a chart on the server side. It&#8217;s one of the most CPU intensive actions a server side solution can have. If you don&#8217;t size and distruibute your apps properly, your site can colapse with a single impatient user clicking quickly a link several times or reloading a page because it takes more time than usual to render.<br />A first look at the API shows a very simple API, with a very limited set of functions. The documentation is very oriented to HTML and Javascript developers, but looks easy to implement something in the server side. So think twice before considering changing <a href="http://www.jfree.org/jfreechart/">JFreeChart</a> with this API. Moreover, the number of request per day is 50000 maximum, so if your site has a lot of traffic you will probably need to implement some kind of server side caching strategy. I will make some tests to test the latency of the API, one of the issues with any chart render engine.<br />Google, now you have started creating APIs for tipically CPU intensive tasks, why don&#8217;t you try something with PDF and document generation? My Hosting provider will hate you, but my budget on dedicated servers will have a relief!
</div>
