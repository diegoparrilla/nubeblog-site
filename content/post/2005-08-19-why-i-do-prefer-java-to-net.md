---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2005/08/why-i-do-prefer-java-to-net.html
categories:
- Uncategorized
date: 2005-08-19T12:26:00Z
dsq_thread_id:
- "204894308"
guid: /2005/08/why-i-do-prefer-java-to-net/
id: 115
title: Why I do prefer Java to .NET
url: /2005/08/19/why-i-do-prefer-java-to-net/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-count="vertical" data-url="/2005/08/19/why-i-do-prefer-java-to-net/">Tweet</a>
</div>

I have been managing (and developing&#8230;) projects in both technologies (Java since 1997 and .NET since 2003), and must recognize that time has only proven my fears about these technologies. So I will enumerate my thoughts about them, and why I do prefer Java:

  * Company philosophy: Microsoft has a non-written rule of &#8216;deliver the product quickly, providing just 90% of the functionality&#8217;. Usually the pending 10% is always the hardest and most critical part of the product. This is the reason why hard to test functionality like threading, managed and unmanaged code integration, multiprocessor support and others does not behave as they should. I think Sun has a different philosophy, and Java has evolved slowly but firmly, being much more predictable in its behavior.
  * IDEs: people use to talk about how Visual Studio is a reference for the IDE market. That&#8217;s because they don&#8217;t know Eclipse and all the army of plugins around. Visual Studio is excellent if you want to deliver something quick and dirty. But if you want to deliver quality&#8230; You cannot refactor or create methods, for example. NANT is the living proof of this assertion: NANT (and ANT, of course) guarantees quality in the building. And we are not going to talk about SourceSafe, right?
  * Server side development: J2EE (or JEE 5&#8230;Who cares) may be is overloaded of functionality that you will never use, but server side developments normally are up and running for several years (if this is not your case, go to LAMP, it is faster, smaller and simpler). Applications evolve and J2EE is the &#8216;army Swiss knife&#8217; that can help you to solve new problems and challenges. .NET has a lighter approach to the server side development, trying to catch developers to their cause easing the development tasks. The price to pay is a product less flexible that lacks of 
  * Java is more predictable: Days when a JVM was a mystery are gone, and all the Java universe is mature and stable (some people say it is as mature as Cobol&#8230; And boring as Cobol too!). It is strange to find unexpected behaviors. As we say in Spain, Java is &#8216;noble&#8217;. .NET sometimes has unexpected behaviors specially when dealing with unmanaged code, and everybody knows that .NET is tightly coupled to Windows. If you have worked in a multithreaded system with .NET interop you know what I mean&#8230;
  * Excellent Opensource products: Java developers can choose between dozens and dozens of frameworks when building an application. Some of these frameworks are not good enough, or does not have the right support, it is true. But the best products are adopted and used by thousands of developers&#8230; For free. So they are always improving. .NET has some good opensource packages, but are ports from Java and they don&#8217;t have the same level of support. For example, check the number of messages in the forums of log4net and log4j, or NANT and ANT.
  * Third party products: This is obvious. If you use .NET you are married with Microsoft. If you use Java you can be &#8216;promiscuous&#8217; regarding Application Servers or other tools. So you can choose to use JBoss for some projects, and Weblogic for others.
  * Release process is predictable: Microsoft guys promised me version 2.0 of .NET for autumn 2004&#8230; And it is still not here. Sun has been always more regular about new versions and patches. May be an inheritance from the good old days of Solaris.
  * Prepared for high scale deployments: The solutions given by Microsoft about clustering are just a joke compared to the solutions given by the J2EE application server vendors. With Microsoft you have to build all the &#8216;plumbing&#8217; regarding clustering, data synchronization between nodes and failover.
  * Prepared for small scale deployments in client side: JVM can run now smoothly on any computer. And if you run SWT, there is no difference in performance with .NET.

I think Java is far better than .NET in almost all aspects&#8230; except in mobile development. J2ME is nice and small, but now devices are bigger and better. There is a gap between J2ME and J2SE. It seems that Sun has a JVM for ARM devices running Windows Mobile and/or Pocket PC called &#8216;Captain America&#8217; with full support for J2SE. I have suffered the big piece of junk that Compact Framework is, as many others. Will &#8216;Captain America come&#8217; to rescue us?
