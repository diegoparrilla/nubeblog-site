---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2007/09/data-normalization-is-not-for-sissies.html
categories:
- Uncategorized
date: 2007-09-05T08:38:00Z
dsq_thread_id:
- "204692712"
guid: /2007/09/data-normalization-is-not-for-sissies-its-just-common-sense/
id: 40
tags:
- architecture
- databases
- designs
title: Data normalization is not for sissies, it&#8217;s just common sense
url: /2007/09/05/data-normalization-is-not-for-sissies-its-just-common-sense/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="architecture,databases,designs" data-count="vertical" data-url="/2007/09/05/data-normalization-is-not-for-sissies-its-just-common-sense/">Tweet</a>
</div>

And I must be the biggest sissy of all. [There is a lot of buzz](http://www.infoq.com/news/2007/08/denormalization "There is a lot of buzz"){#ddz7} about designing your databases thinking in data normalized or denormalized. Now that everybody is building the next Google or YouTube the database design has to support trillions of transactions per second and millions of terabytes, of course running on a multidimensional computing grid of zillions of nodes of databases written in Erlang&#8230; <ironic/>  
Data normalization is common sense because helps you to avoid the Data Inconsistency Hell when data is repeated across different tables. Only a small fraction of us will have the chance to work in an environment with more than a few thousands concurrent users. And in such an environment the running cost of a standard database architecture is lower than the cost of restricting how your Software Architects must design and your programmers must code the applications. That&#8217;s what is all about, economics. It&#8217;s cheaper to have a fully normalized design with no chance of repeating data across different tables and scale the hardware when you need it. If you are not lucky you will probably will have to denormalize part of your datamodels due to performance reasons. This is very common and does not mean to design your core database model denormalized. You can denormalize the database model and create it in another schema, running some batch process to populate it when the impact on the users is lower. This is a typical solution for reporting tools.  
But, if you are the lucky (or unlucky, who knows&#8230;) enough to work in environments like YouTube or Google with zillions of users then it make sense to use denormalized database models. The reason is again economics: It&#8217;s cheaper to restrict how your Software Architects must design and your programmers must code the applications than scaling a non-standard database architecture (being a non-standard database architecture a massive cluster of database servers keeping data consistent among them). And maybe it&#8217;s not possible to scale databases without strong constraints in the application development.  
I think this is a simple axiom coming from my experience, the more exigent demand of database resources, the more restrictions on the application development. As a server side developer, caching techniques and in-memory smart data hierarchies (Web Sessions or Stateful EJBs) are the first step to improve the performance of an application. Very soon the Architects start to design keeping in mind that someday they will have to include caching or cluster data replication, for example. I know this is not a very Agile approach, but depends on the Architects&#8217; experience to provide a good design thinking in performance or not.  
Finally, design fully normalized and move to a denormalized model only when you need it (this is a Agile approach).
