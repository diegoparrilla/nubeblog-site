---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2007/01/killer-app-of-fon-will-be-access-to-p2p.html
categories:
- Uncategorized
date: 2007-01-14T22:20:00Z
dsq_thread_id:
- "204894089"
guid: /2007/01/the-killer-app-of-fon-will-be-access-to-p2p-networks/
id: 82
tags:
- embedded
- fon
- fun
- hackers
- hobbist
- linux
- nokia
- upnp
title: The killer app of FON will be access to P2P networks
url: /2007/01/14/the-killer-app-of-fon-will-be-access-to-p2p-networks/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="embedded,fon,fun,hackers,hobbist,linux,nokia,upnp" data-count="vertical" data-url="/2007/01/14/the-killer-app-of-fon-will-be-access-to-p2p-networks/">Tweet</a>
</div>

I have been tracking [FON](http://www.fon.com/) for two years, and I&#8217;m a &#8216;fonero&#8217; since last summer. Recently I read about the [&#8216;FON Liberator&#8217;](http://english.martinvarsavsky.net/general/fon-liberator.html) project, and it seems that finally the mystery of FON is over. If you analyze seriously the business model of this company and you have some basic knowledge about wireless networks, you easily find that something does not match. The original FON business model (and I say original, because now it has changed) was &#8216;share your bandwidth and you will have access to the enormous WiFi network of FON&#8217;. Once the network is deployed, then the company can bill non-Fon users to use the network. Mr. Varsavsky is really a smart guy, isn&#8217;t it?

But this business model has serious technical restrictions:  
1) The coverage of a standard WiFi hotspot is about 100m. So even in metropolitan areas, you need a FON member in every block!  
2) Why people is going to share their network? People does not use WiFi hotspots every where, only really geek people and executives (and they use 3G connection because they can afford it).

FON trusted in WiMax to fix the first technical restriction: coverage. But WiMax is far from being available as the wireless connectivity for the masses, and may be the WiMax assumptions regarding coverage and deployment that I read in documents they published in FON web site about 18 months ago are not going to be implemented before 2009 or 2010.

So they need a short path to continue with the massive deployment of 802.11b/g hotspots: they need to motivate users to share their bandwidth. How?

80% of the Internet traffic in Europe comes from P2P networks. It means that a lot of people have a computer up and running 24 hours a day seven days a week sharing files with &#8216;colleagues&#8217; all around the world. Whether this practice is legal or not it&#8217;s not my business. It means that people have their personal computer stressed running this P2P software (Emule, Bittorrent, Azureus, MLDonkey&#8230;). What IF you have a specific device that can manage your shares in your P2P networks? You just plug in your 500Gb external USB 2.0 disk drive and voila! No more disturbing noise from fans, no more fear of fire, no more broken computers because of abnormal stress! FON will sell this device below <span style="font-weight: bold;">their manufacturing price for 70€</span>. The trade off? You will have to share your bandwidth with the FON community, of course. I guess this solution can be the killer app for the success of FON.

But is this something new? No, not at all. Basically, FON is going to sell a SBC (System Board Computer) router with a WiFi card and enough RAM memory to run a Linux (may be an embedded version of Debian) and some Flash for the OS and bootstrap. 64Megs of RAM and 64Megs Flash should be enough. And there are some commercial devices that have been modified to run something closer to the Fon Liberator. Here goes a list:

  * Linksys [<span class="wikiword">NSLU2</span>](http://www.linksys.com/servlet/Satellite?c=L_Product_C2&childpagename=US%2FLayout&cid=1119460471050&pagename=Linksys%2FCommon%2FVisitorWrapper)
  * the Synology <span class="wikiword"><a class="wikilink" href="http://www.nslu2-linux.org/wiki/DS101/HomePage">DS101</a></span>
  * the Iomega <span class="wikiword"><a class="wikilink" href="http://www.nslu2-linux.org/wiki/NAS100d/HomePage">NAS100d</a></span>
  * the D-Link <span class="wikiword"><a class="wikilink" href="http://www.nslu2-linux.org/wiki/DSMG600/HomePage">DSMG600</a></span>
  * <span class="wikiword">the <a href="http://www.buffalotech.com/products/network-storage/linkstation/">Buffalo Linkstation</a><br /></span>

You can find some cool stuff on how to flash custom built Linux distributions on these devices in <http://www.nslu2-linux.org/> and [http://www.linkstationwiki.net](http://www.linkstationwiki.net/).

In my spare time (if you run a company and you have a one year old baby that&#8217;s really short) I have built my own FON Liberator with the following hardware: 

  * A Soekris [net4521](http://www.soekris.com/net4521.htm) board, purchased to the European distributor.
  * A Gigabyte [GN-WIAG01](http://www.gigabyte.com.tw/Support/Communication/Driver_Model.aspx?ProductID=949), a cheap Atheros miniPCI card.
  * A [Conceptronic CSP480C2](http://www.conceptronic.net/) PCMCIA 2 Ports USB 2.0 card.
  * A Kingtson 512Mb Compact Flash.
  * An external USB 80GB hard disk.

The total cost of this hardware is about 240€ (excluding the hard disk). Obviously, the FON Liberator will be cheaper!

I decided to use the [Voyage Linux](http://www.voyage.hk/) distribution because it&#8217;s perfect for small systems, and it has a version for Soekris boards. It&#8217;s based on Debian Etch, so it&#8217;s very close to the official release. I have added the following software: 

  * [Samba Server and SWAT console](http://www.samba.org/). So I can access my files from computers running windows.
  * [UShare](http://www.google.com/url?sa=t&ct=res&cd=1&url=http%3A%2F%2Fushare.geexbox.org%2F&ei=ZqyqRZGGOaL0nQP5ls36Dw&usg=__w7i8PUCnXBnHM5nxoi7l3xcZzwc=&sig2=LXQavghHVtQHEbH_V6anBg) as a UPnP media server. I can broadcast my media to my home devices.

I have also tried to install [MLDonkey](http://www.google.com/url?sa=t&ct=res&cd=3&url=http%3A%2F%2Fmldonkey.org%2F&ei=R62qRdrnNKGQnQOEqNAB&usg=__QBj5NnSBzLXa1wyB271M2QCl6Js=&sig2=BWEnwuyhmGi0Wutn-3x9YQ), an implementation of the Donkey protocol for Linux and it works. I just installed it for the purpose of study, later on I switched it off. This software is much better than any other P2P software on Linux, because it implements half a dozen P2P networks (bittorrent, overnet, kademlia and others).

I must admit that it works smoothly, but I have two problems:  
1) I had to create a SWAP partition in the external drive to run ushare, samba and mldonkey.  
2) Sometimes, when transferring files at maximum speed the system crashes. I don&#8217;t know what the problem is, but seems to be a problem of the Conceptronic card.

And here goes a photo of the system&#8230;

<a onblur="try {parent.deselectBloggerImageGracefully();} catch(e) {}" href="http://www.diegoparrilla.com/uploaded_images/DSC00722-792104.JPG"><img style="margin: 0px auto 10px; display: block; text-align: center; cursor: pointer;" src="http://www.diegoparrilla.com/uploaded_images/DSC00722-786506.JPG" alt="" border="0" /></a>

And my Nokia 770 running Canola playing content as a UPnP client&#8230;

<span class="vvqbox vvqyoutube" style="width:425px;height:344px;"><span id="vvq-82-youtube-1"><a href="http://www.youtube.com/watch?v=BVDvEQPl6f8"><img src="http://img.youtube.com/vi/BVDvEQPl6f8/0.jpg" alt="YouTube Preview Image" /></a></span></span> 

Once I have fixed the problem with the crash, I will buy a [DLink DSM-320](http://www.dlink.com/products/?pid=318&pageid=redirectLearnDynamicPathPage&pageregion=A1&src=rotw.learn_homeaudio&amp;pcode=rn&opage=rotw.learn_homeaudio),

<a onblur="try {parent.deselectBloggerImageGracefully();} catch(e) {}" href="http://images.dlink.com/products/DSM-320/DSM-320_main.jpg"><img style="margin: 0px auto 10px; display: block; text-align: center; cursor: pointer; width: 320px;" src="http://images.dlink.com/products/DSM-320/DSM-320_main.jpg" alt="" border="0" /></a>  
to play all my media files on my TV screen.

Cool, isn&#8217;t it?
