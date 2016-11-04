---
author: Diego Parrilla
categories:
- cloud
- opinion
date: 2010-12-02T10:46:22Z
dsq_thread_id:
- "204895177"
guid: /?p=1898
id: 1898
tags:
- aws
- estandar
- opinion
- wikileaks
title: 'Wikileaks expulsado de Amazon: Las Nubes no son ni neutrales ni abiertas'
url: /2010/12/02/wikileaks-expulsado-de-amazon-las-nubes-no-son-ni-neutrales-ni-libres/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="aws,estandar,opinion,wikileaks" data-count="vertical" data-url="/2010/12/02/wikileaks-expulsado-de-amazon-las-nubes-no-son-ni-neutrales-ni-libres/">Tweet</a>
</div>

[<img class="alignright size-medium wp-image-1899" title="Logo_portal_Wikileaks" src="/wp-content/uploads/Logo_portal_Wikileaks-300x300.jpg" alt="" width="300" height="300" srcset="/wp-content/uploads/Logo_portal_Wikileaks-300x300.jpg 300w, /wp-content/uploads/Logo_portal_Wikileaks-150x150.jpg 150w, /wp-content/uploads/Logo_portal_Wikileaks.jpg 340w" sizes="(max-width: 300px) 100vw, 300px" />](/wp-content/uploads/Logo_portal_Wikileaks.jpg)Llevamos varios días [descubriendo gracias a las filtraciones de Wikileaks](http://www.elpais.com/articulo/internacional/Wikileaks/acaba/diplomacia/clasica/elpepuint/20101129elpepuint_41/Tes) que hay mucho mamoneo en el mundo de la diplomacia. Creo que esto no es como para caerse de un guindo, y bueno, tiene más gracia que Gran Hermano 12 y es menos deprimente que las noticias sobre la economía española.

Hace ya varias semanas supimos que Wikileaks había [desplegado parte de sus servidores en Amazon Web Services](http://news.netcraft.com/archives/2010/10/27/wikileaks-edges-away-from-the-us.html). Tanto en sus zonas Europeas como en USA. Debido a la repercusión de las filtraciones de los cables diplomáticos (cablegate) han sufrido diversos ataques de DDoS en su proveedor de hosting tradicional en Suecia. Y bueno, dado que una manera de cubrirte las espaldas en un caso de DDoS es precisamente irte a una arquitectura Cloud con (supuestamente) escalado infinito, el DDoS pasaría a ser únicamente un [EDoS](/2009/01/27/los-riesgos-del-escalado-automatico-edos-economic-denial-of-sustainability/). Y si tienes una buena cuenta corriente, pues te la suda.

Pero ayer [Amazon expulsó a Wikileaks](http://www.itespresso.es/amazon-deja-de-acoger-a-wikileaks-48391.html) de su Nube. La respuesta de Wikileaks fue airada y en [twitter le soltó este recadito a Amazon](http://twitter.com/#!/wikileaks/statuses/10073870316863488). No he encontrado respuesta oficial de Amazon al respecto, pero supongo que Wikileaks habrá violado alguna clausula del contrato de servicio, o eso les han dicho. Lo más probable es que Amazon no haya querido tener problemas y les ha &#8216;desenchufado&#8217;. Hasta aquí un conflicto entre dos entidades/empresas.

Lo que yo me pregunto es: Si Amazon vende recursos de computación en modo utility, ¿puede decidir si es correcto o no el uso del recurso? Es decir, ¿quién es Amazon para decidir en qué debo usar los recursos? ¿Puede una eléctrica cortarme el servicio de la misma manera? ¿Y el Canal de Isabel II el agua? ¿Puede un Proveedor de Servicios de Telecomunicaciones cortarme el acceso? ¡Oh wait!

Efectivamente&#8230; con la Neutralidad hemos topado. No con la Neutralidad de Red, sino con la Neutralidad en el acceso a los recursos. El Cloud Computing lo que hace es ofrecer en modo utility capacidades de computación, almacenamiento y RED. Cuando pienso en Neutralidad, supongo que por deformación profesional ya no pienso en Neutralidad de Red, sino de recursos de red, recursos de computación, recursos de almacenamiento.

Creo que Amazon ha ejercido un derecho que como proveedor de un servicio es legítimo. Pero me asusta pensar que estamos en manos de un único gran proveedor de Cloud global y que puede decidir sobre nuestros recursos de computación. Pensemos por un momento que alguien desarrolla un servicio que compite con su tienda online, y que está alojado en la Nube de Amazon Web Services&#8230; Sería tentador &#8216;desenchufarle&#8217;, ¿no?

Me pueden argumentar ustedes que nadie obliga a contratar Amazon Web Services. Pero&#8230; no estoy de acuerdo. Amazon Web Services supone más del 90% de los servicios de Cloud Pública del mundo. Es un monopolio de facto. Para poder competir en muchos casos el uso del Cloud Computing es inevitable. Por lo que a la fuerza ahorcan: pasarás por el aro para tu supervivencia, o te quedarás en un proveedor &#8216;legacy&#8217; sin los beneficios de la Nube.

Llevo más de dos años abogando por la creación de más proveedores de cloud basados en estándares y abiertos. Todo esto que estoy apuntando aquí arriba son preocupaciones constantes de quien ya lleva tiempo metido en servicios en la Nube. ¿Qué opciones sencillas tiene Wikileaks para moverse a otra Nube? Ninguna&#8230; la portabilidad y interoperabilidad entre Nubes está en pañales. Pero no hace falta irse al caso extremo de Wikileaks, este es un problema más común. Ya se que hay muchas [empresas que son felices](/2010/10/28/el-caso-de-exito-de-netflix-como-una-gran-corporacion-migra-a-la-nube-publica/) así y tienen éxito, pero la gran mayoría prefiere elegir.

**Actualización 03/12/2010: Amazon ha sacado [esta nota aclarando porqué desenchufaron a Wikileaks](http://aws.amazon.com/message/65348/).**
