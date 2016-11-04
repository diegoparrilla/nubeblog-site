---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2007/08/birthmarking-how-to-detect-and-prove.html
categories:
- Uncategorized
date: 2007-08-26T09:54:00Z
dsq_thread_id:
- "221562150"
guid: /2007/08/birthmarking-how-to-detect-and-prove-gpl-violations-in-java-propietary-code/
id: 52
tags:
- architecture
- hackers
- java
title: 'Birthmarking: How to detect and prove GPL violations in Java propietary code'
url: /2007/08/26/birthmarking-how-to-detect-and-prove-gpl-violations-in-java-propietary-code/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="architecture,hackers,java" data-count="vertical" data-url="/2007/08/26/birthmarking-how-to-detect-and-prove-gpl-violations-in-java-propietary-code/">Tweet</a>
</div>

I have just read the news in Slashdot (Yes, I still read Slashdot) and I found this very interesting [article about a new technique to detect GPL violations in proprietary obfuscated code](http://developers.slashdot.org/article.pl?sid=07/08/25/1648253&from=rss). The technique is called <span style="font-style: italic;">Birthmarking </span>and basically it <span style="font-style: italic;">&#8216;observes short sequences of method calls received by </span><span style="font-style: italic;">individual objects from the Java Platform Standard API, which is part of the Java Runtime Environment. By aggregating sets of short call sequences the otherwise overwhelming volume of trace data becomes manageable.&#8217; </span>

In other words, every piece of java code (and a library is not an exception) moves at bytecode level the information coming and going from the stack following a pattern. So, they identify and classify the patterns of some key objects of a specific GPL piece of code and then they check how the proprietary code uses the stack. If it matches&#8230; gotcha!

But I will tell you something&#8230; <span style="font-weight: bold;">I have seen this concept implemented 15 years ago!!!</span> Not for Java, obviously. Where? At the [Faculty of Computer Science](http://www.fi.upm.es/) of the [Polytechnic University of Madrid](http://www.upm.es/). There was two terms called [Computers Architecture and Computers Fundamentals](http://www.datsi.fi.upm.es/departamento-english.html). We had practices to learn how to code in assembler and microcode. It seems that students copied practices from each other, but students where so smart that they just copied piece of code of other students, or renamed the variables (or labels, it was low level programing). But the core functionality was copied intact. So, the department in charge developed a program called &#8216;El Corrector&#8217;. This program checked the input and outputs of each practice automatically (just like today we do with automatic unit testing) and they checked how the program move data to and from the stack. All the practices were compared each other (the patterns were the other students). If they detected similarities in the behaviour of the applications with the stack, they examined the source code and then visually tried to identify a possible copy.  
A friend of mine was a bit desperate with the practice, so he asked another friend to have a look to his practice <span style="font-style: italic;">&#8216;to get some inspiration&#8217;</span>. He gave him his source code, and he copied parts of it. Both of them were caught by &#8216;El Corrector&#8217;, and both of them had to repeat the term.

So the ideas behind [this paper](http://www.st.cs.uni-sb.de/birthmarking/schuler-ase-2007.pdf) are not so new, but they are applying it for a real world problem.
