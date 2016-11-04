---
author: Diego Parrilla
categories:
- Uncategorized
date: 2008-12-10T11:03:27Z
dsq_thread_id:
- "204693018"
guid: /?p=465
id: 465
title: Amazon EC2 desembarca en Europa con dos nuevas zonas
url: /2008/12/10/amazon-ec2-desembarca-en-europa-con-dos-nuevas-zonas/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-count="vertical" data-url="/2008/12/10/amazon-ec2-desembarca-en-europa-con-dos-nuevas-zonas/">Tweet</a>
</div>

[<img class="aligncenter size-full wp-image-121" title="logo_aws" src="/wp-content/uploads/logo_aws.gif" alt="" width="164" height="60" />](/wp-content/uploads/logo_aws.gif)

Esta noticia si que la estaba esperando: [Amazon EC2 tendrá dos zonas disponibles en Europa](http://www.allthingsdistributed.com/2008/12/amazon_ec2_in_europe.html). Leo en el blog del CTO de Amazon Werner Vogels que finalmente se ha lanzado el servicio debido a las numerosas peticiones de sus clientes en Europa (incluida la mía).

Las principales ventajas para los Europeos se pueden resumir en:

  * La menor latencia de acceso hace que los servicios sean más rápidos a este lado del atlántico.
  * Acceso más rápido al contenido que ya está en Europa en S3 desde EC2.
  * Las empresas cumplirán las condiciones regulatorias de la EU, especialmente en lo que a datos sensibles se refiere.

Pero no todo es tan bonito: las instancias con Microsoft Windows todavía no está disponibles, ni tampoco [Amazon DevPay](http://aws.amazon.com/devpay/). Pero lo realmente relevante es que el coste en Europa es superior porque [los costes operacionales en Europa son mayores](http://aws.amazon.com/ec2/#pricing). El coste del canuto es mismo, pero EC2 y Elastic Block Storage (EBS) son un 10% más caras en Europa.

Además no he podido encontrar donde se encuentran alojadas las zonas, si alguien lo encuentra, que por favor envíe un mensaje con la información.

Si tus clientes están mayoritariamente en Europa sin duda se benificiarán de una menor latencia en los servicios, pero si tus clientes son globales probablemente el balanceo por localización geográfica puede incrementar la calidad de tu servicio.

Tendré que hacer mis cuentas, pero es posible que dentro de un par de meses considere migrar mis instancias a las zonas Europeas.

**Actualización**: Ryan Koop de [CohesiveFT](http://www.cohesiveft.com/) me indica que la infraestructura de AWS en Europa se encuentra en Irlanda. Y me pasa el [enlace en Techcrunch donde se confirma que es Irlanda](http://www.techcrunch.com/2008/12/10/amazon-ec2-now-available-in-europe/).
