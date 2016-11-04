---
author: Diego Parrilla
bttc_cache:
- "1283694588:1"
categories:
- cloud
- datacenter
date: 2010-04-04T17:51:06Z
dsq_thread_id:
- "204895361"
guid: /?p=1158
id: 1158
tags:
- hardware
- infraestructura
- servidores
title: Supermicro mete 96 cores y 1TB de RAM en una caja 2U
url: /2010/04/04/supermicro-mete-96-cores-y-1tb-de-ram-en-una-caja-2u/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="hardware,infraestructura,servidores" data-count="vertical" data-url="/2010/04/04/supermicro-mete-96-cores-y-1tb-de-ram-en-una-caja-2u/">Tweet</a>
</div>

Hace ya más de un año que Cisco anunció la gama de productos herederos de su [Proyecto California](http://www.amazon.com/Project-California-Virtualization-Unified-Computing/dp/0557057396), los [UCS (Unified Computing System)](http://www.cisco.com/en/US/netsol/ns944/). El proyecto California significó el desembarco de Cisco en el mercado de los servidores, aunque en realidad lo que hizo es una plataforma completa para el Centro de Datos: servidores, redes y gestión (espera&#8230; ¿y el almacenamiento?). Una cosa que llamó la atención enseguida era que [los servidores UCS se anunciaban como &#8216;blades&#8217; pero venían en un formato horizontal en vez de vertical](http://www.cisco.com/en/US/products/ps10279/index.html). Por cada 1U se pueden meter 2 &#8216;blades&#8217; gemelos (twin) o bien un servidor 1U completo. La conexión a las [&#8216;unified fabrics](http://www.cisco.com/en/US/netsol/ns945/index.html)&#8216; se hacen en el chasis y se ahorra en costes a la vez que se obtiene una gran densidad.

Si realmente Cisco ha tenido éxito o no con esta propuesta entre sus clientes, lo desconozco, aunque se que tiene grandes proyectos en cartera con esta plataforma. Lo que sí tengo claro es que los competidores le han copiado hasta donde han podido. Así, Dell ha anunciado su nueva gama de servidores PowerEdge C (C de Cloud, claro) donde aparece este nuevo formato en el [PowerEdge C6100](http://www1.euro.dell.com/es/es/empresas/Servidores/poweredge-c6100/pd.aspx?refid=poweredge-c6100&s=bsd&cs=esbsdt1), un chasis 2U para cuatro nodos. HP tambíen tiene su chasis 2U para cuatro nodos en su gama Proliant SL, en el [modelo SL2x170z](http://www1.euro.dell.com/es/es/empresas/Servidores/poweredge-c6100/pd.aspx?refid=poweredge-c6100&s=bsd&cs=esbsdt1).

Pero quien se lleva la palma sin duda es Supermicro. Los californianos han anunciado su [&#8220;2U Twin2 System&#8221;](http://www.supermicro.com/Aplus/system/2U/2022/AS-2022TG-HIBQRF.cfm), un  chasis 2U donde pueden meter cuatro nodos. Gracias a que cada nodo soporta dos de los nuevos [AMD Opteron 6100](http://www.slideshare.net/AMDUnprocessed/amd-opteron-6000-series-platform-press-presentation-final-3564470) con 12 cores y hasta 256GB de RAM DDR3-1333, tenemos que en una caja 2U podemos llegar a tener 96 Cores y 1TB de RAM. Una bestialidad. Cada nodo puede albergar 3 discos de 3.5&#8243; hot swap. Le acompaña una unidad de alimentación de 1400W y como opción trae en placa base una conexión QDR Infiniband de 40Gbps.

<p style="text-align: center;">
  <img class="size-full wp-image-1159  aligncenter" title="SuperMicro_8S_2U_350" src="/wp-content/uploads/SuperMicro_8S_2U_350.jpg" alt="SuperMicro_8S_2U_350" width="350" height="300" srcset="/wp-content/uploads/SuperMicro_8S_2U_350.jpg 350w, /wp-content/uploads/SuperMicro_8S_2U_350-300x257.jpg 300w" sizes="(max-width: 350px) 100vw, 350px" />
</p>

Es evidente que el Cloud Computing, la Virtualización y las Infraestructuras como Servicio están acelerando los cambios dentro del Centro de Datos, hasta el punto que empresas centradas en el hardware más estandarizado empiecen a ofrecer pequeños monstruos como estos. La información que he encontrado sobre los precios de todos estos productos es muy escasa y contradictoria. En el caso de Supermicro ya aparece en listas de precios de vendedores americanos, aunque con una disparidad de precio muy grande, sin dejar claro qué partes componen la solución.

Este tipo de plataformas son perfectas para la implantación de soluciones Cloud dentro de las empresas o los proveedores, sin duda, ya que el coste por core de una plataforma como estas baja de manera significativa. No tardaremos mucho antes de que en la división de costes de una plataforma Cloud, el software de gestión y virtualización suponga más del 30% o el 40% de la solución. Bueno, algunos proveedores ya tienen ese porcentaje y más&#8230; pero tendrán que bajarse de la &#8216;nube&#8217;.
