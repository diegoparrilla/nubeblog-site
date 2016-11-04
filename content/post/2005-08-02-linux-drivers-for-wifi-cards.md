---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2005/08/linux-drivers-for-wifi-cards.html
categories:
- Uncategorized
date: 2005-08-02T12:24:00Z
dsq_thread_id:
- "204894325"
guid: /2005/08/linux-drivers-for-wifi-cards/
id: 117
title: Linux drivers for Wifi cards?
url: /2005/08/02/linux-drivers-for-wifi-cards/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-count="vertical" data-url="/2005/08/02/linux-drivers-for-wifi-cards/">Tweet</a>
</div>

May be Linux is the most popular OS for server side applications in small environments, but still lacks of popularity in the desktop. As an example, buy a Wifi card and look for its Linux drivers. Surprise! The manufacturer includes drivers for all Windows species, but nothing about Linux.  
Thanks to the Open Source Community, there are some good implementations of drivers for some chipsets: 

  * [MADWIFI](http://madwifi.sourceforge.net/) is a free implementation of drivers for cards using the Atheros chipset. 
  * [rt2x00 Open Source Project](http://rt2x00.serialmonkey.com/) for cards using the Ralink rt2400 and rt2500 chipsets.
  * [Prism54.org](http://www.prism.org/) linux driver for the 802.11g Prism GT / Prism Duette / Prism Indigo Chipsets.
  * [NDIS Wrapper](http://ndiswrapper.sourceforge.net/)It is the last resort. If you cannot find a linux driver for your card, you can try this Windows wrapper of NDIS (Windows network driver API).

If you know some other projects, please let me know.
