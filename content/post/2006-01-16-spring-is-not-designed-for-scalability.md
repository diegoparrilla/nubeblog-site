---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2006/01/spring-is-not-designed-for-scalability.html
categories:
- Uncategorized
date: 2006-01-16T09:23:00Z
dsq_thread_id:
- "204894250"
guid: /2006/01/spring-is-not-designed-for-scalability/
id: 107
title: Spring is not designed for scalability
url: /2006/01/16/spring-is-not-designed-for-scalability/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-count="vertical" data-url="/2006/01/16/spring-is-not-designed-for-scalability/">Tweet</a>
</div>

Reading blogs most of the time does not give you any value, because 90% of the content is just people referencing other people. It&#8217;s good to know people opinions, but it takes some time to find good stuff.  
This blog has really good stuff, [POJO Mojo](http://blog.terracottatech.com/archive/2006/01/conflicting_gal.html), and some times you can find pearls like this.  
First, I really love Spring and I love all these new light frameworks growing thanks to the lacks of J2EE. They are really excellent if you want to build quickly web applications. But they are not good if you want to build your application thinking in scalability. Basically you have two options if you want to scale with pure web applications:  
a) Use a HTTP cluster. You have to trust in the implementing made by your servlet container provider,and follow some simple rules. With this solution you only replicate the content of the HTTP session, but what about the &#8216;live&#8217; data of the application?  
b) Implement an ad-hoc clustered solution for the data in the &#8216;model&#8217;.  
Most of the developers understand a), but only a reduced set of developers can really see the complexity of b). Even experienced developers crash when dealing with ad-hoc clustered solutions.  
Strictly speaking, Spring is not bad scaling, simply it was not designed to scale.  
EJB3 is really good simplifying the complexity of developing enterprise class applications, but the new POJO entities are really good not only simplifying the development, but hiding the complexity of clustering data to the developers. This is why I see EJB3 as a winner.  
In years to come we will see the rise of the pervasive computing and grid computing. And only a selected set of people can really handle the complexity of these solutions. So we will see how more layers will cover all these new complexity, to help ordinary people like me to build scalable apps.  
But who is building these products?<span style="font-weight: bold;"></span>
