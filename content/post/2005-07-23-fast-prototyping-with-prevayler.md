---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2005/07/fast-prototyping-with-prevayler.html
categories:
- Uncategorized
date: 2005-07-23T01:29:00Z
dsq_thread_id:
- "219555407"
guid: /2005/07/fast-prototyping-with-prevayler/
id: 1242
title: Fast prototyping  with Prevayler
url: /2005/07/23/fast-prototyping-with-prevayler/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-count="vertical" data-url="/2005/07/23/fast-prototyping-with-prevayler/">Tweet</a>
</div>

When you have to build a prototype to find the approval of the customer, or just explore a possible solution to a problem, you don&#8217;t focus on a good Object Oriented design of the solution, or a detailed relational model (unless what your are trying to validate are these things!). You just focus on the problem you are investigating, or if the prototype has to do with the validation of the look and feel of the application by the customer, a nice User Interface.
  
  
So looking for tools to improve the development of a prototype, I think that [Prevayler](http://www.prevayler.org/wiki.jsp) is the best one if you want to get rid of a database, but you still have to persist (o prevayl, like they say) the information. Prevayler is an advanced Serialization mechanism that simulates transactions and can take &#8216;snapshots&#8217; of the objects model of your application. The information is persisted in files, and the developers claims to be 3000 faster than MySQL and 9000 faster than Oracle! And probably it is true. How? well, it is just serialization of objects&#8230; no SQL, no relationships&#8230; nothing more and nothing else than putting on disk the changes in the objects model.
  
  
In my prototype, I had to show the evolution of some file transfers, navigating in a simple hierarchical object model of three levels. MySQL could work with a very simple model, but you need a MySQL installation and configuration, and we are not testing MySQL, we are testing files transfering with our wireless protocol!
  
  
The learning curve is non-existant, there are plenty of examples, and basically you only need to know how to create the objects to prevayl, and how to manipulate the data contained in these objects. It took me a couple of hours to learn and build the persistence of these objects.
  
  
The development team of Prevayler has created the &#8216;[Prevalent Manifesto](http://www.prevayler.org/wiki.jsp?topic=PrevalentManifesto)&#8216;. They claim that the &#8216;OO community is finally free to recover from the atrophy caused by database and application server restraints&#8230;&#8217;, &#8216;no more DBAs imposing us database restrictions&#8230;&#8217;.
  
  
I don&#8217;t know if the &#8216;samba&#8217; has some strange side effect on these brilliant brazilian developers, but obviously these guys are good programmers but probably they have never faced the sad truth of enterprise development: data rules. When you evolve an existing system, you cannot throw away all the data and start from the scratch, you have to migrate the data to a new model or adapt your application to existings data models.
  
  
A very common mistake of non-experienced developers is not to implement data modification SQL scripts to convert existing data models with real data to the target model of their applications. Then they finish the developemnt and when they are asked about how to use the old data, they say &#8216;Old data? &#8230; well, you know&#8230; errr&#8230; we can write a Java program that loads all the data and then dumps it in the new model!&#8217; Then I start crying as a crocodile&#8230;
