---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2008/02/grails-diaries-5-do-you-need-software.html
categories:
- Uncategorized
date: 2008-02-20T00:08:00Z
dsq_thread_id:
- "204692523"
guid: /2008/02/the-grails-diaries-5-do-you-need-a-software-architect/
id: 9
tags:
- agile
- architecture
- development
- grails
- rails
title: 'The grails diaries #5: Do you need a software architect?'
url: /2008/02/20/the-grails-diaries-5-do-you-need-a-software-architect/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="agile,architecture,development,grails,rails" data-count="vertical" data-url="/2008/02/20/the-grails-diaries-5-do-you-need-a-software-architect/">Tweet</a>
</div>

[Previous: Grails, is it really worth it?](http://www.diegoparrilla.com/2008/02/grails-diaries-4-grails-is-it-really.html)

I think there is a general misunderstanding of what kind of value can give Grails to a development shop. It seems that there are people out there that believe Grails, RoR and other breeds mean the end of Software Architectures in the web layer. The reasoning is: if the workload to develop a web application is shorter probably it means we need less skilled developers to code our applications.

Wrong.

This is a bizarre way of thinking from my point of view. I have heard of this before. Lowering the workload of development does not mean poorer skills in your development team. The workload is lower because these frameworks follow the Don&#8217;t Repeat Yourself (DRY) principle. This means that all developers (seniors and juniors) can deliver faster because they don&#8217;t have to perform repetitive tasks. That&#8217;s all. But developers still have to face problems, and have to take decisions about their design to fix them. And experienced developers can identify better solutions.

Back to the original question: Do you need a software architect in a project with Grails? Yes, you do. But may be you don&#8217;t need a full time architect. I have identified several scenarios: 

  * Cowboy developer: Grails is a great framework if you are cowboy developer. The framework can enhance your productivity if you are a freelance developer working alone. If you don&#8217;t need to work with colleagues it means you probably don&#8217;t need to integrate with third parties (services, legacy databases, existing code). In this case, the cowboy developer can play the role of the architect, which makes all the sense. But, I&#8217;m not sure if Grails can be successful in this scenario: Ruby on Rails can fit better from my point of view (cheaper hosting, more accepted&#8230;).
  * Development shop: Your customers accept Grails as a valid option (this is a prerequisite, don&#8217;t&#8217; forget to confirm first if they are happy with Groovy on Grails. Running inside a JVM and an application server is not enough!). You have a trained team of Grails developers. You probably have requirements regarding integration with third parties. In this scenario you need an architect (or a senior developer that can take the role) to take decisions about how to do the things and draft a design. Due to the fact that Grails is a very constrained development environment, you can save time of your architects. They will focus on giving the best solution, but they don&#8217;t have to care about small details that Grails takes care of (remember, convention over configuration).
  * IT Departments: Congratulations, you have persuaded your management about the benefits of Grails. You have now a team in your staff of Grails developers plus some contractors. Normally, development teams inside the companies focus on the core business.The projects are evolution of others, there is a lot of service integration and maintenance. So your architect(s) will focus on smooth integrations with existing legacy code and services. In this scenario a strong architect is a must because you need somebody with good skills to design the bridge between your existing legacy systems and your shiny new Grails applications. This architect has to be a Grails believer: otherwise he will lose the faith when the firsts unexpected problems arrive, something common when starting with new frameworks and technologies (do you remember your first experiences with Struts, Maven or Hibernate ?)

An architect can save time with Grails because it&#8217;s a constrained development environment and web developers can be very productive, but forget about saving time in the service layer if you have to integrate with a legacy middleware system, a complex database or web services. The best scenario for the service layer can be compared to a classic development using Spring and Hibernate. Still, I have some doubts about how is the development process and the architecture of a Grails application using a rich middle layer with EJBs and Web Services. I feel like a void under my feet when there is no database and the domain classes are not mapped to this database.
