---
author: Diego Parrilla
categories:
- amazon
- seguridad
date: 2009-09-01T13:06:08Z
dsq_thread_id:
- "204693976"
guid: /?p=1048
id: 1048
tags:
- amazon
- blackhat
- seguridad
title: Magnífico post sobre cómo comprometer la seguridad de Amazon Web Services
url: /2009/09/01/magnifico-post-sobre-como-comprometer-la-seguridad-de-amazon-web-services/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,blackhat,seguridad" data-count="vertical" data-url="/2009/09/01/magnifico-post-sobre-como-comprometer-la-seguridad-de-amazon-web-services/">Tweet</a>
</div>

<p style="text-align: center;">
  <img class="aligncenter size-full wp-image-1049" title="headbak2" src="/wp-content/uploads/headbak2.jpg" alt="headbak2" width="570" height="134" srcset="/wp-content/uploads/headbak2.jpg 950w, /wp-content/uploads/headbak2-300x70.jpg 300w" sizes="(max-width: 570px) 100vw, 570px" />
</p>

Yago Jesús, uno de los bloggers de [SecurityByDefault](http://www.securitybydefault.com/) y enorme experto en seguridad me pasa un post de una presentación que se hizo en el [Black Hat&#8217;09](http://www.blackhat.com/) en la que se muestra como implementar un ataque DoS contra la Nube de Amazon (Amazon EC2) y cómo meter una imagen AMI maliciosa en su repositorio de imágenes.

Para el Denial of Service lo que hacen es generar de manera automática cuentas nuevas de usuario en Amazon AWS, y lanzar las 20 máquinas que tiene cada servicio. Y encima, usaron una sola tarjeta de crédito para todas las cuentas.

Lo de las imágenes es curioso. Crearon una imagen &#8216;fake&#8217; con un Sistema Operativo Fedora, le metieron en el arranque se bajara un fichero de su site, y lo consiguieron &#8216;colocar&#8217; entre los cinco primeros de la lista de AMIs públicas. Para ello, generaron 4000 imágenes de prueba hasta que encontraron una cuyo identificador alfanumérico aleatorio estuviese en lo más alto del ranking.

El post completo [aquí](http://www.sensepost.com/blog/3797.html).
