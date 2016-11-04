---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2006/01/hole-in-ejb3-spec.html
categories:
- Uncategorized
date: 2006-01-23T23:18:00Z
dsq_thread_id:
- "206223845"
guid: /2006/01/hole-in-the-ejb3-spec/
id: 103
title: Hole in the EJB3 spec?
url: /2006/01/23/hole-in-the-ejb3-spec/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-count="vertical" data-url="/2006/01/23/hole-in-the-ejb3-spec/">Tweet</a>
</div>

One of the smartest moves in J2EE (or JEE, who cares&#8230;) is how Hibernate has influenced the Persistence API. You can smell the Hibernate flavor. This API is a light wrap of Hibernate. If you are familiar with Hibernate, POJOs and hbm.xml files, you can start working with EJB3 Entities.

One of the magical things of Hibernate is how to retrieve graphs of objects &#8216;lazily&#8217;. You can do things like:

<div style="text-align: center;">
  <span style="font-family: courier new;">user.getProvince().getCountry().getLanguage();</span>
</div>

and Hibernate takes care of retrieving information from the tables PROVINCE, COUNTRY and LANGUAGE to populate the mapped POJOs. The magic wand is what they call &#8216;Instrumentation&#8217; of the POJOs: They manipulate the bytecode in runtime thanks to the cglib library.

This approach has a lot of advantages, but a little disadvantage. If you want to transfer an instrumented POJO from one application to another application using RMI (or CORBA), you will need all the Hibernate libraries in both sides. Why? Because the instrumented POJO references Hibernate classes. This process is done transparently to the developer (and this is great!), but it arises as something annoying when using remote invocations. A couple of years ago, I tried to use Hibernate POJOs inside SLSB EJBs, and instead of using Transfer Objects, I used the same instrumented POJOs. It worked, but I had to put in my remote client the Hibernate jars, and I had to be cautious using lazy fetching of data. But it worked.

Now we have started a project with a mid-term roadmap, and we are going to use the new EJB3 spec on JBoss Application Server. One of the requirements is that maybe in a not so near future, the web layer is going to be physically placed in a different server. So we tried to use EJB3 entities as Transfer Objects. And&#8230; Surprise! We found out that the EJB3 Entities are instrumented Hibernate objects! So we had to put the Hibernate libraries in the remote TOMCAT client in order to work.

I was a bit surprised, and I posted this message in the [JBoss.com &#8211; Forums &#8211; Attaching and detaching EJB3 Entities](http://www.jboss.com/index.html?module=bb&op=viewtopic&t=75971) asking for some help (JBoss guys answer promptly), and the answer was: &#8216;Put the hibernate jars in the client&#8217;. Ok&#8230; Thanks a lot&#8230; But&#8230; Is this what the specification says? If you read the [specification](http://sdlc-esd.sun.com/ESD20/JSCDL/ejb/3.0-pfd/ejb-3_0-pfd-spec-persistence.pdf?AuthParam=1138051670_d5a7be635521e3a0f4d89052f2629b4d&TUrl=EMr8DPgljlCngjJlNnNDcFaPvU7tT+IO859ZF2EwLi4b1e0IkW/TF/LVaA==&TicketId=dlV6NgVKMeg//Q==&GroupName=SDLC&BHost=sdlcweb9a.sun.com&FilePath=/ESD20/JSCDL/ejb/3.0-pfd/ejb-3_0-pfd-spec-persistence.pdf&File=ejb-3_0-pfd-spec-persistence.pdf) in Chapter 3.2.4 &#8216;Detached Entities&#8217;, it is not clear if it&#8217;s mandatory to implement the Entities marked with fetch=EAGER without any kind of manipulation: <span style="font-style: italic;">The application may access the available state of available detached entity instances after the persistence </span><span style="font-style: italic;">context ends. </span>If you are using POJOs, and you are not using Hibernate explicitly, why do I need the Hibernate jars?

This problem has arisen too in the [Glassfish project](http://forums.java.net/jive/thread.jspa?messageID=36803&tstart=0), and some people have suggested to implement some kind of <span style="font-style: italic;">transparent detaching </span>of the POJOs before serialization. I think this is something the specification lacks of, and should be updated in order to fix this annoying problem.
