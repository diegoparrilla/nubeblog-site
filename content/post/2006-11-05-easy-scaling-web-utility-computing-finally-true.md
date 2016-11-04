---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2006/11/easy-scaling-web-utility-computing.html
categories:
- Uncategorized
date: 2006-11-05T14:21:00Z
dsq_thread_id:
- "211116677"
guid: /2006/11/easy-scaling-web-utility-computing-finally-true/
id: 87
title: 'Easy scaling: Web Utility Computing finally true'
url: /2006/11/05/easy-scaling-web-utility-computing-finally-true/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-count="vertical" data-url="/2006/11/05/easy-scaling-web-utility-computing-finally-true/">Tweet</a>
</div>

One of our customers is going to launch a service in Europe and the US. Due to localization issues, he will start in a small (in population) country of Europe and the US. The scaling of the system for the European country is easy because the number of people that could use the system is limited, due to the language of the country. But the scaling of the service for the US is something serious: if the service is successful, my client could die of success if we fail sizing the solution correctly.  
I have made some research on hosting providers of clustered solutions in JAVA in the US, and I found this report from [Netcraft](http://www.netcraft.com) about how <span style="text-decoration: underline;"></span>[Price Competition Emerges in Grid Hosting .](http://news.netcraft.com/archives/2006/10/17/price_competition_emerges_in_grid_hosting.html)  
Honestly it&#8217;s not very clear how these hosting providers set up and run their Grid, except [UtilityServe](http://www.utilityserve.com/) which runs on top of a software called AppLogic built by [3tera](http://www.3tera.com): in the website of UtilityServe you can find a comprehensive price list targeting different client profiles, and in the website of 3tera you can find good technical stuff about the solution, specially a Flash demo quite impressive.  
Apart from easy scaling web applications running Linux, Apache, JBoss, MySQL (my 3-tier architecture), you can add to your network on-demand architecture firewalls, gateways, load balancers, NAS and other software stuff. So you can use it too to run your performance test in an environment almost identical to the production environment just for the time you are going to use it. You can tweak your system adding or removing these pieces! This is really valuable.  
The pricing model sounds to me exotic: you pay per Gigabytes of memory per hour. So, if you contract 4Gigs of memory and you use for ten hours, you will for the fee of 4Gb per hour multiplied by the number of hours in use of your utility system.  
Smart, isn&#8217;t?
