---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2007/09/how-to-embed-adsense-ads-inside.html
categories:
- Uncategorized
date: 2007-09-03T13:03:00Z
dsq_thread_id:
- "204692717"
guid: /2007/09/how-to-embed-adsense-ads-inside-a-blogger-com-post/
id: 43
tags:
- blog
- hackers
title: How to embed Adsense ads inside a Blogger.com post
url: /2007/09/03/how-to-embed-adsense-ads-inside-a-blogger-com-post/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="blog,hackers" data-count="vertical" data-url="/2007/09/03/how-to-embed-adsense-ads-inside-a-blogger-com-post/">Tweet</a>
</div>

One of the most annoying things of a Blogger.com blog was how difficult was to add AdSense ads in your blog. Currently this is not an issue anymore because you can add automatically AdSense ads in your page thanks to the Blogger dashboard. But if you read blogs you will realize that some blogs embed Google AdSense ads inside the post. Most tutorials on how to monetize your blog recommends it. But it&#8217;s not possible in Blogger. Why? Because the content of every post is wrapped by a DIV element with the style &#8216;clear:both;&#8217;. And it&#8217;s not possible to modify it in the template, it&#8217;s created by the Blogger.com&#8217;s render engine.  
So here goes the steps I have followed to embed AdSense ads inside a Blogger.com post:

  * Edit your template
  * Find this tag: 
<span style="font-family:courier new;"> 
    
    <div class="post-body">
    </div>
    
    <p>
      </span>, inside you will find this tag <span style="font-family:courier new;"><$BlogItemBody$>.</span></li> 
      
      <li>
        Insert your Google AdSense code wrapped by a floating layer between both tags. You can change to <span style="font-size:85%;"><span style="font-family:courier new;">style=&#8221;float:left&#8221;</span></span> if you want to align at the left hand side:
      </li></ul> 
      
      <p>
        <span style="font-size:85%;"><span style="font-family:courier new;"> 
        
        <div style="float: right;">
          <span style="font-family:courier new;"> </span><br /><span style="font-family:courier new;"></span>
        </div>
        
        <p>
          </span><br /></span> 
          
          <ul>
            <li>
              Now you have to find the DIV tag that contains the id to the 'sidebar'. Normally it's after all the comments stuff. Insert BEFORE this DIV tag the following javascript code:
            </li>
          </ul>
          
          <p>
            <span style="font-size:85%;"><span style="font-family:courier new;"><!-- START: Remove the stupid clear: both; added by blogger render engine --></span>
            
            <br /><span style="font-family:courier new;"></span><br /><span style="font-family:courier new;"><!-- END: Remove the stupid clear: both; added by blogger render engine --></span>
            
            <br /></span><br />And that's all folks. Test it before publishing. I have tested it in FireFox and Internet Explorer in Windows. If you can test it in Safari or Opera, please send me some feedback.
          </p>
          
          <p>
            Comments, improvements and problems will be welcomed!
          </p>
          
          <p>
            <span style="font-weight: bold;">Update 1:</span> A colleague sent me a CSS hack. You can find it <a href="http://www.bloggerforum.com/modules/newbb/viewtopic.php?viewmode=flat&topic_id=6706&forum=2">here</a>.<br /><span style="font-weight: bold;">Update 2: </span>To restrict the effect of the script to the posts avoiding the sidebars and other effects, this version modified of the script only affects the post bodies.
          </p>
          
          <p>
            <span style="font-size:85%;"><span style="font-family:courier new;"></span></span>
          </p>
