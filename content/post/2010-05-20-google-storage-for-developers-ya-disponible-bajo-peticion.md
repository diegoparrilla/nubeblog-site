---
author: Diego Parrilla
bttc_cache:
- "1283694585:8"
categories:
- almacenamiento
- google
date: 2010-05-20T07:22:35Z
dsq_thread_id:
- "204894676"
guid: /?p=1191
id: 1191
tags:
- almacenamiento
- google
title: Google Storage for Developers ya disponible bajo petición
url: /2010/05/20/google-storage-for-developers-ya-disponible-bajo-peticion/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="almacenamiento,google" data-count="vertical" data-url="/2010/05/20/google-storage-for-developers-ya-disponible-bajo-peticion/">Tweet</a>
</div>

<p style="text-align: center;">
  <img class="aligncenter" src="http://code.google.com/intl/es-ES/events/images/io2010logo.png" alt="" width="300" height="158" />
</p>

Se rumoreaba que el anuncio del [Amazon S3 &#8216;light&#8217;](/2010/05/19/amazon-s3-rrs-una-version-mas-barata-de-s3-con-menor-durabilidad/) presentado ayer era pura contraprogramación de Amazon. En el Google I/O 2010, se ha anunciado la disponibilidad del nuevo servicio [Google Storage for Developers](http://code.google.com/intl/es-ES/apis/storage/docs/overview.html). Resumiendo, si conoces Amazon S3 o cualquier otro servicio de almacenaje en la nube de objetos, es lo mismo, pero hecho por Google.

Cuando veo la etiqueta &#8216;for Developers&#8217;, me hecho a temblar. ¿Esta coletilla se pone para indicar que el servicio no es lo suficientemente estable para el uso por el público general? ¿O bien porque para aprovechar este servicio hay que tener conocimientos de programación para usar su API REST? No lo se&#8230; pero bien la lamentable página de información del producto, me inclino a pensar lo primero. No se a qué  clase de público quieren atraer, pero dado que el servicio es de pago, me parece que deberían cuidar un poco más la presentación del producto. Son Google, no una frikistartup.

Lo que me más me ha extrañado ha sido el precio. Dado que ni están en Beta, debería ser gratis hasta cierto límite. Pero no, de gratis nada. Más aún, [es más caro que Amazon S3](http://aws.amazon.com/s3/#pricing). Comparemos:

  * Coste por Gigabyte al mes: Google=$0.17 , Amazon=$0.15
  * Coste por Gigabyte de subida de datos: Google=$0.10 , Amazon= $0.1
  * Coste por Gigabyte de bajada de datos: Google Americas y EMEA=$0.15 , Amazon=$0.15
  * 1.000 peticiones PUT, POST, LIST = Google=$0.01 ,  Amazon=$0.01
  * 10.000 peticiones GET, HEAD: Google=$0.01,  Amazon=$0.1

El coste por gigabyte guardado es $0.02 menor en Amazon, pero dado que Amazon ofrece descuentos importantes en función del volumen, esta cifra disminuye en cuando pasamos de los 10TB de almacenamiento.

La verdad es que no veo todavía ninguna razón por la que alguien quisiera migrar de Amazon S3 (o de cualquier otro servicio similar) a Google Storage. No se integra con Google Apps, y por si fuera poco Google no explica cual es su arquitectura de red y sistemas, así que no sabemos si puede tener interés para reducir latencias a la hora de servir datos, por ejemplo. Es decir, nos piden que confiemos a ciegas en un producto más caro, más oscuro e inmaduro.

Quien quiera probar el servicio, debe apuntarse a una lista de espera. Y solo si eres un ciudadano americano podrás hacerlo. Así que si alguien consigue una cuenta y lo prueba, estoy encantado de ofrecerle el blog para que nos cuente la experiencia.

**Actualización: Google ha anunciado que los primeros 100GB de almacenamiento y los primeros 300GB de transferencia son gratuitos durante el período de preview.**
