---
author: Diego Parrilla
categories:
- cloud
date: 2008-10-17T14:57:24Z
dsq_thread_id:
- "209890953"
guid: /?p=120
id: 120
tags:
- amazon
- ec2
title: Amazon Elastic Compute Cloud (EC2) modifica el comportamiento de las IP elásticas
url: /2008/10/17/amazon-elastic-compute-cloud-ec2-modifica-el-comportamiento-de-las-ip-elasticas/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,ec2" data-count="vertical" data-url="/2008/10/17/amazon-elastic-compute-cloud-ec2-modifica-el-comportamiento-de-las-ip-elasticas/">Tweet</a>
</div>

[<img class="alignright size-full wp-image-121" title="logo_aws" src="/wp-content/uploads/logo_aws.gif" alt="" width="164" height="60" />](/wp-content/uploads/logo_aws.gif)Ayer se anunció en el [foro sobre EC2 de Amazon](http://developer.amazonwebservices.com/connect/forum.jspa?forumID=30&start=0) pequeños [cambios para mejorar el servicio de IPs virtuales](http://developer.amazonwebservices.com/connect/ann.jspa?annID=354) (o elásticas como dicen ellos).

Los cambios introducidos son dos:

  * Un mapeo más rápido de las direcciones IP elásticas. Ahora un cambio podía tardar unos cuantos minutos. No se cuanto se tardará ahora, pero lo probaremos.
  * Las conexiones existentes cuando se realiza un remapeo son eliminadas de manera inmediata. Ya no hay que esperar a que el stack de red se de cuenta de que ya no existe conexión con el extremo. Hasta ahora lo que ocurría es que las conexiones abiertas se quedaban así durante un rato. 

Estos cambios afectan a su infraestructura, pero no afectan al código de nuestras aplicaciones. Bueno, yo creo que puede tener un efecto positivo ya que no tienes que preocuparte de implementar algoritmos de &#8216;[KeepAlive](http://en.wikipedia.org/wiki/Keepalive)&#8216; entre tus sistemas en la nube.
