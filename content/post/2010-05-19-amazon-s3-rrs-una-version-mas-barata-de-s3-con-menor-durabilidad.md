---
author: Diego Parrilla
bttc_cache:
- "1283694585:4"
categories:
- amazon
date: 2010-05-19T10:03:37Z
dsq_thread_id:
- "204894659"
guid: /?p=1188
id: 1188
tags:
- amazon
- s3
title: 'Amazon S3 RRS: una versión más barata de S3 con menor &#8216;durabilidad&#8217;'
url: /2010/05/19/amazon-s3-rrs-una-version-mas-barata-de-s3-con-menor-durabilidad/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,s3" data-count="vertical" data-url="/2010/05/19/amazon-s3-rrs-una-version-mas-barata-de-s3-con-menor-durabilidad/">Tweet</a>
</div>

[<img class="aligncenter size-full wp-image-121" title="logo_aws" src="/wp-content/uploads/logo_aws.gif" alt="" width="164" height="60" />](/wp-content/uploads/logo_aws.gif)

Amazon Web Services acaba de anunciar un nuevo servicio llamado Amazon S3 Reduced Redundancy Storage (RRS). ¿Y qué es esto? Pues en sus palabras, este nuevo servicio permite a los clientes reducir sus costes guardando informacion no tan crítica en un servicio de almacenamiento similar a S3 pero con menores niveles de redundancia. Parece que es un servicio interesante para quien almacenar información temporal o que se encuentra ya almacenada en otro sitio.

El servicio tradicional de S3 lo que hace es replicar el contenido en múltiples localizaciones, por lo que ante un fallo en una de estas localizaciones, los objetos almacenados se encuentran &#8216;replicados&#8217; y es posible recuperar la información. Este nivel de redundancia permite a S3 ofrecer (que no garantizar, [mirad el SLA](http://aws.amazon.com/s3-sla/)) una &#8216;durabilidad&#8217; de 99.999999999%. Es decir, [si tu guardas 10.000 objetos en S3, de media podrías perder uno cada 10 millones de años](http://aws.typepad.com/aws/2010/05/new-amazon-s3-reduced-redundancy-storage-rrs.html).

Este nuevo servicio lo que hace es reducir el número de localizaciones donde se encuentra replicada la información, por lo que esta &#8216;durabilidad&#8217; se reduce hasta un 99.99%. De nuevo, si guardas 10.000 objetos, de media puedes perder uno cada año.

El [coste de este nuevo servicio](http://aws.amazon.com/s3/#pricing) es de $0.10 por Gigabyte al mes, es decir, un 33% más barato que Amazon S3 tradicional.

Werner Vogels,el CTO de Amazon.com explica [cómo funciona S3 y el concepto de durabilidad](http://www.allthingsdistributed.com/2010/05/amazon_s3_reduced_redundancy_storage.html) en su blog. Una lectura interesante.

Y por último, si alguien tiene interés en atender al webinar de presentación, [aquí está el enlace](https://www2.gotomeeting.com/register/590572123).
