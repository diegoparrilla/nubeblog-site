---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2005/07/swt-and-multithreading.html
categories:
- Uncategorized
date: 2005-07-18T23:56:00Z
dsq_thread_id:
- "204894337"
guid: /2005/07/swt-and-multithreading/
id: 123
title: SWT and multithreading
url: /2005/07/18/swt-and-multithreading/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-count="vertical" data-url="/2005/07/18/swt-and-multithreading/">Tweet</a>
</div>

I must admit that I have always hated Swing and AWT. It took me several weeks to (fully?) understand all the events stuff. Regarding the GUI, I was a VB guy, and that means dragging and dropping visual components. In the early days it was slow, very slow. I remember running a Swing application remotely in a HPUX server using a X server like a bad nightmare. So I dropped rich clients in Java and embraced server side development with Servlets and JSPs.

When I saw Eclipse and SWT for the first time, I thought &#8216;this guys have the killer rich client libraries for Java&#8217;. I threw away Netbeans and became an Eclipse believer. And SWT was like my &#8216;pending&#8217; issue in my &#8216;favourites technologies to study&#8217; list. Finally, I had the oportunity to use SWT in pure research project, just for fun. The learning curve for a Java guy with experience in Swing or AWT is almost non-existant&#8230;except for the multithreading.

SWT is not thread safe. Swing guys can say now: &#8216;Ok, Swing is not thread safe either, but who cares&#8217;. If you want to use SWT in a multithreaded environment, you should care&#8230; Because SWT enforces good thread safe code. Otherwise you will get a &#8216;org.eclipse.swt.SWTException: Invalid thread access&#8217;.  
I found this through the hard way. My application has a Table widget, and it is updated based on the events triggered by our network API in the [Opengate](http://www.opengate.es/) platform. When the Opengate event was triggered, I got the SWTException.

Basically, we have to make the SWT thread to manage all the User Interface events. The &#8216;Display&#8217; class has a method called &#8216;asyncExec&#8217; that enqueues a piece of code in the SWT thread events dispatcher. It works as follows:

<span style="font-size:85%;"><span style="font-family: courier new;"> public void refresh() {</span><br /> <span style="font-family: courier new;"> Display display = shell_.getDisplay();</span><br /> <span style="font-family: courier new;"> if (!(display==null || display.isDisposed())) {</span><br /> <span style="font-family: courier new;"> display.asyncExec(new Runnable () {</span><br /> <span style="font-family: courier new;"> public void run() {</span><br /> <span style="font-family: courier new;"> Table t = shell_.getTable();</span><br /> <span style="font-family: courier new;"> t.removeAll();</span><br /> <span style="font-family: courier new;"> Iterator i = table_.values().iterator();</span><br /> <span style="font-family: courier new;"> while (i.hasNext()) {</span><br /> <span style="font-family: courier new;"> String[] rowData = (String[]) i.next();</span><br /> <span style="font-family: courier new;"> (new TableItem(t, SWT.NONE)).setText(rowData);</span><br /> <span style="font-family: courier new;"> }</span><br /> <span style="font-family: courier new;"> }</span><br /> <span style="font-family: courier new;"> });</span><br /> <span style="font-family: courier new;"> }</span><br /> <span style="font-family: courier new;"> }</span></span>

This piece of code refresh the content of a table stored in an instance of HashMap. &#8216;shell\_&#8217; is the reference to the SWT Shell where the table is contained. The method &#8216;getTable&#8217; returns a reference to the table itself. &#8216;table\_&#8217; is the HashMap that contains the values of the table. I have used a HashMap because I need to keep a reference to the row of the table easily. The core functionality is inside the &#8216;asyncExec&#8217; method, which needs an object of the Runnable class. Then the &#8216;run&#8217; method must implement the code that must be thread safe.

SWT is single threaded, so it means that long running processes invoked from the events of the widgets can halt the execution of the application for a long period of time. The &#8216;asyncExec&#8217; method can be used to execute long running processes.
