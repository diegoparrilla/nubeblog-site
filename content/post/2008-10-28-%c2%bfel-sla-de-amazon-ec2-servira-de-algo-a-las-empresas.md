---
author: Diego Parrilla
categories:
- cloud
date: 2008-10-28T09:00:34Z
dsq_thread_id:
- "204894510"
guid: /?p=182
id: 182
tags:
- amazon
- ec2
- sla
title: ¿El SLA de Amazon EC2 servirá de algo a las empresas?
url: /2008/10/28/%c2%bfel-sla-de-amazon-ec2-servira-de-algo-a-las-empresas/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,ec2,sla" data-count="vertical" data-url="/2008/10/28/%c2%bfel-sla-de-amazon-ec2-servira-de-algo-a-las-empresas/">Tweet</a>
</div>

[<img class="aligncenter size-full wp-image-121" title="logo_aws" src="/wp-content/uploads/logo_aws.gif" alt="" width="164" height="60" />](/wp-content/uploads/logo_aws.gif)

> <p style="text-align: center;">
>   You can&#8217;t control what you can&#8217;t measure
> </p>
> 
> <p style="text-align: right;">
>   Tom DeMarco
> </p>

<p style="text-align: center;">
  <p>
    Cuando el otro día leí el anuncio del <a href="http://aws.amazon.com/about-aws/whats-new/2008/10/23/amazon-ec2-exits-beta-and-now-offers-a-service-level-agreement/">paso de Beta a Producción de Amazon EC2</a> me pareció una noticia interesante ya que con ello se anuncia <a href="http://aws.amazon.com/ec2-sla/">la existencia de un SLA asociado al servicio</a>. Pero cuando leí el SLA&#8230; me pareció decepcionante.
  </p>
  
  <p>
    Para mi desgracia he tenido que lidiar con unos cuantos Acuerdos de Nivel de Servicio. Tanto en el lado del cliente como el del proveedor, y puedo asegurar que pueden ser documentos infernales, donde se computan docenas de métricas para garantizar el nivel de servicio contratado u ofrecido. ¿Y cuantas metricas tiene el SLA de Amazon EC2?
  </p>
  
  <p>
    ¡Una! Annual Uptime Percentage o Porcentage de Disponibilidad Anual. Es decir, la única métrica válida es si nuestras instancias se encuentran en estado &#8216;Región No disponible&#8217;. ¿Y cual es el umbral de tiempo definido? Pues un 99.95% anual, 4.38 horas exactamente en un año. No está mal.
  </p>
  
  <p>
    Pero la mayoría de las veces no nos sirve una métrica que nos diga si funciona o no funciona. Necesitamos otro tipo de métricas que nos indiquen:
  </p>
  
  <ul>
    <li>
      Tendencias: ¿se está degradando el servicio?
    </li>
    <li>
      Quality of Services (QoS): ¿La calidad que nos ofrecen está por debajo de los umbrales establecidos?
    </li>
    <li>
      Metricas derivadas: Estadísticas acumuladas y correladas entre sí.
    </li>
  </ul>
  
  <p>
    Estas métricas (y otras muchas) son las que piden los clientes empresariales, ya que tienen herramientas que permiten gestionar esto en sus sistemas. Todos las grandes empresas tienen sus <a href="http://www-01.ibm.com/software/es/tivoli/index.html?&S_TACT=none&S_CMP=none?">Tivoli</a>, <a href="http://www.bmc.com/products/products_services_detail/0,,0_0_0_2001,00.html">Patrol</a>, <a href="http://en.wikipedia.org/wiki/OpenView_Operations">Openview</a> para controlar el nivel de servicio de sus sistemas.
  </p>
  
  <p>
    Hace unos meses un director de Amazon AWS me preguntaba que le faltaba en mi opinión a Amazon Web Services para que fuere &#8216;Enterprise-class&#8217;. Le dije tres cosas:
  </p>
  
  <ul>
    <li>
      Un SLA
    </li>
    <li>
      Una red de integradores
    </li>
    <li>
      Una red de formación en sus tecnologías
    </li>
  </ul>
  
  <p>
    Creo que el SLA de Amazon no va a cubrir las expectativas mínimas para aplicaciones empresariales. Y me temo que cuando haga presentaciones de Amazon EC2 y sus bondades a potenciales clientes, ante la pregunta de cómo monitorizar el nivel de servicio, tendré todavía pocos argumentos para justificar La Nube como un entorno para el software empresarial.
  </p>
  
  <p>
    Pero bueno, por lo menos es un comienzo.
  </p>
  
  <p>
  </p>
