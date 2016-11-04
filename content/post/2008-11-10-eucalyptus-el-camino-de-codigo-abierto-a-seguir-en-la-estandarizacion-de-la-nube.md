---
author: Diego Parrilla
categories:
- cloud
- opensource
date: 2008-11-10T08:10:44Z
dsq_thread_id:
- "204692861"
guid: /?p=248
id: 248
tags:
- eucalyptus
- opensource
title: 'Eucalyptus: el camino de código abierto a seguir en la estandarización de
  La Nube'
url: /2008/11/10/eucalyptus-el-camino-de-codigo-abierto-a-seguir-en-la-estandarizacion-de-la-nube/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="eucalyptus,opensource" data-count="vertical" data-url="/2008/11/10/eucalyptus-el-camino-de-codigo-abierto-a-seguir-en-la-estandarizacion-de-la-nube/">Tweet</a>
</div>

[<img class="aligncenter size-full wp-image-251" title="eucalyptuslogotext-300px" src="/wp-content/uploads/eucalyptuslogotext-300px.png" alt="" width="300" height="67" />](/wp-content/uploads/eucalyptuslogotext-300px.png)Cuando uno empieza a usar Amazon EC2, le vienen a la cabeza varias cuestiones, pero probablemente las más importantes son:

  * ¿Me voy a tener que &#8216;casar&#8217; con Amazon el resto de mi vida?
  * ¿Esto no es más caro que un hosting?
  * Amazon es casi un monopolio en esto, ¿me tratará bien como cliente?

Estas preguntas no son particulares a Amazon EC2 -exceptuando la comparación con el hosting-, y nos las encontramos cada vez que optamos por un producto de software cerrado. No hace falta ser muy inteligente para entender una de las ventajas del código abierto: ser un &#8216;cliente cautivo&#8217; (vendor lock-in lo llaman los anglos) es más complicado.

[Eucalyptus](http://eucalyptus.cs.ucsb.edu/) es un proyecto de código abierto que pretende evitar la posibilidad de caer cautivo de Amazon, ya que es un clon de la API de gestión de Amazon EC2 sobre otro tipo de infraestructura. Lo que hace es duplicar la funcionalidad de Amazon EC2 a través de sus comandos en línea y su API REST. Se ha implementado usando herramientas Linux disponibles a todo el mundo, y sus interfaces de gestión se basan en Servicios Web.

Las primeras versiones de Eucalyptus aprovechan un paquete de software de gestión de clusters linux llamado [Rocks](http://www.rocksclusters.org). En versiones recientes es posible instalarlo diréctamente sobre máquinas stand-alone, aunque ellos mismos reconocen que con Rocks la cosa es bastante más sencilla. La documentación de instalación [parece sólida y sencilla](http://eucalyptus.cs.ucsb.edu/wiki/EucalyptusAdministratorGuide) (aunque no lo he probado&#8230;). Como tecnología de virtualización se usa Xen en versiones 3.X. Pero no veo ninguna razón por la que se deba restringir a esta tecnología, exceptuando que Amazon EC2 se basa en Xen (aunque no por mucho tiempo, [según dicen](http://qumranet.com/)).

¿Por qué este software es tan importante? Bueno, puede que Eucalyptus no sea importante&#8230; pero si el concepto que subyace: **una infraestructura y una interfaz de gestión estándar e independiente del proveedor de Cloud**. Y todos conocemos los efectos benificiosos de la competencia. Así, un proveedor tendrá que esforzarse por tenernos como clientes ya que no somos  cautivos, y al poder movernos entre proveedores con facilidad los precios deberán bajar y los margenes se ajustarán.

Hay empresas que han empezado a probar Eucalyptus como alternativa a Amazon EC2, las más notables [RightScale](http://ostatic.com/176399-blog/rightscale-teams-with-eucalyptus-for-cloud-solutions) y [Elastra](http://www.marketwatch.com/news/story/elastra-delivers-cloud-portability-support/story.aspx?guid={B402B751-1E97-410C-8EE0-328CB4329880}&dist=hppr). RightScale ha sido uno de los mayores partners de Amazon EC2, y es absolutamente dependiente de ellos. Así que este movimiento va dirigido a no seguir siendo un &#8216;cliente cautivo&#8217;.
