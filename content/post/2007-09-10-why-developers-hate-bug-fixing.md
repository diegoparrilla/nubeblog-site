---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2007/09/why-developers-hate-bug-fixing-probably.html
categories:
- Uncategorized
date: 2007-09-10T12:35:00Z
dsq_thread_id:
- "204692666"
guid: /2007/09/why-developers-hate-bug-fixing/
id: 38
tags:
- agile
- architecture
- enterprise
- management
- qa
title: Why developers hate bug-fixing
url: /2007/09/10/why-developers-hate-bug-fixing/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="agile,architecture,enterprise,management,qa" data-count="vertical" data-url="/2007/09/10/why-developers-hate-bug-fixing/">Tweet</a>
</div>

Probably the only common thing among all developers I have worked with is the hate to bug-fixing. No matter if bugs belong to them or not. As a developer and as a manager I have quite contradictory feelings.

As a developer there was nothing more irritating than the hateful <span class="blsp-spelling-error" id="SPELLING_ERROR_0">Bugzilla</span> emails. When I was working as Technical Lead of a development team in Madrid with a <span class="blsp-spelling-error" id="SPELLING_ERROR_1">QA</span> team in the West Coast of USA they usually started to work at our 18:00 and we usually left at 19:00 (Madrid is GMT+2 summer time). So we counted the number of bugs per hour submitted in <span class="blsp-spelling-error" id="SPELLING_ERROR_2">Bugzilla</span> and extrapolated to their 8 working hours to get the number of new bugs in the system. We left the office betting on the number of new bugs for the next day. We felt the <span class="blsp-spelling-error" id="SPELLING_ERROR_3">QA</span> team was our enemy and the relationship between both teams was difficult. We felt like being in &#8216;Groundhog day&#8217; movie! We were listening constantly how bug-fixing is important for the customer, how new features were delayed because stupid bugs and so on&#8230;

As a manager I knew that bug-fixing was the most irritating part of development for developers, but you cannot avoid it. Bug fixing is a must. I&#8217;m very happy when I found new bugs in our products or projects and I tried to make developers to understand that it&#8217;s great to find bugs before our customers find them -wrong!-. This is true for managers, if you find bugs in advance then the management team does not need to loose the face with the client due to problems with the quality of the product. But it is not true for developers, and I will try to explain why. 

  * Good developers are **creators**. They feel their work as part of them. Most of the programmers are people very motivated because they like what they do. As a creator their work is his/her creation and telling them &#8216;your creation has a defect&#8217; it&#8217;s a bit like saying &#8216;your kid is ugly&#8217;. We react like feeling attacked by the management, the customer or <span class="blsp-spelling-error" id="SPELLING_ERROR_4">QA</span> team.
  * Programmers don&#8217;t work like Managers do. Programmers need to find &#8216;the flow&#8217;. We need time to get the focus on the problem, and &#8216;the flow&#8217; must be durable. Managers work in &#8216;constantly interrupted&#8217; mode. So emails reporting defects every X minutes, phone calls or &#8216;mini-meetings&#8217; really disturb. Developers mentally link bugs to interruptions.
  * Bug-fixing is normally underestimated in the project plans.They normally include the raw time to fix the defects, but not the time taken due to the &#8216;context change&#8217; of the developer: from new feature mode to bug-fixing mode and back to new feature mode. These means that developers link again bug fixing to overtime, because it delays the development of the new features with due date.
  * Programmers hate to hear from Management: &#8216;It&#8217;s great to find bugs before the customer finds them&#8217;. Why? Because we are not stupid. We know it. It&#8217;s great to finds bug before the customer finds them **and report to you**, Bastard Manager. I will have to fix the bug anyway, no matter if the <span class="blsp-spelling-error" id="SPELLING_ERROR_5">QA</span> team or the Customer finds them. I have no tangible gain for fixing the bug before the delivery. But the Evil Manager does, he won&#8217;t have to justify bugs to the customer, he will live better.

The summary is: Developers hate to fix bugs because they feel like being insulted (your kid is ugly), annoyed (emails, phone calls, <span class="blsp-spelling-error" id="SPELLING_ERROR_6">minimeetings</span>), poorly managed (overtime), cheated (finding bugs in advance is great!).

What can we do -as a Manager- to minimize the impact of bug-fixing in your team?: 

  * Developers will feel attacked every time a bug is found. Remove all adjectives when referring to bugs. Example: This is a stupid bug, this is a trivial bug&#8230; Just use the adjectives to categorize them. Use the terms used by your tools.
  * Never ever tell a developer how to fix a bug, except if he/she asks for it. Example: This is just an &#8216;if&#8230;then&#8230;else&#8217;&#8230; &#8216;Use a try&#8230;catch&#8230;&#8217;.
  * Do not allow customers to call or send emails directly to the developers. Customer does not know how to communicate the defects. The defects reported by the customer must be handled by the Managers.
  * Set up your bug-fixing reporting tools to send the bugs once everyday or better, once per iteration. Only categorized and approved bugs must reach the developers. Avoid unnecessary stress.
  * Don&#8217;t forget to size your projects with enough time for bug-fixing.
  * Dedicate one or two days per iteration to &#8216;bug-fixing days&#8217;. Stop the development of new features and get the commitment of the team to work hard that couple of days to &#8216;clean the bug list&#8217;. If the environment of your organization allows it, bring drinks, food and have some beers afterwards. Give the same relevance to the bug-fixing days than delivery days.
  * It&#8217;s great to find bugs before customer finds them, that&#8217;s true. But don&#8217;t use the excuse of the customer anymore, or at least not so often. For programmers customers are irrelevant, they/we are not customer oriented. Change to &#8216;We will find bugs for sure, and every time we find a bug we should congratulate because the <span class="blsp-spelling-error" id="SPELLING_ERROR_7">QA</span> team is doing an excellent job. If we don&#8217;t find bugs then we are not doing good <span class="blsp-spelling-error" id="SPELLING_ERROR_8">QA</span>&#8216;.

What do you think? What do you recommend to help developers to fix bugs?
