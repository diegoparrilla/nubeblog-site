---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2006/01/spring-is-not-designed-for-scalability_17.html
categories:
- Uncategorized
date: 2006-01-17T00:38:00Z
dsq_thread_id:
- "217171185"
guid: /2006/01/spring-is-not-designed-for-scalability-part-2/
id: 106
title: Spring is not designed for scalability, part 2
url: /2006/01/17/spring-is-not-designed-for-scalability-part-2/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-count="vertical" data-url="/2006/01/17/spring-is-not-designed-for-scalability-part-2/">Tweet</a>
</div>

You never know when a post in your personal blog can make people like [Cameron Purdy](http://jroller.com/page/cpurdy?entry=escapismability_correcting_the_corrections) (one of my java-hero) or Bob Griswold (Senior Vice President of Terracotta Tech.) start an interesting discussion about different solutions to architect data clustering.  
Cameron Purdy has been behind [Tangosol Coherence](http://www.tangosol.com) since the beginning, may be he is (or was) the main developer. Simplifying, it was an implementation of the Map interface that replicates data across different JVMs using different policies. I evaluated it three years ago and I made a strong recommendation of purchase in my former company (and they ignored me, as usual). I have reviewed it recently and it has improved a lot. I guess Cameron&#8217;s product represents one trend in data clustered architectures: extend and existing API (Collections) to help developers to build the data clustered solution.  
[Terracotta](http://www.terracottatech.com/) is something new, and apart from [Azul Systems](http://www.azulsystems.com/), may be the most interesting technology in the very mature Java market. Its technology can make applications to share data transparently between JVMs. How? I don&#8217;t know, honestly, but I will try to figure out how&#8230; They represent another trend in data clustering architectures: developers don&#8217;t need to know new APIs to manage clustered data.  
Both solutions help developers to build highly scalable solutions when shared data is necessary (most of the times, BTW). Both have pros and cons, but basically you can build the same things with them. If the application needs to share data in not a very complex way, may be a non-explicit solution like Terracota&#8217;s Virtualization Server can do better than Tangosol Coherence. But if the application is complex enough to required some kind of &#8216;ad-hoc&#8217; replication strategy or policy, then a explicit solution like Cameron&#8217;s product can do it better.  
Regarding Spring, it is not just a framework: it is THE FRAMEWORK. I have discussed with colleagues several times about Spring, and we really think that people developing Spring KNOW about building applications, because it is designed to be <span style="font-weight: bold;">effective</span>. But I cannot agree with people thinking Spring can make applications more scalable than any other framework. Spring has a lot of advantages, but making an application scalable has nothing to do with frameworks (can Struts help you to build scalable applications? No!). May be Hibernate or EJB3 Entities for instance can help you to make your application to scale because of its caching capabilities (EJB3 depending on the app server provider), but then we have to focus on frameworks that manage data. Spring and Hibernate is the perfect duo, but they are different stuff.  
Finally, [better performance can be a side effect of scalability](http://www.digizenstudio.com/blog/2006/01/16/what-exactly-is-scalability/), but it is not the goal of scalability. Actually, most of the times making an application to scale (horizontally) has a price in performance. Scalability is how to make your application to perform with 1000000 users just like if your application has only 1000.

Anyway, thank you all for your very interesting thoughts.
