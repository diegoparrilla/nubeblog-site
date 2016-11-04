---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2006/10/yes-we-still-need-transfer-objects.html
categories:
- Uncategorized
date: 2006-10-09T16:13:00Z
dsq_thread_id:
- "204894848"
guid: /2006/10/yes-we-still-need-transfer-objects-with-ejb3-jpa/
id: 1232
title: Yes, we still need Transfer Objects with EJB3 JPA
url: /2006/10/09/yes-we-still-need-transfer-objects-with-ejb3-jpa/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-count="vertical" data-url="/2006/10/09/yes-we-still-need-transfer-objects-with-ejb3-jpa/">Tweet</a>
</div>

When we started our first project with the Java Persistence API (JPA) and EJB3, we made some decisions about the design following the recommendation of &#8216;experts&#8217; in the domain (see [ONJava.com &#8212; Standardizing Java Persistence with the EJB3 Java Persistence API](http://www.onjava.com/pub/a/onjava/2006/05/17/standardizing-with-ejb3-java-persistence-api.html?page=1), for example).  
One of the decisions was to <span style="font-weight: bold;">get rid of Data Transfer Objects. </span>We took this decision because we firmly believed that the new annotated POJOs could be used a Transfer Objects between the different layers of our architecture. But it was not a good decision.  
Our database model was mapped to our entity model, and about 60-something classes aroused. I don&#8217;t think this is a complex model, but we can say it was &#8216;complex enough&#8217;. We found out very soon that the JPA POJOs were not good when they played the role of DTOs. These are the reasons:

1) We had to tweak the annotations to do EAGER loads of data instead of LAZY loads. Web developers building on top of the EJB3 architecture tried to use objects that were not loaded eagerly, and then they had to make a request to the middle layer developers in order to change the way data load was done.  
2) Detached annotated POJOs were not Plain Old Java Objects, but Plain Old INSTRUMENTED Java Objects. This means that we had to put in the web layer references to Hibernate classes, for instance.  
3) A business method using a set of POJOs had as an extra load the eagerly loaded POJOs, no matter if this business method needed them or not: if another business method was using one of the POJOs, then you have to load even if you don&#8217;t need it. This overhead can be irrelevant in unit testing, but it&#8217;s relevant in stressed systems.  
4) Changes in the ER to OO mapping were propagated to the web layer, forcing the web development team to refactor their code to fix the problem.

All these events were enough to rethink the architecture, and let the Data Transfer Objects come back to our lives. Two new projects with EJB3 with JPA are in development, and we are making a smarter approach: DTOs are used when dealing with data from more than one or two annotated POJOs, and annotated POJOs are used only if they can be used detached from the instrumentation tool (Hibernate in JBOSS). And now things are working much better.

Why all these experts suggested the deprecation of DTOs? I think because of these two reasons:  
1) If the number of POJOs is low, just like in articles and examples happens, then DTOs is a nosense. When the number of POJOs grows and teams of developers are in the battlefield, then sounds reasonable to use DTOs.  
2) If you compare the number of Lines of Code of a solution with DTOs or without DTOs, the less LOC the better to sell the technology. One of the arguments to go with JPA and EJB3 is less code to write. Obviously, if there is no gain, why do we adopt these new technologies? In .NET DTOs are part of the architecture (Datasets and Tablesets). It has strong advantages in small projects, but with big layered architectures they can kill your project: if you want to success with .NET in big enterprise projects you have to choose the &#8216;java style&#8217; and forget about strange artifacts like the Table/Datasets.

EJB3 and JPA are the best thing in J2EE since it&#8217;s creation: simple and smart. But &#8216;experts&#8217; please, ask people in the battlefield of the real life projects before making recommendations.
