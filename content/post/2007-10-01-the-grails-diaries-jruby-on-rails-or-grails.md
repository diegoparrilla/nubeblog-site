---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2007/10/grails-diaries-jruby-on-rails-or-grails.html
categories:
- Uncategorized
date: 2007-10-01T15:27:00Z
dsq_thread_id:
- "204692616"
guid: /2007/10/the-grails-diaries-jruby-on-rails-or-grails/
id: 34
tags:
- agile
- designs
- grails
- java
- jruby
- rails
- ruby
title: 'The Grails Diaries: JRuby on Rails or Grails?'
url: /2007/10/01/the-grails-diaries-jruby-on-rails-or-grails/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="agile,designs,grails,java,jruby,rails,ruby" data-count="vertical" data-url="/2007/10/01/the-grails-diaries-jruby-on-rails-or-grails/">Tweet</a>
</div>

I must admit it: I&#8217;m weak. During last two years I have been trying to avoid the dark attraction of Ruby on Rails. And it was hard. I have been searching for almost seven years something that alleviates my feeling of waste of time when developing a Web user interface. And I have been promiscuous, believe me. I have tried everything in the Java world: Tapestry, Velocity, Cocoon,Altio, GWT, Flex, Laszlo&#8230; I even tried ASP.NET!!! But finally I gave up. It took me a lot of time to realize that <span style="font-weight: bold;">it&#8217;s not about the framework, it&#8217;s about the level of details in the development of Web applications.</p> 

<p>
  </span>So I stopped looking for my Golden Hammer and assumed that Web development is hard. But I still listened the mermaids in the blogosphere claiming for the Holy Grail of Web Development: Ruby on Rails. The approach was different: &#8216;OK, Web development is hard, but may be we can try to avoid the repetitive tasks using a language full of expressiveness -Ruby- and a framework based on conventions and not on configuration. Coming from the Java World this convention over configuration thing was like a heresy, but an attractive heresy.<br />In my daily job -the one I do for living- I just code after 5PM and/or because there is an emergency. But I still enjoy coding and it&#8217;s something I do in my spare time. It&#8217;s like blogging, only if I have time to do it. So I have decided to perform a project to testJRuby on Rails or Grails just for fun. A very simple project, because I still think this frameworks only work for small projects.
</p>

<p>
  But why not pure Ruby on Rails? Here goes my reasons: 
  
  <ul>
    <li>
      I&#8217;m going to do this test just for fun, but I feel it&#8217;s possible to use these frameworks inside the Enterprise. And the only way to convince IT departments to run these frameworks is reusing all their Java infrastructure.<span style="font-weight: bold;"> If it runs on top of a JVM and inside the application server X, then it&#8217;s OK.</span>
    </li>
    <li>
      There are TONS of excellent open source software for Java. And we have already built some nice components running with Spring orEJB containers. It makes a lot of sense to reuse it. So, <span style="font-weight: bold;">Integration of existing components is an added value for Grails and JRoR</span>.
    </li>
  </ul>
  
  <p>
    Now the thing is, should I use JRuby on Rails or Grails? I have decided to use Grails because of the following reasons: 
    
    <ul>
      <li>
        The main reason is laziness: I have a little notion of Groovy, but very few of Ruby.
      </li>
      <li>
        Spring integration. I need to integrate this website with some business logic already developed. Grails have a good Spring integration.
      </li>
      <li>
        ActiveRecord pattern. I don&#8217;t like this pattern. I feel it cannot work in complex models. I prefer the Hibernate approach of Grails.
      </li>
      <li>
        The development IDE. I&#8217;m fed up of Eclipse. I want to try Jetbrains IDEA 7.0 with Grails support.
      </li>
      <li>
        I have the feeling that JRuby is not still mature enough. Charles Nutter is making an incredible job, but Groovy works solid as a rock.
      </li>
    </ul>
    
    <p>
      So, the first step is done: I will go for Grails. The next is step is to define the project scope and the development methodology. So stay tuned!
    </p>
    
    <p>
      <a href="http://www.diegoparrilla.com/2007/10/grails-diaries-2-setting-up-development.html">Next: Setting up the development environment</a>
    </p>
