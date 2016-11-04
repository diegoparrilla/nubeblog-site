---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2007/11/ball-and-chain-of-iphone-was-not-java.html
categories:
- Uncategorized
date: 2007-11-12T22:36:00Z
dsq_thread_id:
- "204893915"
guid: /2007/11/the-ball-and-chain-of-iphone-was-not-java-its-google-android/
id: 21
tags:
- architecture
- development
- embedded
- google
- gphone
- iphone
- java
- linux
- mobile
title: 'The ball and chain of iPhone was not Java:  it&#8217;s Google Android'
url: /2007/11/12/the-ball-and-chain-of-iphone-was-not-java-its-google-android/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="architecture,development,embedded,google,gphone,iphone,java,linux,mobile" data-count="vertical" data-url="/2007/11/12/the-ball-and-chain-of-iphone-was-not-java-its-google-android/">Tweet</a>
</div>

Sometimes you only need to wait to understand why things happen. When Steve Jobs said [&#8216;Java is not worth building in. Nobody uses Java anymore. It&#8217;s this big heavyweight ball and chain&#8217;](http://jdj.sys-con.com/read/331264.htm), we were surprised and disappointed because like me a lot of people think that there is still room for Java in the mobile platforms. Of course we have J2ME, but we can do very few things with it. What we need is a full J2SE stack for mobiles. And the iPhone could do it&#8230; if Mr. Jobs wants. But he does not want because Java has become the flag of Google to do developers to follow them. He chose to keep Java out of the iPhone to keep a strict control of the platform, to keep Google out of his business.  
I have just reviewed what [Google Android is, it&#8217;s architecture and the SDK](http://code.google.com/android/what-is-android.html) and I think it&#8217;s much more than a smart mobile platform: it&#8217;s a philosophy. Think of what [SWT](http://en.wikipedia.org/wiki/Standard_Widget_Toolkit) is to the Java User Interfaces and apply it to the Android Architecture. The access to the physical layer has been developed in C/C++ on top the Linux OS, and on top of it there is a pseudo-Java Virtual Machine called **Dalvik virtual machine**. As they say, <span style="font-style: italic;">&#8220;Dalvik has been written so that a device can run multiple VMs efficiently. The Dalvik VM executes files in the Dalvik Executable (.dex) format which is optimized for minimal memory footprint. The VM is register-based, and runs classes compiled by a Java language compiler that have been transformed into the .dex format by the included &#8220;dx&#8221; tool.&#8221;</span>  
J2ME is very similar in the approach, but what looks new is the tight integration with the OS and the use of Java 5 extensions of the language. J2ME is almost JDK 1.0, but if you read the source code of the samples, you can recognize some coding practices of Java 5. I still don&#8217;t know if the Dalvik VM can do reflection or annotations, I will need some time to test it.  
The access to the physical elements of the mobile device are performed thanks to the set of android.* packages. So, it will be a task of the device manufacturer to migrate the C/C++ libraries layer for their devices. I have tried to find some information about how to certificate that the libraries has been migrated correctly. This was one of the key elements for the success of J2ME on the mobile phones, and should be done the same way.  
The Java applications are what they call &#8216;Third party applications&#8217;. It&#8217;s not possible yet to develop or modify the underlying Linux OS and the C/C++ libraries. Again, Java runs in a sandbox -sounds familiar, eh?-.  
I will continue playing with it. Just some random thoughts, will Sun Microsystems get some money for the licensing of Dalvik VM? How much? Will J2ME be replaced by the Dalvik VM?

<span style="font-style: italic;"><span style="font-style: italic;"><span style="font-style: italic;"></span></span></span>
