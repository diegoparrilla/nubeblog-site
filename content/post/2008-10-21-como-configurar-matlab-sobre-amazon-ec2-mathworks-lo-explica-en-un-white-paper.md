---
author: Diego Parrilla
categories:
- cloud
- grid
date: 2008-10-21T09:55:46Z
dsq_thread_id:
- "204894437"
guid: /?p=135
id: 135
tags:
- amazon
- grid
- matlab
title: Cómo configurar MATLAB sobre Amazon EC2, Mathworks lo explica en un White Paper
url: /2008/10/21/como-configurar-matlab-sobre-amazon-ec2-mathworks-lo-explica-en-un-white-paper/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,grid,matlab" data-count="vertical" data-url="/2008/10/21/como-configurar-matlab-sobre-amazon-ec2-mathworks-lo-explica-en-un-white-paper/">Tweet</a>
</div>

[<img class="alignright size-full wp-image-137" title="matlab" src="/wp-content/uploads/matlab.gif" alt="" width="45" height="38" />](/wp-content/uploads/matlab.gif)Hace unos días en la lista de correo de [cloud-computing](cloud-computing@googlegroups.com) alguien preguntaba sobre experiencias con MATLAB en La Nube. Cualquier que visite la lista verá que MATLAB soporta soluciones variopintas, con implementaciones de todos los colores en Grid.

Hoy leo que la misma persona que inició la conversación anunciaba que [Mathworks](http://www.mathworks.com) había liberado un white paper explicando cómo usar [MATLAB](http://www.mathworks.com/products/matlab/) con Amazon Elastic Compute Cloud (EC2). El documento te lo puedes bajar [aquí](http://www.mathworks.com/programs/techkits/ec2_paper.html).

El documento explica cómo configurar las AMIs, además de explicar los pros y contras de la solución sobre EC2:

  * Coste: pagas por lo que usas.
  * Puesta en marcha: muy rápida, entre 6 y 8 horas de un administrador de sistemas sin experiencia con EC2
  * Licencias: Ojo, necesitas una licencia por cada &#8216;Worker&#8217; del pool.
  * QoS: Es una cuestión importante ya que funciona sobre internet (obvio&#8230;)
  * Rendimiento: La virtualización puede afectar a la entrada y salida, pero el verdadero problema es la latencia de red y el ancho de banda entre el entorno de escritorio y La Nube.
  * Seguridad: Es necesario crear una VPN entre los &#8216;Workers&#8217; y el entorno de escritorio.

¿Alguien lo ha probado?
