---
author: Diego Parrilla
bttc_cache:
- "1283694584:0"
categories:
- amazon
date: 2010-09-02T11:55:15Z
dsq_thread_id:
- "204894968"
guid: /?p=1283
id: 1283
tags:
- amazon
- blog
title: Por qué dejo de usar Amazon EC2
url: /2010/09/02/por-que-dejo-de-usar-amazon-ec2/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,blog" data-count="vertical" data-url="/2010/09/02/por-que-dejo-de-usar-amazon-ec2/">Tweet</a>
</div>

[<img class="size-full wp-image-121 alignright" title="logo_aws" src="/wp-content/uploads/logo_aws.gif" alt="" width="164" height="60" />](/wp-content/uploads/logo_aws.gif)Cuando alguien anuncia en un blog o alguna red social que deja un servicio la mayoría de las veces tiene que ver con una mala experiencia con el servicio, o una mala experiencia con el Servicio de Atención al Cliente.  En este caso, no ha ocurrido ninguna de estas dos cosas.

Más bien todo lo contrario, mi experiencia usando Amazon EC2 en estos tres últimos años ha sido magnífica. La disponibilidad del servicio si no me equivoco ha sido del 100% o rozándolo. He probado casi todo lo probable en Amazon Web Services, y la verdad es que es un ejemplo de calidad de servicio y de mejora continua. Siempre he echado de menos un servicio de atención al cliente al otro lado, pero nunca se pensó esta plataforma para eso.

He usado Amazon EC2 principalmente para varias cosas:

  * Desarrollar un proyecto ultrasecreto que sigue guardado en un cajón desde que empecé a currar con Abiquo que necesitaba escalabilidad salvaje. Y por lo que he visto recientemente, sigue siendo una posibilidad de negocio real (¿Algún BA en la sala?).
  * Alojar el proyecto urlhint.com, un acortador de URLs que usaba todo el stack Amazon Web Services. Debería publicar el código en sourceforge o algo así, como ejemplo de uso de las APIs AWS en java.
  * Alojar el blog nubeblog.com
  * Ejecutar tareas de computación intensiva para la conversión de imágenes virtuales entre diferentes formatos para los repositorios públicos de Abiquo.

Los dos primeros proyectos están muertos o congelados. Las tareas de computación necesarias por Abiquo ahora se pueden hacer con nuestro módulo de Virtual-to-Virtual dentro de la plataforma (V2V). Y el blog, pues **hay alternativas más baratas en el mundo SaaS.**

¿Y qué quiero decir con esto? Pues que según madure el mundo SaaS cada vez será menos habitual tener infraestructura para servicios o aplicaciones que no sean complejas o que por su criticidad no puedan alojarse compartidas con otros. Veo mucha gente empeñada en seguir vendiendo el &#8216;servidor dedicado&#8217; pequeñito para alojar cosas que pueden alojarse en otro tipo de plataformas, y que por precio a la larga ganarán. Y donde hay presión de precios no puedes compartir con quien tiene más volumen que tú.

Mi caso igual es un poco extremo, pero creo que anuncia una tendencia en este mercado: la hiperespecialización o verticalización de  las soluciones.
