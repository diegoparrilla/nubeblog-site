---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2007/04/meraki-mesh-networks-can-kill-wimax.html
categories:
- Uncategorized
date: 2007-04-19T00:08:00Z
dsq_thread_id:
- "204894837"
guid: /2007/04/meraki-mesh-networks-can-kill-wimax/
id: 1228
tags:
- architecture
- enterprise
- google
- M2M
- mesh
- mobile
- wimax
title: 'Meraki: Mesh networks can kill Wimax'
url: /2007/04/19/meraki-mesh-networks-can-kill-wimax/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="architecture,enterprise,google,M2M,mesh,mobile,wimax" data-count="vertical" data-url="/2007/04/19/meraki-mesh-networks-can-kill-wimax/">Tweet</a>
</div>

One of the most interesting technologies to come are mesh networks. In [<span class="blsp-spelling-error" id="SPELLING_ERROR_0">Amplia</span>](http://www.amplia.es) we are making some prospects on these technology applied to the M2M (machine to machine) communication. <span class="blsp-spelling-error" id="SPELLING_ERROR_1">Zigbee</span> fits perfectly for small amount of data, but it&#8217;s not good when dealing with mobile communications (<span class="blsp-spelling-error" id="SPELLING_ERROR_2">PDAs</span>, laptops, MP3 players&#8230; anything interactive and portable).  
The only real <span class="blsp-spelling-corrected" id="SPELLING_ERROR_3">ubiquitous</span> networks today are the mobile operators networks. <span class="blsp-spelling-error" id="SPELLING_ERROR_4">GPRS</span> has an acceptable deployment, closer to 100% of the population in developed countries, but 3G technologies are still far from being everywhere. And probably they will never replace the <span class="blsp-spelling-error" id="SPELLING_ERROR_5">GSM</span>/<span class="blsp-spelling-error" id="SPELLING_ERROR_6">GPRS</span> in some areas. 3G networks let the users enjoy of the &#8220;mobile experience&#8221;, providing connectivity anywhere. The problem? The concept of flat fee is out of the scope of the mobile operators, and they charge per use (<span class="blsp-spelling-error" id="SPELLING_ERROR_7">ok</span>, they give flat fee with a traffic cap). This means that mobile operators cannot attract to the mass of users that use the <span class="blsp-spelling-corrected" id="SPELLING_ERROR_8">Internet</span> to share media content, 80% of the <span class="blsp-spelling-corrected" id="SPELLING_ERROR_9">Internet</span> traffic in Spain, for example. They only attract business users.  
A couple of years ago, <span class="blsp-spelling-error" id="SPELLING_ERROR_10">Wimax</span> looked like the perfect technology for mobile operators (or alternative operators) to reach out the average <span class="blsp-spelling-corrected" id="SPELLING_ERROR_11">Internet</span> user. The deployment was cheaper because of the operation range of the stations and the speed of communication was higher than 802.11G. But we are in 2007 and <span class="blsp-spelling-error" id="SPELLING_ERROR_12">Wimax</span> has not exploded. Why? There are several reasons:  
1) it seems that the deployment of the network is not so cheap,  
2) <span class="blsp-spelling-error" id="SPELLING_ERROR_13">Wimax</span> was sold as a replacement of <span class="blsp-spelling-error" id="SPELLING_ERROR_14">Wifi</span>, but actually is a replacement for Cable and <span class="blsp-spelling-error" id="SPELLING_ERROR_15">DSL</span>, very mature technologies.  
3) <span class="blsp-spelling-error" id="SPELLING_ERROR_16">Wimax</span> hardware is not very popular, and it&#8217;s expensive compared to <span class="blsp-spelling-error" id="SPELLING_ERROR_17">DSL</span>+<span class="blsp-spelling-error" id="SPELLING_ERROR_18">Wifi</span> solutions, for example.  
4) The spectrum limits the amount of data guaranteed per users. So, depending the density of the area, the size of the cell can be like the size of standard mobile networks.

So basically if you want to deploy a <span class="blsp-spelling-error" id="SPELLING_ERROR_19">Wimax</span> network in metropolitan areas, you will have to compete with Mobile Operators and Internet Service Providers. The niche where <span class="blsp-spelling-error" id="SPELLING_ERROR_20">Wimax</span> can beat other technologies are: 

  1. non very populated flat areas, here <span class="blsp-spelling-error" id="SPELLING_ERROR_21">Wimax</span> is a winner.
  2. metropolitan areas with flat-fee of traffic data, for mobile users.

I think that cheap mesh networks can really beat <span class="blsp-spelling-error" id="SPELLING_ERROR_22">Wimax</span>, because of the cost of the deployment. We can read [here](http://www.wimaxforum.org/technology/downloads/Deployments_with_Indoor_Terminals_Rev1_2_2_.pdf) how the deployment of a single base station can grow over 120000$. With this base station, 1200 users in a path length below 1km could share a 384<span class="blsp-spelling-error" id="SPELLING_ERROR_23">kbits</span> connection. A path length of more than 1km needs an outdoor terminal to get a good download ratio.  
I read in [<span class="blsp-spelling-corrected" id="SPELLING_ERROR_24">Linux</span> devices](http://www.linuxdevices.com) that [<span class="blsp-spelling-error" id="SPELLING_ERROR_25">Meraki</span>](http://meraki.net/) was selling a [<span class="blsp-spelling-error" id="SPELLING_ERROR_26">Wifi</span> mesh router for less than 50$ (37€)](http://meraki.net/products/mini/). There are also discounts per volume. We have tested mesh networking with <span class="blsp-spelling-error" id="SPELLING_ERROR_27">OpenWRT</span> and it works, the problem was the cost of the devices. The cheapest one was three times the cost of the <span class="blsp-spelling-error" id="SPELLING_ERROR_28">Meraki&#8217;s</span> gadget. If we take the budget of the <span class="blsp-spelling-error" id="SPELLING_ERROR_29">Wimax</span> base station, we can buy 2000 routers, and we still have 20000$ to pay the installation of the devices (10$ per device&#8230; a bit low). If we deploy the network in a grid of 5Km x 4Km, we can cover 20 sq-Km, assuming a distance between nodes of 100meters. That&#8217;s 4-5 times the area covered of by the <span class="blsp-spelling-error" id="SPELLING_ERROR_30">Wimax</span> base station!  
May be I&#8217;m making some <span class="blsp-spelling-error" id="SPELLING_ERROR_31">naïve</span> assumptions, but the point is: <span style="font-weight: bold;">may be </span><span style="font-weight: bold;" class="blsp-spelling-error" id="SPELLING_ERROR_32">Wimax</span> <span style="font-weight: bold;">is dead because Mesh Networks are cheaper to deploy</span>. <span class="blsp-spelling-error" id="SPELLING_ERROR_33">Wimax</span> follows the &#8216;mobile operator&#8217; approach: complex centralized infrastructure. Mesh networks follows the opposite approach: simple distributed infrastructure. In the wired world, <span class="blsp-spelling-error" id="SPELLING_ERROR_34">internet</span> has proven that the distributed approach is the right one. Google is the perfect example of the success based upon the concept of distributed computing. And do you know who is backing up <span class="blsp-spelling-error" id="SPELLING_ERROR_35">Meraki</span>? Google, of course&#8230;  
Mobile operators and <span class="blsp-spelling-error" id="SPELLING_ERROR_36">ISPs</span>, Google is going to take over your business soon!
