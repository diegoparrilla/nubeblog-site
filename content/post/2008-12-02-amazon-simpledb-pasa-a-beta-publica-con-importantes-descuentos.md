---
author: Diego Parrilla
categories:
- cloud
date: 2008-12-02T10:02:39Z
dsq_thread_id:
- "260936626"
guid: /?p=404
id: 404
tags:
- amazon
- simpledb
title: Amazon SimpleDB pasa a beta pública con importantes descuentos
url: /2008/12/02/amazon-simpledb-pasa-a-beta-publica-con-importantes-descuentos/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,simpledb" data-count="vertical" data-url="/2008/12/02/amazon-simpledb-pasa-a-beta-publica-con-importantes-descuentos/">Tweet</a>
</div>

[<img class="aligncenter size-full wp-image-121" title="logo_aws" src="/wp-content/uploads/logo_aws.gif" alt="" width="164" height="60" />](/wp-content/uploads/logo_aws.gif)Durante la revisión matutina de mis feeds este Lunes, pude leer la siguiente noticia en el [Amazon Web Services Blog: Amazon SimpleDB Grows up](http://aws.typepad.com/aws/2008/11/amazon-simpledb-grows-up.html). Al pinchar sobre el enlace para leer el contenido en la web y no en el Google Reader, me dió un 404. Alguien en Amazon se había colado y había publicado el post antes de tiempo, cuando lo retiraron ya era demasiado tarde y era parte de la caché de Google.

A lo largo de la tarde la noticia se ha confirmado, así que ya puedo escribir con libertad sobre ello -aunque supongo que como yo otros tantos habrán leido el feed-. Amazon SimpleDB deja de ser una beta por invitación y pasa a beta pública o &#8216;ilimitada&#8217;, como ellos dicen. Aunque el servicio ha ido evolucionando a lo largo de los meses con cambios más o menos importantes, ahora nos encontramos ante un cambio en su política de precios bastante curiosa. Paso a resumirla:

  * Los primeros seis meses, puedes consumir hasta 500Mb de almacenamiento gratis, y puedes usar 25 horas/máquina cada mes. El tráfico entre EC2 y SimpleDB, ni tampoco los primeros 1Gb de entrada y 1Gb de salida se tarificarán.
  * Se baja el precio desde los $1.50 por GB al mes a $0.25 por Gb mensual

Como ejemplo, tengo un servicio corriendo en Amazon SimpleDB que no llegó a consumir ni una hora de computación al mes. Aunque he de confesar que no tiene mucho tráfico y tengo implementada una política de cache write-through que limita los hits a SimpleDB de manera drástica. Del coste mensual de mis servicios con Amazon, el más caro es EC2, luego es el ancho de banda consumido, y luego SimpleDB. Tengo muy poco contenido estático en S3, eso también es cierto.

Mi impresión es que posiblemente este es un servicio que está costando que adopten los clientes. Las razones pueden ser varias, pero voy a apuntar un par de ellas:

  * La sombra del modelo relacional es muy alargada&#8230; y SimpleDB no sigue un esquema relacional.
  * La posibilidad de caer cautivo de Amazon con SimpleDB es mayor que con otros servicios como S3 o EC2.
  * No existe un entorno donde realizar pruebas unitarias sin pagar por ello a Amazon. Un poco como el entorno que ofrece Google AppEngine, por ejemplo. No es el coste de la tarifa -no es relevante-, son problemas de latencia y ancho de banda entre el entorno de desarrollo y el servicio SimpleDB.
  * La necesidad de implementar procesos de sincronización entre las bases de datos locales de los clientes -normalmente relacionales- y SimpleDB -no relacional- dispara el coste total del servicio. Faltan herramientas que hagan esto de manera transparente.
