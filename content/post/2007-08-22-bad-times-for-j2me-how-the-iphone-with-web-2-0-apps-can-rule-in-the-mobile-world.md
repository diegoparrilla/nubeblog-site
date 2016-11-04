---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2007/08/bad-times-for-j2me-how-iphone-with-web.html
categories:
- Uncategorized
date: 2007-08-22T12:46:00Z
dsq_thread_id:
- "204771577"
guid: /2007/08/bad-times-for-j2me-how-the-iphone-with-web-2-0-apps-can-rule-in-the-mobile-world/
id: 1225
tags:
- architecture
- designs
- embedded
- enterprise
- iphone
- java
- mobile
title: Bad times for J2ME. How the iPhone with Web 2.0 apps can rule in the mobile
  world
url: /2007/08/22/bad-times-for-j2me-how-the-iphone-with-web-2-0-apps-can-rule-in-the-mobile-world/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="architecture,designs,embedded,enterprise,iphone,java,mobile" data-count="vertical" data-url="/2007/08/22/bad-times-for-j2me-how-the-iphone-with-web-2-0-apps-can-rule-in-the-mobile-world/">Tweet</a>
</div>

The day Steve Jobs said [&#8216;Java’s not worth building in. Nobody uses Java anymore. It’s this big heavyweight ball and chain&#8217;](http://jdj.sys-con.com/read/331264.htm) . Being a Java Zealot as I am, I should find easily a fist full of arguments, but may be he is right.

I have been working in the embedded and mobile world for almost four years in [Amplia](http://www.amplia.es/), and I can tell you that Java is far from being the best option for mobile and embedded development. Even for complex mobile applications I think it&#8217;s not even an option. There is not a decent implementation of the J2SE for ARM microprocessors, on Linux or Windows CE. There are some implementations out there, but believe me, they are far from the quality standards that Java developers expect. Sun Microsystems realized long time ago that building a J2SE for ARM and embedded OS was hard and expensive and they gave up, [abandoning the project](http://forum.java.sun.com/thread.jspa?threadID=408223&start=75).

Of course J2ME it&#8217;s there. But J2ME was designed for devices with a lot of limitations in term of resources. Devices like mobile phones and embedded hardware. But not for PDAs and the new Smartphones with big screens. Try to build an application with a rich UI with J2ME. It&#8217;s a nightmare compared to CF.NET for example. J2ME has been very successful for games and simple apps for mobile phones which can gain access to the hardware layer, but nothing else.

But Steve Jobs was not talking about the heavyweight ball and chain of Java because his big memory footprint, slow start up and all that techie stuffs. <span style="font-weight: bold;">It&#8217;s a ball and chain because means a marriage with Sun Microsystems.</span> Steve Jobs would love to have a J2ME virtual machine for the iPhone&#8230; if it was for free. But it&#8217;s not. All devices running J2ME must pay a fee to Sun, no matter if they use it or not. And that&#8217;s a lot of money. For example, the IBM J9 J2ME implementation for ARM costs $6 per license. Why should Apple pay for it? They have the OS for free -a Symbian license costs between $2.5 and $5-, they have the browser for free -I don&#8217;t know the license costs of Opera-. So probably Apple can save around $15 per device just using their own dog food. So they said:  
1) is it possible to build web applications with HTML and Javascript on Safari? Yes, we just need to allow developers to test easily on Safari. Voila! Safari for Windows!  
2) Can we migrate Flash to the iPhone? Yes, and it is easier to port it than a full J2ME stack. Games, Video Streaming and Rich UI apps can be done in Flash too.  
3) How many applications today need offline behaviour? Not too much, but less than a few years ago with a rise in the trend. And the device have been designed to be &#8216;always on and connected&#8217; to the GSM network and WiFi. The &#8216;offline&#8217; behaviour is not so important.

And they decided not to include Java because gave nothing to the business model behind iPhone.

But Mr. Jobs forgot something:  
1) Mobile devices (and iPhone too) needs to have access to the hardware to control the low level resources like Bluetooth, GPRS modem, SMS messaging, Wifi connection, Serial ports. <span style="font-weight: bold;">A web application cannot access the hardware layer.</span>  
2) May be the offline behaviour is not so important, but [wireless networks are not as reliable as fixed networks](http://www.opengate.es/). Offline behaviour from the browser is not mature at all.

So Mr. Jobs and the iPhone needs a piece of software to complete his Masterplan. They need an Embedded Application Server. What? Are you crazy? An application server? In a device? I will explain myself. When we think of an application server, we imagine a J2EE implementation with a plethora of functionality. But this app server is different. Here goes a list of what I think it should implement:  
&#8211; A small web server to deliver content to the local Safari web browser.  
&#8211; A scripting language to write server side code. Of course this dynamic content should only be served to the local Safari web browser.  
&#8211; Massive Multithreading is not a must (it&#8217;s all local).  
&#8211; A permanent storage in the device for offline operation.  
&#8211; Management of the low level resources of the device.  
&#8211; Some kind of queuing system for asynchronous operations between the device and the remote elements.  
&#8211; A synchronization service between local storage and remote storage.

This embedded application server should implement a scripting language. Why scripting? Because the logic to implement in a device must be simple by definition. The really complex stuff is the management of the hardware layer, and that&#8217;s should be implemented in C/C++ and be very restrictive regarding the access of applications to this layer.

There are already some solutions out there in the embedded world but most of them focus on the Synchronization service when the really hard stuff is to control the hardware layer.
