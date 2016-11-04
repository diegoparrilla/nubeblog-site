---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2007/09/rise-and-fall-of-dbas-tiranny-of-orm.html
categories:
- Uncategorized
date: 2007-09-14T11:32:00Z
dsq_thread_id:
- "204692657"
guid: /2007/09/rise-and-fall-of-dbas-the-tyranny-of-the-orm/
id: 37
tags:
- architecture
- databases
- enterprise
- fun
- java
title: 'Rise and fall of DBAs: The tyranny of the ORM'
url: /2007/09/14/rise-and-fall-of-dbas-the-tyranny-of-the-orm/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="architecture,databases,enterprise,fun,java" data-count="vertical" data-url="/2007/09/14/rise-and-fall-of-dbas-the-tyranny-of-the-orm/">Tweet</a>
</div>

There was a time when DBAs dictate how developers should use Their databases. It was early and mid-nineties and Their Word was The Truth. Those poor guys building client-server applications had to bow down before Him/Her and implement the Business Logic inside The Database Manager. Database hardware was expensive, but His/Her Highness could size the system easily because the number of clients connected was predictable. And that&#8217;s what the IT Manager wanted; predictable figures.

Late nineties came and Web Application started to rule. Suddenly, the number of clients were unpredictable, the behaviour of the applications was radically different and for the first time in years, the DBMS was the bottleneck and The Master of the Data did not realize on time. So He/She asked to the IT Manager for better and bigger hardware.

<span style="font-style: italic;">IT Manager: Will it fix the performance problems?</span>  
<span style="font-style: italic;">DBA: We don&#8217;t know, it depends on the number of clients on peak, the number of users in the critical path, the TV ads campaigns with the URL of the company&#8230;</span>  
<span style="font-style: italic;">IT Manager: So the bottleneck is the database?</span>  
<span style="font-style: italic;">DBA: Yes, the Web servers are almost idle&#8230;</span>  
<span style="font-style: italic;">IT Manager: Idle? My god! Can they do anything to relief the database?</span>  
<span style="font-style: italic;">DBA: Well, we can try move some business logic out to the application layer. If those lazy and hairy web developers could write good </span>SQL<span style="font-style: italic;">&#8230;</span>

And then a new trend started: move out of the database as much business logic as possible. The web developers started to code the SQL inside the application to relief the database.

The DBAs were upset, because these web developers coded really poor SQL and they don&#8217;t even know about triggers, functions or views that could reduce the size or complexity of some of the statements. And they had to get involved in development almost like a Quality Assurance Team, rejecting poor SQL or aggressive tasks against the RDBMS. That was really disgusting!

By nature Good Developers are lazy. Writing SQL was like a pain in the ass, and wrapping the results in object models took a lot of time. The laziest of them all started to write little applications to create automatically the SQL and the code to return the results as object models. These little tools became in Object-Relational Mapping libraries. The Technical Leads explained to the IT Managers how they could save time using them, and the IT Manager was happy because he could show to the CFO and CEO that they were doing something to make that lazy web developers productive.

Then the nightmare of DBA started.

The DBA realized that the number of queries to the databases were increasing, and the complexity of the query was lower. A lot of simple queries&#8230; What&#8217;s going on here? Sounds like a new intern writing crappy code&#8230;

<span style="font-style: italic;">DBA: Hi, is there a new intern in the team writing crappy SQL?</span>  
<span style="font-style: italic;">Development Lead: No, we don&#8217;t have new people. What is going on?</span>  
<span style="font-style: italic;">DBA: Then somebody of your team is writing really poor code. I can see tons of queries as simple as a line of SQL!</span>  
<span style="font-style: italic;">Development Lead: Ah yes! That&#8217;s the new ORM library we are using!</span>  
<span style="font-style: italic;">DBA: Well, that library is rubbish. It generates tons of shitty SQL. Ask the reseller to give your money back 😉</span>  
<span style="font-style: italic;">Development Lead: No, it&#8217;s opensource and free. And I see a lot of advantages using it. I think we should discuss it with the IT Manager.</span>

<span style="font-style: italic;">IT Manager: Why this tool writes crappy SQL?</span>  
<span style="font-style: italic;">Development Lead: It does not write poor SQL. It creates simple queries, that&#8217;s all. We can configure it to create more complex SQL, but sometimes the number of objects explodes and the application run out of memory.</span>  
<span style="font-style: italic;">DBAs: Why don&#8217;t you use the already created Views? </span>  
<span style="font-style: italic;">Dev Lead: We cannot map Views to objects.</span>  
<span style="font-style: italic;">DBAs: So you are not going to use views anymore? </span>  
<span style="font-style: italic;">Dev Lead: If we can avoid them, yes.</span>  
<span style="font-style: italic;">DBAs: No views!? How am I going to optimize your complex queries?</span>  
<span style="font-style: italic;">Dev Lead: Well, we are not going to write complex SQL anymore. The ORM will do.</span>  
<span style="font-style: italic;">DBAs: And what about triggers and stored procedures? </span>  
<span style="font-style: italic;">Dev Lead: Out. Triggers and ORM does not match very well because it&#8217;s hard to keep under control the changes performed in the DBMS. And Stored Procedures sucks, we have Java.</span>  
<span style="font-style: italic;">IT Manager: So, if there is no views, triggers and stored procedures, the DBAs can set your focus on keeping the system healthy and optimized, but not coding processes. Right?</span>  
<span style="font-style: italic;">DBAs: Errr&#8230; that&#8217;s not exactly right&#8230;</span>  
<span style="font-style: italic;">IT Manager: And we can also transfer all these development tasks to the development team. Right?</span>  
<span style="font-style: italic;">DBAs: Correct, but&#8230;</span>  
<span style="font-style: italic;">IT Manager: And if the DBMS has no heavy processes inside, we can save some bucks in hardware, isn&#8217;t?</span>  
<span style="font-style: italic;">DBAs: Probably yes, but if I don&#8217;t track what is going on in the database system the system can die!</span>  
<span style="font-style: italic;">IT Manager: Of course! And that&#8217;s what you are suppossed to do from now on. Help the development team to optimize how the ORM tools and libraries performs before going live.</span>

Then the DBA role changed and became a slave of the ORM tools.

She could not recommend any more how to code the SQL code because it was an automatic process. And she saw how there was no gain in the performance because of the use of these ORM tools, even worse, she saw how the tuning of the database now was radically different due to the different characteristics of the SQL code. He thought that may be these new problems in the performance could make IT Manager to roll back to the old way, but it never happened. Actually, the IT Manager asked if it was necessary to have that very expensive Enterprise licenses if triggers, views and stored procedures were declining. Moreover, the application developers were implementing some smart caching strategies that really reduce the overhead in the database, saving millions to the company in hardware and licenses.

<span style="font-style: italic;">IT Manager: Should we try an opensource database?</span>  
<span style="font-style: italic;">DBA: <snip>Damn Gaving King&#8230;</snip></span>
