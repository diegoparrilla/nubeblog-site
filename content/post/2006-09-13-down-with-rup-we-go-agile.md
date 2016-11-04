---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2006/09/down-with-rup-we-go-agile.html
categories:
- Uncategorized
date: 2006-09-13T00:04:00Z
dsq_thread_id:
- "210016982"
guid: /2006/09/down-with-rup-we-go-agile/
id: 91
title: 'Down with RUP: We go agile'
url: /2006/09/13/down-with-rup-we-go-agile/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-count="vertical" data-url="/2006/09/13/down-with-rup-we-go-agile/">Tweet</a>
</div>

In late &#8217;90s we realized that the waterfall was an awful methodology for that time: lifecycle of the products were shorter and there are was something terribly wrong with the waterfall approach: it did not leave any margin for the intrinsic uncertainty of the projects.

So UML came to unify the OO modeling, and the (Rational) Unified Process looked like the correct approach to fix the structural problems of the waterfall and use OO modeling with UML.

Honestly, I have tried to use the RUP for years, and I think is a good methodology for giant-size projects, but it does not work with small projects (about <100000 LOCs). Why? Well, my experience with the RUP is:  
* Too strict about the 4 phases: Inception, Elaboration, Construction, Transition. They are all just sets of iterations. It does not make sense to use them most of the times.  
* Too UML centric: UML is a tool, any other language to transmit knowledge between members of the team is valid if it works.  
* Use Cases are naive: I have been working with Use Cases for 6 years now, and honestly I don&#8217;t know how to use them. Why don&#8217;t use just plain text with some charts?  
* Difficult to manage: It&#8217;s really hard to keep all the workflows in a project going, so naturally many often the project derives to a linked list of waterfall project plans.  
* It&#8217;s hard to keep updated the designs: I know some tools helps with this taks, but sometimes it&#8217;s not so important to have the designs updated, and it takes so long&#8230;  
* What about modeling non-OO artifacts? It seems that Database Relational models does not fit into UML, but all the projects I have worked used a E-R database. So you need to give some space to non-natural artifacts like E-R charts. 

We have been trying Agile practices for some years, and they are really effective. Basically, I think Agile methodologies are naked RUP (iterative-incremental, focused on the architecture) plus some good ideas thanks to the evolution of software tools (automatic builds that makes early deliveries easy, test-driven development&#8230;). Some concepts are really hard to implement (pair programming), but the essencee behind them is valid. 

Now we are in the process of implementing estimation and scoping of projects using Agile methodologies, and it means:  
* No more tasks: we talk User Stories  
* No more fixed delivery dates: we will give estimated dates based on development speed, not on early estimations.  
* Developers participate on the estimation of the efforts.  
* Feature-Driven or Delivery-Date-Driven approaches, but not both at the same time and level of priority. 

I really recommend Mike Cohn&#8217;s book [Agile Estimating and Planning](http://www.mountaingoatsoftware.com/books.php) . It&#8217;s helping us a lot to estimate and plan projects in a different way. And hopefully it will help us to manage the uncertainty of the software development.
