---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2007/10/grails-diaries-2-setting-up-development.html
categories:
- Uncategorized
date: 2007-10-04T01:00:00Z
dsq_thread_id:
- "204692591"
guid: /2007/10/the-grails-diaries-2-setting-up-the-development-environment/
id: 33
tags:
- agile
- designs
- grails
- java
- jruby
- rails
- ruby
title: 'The Grails Diaries #2: Setting up the development environment'
url: /2007/10/04/the-grails-diaries-2-setting-up-the-development-environment/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="agile,designs,grails,java,jruby,rails,ruby" data-count="vertical" data-url="/2007/10/04/the-grails-diaries-2-setting-up-the-development-environment/">Tweet</a>
</div>

[Previous: JRuby on Rails or Grails?](http://www.diegoparrilla.com/2007/10/grails-diaries-jruby-on-rails-or-grails.html)

Once I have explained why I will use Grails I will go deeper in the development environment.
  


## Methodology: Scrum  


One of the things I would like to test is how Grails works with Agile development methodologies. I&#8217;m not a ScrumMaster but I like Scrum and I would like to go deeper in this methodology. So I will divide the development of the project in two Scrum Sprints: 

  1. Basic functionality of the web site and
  2. Some extra functionality integrating Spring an OpenID java library for authentication.

## Tools

### Mingle

<div id="yvrf" style="padding: 1em 0pt; background-color: rgb(255, 102, 0); text-align: center;">
  <img style="width: 125px; height: 63px;" src="http://docs.google.com/File?id=dcvnhchp_197hk7km6db" />
</div>

Since I cannot guarantee how much of my time I will dedicate to this project every day, the Scrum approach of relative estimations is perfect.  
I have been testing a tool from [Thoughtworks](http://studios.thoughtworks.com/ "Thoughtworks"){#t4ej} called [Mingle](http://studios.thoughtworks.com/mingle-project-intelligence "Mingle"){#tx7-}. This tool is not a supertool, but the interface is very simple and it&#8217;s very configurable. The funny thing about this tool is it has been developed with JRuby on Rails!? The only bad thing about this tool is the slow response of some of the actions. And I guess it&#8217;s not a problem of JRuby ([Charles Nutter commented something about it](http://www.diegoparrilla.com/2007/08/what-is-slow-jruby-or-mingle.html "Charles Nutter commented something about it"){#ooc3} ), but a problem of the application in itself (a problem with the ActiveRecord pattern?). All the user stories and tasks will be created with this tool, and I will publish them in my blog.
  


### JetBrains IDEA 7.0M2

<div id="ware" style="padding: 1em 0pt; text-align: center;">
  <img style="width: 320px; height: 240px;" src="http://docs.google.com/File?id=dcvnhchp_198mv7fpmcz" />
</div>

I was not a [Jetbrains IntelliJDEA](http://www.jetbrains.com/idea/ "Jetbrains IntelliJDEA"){#f2ug} guy, but I have been testing a little bit the tool with Grails and it&#8217;s the right tool for me. Sorry Emacs and Vi talibans, I need auto-complete and a lot of windows in my desktop. I will use a 30 days trial license. If the tool convince me,I will probably change from Eclipse.
  


### EMS SQL Manager

<div id="nifq" style="padding: 1em 0pt; text-align: center;">
  <img style="width: 320px; height: 187.17px;" src="http://docs.google.com/File?id=dcvnhchp_199ghwcr2cb" />
</div>

My favourite [SQL Administration Tool for MySQL](http://www.sqlmanager.net/ "SQL Administration Tool for MySQL"){#kycg}. I can do almost everything from it.
  


### CVS

<div id="rytl" style="padding: 1em 0pt; text-align: center;">
  <div id="gsaz" style="padding: 1em 0pt; text-align: center;">
    <img style="width: 320px; height: 363px;" src="http://docs.google.com/File?id=dcvnhchp_201dfvpn5c5" />
  </div>
</div>

I have a CVS server at home (and who doesn&#8217;t?) running in my little and beautiful [Buffalo Kurobox](http://www.revogear.com/ "Buffalo Kurobox"){#kwvj}.
  


## Books

<div style="text-align: left;">
  I have these books to help me with this task:
</div>

<h3 style="text-align: center;">
</h3>

<div>
  <table style="width: 477px; height: 325px; text-align: left; margin-left: auto; margin-right: auto;" id="xyk3" border="0" cellpadding="3" cellspacing="0">
    <tr>
      <td width="50%">
        <div id="kfeg" style="padding: 1em 0pt; text-align: center;">
          <img style="width: 181px; height: 181px;" src="http://docs.google.com/File?id=dcvnhchp_195gf5mp8gb" />
        </div>
      </td>
      
      <td style="text-align: center;" width="50%">
        <div id="wj47" style="padding: 1em 0pt;">
          <img style="width: 172px; height: 172px;" src="http://docs.google.com/File?id=dcvnhchp_196fjs43smq" />
        </div>
      </td>
    </tr>
  </table>
  
  <p>
    <a title="Groovy in Action" href="http://www.amazon.com/Groovy-Action-Dierk-Koenig/dp/1932394842/ref=pd_bbs_sr_1/105-4834496-6428427?ie=UTF8&s=books&qid=1191272498&sr=8-1" id="emrx">Groovy in Action</a> is probably the best guide to Groovy language. It&#8217;s an excellent book, with lots of examples and I think covers all the things that matters in Groovy. If you are familiar with Java reading this book will make the transition very smooth. If you are not familiar with Java then you will need a Java language book by your side for sure.<br /><a title="Getting Started with Grails" href="http://www.amazon.com/Getting-Started-Grails-Jason-Rudolph/dp/143030782X/ref=pd_bbs_sr_1/105-4834496-6428427?ie=UTF8&s=books&qid=1191272679&sr=1-1" id="c:c-">Getting Started with Grails</a> is like a very big tutorial about how to build Grails applications. My first impression was poor, because the book is very short: 120 pages. I read it a Sunday afternoon. The book is short, but it&#8217;s good. It does not go into the details of Grails because when something deeper and detailed is needed then it refers to the content in the website of Grails. It just focuses in a step by step example of how to build an application. So I think it will help in my tests.</div> 
    
    <h3>
    </h3>
    
    <h2>
      Software Architecture: The basics
    </h2>
    
    <p>
      And the software products I&#8217;m going to use.
    </p>
    
    <div>
      <table id="f-mw" border="1" bordercolor="#000000" cellpadding="3" cellspacing="0">
        <tr>
          <td>
            Operating System
          </td>
          
          <td>
            Windows XP SP2
          </td>
        </tr>
        
        <tr>
          <td>
            JDK
          </td>
          
          <td>
            6 Update 2
          </td>
        </tr>
        
        <tr>
          <td>
            Database
          </td>
          
          <td>
            MySQL Server 5.0 Community Edition
          </td>
        </tr>
        
        <tr>
          <td>
            Development Application Server
          </td>
          
          <td>
            Jetty 6
          </td>
        </tr>
        
        <tr>
          <td>
            Production Application Server
          </td>
          
          <td>
            Tomcat 6.0
          </td>
        </tr>
        
        <tr>
          <td>
            JDBC Driver
          </td>
          
          <td>
            ConnectorJ 5.0.7
          </td>
        </tr>
        
        <tr>
          <td>
            IDE
          </td>
          
          <td>
            IntelliJ IDEA 7.0M2
          </td>
        </tr>
      </table>
    </div>
    
    <p>
      <h2>
        Installing the IDE and the Grails development environment<br />
      </h2>
      
      <p>
        If you are not familiar with IntelliJ like me then you will probably waste a lot of time trying and discovering all the features of the tool. The first thing to do is to download the JetGroovy plugin. Go to &#8216;IDE Settings > Plugins > Available&#8217; and find &#8216;JetGroovy&#8217;. Click on the right button and download and install the plug-in. You will have to restart the IDE. Now we have to download the Groovy 1.0 libraries and Grails 0.5.6. You can install them anywhere, it seems there is not any directory restrictions. Now go to the Groovy/Grails node in IDE Settings and select the existing directories of the tools.<br /><a title="The current version of IntelliJ IDEA 7.0M2 does not support version 0.6" href="http://www.jetbrains.net/jira/browse/GRVY-269" id="khts">The current version of IntelliJ IDEA 7.0M2 does not support version 0.6</a><b>.</b> It seems that the groovy-starter.jar has been re-factored in another jar file and now you cannot run the grails applications. Hopefully it will be fixed in future versions of the IDE.<br /><span style="font-weight: bold;">Update: Read the comments at the bottom to fix this issue. It&#8217;s possible to use 0.6 with IDEA 7.0M2. Thanks Dierk and Graeme.</span>
      </p>
      
      <p>
        Now we have to create a Grails project from the scratch. No problem, go to &#8216;New Project&#8217; > Select &#8216;Create Project from scratch&#8217; > Choose your favourite name and &#8216;Grails Application > Create a source directory and click &#8216;Finish&#8217;. The tool creates all the Grails stuff, just like running the <span style="font-family:Courier New;">create-app</span> command from the command line. Be patient, it can take some time.<br />The setup of the server running the code is easy: go to &#8216;Run > Run/Debug Configurations&#8217; and &#8216;Add a new Configuration&#8217;, &#8216;Grails Application&#8217;. I have named it &#8216;website&#8217;. I have used the default parameters (Run Application, No VM parameters, Make before launch). Click on the &#8216;Run&#8217; button and voila! if you connect to http://localhost:8080/website you<br /> will see the Grails Welcome Page.<br />The environment is ready. In future posts I will show how I&#8217;m going to plan the development of the project.
      </p>
      
      <p>
        <a href="http://www.diegoparrilla.com/2007/10/grails-diaries-3-how-grails-will-change.html">Next: How Grails will change my project plan</a>
      </p>
