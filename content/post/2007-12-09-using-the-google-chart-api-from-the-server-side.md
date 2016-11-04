---
author: Diego Parrilla
blogger_author:
- Diego Parrilla
blogger_blog:
- www.diegoparrilla.com
blogger_permalink:
- /2007/12/using-google-chart-api-from-server-side.html
categories:
- Uncategorized
date: 2007-12-09T01:30:00Z
dsq_thread_id:
- "204893855"
guid: /2007/12/using-the-google-chart-api-from-the-server-side/
id: 19
tags:
- api
- chart
- development
- google
title: Using the Google Chart API from the server side
url: /2007/12/09/using-the-google-chart-api-from-the-server-side/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="api,chart,development,google" data-count="vertical" data-url="/2007/12/09/using-the-google-chart-api-from-the-server-side/">Tweet</a>
</div>

<div xmlns="http://www.w3.org/1999/xhtml">
  The new <a href="http://code.google.com/apis/chart">Google Chart API</a> says<br /> 
  
  <blockquote>
    <span style="font-style: italic;">You can include a Chart API image in a webpage by embedding a URL within an <img /> tag. When the webpage is displayed in a browser the Chart API renders the image within the page.</span> </p>
  </blockquote>
  
  <p>
    There are some references about how to encode the information in the URLs in javascript. And I was wondering: Can I use it from the server side in my Java applications? Is it difficult? JFreeChart is a good API Chart but it consumes a lot of resources, can I save money in hosting servers delegating the rendering of my charts to Google?
  </p>
  
  <p>
    So I wrote this little example about how to use the Google Chart API in Java with the <a href="http://jakarta.apache.org/httpcomponents/httpclient-3.x/">Apache Jakarta Commons HTTP Client</a>. It is very easy, and I wrote a little helper class to avoid the crazy encoding implemented by Google. You can <a href="http://www.diegoparrilla.com/docs/GChartAPITest.java">download the source code of the class here</a>. Remember to include these libraries: 
    
    <ul>
      <li>
        commons-logging.jar
      </li>
      <li>
        commons-httpclient-3.1.jar
      </li>
      <li>
        commons-codec-1.3.jar
      </li>
    </ul>
    
    <p>
      The piece of code to perform the HTTP request is about 20 lines. You need to pass as an argument the parameters at the right hand side of this url<br /> 
      
      <blockquote style="font-family: courier new;">
        http://chart.apis.google.com/chart?</p>
      </blockquote>
      
      <p>
        It returns an array of bytes with the image in PNG format. You only need to push it into the output stream of a servlet, or save it in a file like I do. Ok. here goes the snippet:
      </p>
      
      <p>
        <span style="font-family:courier new;"></span><span style="font-family:courier new;"></span><br /> 
        
        <blockquote>
          <span style="font-family:courier new;"> private String url_ = &#8220;http://chart.apis.google.com/chart?&#8221;;</span><br /><span style="font-family:courier new;"> private int timeout_ = 30000; // milliseconds</span></p> 
          
          <p>
            <span style="font-family:courier new;"> public byte[] create(String postUrl) {</span>
          </p>
          
          <p>
            <span style="font-family:courier new;"> HttpClient client = new HttpClient();</span><br /><span style="font-family:courier new;"> client.setConnectionTimeout(timeout_);</span>
          </p>
          
          <p>
            <span style="font-family:courier new;"> String url = url_ + postUrl;</span><br /><span style="font-family:courier new;"></span><span style="font-family:courier new;"> HttpMethod method = null;</span>
          </p>
          
          <p>
            <span style="font-family:courier new;"> method = new GetMethod(url);</span><br /><span style="font-family:courier new;"> method.setRequestHeader(&#8220;accept&#8221;, &#8220;image/png&#8221;);</span><br /><span style="font-family:courier new;"> byte[] image = null;</span><br /><span style="font-family:courier new;"> try {</span><br /><span style="font-family:courier new;"> client.executeMethod(method);</span><br /><span style="font-family:courier new;"> image = method.getResponseBody();</span><br /><span style="font-family:courier new;"> } catch (Exception e) {</span><br /><span style="font-family:courier new;"> e.printStackTrace();</span><br /><span style="font-family:courier new;"> } finally {</span><br /><span style="font-family:courier new;"> method.releaseConnection();</span><br /><span style="font-family:courier new;"> return image;</span><br /><span style="font-family:courier new;"> }</span><br /><span style="font-family:courier new;"> }</span><br /> 
            
            <blockquote>
            </blockquote>
            
            <p>
            </p></blockquote> 
            
            <p>
              The rest of the class includes some helper methods that wraps the crazy encoding made by Google. The reason for this crazy encoding is to avoid the use of POST parameters normally harder to use in the client side. I have coded the class quick and dirt, so if you think it&#8217;s possible to do it better you are probably right!
            </p>
            
            <p>
              I have performed some tests and the latency of the service is excellent: it never took more 2.5 seconds to render a chart, taking from 300ms to 800ms on average. Normally the network latency of Google is very low (less than 100ms), so the time it takes to render a chart is excellent considering this is a very CPU time consuming activity. As a rule of thumb you should cache the requests made to the Google Servers to avoid requesting twice the same chart. You will respect the Terms of the Service (50000 request per day and user, remember!) and your users will be happy because they will get the charts without any delay.
            </p>
            
            <p>
              Finally, I think it&#8217;s worth to use this API instead of JFreeChart if you need to render a lot of charts with a very high granularity that impacts in the performance of your servers.
            </p>
            
            <p>
              </div>
