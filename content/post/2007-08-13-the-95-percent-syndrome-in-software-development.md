---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2007/08/being-project-manager-architect-analyst.html
categories:
- Uncategorized
date: 2007-08-13T14:17:00Z
dsq_thread_id:
- "204893987"
guid: /2007/08/the-95-percent-syndrome-in-software-development/
id: 61
tags:
- architecture
- designs
- enterprise
- java
- management
title: The 95 percent syndrome in Software Development
url: /2007/08/13/the-95-percent-syndrome-in-software-development/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="architecture,designs,enterprise,java,management" data-count="vertical" data-url="/2007/08/13/the-95-percent-syndrome-in-software-development/">Tweet</a>
</div>

Being a Project Manager, Architect, Analyst, Developer or anybody involved in the development of software, you have probably suffered the <span style="font-weight: bold;">95 percent syndrome.<br /></span>Imagine a software development project where things are going reasonably well: things are on schedule, Quality Assurance says things delivered are OK, the customer feel the progress, people are happy because they don&#8217;t have to work overtime and they architect and developers can apply the Best Practises. You are very close to the end of the development cycle (if you are working with an iterative and incremental methodology) and confident about the result. It&#8217;s time to review the overall status of the project, and then you check with the development team what is done and what is pending.  
Project Manager: &#8216;Requirement X is implemented&#8217;  
Architect: &#8216;Yes, it has been developed&#8217;  
Quality Assurance: &#8216;We have tested it and it has some bugs&#8217;  
PM: &#8216;How many bugs?&#8217;  
QA: &#8216;About 50&#8217;.  
PM: &#8217;50???&#8217;  
Architect: &#8216;Yes, but they are trivial.&#8217;  
PM: &#8216;OK, great. I need an estimation for these bugs&#8217;.  
Architect: &#8216;OK. We have first to finish the pending tasks.&#8217;

And iterating over each requirement, we find out that most of the requirements are not fully implemented. Your feelings of confidence on the schedule are starting to fade away&#8230;  
PM: &#8216;What about the status of the Integration Environment?&#8217;  
Architect: &#8216;Well, we are having some trouble putting together all the stuff developed by the team&#8217;.  
PM: &#8216;What can of problems?&#8217;  
Architect: &#8216;Stupid things like different naming conventions in the URLs and connection strings, corrupt data in the database, etc&#8230;&#8217;  
PM: &#8216;Who is in charge of fixing this things?&#8217;  
&#8230;<silence>&#8230;  
PM: &#8216;I know, everybody is busy finishing their tasks&#8230; But somebody must work in the Integration environment&#8217;.  
Architect: &#8216;I can do it&#8230;&#8217;  
PM: &#8216;No, I need you to work with the developers to fix the bugs.&#8217;  
Architect: &#8216;Me fixing bugs?&#8217;  
PM: &#8216;Yes, what&#8217;s wrong?&#8217;  
Architect: &#8216;Nothing&#8230; I will work in the bugs&#8217;.  
PM: &#8216;I know nobody wants to fix bugs. OK. Can developer X work on the Integration stuff?  
Architect: &#8216;He has pending tasks&#8217;.  
PM: &#8216;I know&#8230; We can assign his pending tasks to developer Y.&#8217;  
Architect: &#8216;But the context change can kill his productivity. Can we contract another developer?&#8217;  
PM: &#8216;No, budget is very tight and the a contractor will need to be in context anyway?&#8217;.

So now your feelings of confidence have fully faded away. Now it&#8217;s time to calculate the delays and reschedule the project. Things are not going so well, so you decided to meet more often to track the status of the project. After a couple of Status Meetings, you realise that the bugs are being fixed, but new bugs arise. The integration environment does not work properly yet, and now the Business Analysts come with requirement changes from the client. Meanwhile, the client is getting nervous because he cannot see the progress like he saw in the beginning of the project. Developers are now working overtime to fix bugs and complete pending tasks and some of them are starting to complain about your poor management skills in the coffee breaks.

So what have happened here? 

<ol type="a">
  <li>
    May be things were not going so well and you did not realise of it.
  </li>
  <li>
    May be these problems are part of software development and you cannot avoid it.
  </li>
</ol>

I think this is part of the Software Development Game. The <span style="font-weight: bold;">95 percent syndrome</span> comes as result of our education as Software Engineers. At the university they told us that everything has a solution, that there is only a way to build software. Wrong. They did not tell us that the biggest problem of software development is <span style="font-weight: bold;">uncertain</span>. Software Engineering has a very big problem as a Science: It has been created by Mathematicians and not by Engineers. For a Mathematician, uncertain is Hell. So they avoided uncertainty. I still can remember how Software Development was seen as a mathematical function,

<div style="text-align: center; font-weight: bold;">
  Y = F(x)
</div>

Where x where the requirements, and Y was the software build. Terrible mistake. The waterfall model was defeated and iterative-incremental models came. And things were better. Now we had the following polynomial representation of software development.

<div style="text-align: center; font-weight: bold;">
  P(x) = a<span style="font-size:78%;">n</span>x<span style="font-size:78%;">n</span>+a<span style="font-size:78%;">n</span>x<span style="font-size:78%;">n-1</span>+&#8230;+a<span style="font-size:78%;">3</span>x<span style="font-size:78%;">3</span>+a<span style="font-size:78%;">2</span>x<span style="font-size:78%;">2</span>+a<span style="font-size:78%;">1</span>x<span style="font-size:78%;">1</span>+a<span style="font-size:78%;"></span>
</div>

Where each monomial can be an iteration. <span style="font-weight: bold;">The good thing of this approach is that it assumes is not possible to build software as an image of the requirements, but it&#8217;s possible to build software that can get closer and closer to the requirements. </span>Why? let&#8217;s put both formula together:<span style="font-weight: bold;"></p> 

<p>
  </span> 
  
  <div style="text-align: center;">
    <span style="font-weight: bold;">Y = F(x) = P(x) = a</span><span style="font-weight: bold;font-size:78%;">n</span><span style="font-weight: bold;">x</span><span style="font-weight: bold;font-size:78%;">n</span><span style="font-weight: bold;">+a</span><span style="font-weight: bold;font-size:78%;">n</span><span style="font-weight: bold;">x</span><span style="font-weight: bold;font-size:78%;">n-1</span><span style="font-weight: bold;">+&#8230;+a</span><span style="font-weight: bold;font-size:78%;">3</span><span style="font-weight: bold;">x</span><span style="font-weight: bold;font-size:78%;">3</span><span style="font-weight: bold;">+a</span><span style="font-weight: bold;font-size:78%;">2</span><span style="font-weight: bold;">x</span><span style="font-weight: bold;font-size:78%;">2</span><span style="font-weight: bold;">+a</span><span style="font-weight: bold;font-size:78%;">1</span><span style="font-weight: bold;">x</span><span style="font-weight: bold;font-size:78%;">1</span><span style="font-weight: bold;">+a</span><span style="font-weight: bold;font-size:78%;"></span>
  </div>
  
  <p>
    <span style="font-weight: bold;"><b><br />The only way to get P(x) = F(x) is when n is infinite. This means that we need infinite iterations to build Software that covers 100% the requirements.</p> 
    
    <p>
      </b></span>Going back with the mere mortals, it&#8217;s not strange to have a beautifully crafted Project Plan and a Gantt chart with a workload assigned for each tasks. We can create easily a chart like this:
    </p>
    
    <div style="padding: 1em 0pt; text-align: center;">
      <img style="width: 354px; height: 255px;" src="http://docs.google.com/File?id=dcvnhchp_66zprq8bd9" />
    </div>
    
    <p>
      <img src="http://www.blogger.com/post-edit.g?blogID=11583932&postID=3490945643825334407" alt="" /><br />The Project Manager thinks that the tangent of the function can vary, and with the changes he can control the delays from the schedule, and recalculate the schedule. But he is wrong. <span style="font-weight: bold;">He is wrong because he is assuming a function like the one above, a function that assumes that the workload to build a requirement is the same at the beginning of the project and at the end.</p> 
      
      <p>
        </span>The truth is that the function that describes the progress of a development is like this:<br /><span style="font-weight: bold;"><br /></span> 
        
        <div style="padding: 1em 0pt; text-align: center;">
          <img style="width: 336px; height: 241px;" src="http://docs.google.com/File?id=dcvnhchp_67g8qwpchn" />
        </div>
        
        <p>
          And this chart says a lot of things:
        </p>
        
        <ol>
          <li>
            The workload to build a requirement is dependant of when is being developed. There are a lot of factors (integratio<br /> n tasks, QA team performance, requirement changes&#8230;).
          </li>
          <li>
            Requirements being developed at the end of the cycle are more &#8220;expensive&#8221; than requirements at the beginning. The requirement can be simple in itself, but now it&#8217;s part of a very complex situation.
          </li>
          <li>
            It&#8217;s almost unavoidable to leave requirements out of the iteration. If you want to keep the schedule, you will have to move requirements to the next iteration.
          </li>
          <li>
            And 5% of the project can cost like 95% of the project. <span style="font-weight: bold;">This is the 95 percent syndrome.</span>
          </li>
        </ol>
        
        <p>
          What can we do to manage the 95 percent syndrome? I&#8217;m afraid this is part of the Software Development game and we can&#8217;t avoid it. So we will have to live with it. How? My personal recipes:
        </p>
        
        <ol>
          <li>
            Ask the client to classify the requirements by priority before starting the iteration.
          </li>
          <li>
            Ask the architect to classify the requirements by complexity before starting the iteration.
          </li>
          <li>
            Build highest priority and complexity first.
          </li>
          <li>
            Schedule several &#8216;bug fixing days&#8217; in between the iteration. Stop the development progress and work on the bugs these days.
          </li>
          <li>
            Keep in mind that Integration tasks depends directly on the amount of elements to integrate and it&#8217;s not a linear function. Probably it can a be logarithmic.
          </li>
          <li>
            Keep a buffer in the Project Plan, and do not say a word to anybody.
          </li>
          <li>
            Do not accept changes in the current iteration. If you don&#8217;t have any choice, then reschedule the project as if you were punishing the client.
          </li>
          <li>
            Explain to the client on every meeting that most of the times some requirements are moved to the next iteration. Since most important requirements are built first in the iteration, only low priority requirements are moved.
          </li>
          <li>
            Do not reschedule the iteration eternally. Try to close it, even with less of the 95% of the requirements.
          </li>
        </ol>
        
        <p>
          These are my thoughts about this special syndrome, but I would like to hear from you. Please post your tips and recipes.</silence>
        </p>
