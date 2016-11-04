---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2007/10/grails-diaries-3-how-grails-will-change.html
categories:
- Uncategorized
date: 2007-10-09T09:43:00Z
dsq_thread_id:
- "204692581"
guid: /2007/10/the-grails-diaries-3-how-grails-will-change-my-project-plan/
id: 32
tags:
- agile
- designs
- grails
- java
- jruby
- rails
- ruby
title: 'The Grails Diaries #3: How Grails will change my project plan'
url: /2007/10/09/the-grails-diaries-3-how-grails-will-change-my-project-plan/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="agile,designs,grails,java,jruby,rails,ruby" data-count="vertical" data-url="/2007/10/09/the-grails-diaries-3-how-grails-will-change-my-project-plan/">Tweet</a>
</div>

[Previous: Setting up the development environment](http://www.diegoparrilla.com/2007/10/grails-diaries-2-setting-up-development.html)

## The strategy

One of the most important reasons why I have chosen Grails and not JRuby/Ruby on Rails is that I&#8217;m lazy and I do not want to throw away all my Java knowledge. But now I&#8217;m wondering if Grails will change too much the way I plan my projects. And what do I mean with &#8216;the way I plan my projects&#8217;? I mean the strategic decisions I usually take when planning my project. OK, and what &#8216;strategic decisions&#8217;? A strategy is a long term plan of action designed to achieve a particular goal. Examples of strategic decisions planning a project sorted by (my) relevance are: 

  1. **What development technology I will use:** A very common mistake when planning a project is the assumption that the development technology does not affect the development processes and workflows. I will show you later how Grails can modify the development workflow compared to Struts.
  2. **How I will assign the resources:** Though I&#8217;m a music man playing all the instruments in this project, in bigger projects you should normally find the following resources playing single roles. I will show you later why with Grails I think some of these roles can be redundant or even irrelevant:

  * Project Manager
  * Software Architect / Technical Lead
  * HTML Designers / Developers
  * Web layer developers
  * Business layer developers
  * Testers

<ol start="3">
  <li>
    <b>What development workflow I will use: </b>Each member of the development team creates small deliverables to be consumed by the next member in the chain. Again, the standard development workflow (analyze-design-implement-test roundtrips) can change.
  </li>
  <li>
    <b>How I will design the solution:</b> Some of the design decisions, blue prints and patterns used in other web frameworks like Struts or others MVC implementations do not apply with Grails and it&#8217;s convention over configuration approach. I will talk about it in future posts in this blog.
  </li>
</ol>

So yes, I think Grails will change how you plan your project. Here goes the details:
  


## The development technology

I have seen some really big projects failing because of this naive assumption: a development technology can work just like another &#8216;similar&#8217; technology. So, even before starting to analyze the project and with my short knowledge of Grails, I can forecast that **Grails will constrain my planning in a way or another**. Due to my lack of knowledge of Grails I cannot budget how much time and resources I will need as a buffer, so I should be conservative and reserve a good development buffer to manage the uncertain.
  


## The resources assignment  


In a classical Web project in Java it&#8217;s very common to have a HTML Designer/Developer that builds the static pages of the site. Then he/she gives the pages to the Java Web developer. He/she converts them to JSP pages and creates the Action and Form Classes (if he/she works with Struts) and implements the logic regarding HTTP Sessions, cookies and all the web stuff. Finally, the business layer developer(s) build(s) the components that interacts with the database or other third party systems and expose(s) the interfaces to the web developers. This horizontal layered distribution of the developers helps the isolation of roles in teams and encourages the use of clear interfaces and pushes the implementation of automatic unit tests specially in the business layer.  
**Grails forces a different approach: The Vertical Slice.** The Vertical Slice developer works in all the layers crossing the boundaries of the systems. It works changing HTML, GSP, Controllers and Domain classes at once. I guess this is one of the reasons of the productivity of Grails and RoR. Removing the public interfaces between layers avoids repeating unnecessary code. I have always liked the Vertical Slice approach because it fits perfectly with UML Use Cases. A Use Case is normally described crossing different layers, just like the Vertical Slice.  
So, **the roles of Web and Business layer developers can merge**. Hence you need developers with a broader range of knowledge (HTML, Javascript, GSP, Groovy and or Java and HQL) and may be more experienced, but if Grails is more productive you can save in headcounts.  
**The Software Architect role is not clear in a Grails project.** Due to the fact that the configuration is almost null and the architecture is so rigid I think that a full-time architect is an unnecessary resource. I would only consider a full-time architect if I need to integrate Grails with external components or existing Java projects (like OpenID in Sprint 2). If you only need to use the database, you don&#8217;t need a full-time architect.
  


## The development workflow

As I have said above, the development of a web interface with the classical approach is: 

  1. A designer creates the look and feel, and then draft the CSS.
  2. The HTML Developer builds the pages and the navigation. Javascript code is also added here.
  3. The Web developer converts the HTML pages to JSP pages, adding the server side code and creating the Action and Form classes
  4. (Optional) The Web developer uses the business logic layer or develops the business logic by herself.

One of the most popular features of Ruby on Rails and Grails is the creation of automatic web controllers for basic CRUD actions, the _scaffolding_. The dynamic generation of code to manipulate classes of the Domain reduce the repetitive tasks of building Create-Retrieve-Update-Delete logic. And this is one of my doubts about the development workflow. **Should I modify the HTML pages and convert them to GSPs and then create the controllers and their CRUD actions manually? Or should I use the automatically created scaffolding first, and then merge the HTML page and the automatically generated GSP?** I can see pros and cons for both, and I will probably take the decision based on the complexity of the User Story to implement. **Help and advice from experience Rails and Grails developers will be welcomed!  
** There is another workflow that can change: **classic Web development takes the bottom-up approach** to build the applications**. Grails encourages the top-down approach** because of its use of Hibernate and Domain classes. With the bottom-up approach, the database entity-relationship model should be implemented before starting with the business logic. With the top-down, the databases ER model arises as result of the Domain classes. This is not a trivial change in the workflow. In classic web development the Data architect tries to build a very stable version of the ER model before starting with the business logic, because the roundtrips &#8216;change ER model, change business logic,change ER model, etc.&#8217; are &#8216;expensive&#8217;. Developing with Grails (and with Hibernate too) the top-down approach and the features of Hibernate synchronizing the changes of the Domain classes with the ER model automatically set the developer free of the manual tracking of the changes and can build very fast the Domain classes.  
There is an exception to the top-down approach with Grails: if you are using a legacy database you cannot take this approach. You must map the database to the domain classes, and probably the naming convention won&#8217;t match, making necessary the use of hbm.xml Hibernate configuration files or annotations.

These are my thoughts about how to plan the development.In my next post I will talk about the analysis and design phases of the project.

[Next: Grails, is it really worth it?](http://www.diegoparrilla.com/2008/02/grails-diaries-4-grails-is-it-really.html)
