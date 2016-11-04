---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2008/02/grails-diaries-4-grails-is-it-really.html
categories:
- Uncategorized
date: 2008-02-06T00:07:00Z
dsq_thread_id:
- "204808403"
guid: /2008/02/the-grails-diaries-4-grails-is-it-really-worth-it/
id: 13
tags:
- agile
- designs
- grails
- java
- jruby
- rails
- ruby
title: 'The Grails Diaries #4: Grails, is it really worth it?'
url: /2008/02/06/the-grails-diaries-4-grails-is-it-really-worth-it/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="agile,designs,grails,java,jruby,rails,ruby" data-count="vertical" data-url="/2008/02/06/the-grails-diaries-4-grails-is-it-really-worth-it/">Tweet</a>
</div>

[Previous: How Grails will change my project plan](http://www.diegoparrilla.com/2007/10/grails-diaries-3-how-grails-will-change.html)
  


<h3 style="font-weight: bold;">
  The results
</h3>

I wanted to post my impressions and thoughts about Grails before, but you don&#8217;t know how the events in your life can twist your plans: a delay in the delivery of the HTML designer, a flu followed by a nephritic colic, a laptop dying with all your development environment inside, the wrap up in [Amplía](http://www.amplia.es/), the Christmas holidays and my new start in [The Server Labs](http://www.theserverlabs.com/). All these things made impossible for me to write down my conclusions about Grails applied to a small size project. Well, finally here it is, it&#8217;s not a broad post-mortem analysis, but probably it will help you to take some decisions about this new technology.
  


<h3 style="font-weight: bold;">
  The development environment
</h3>

You can read in my previous post my development environment. I&#8217;m a Eclipse fan, but Eclipse still lacks of a good Grails IDE. So IntelliJ is an excellent option. I used the 30 days trial to develop the Proof of Concept, and I recommend it if you are going to use it for Grails development professionally. Sadly, I will not have the chance to use it in the near future unless in The Server Labs we have the chance to work in a Grails project soon. But if you are one of the lucky ones to work with Grails in an Enterprise environment, go for it. The learning curve of IntelliJ is not flat coming from Eclipse, but it&#8217;s not hard. I think IntelliJ is more developer-oriented than Eclipse, honestly. The integration of Groovy and Grails is excellent, you can create specific artifacts because it acts as a Visual facade to the Grails commands. It took me just a couple of hours to understand the naming conventions, what artifacts were created from the menus and how to setup a Grails project. A tip: don&#8217;t add the suffix of the type of the artifact to create; the commands will add the suffix automatically (convention over configuration, remember this my Java brain&#8230;). I changed the version of Grails several times, from 0.5.6 to 1.0RC3, with no major issue.  
The configuration of a Grails application is simple because it&#8217;s centralized under the <span style="font-family:onload;">/conf</span> directory. I modified the <span style="font-family:Courier New;">Datasource.groovy</span> and <span style="font-family:Courier New;">resources.xml</span> under the <span style="font-family:Courier New;">/spring</span> directory. I kept unmodified <span style="font-family:Courier New;">Bootstrap.groovy</span>, <span style="font-family:Courier New;">Config.groovy</span> and <span style="font-family:Courier New;">UrlMappings.groovy. <span style="font-family:Arial;">Again, convention over configuration shows it pays off.<br />I started my project in debug mode, and then I modified all the artifacts (Java and Groovy classes, static files, Groovy Server Pages, properties files) without restarting the project. The environment detected the change and then reloaded the modified artifact. In some cases it did not relaunch the application, but in some others did. A change in a groovy or a java class under <span style="font-family:Courier New;">/src</span> was followed by a reload of the application. The behaviour is similar to Sysdeo Tomcat, for example.<br /></span></span>
  


<h3 style="font-weight: bold;">
  Groovy for an (experienced?) Java developer
</h3>

I think this is the main concern of all Java developers when starting with Grails: how long will it take to learn Groovy? I cannot say learning Groovy is hard, but it takes time to change your mind to the new syntax, and of course it takes much more time to get full advantage of the features of the language. There are good resources out there to help, but I recommend to buy a book about the language. I started to read Groovy in Action as an ordinary book, but soon I realized it was better to have it by my side while coding as a reference guide.  
First thing you realize is how you end all the lines of your code with a semicolon when it&#8217;s not necessary 🙂 Not a big deal. Groovy can do more things with less lines of code once you use all the stuff the language provides. But it&#8217;s not so easy to use them at the beginning. Your first lines of code with look like Java. As rule of thumb I coded first _a la Java_, and then I refactored the code with the help of the book Groovy in Action. My code was groovier and groovier day after day. Still, I think I did not get full advantage of some features of the language, specially dynamically extending the language and dynamic types. I did not use dynamic types, and my experience with loosely typed languages like Visual Basic made me a supporter of strongly-typed languages.  
The excellent integration of Grails with Spring does not help either. Instead of trying to implement something more complex in Groovy, you implement it in Java and use it just adding the variable to inject the dependency in your Controller or Service classes. Obviously this is an advantage, but you have to disciplined if you want to learn Groovy using Grails and follow the approach &#8216;Groovy first&#8217;.
  


### <span style="font-weight: bold;">Using GORM</span>  


**GORM** (Grails Object Relational Mapping) is the solution to map the Domain model to your database to hold the state of your business and blah, blah, blah&#8230; GORM sometimes made me feel like using a Domain Specific Language. The navigation through the object hierarchy of your domain classes is simpler because you avoid the getters and setters. Code is shorter and more expressive. I used dynamic finders for all the queries, I did not need to use Hibernate criterias -I didn&#8217;t need them-. I don&#8217;t know if I was doing something wrong, but I tried a dynamic finder with more than two parameters and it didn&#8217;t work. I should check now with the new 1.0 final. I used constraints to check the input fields and get better scaffolding. It worked except for the email field (again my fault?).  
My first version of the domain classes tried to reuse an existing database schema. But this database schema followed a naming convention very common in Entity-Relationship modelling, but an absolute nightmare in a Domain model. The properties and class names killed all the expressiveness of GORM as DSL language. In a real-life project, you should probably map the domain model to the ER model with .hbm.xml files -the old Hibernate way, killing the convention over configuration approach- if you cannot modify your database schema, but I decided to change the naming conventions of the ER model to something that GORM could digest with convention over configuration.  
I think this is going to be one of the main problems to implement Grails in Enterprise environments where it&#8217;s mandatory to follow some strict guidelines regarding naming at database level. It will work with the .hbm.xml Hibernate files workaround, but killing the convention over configuration.

**Update:** It seems that Grails 1.0 Final allows the direct mapping in the domain classes.

<h3 style="font-weight: bold;">
  The scaffolding
</h3>

It does not matter if you are going to use CRUD only operations or not, the scaffolding generates the basic skeleton for the typical cases in a web application. It means you will have code ready to use. I followed an agile approach, refactoring the generated code again and again until I got the functionality I wanted. After several iterations, part of the code was removed because it was unnecessary while the rest of the code was improved until it covered my initial specifications.  
I tried to develop something from the scratch, without the scaffolding, but I found myself cutting and copying the code from other parts of the application. Then I decided to generate the CRUD operations with the scaffolding and modify the automatically generated code.

### <span style="font-weight: bold;">Web development basics</span>  


I have used several MVC impleme
  
ntations -basically Struts-, and some Web frameworks like Sitemesh and Tiles. Struts and Tiles configuration is hell: I tried Xdoclet to relief this pain, but I configuration was still and issue. With Grails you don&#8217;t have to configure anything. Only plain convention over configuration. And I can&#8217;t say it took me time to understand how it worked, the learning curve was almost non existent. I had already worked before with Sitemesh, and the concepts behind this framework applies 100% in Grails. I think I really save a lot of time with Grails configuring the layouts of the views.  
GSP are almost identical to JSP. Just change the scriptlets code from Java to Groovy and use the Grails tag libraries. The number of tag libraries is big, but honestly I have just coded with the basic ones: conditionals, loops, access to form values, errors&#8230;). My HTML designer gave me the pages, and I just modified them to insert the dynamic stuff. I did not use any scriptlet, only the tags libraries. The localization of the pages was like in classic web development: modify the messages_*.properties files and use the g:message tab library.  
There is a new scope concept called &#8216;Flash&#8217; scope. With this scope, the information only is available for the current request and the next request. It&#8217;s great to render errors text or warnings.  
By the way, I tried to implement my test application avoiding the usage of HTTP sessions.
  


<h3 style="font-weight: bold;">
  The controllers
</h3>

All the controllers were created in the beginning with the scaffolding, but I refactored them iteration after iteration until I get functionality I wanted. Again convention over configuration for the name of the actions helps you to save precious time (compared to Struts this is really an advantage). Closures are key in Groovy and Controllers. You can feel intimidated with the code generated if you don&#8217;t understand closures and don&#8217;t know very well the Groovy syntax. I needed some time to understand the structure of a Controller and to double check how render, redirect and direct return of model objects worked. Probably this was my hardest time with Grails: fully understand how to extend Controllers and writing good Groovy code.
  


<h3 style="font-weight: bold;">
  Spring to rescue
</h3>

In my test application I wanted to send an email rendering a Velocity template with some basic information (username, password, url, etc&#8230;). I have developed this functionality for several projects in the past with Java, and I have already integrated it with Spring. So I took the Java code and pasted in the project. I updated the resources.xml file of Spring and modified a Controller to reference the bean. The integration of Groovy code and Java code using Spring was perfect. Spring wired the bean automatically, injecting the bean into the Controller. I could recycle my Java code like breeze.

### <span style="font-weight: bold;">Still not very clear&#8230;</span>  


I think there are several things to polish: 

  * If you modify a domain class, the application will enter in an endless loop. Every time I modified a domain class I had to restart my project in debug mode. This was really annoying.
  * I could not force the change of the language adding a parameter in the url, as the documentation said.
  * The application created a session for every single element of the web application -static and dynamic-. It was a reported bug that should have been already fixed.
  * The problem with the session made me wonder if Grails was really ready for production. I tracked down the issue in the Jira of the project and it seems they knew and was scheduled to be fixed in RC4. Still, I think it was a serious bug that impacts directly on the scalability.

### <span style="font-weight: bold;">Conclusions</span>  


I took me about 40 hours of development to implement my test application. I sized the project with the classic Java web stack of Struts+Tiles+XDoclet+Spring+Hibernate in a range of 60-80 hours. So I was quite surprised with the results. I met a Ruby on Rails developer that told me it took him only 25% of the time to develop a simple web application in RoR compared to the classic Java web stack. I think he was exaggerating, but probably he could improve more than 50%. Now that I have more experience with Groovy and Grails I could improve my performance in future Grails projects reducing from 40 to 30 hours. That&#8217;s one third of the work needed for a classic Java web stack. Of course, stand alone development cannot be compared with team development. A developer can build in 800 hours more than a team of four people in 200, because of code integration issues, knowledge transfer, meetings, etc. But you can really feel that Grails improves your performance. A lot.  
Regarding the adoption of Grails in Enterprise environments, I would like to explain why I think it will be adopted broadly instead of Ruby on Rails. But that&#8217;s a new story for a new post more focused on management and architectural topics.

[Next: Do you need a Software Architect?](http://www.diegoparrilla.com/2008/02/grails-diaries-5-do-you-need-software.html)
