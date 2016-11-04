---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2006/05/dwr-as-productivity-weapon.html
categories:
- Uncategorized
date: 2006-05-13T13:07:00Z
dsq_thread_id:
- "221509543"
guid: /2006/05/dwr-as-a-productivity-weapon/
id: 98
title: DWR as a productivity weapon
url: /2006/05/13/dwr-as-a-productivity-weapon/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-count="vertical" data-url="/2006/05/13/dwr-as-a-productivity-weapon/">Tweet</a>
</div>

If you don&#8217;t know [DWR](http://getahead.ltd.uk/dwr/)(Direct Web Remoting), you should check this framework right now. They define themselves as the &#8216;easy AJAX&#8217; for Java. And they give easiness in the development, but they also give something not so easy to measure like increase in the productivity of Web developments.  
Our experience with DWR has been more than satisfactory, and I will try to enumerate why I think so:  
1) First of all, it gives Java developers and HTML+Javascript developers TRANSPARENCY when dealing with information coming and going from the server to the browser. They both work with natural assets of each development world: Java POJOs and Javascript Objects. No more marshalling nightmares.  
2) Separation of roles: Java developers build business logic, and expose the business logic to the HTML+JS developers. Just like building a SOA architecture. HTML+JS developers connect to the service layer and build the UI layer, and they don&#8217;t have to care about scriptlets, java tags or JSTL stuff.  
3) Forget about Forms classes or DynaForms (if you are working with Struts, but other MVC can apply). Create Java POJOs and use them. Period.  
4) You don&#8217;t need to rely on MVC frameworks to build web apps. You can follow the MVC pattern, but you don&#8217;t need to care about configuration files, Action classes and other plumbing around these frameworks. You just need a Controller class, accessible from DWR, and a good set of POJOs as Transfer Objects between the browser and the server.  
5) It includes an excellent set of utilities for the repetitive tasks. Once you manage them, they really help.  
6) Documentation: above the average if we compare with other frameworks.

There is also a 2.0 version in progress, with a (not so new) technology called &#8216;Reverse Ajax&#8217;. They claim to execute JavaScript client code from theJava Server Side. It opens a broad range of possibilities for the web 2.0, if you can manage the overhead that this technology puts on top of your infrastructure.
