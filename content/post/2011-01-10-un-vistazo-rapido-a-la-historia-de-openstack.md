---
author: Diego Parrilla
categories:
- opensource
- openstack
- opinion
date: 2011-01-10T08:08:57Z
dsq_thread_id:
- "206123899"
guid: /?p=1957
id: 1957
tags:
- eucalyptus
- nasa
- openstack
- rackspace
title: Un vistazo rápido a la historia de OpenStack
url: /2011/01/10/un-vistazo-rapido-a-la-historia-de-openstack/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="eucalyptus,nasa,openstack,rackspace" data-count="vertical" data-url="/2011/01/10/un-vistazo-rapido-a-la-historia-de-openstack/">Tweet</a>
</div>

[<img class="alignright size-full wp-image-1964" title="OpenStackLogo_270x279" src="/wp-content/uploads/OpenStackLogo_270x279.jpg" alt="" width="270" height="279" />](/wp-content/uploads/OpenStackLogo_270x279.jpg)A mediados de 2010 se produjo un &#8216;evento sistémico&#8217; en el mundo del software de Infraestructura como Servicio (IaaS). [Rackspace y la NASA anunciaban de manera conjunta que estaban desarrollando un nuevo software de IaaS](http://techcrunch.com/2010/07/18/openstack-org-rackspace-open-sources-their-cloud-services-platform-and-gets-nasa-on-board/) que venía a solucionar los problemas que la NASA le había encontrado a [Eucalyptus](http://www.eucalyptus.com), y a convertirse en una alternativa real a Amazon Web Services.

Que [Rackspace](http://www.rackspace.com) esté interesado en competir con Amazon Web Services es lógico, pero ¿la NASA? ¿Por qué [semejante palo a Eucalyptus](http://www.channelregister.co.uk/2010/07/20/why_nasa_is_dropping_eucalyptus_from_its_nebula_cloud/)? Se habló de dos razones principales: que Eucalyptus no escala y que no es realmente de código abierto, sino más bien &#8216;open core&#8217;. Al parecer Eucalyptus está pensado como un producto completo para unas necesidades concretas: La Nube Privada. Sin embargo, la NASA buscaba algo que escalase a lo bestia-bestia: un millón de servidores o 60 millones de máquinas virtuales. Para conseguir eso, es necesario abrir las tripas de Eucalyptus y modificarlo de tal manera que soporte ese nivel de escalado. Pero&#8230; resulta que no es &#8216;abierto&#8217; de verdad&#8230; y la NASA decidió que no podía meter recursos en algo que no controlaba.

Así que [OpenStack](http://www.openstack.org) nació como una alternativa completamente abierta al amparo de Rackspace y gran parte de la industria. A diferencia de Eucalyptus no es un producto, sino un &#8216;Framework&#8217;. Es decir, puede manipularse de tal manera que puede adaptarse a las necesidades de los clientes. Y por supuesto todo el código se encuentra disponible bajo licencia Apache 2.0.

El lanzamiento fue todo un ejemplo de cómo presentar en sociedad un producto. Consiguieron pasar de la nada al infinito en un instante. Se colocaron en lo más alto del &#8216;hype&#8217; del Cloud. Todo el mundo hablaba (y sigue hablando) de OpenStack. Unos con esperanza, y otros con temor. El músculo financiero de Rackspace y sus socios hizo temblar los cimientos de unas cuantas startups competencia de Eucalyptus.

Una vez que se disipó el ruido de las notas de prensa, era hora de ver qué era realmente OpenStack, y aquí es donde nos encontramos con dos sorpresas: la primera es que el framework  estaba por hacer, y la segunda es que Rackspace controlaba completamente el roadmap.

Que el framework estaba por hacer no estaba muy claro al principio&#8230; pero la cosa quedó clara rápidamente. OpenStack está compuesto de dos proyectos principales: [Cloud Storage  con el proyecto SWIFT](http://openstack.org/projects/storage/) y [Cloud Computing con el proyecto NOVA](http://openstack.org/projects/compute/). SWIFT es un proyecto mucho más avanzado y creo realmente que con posibilidades de ser desplegado por clientes. Sin embargo NOVA está aún hoy muy verde. NOVA coge el código del [proyecto Nebula de la NASA](http://nebula.nasa.gov/) como base, y lo modifica para adaptarse a las necesidades de los Directores del Proyecto en Rackspace.

Al principio, NOVA era un clon puro y duro de Amazon EC2. Para manejar NOVA tenías que usar la API de EC2, de hecho. Pero las cosas han ido cambiando y se diseñó un nuevo API  basado en la Nube de Rackspace. El objetivo es que si se quiere usar el API de EC2, que se pueda usar. Y si se quiere usar el de Rackspace, que se pueda usar también.

La primera release disponible de NOVA llamada Austin, la verdad es que fue muy decepcionante desde el punto de vista de funcionalidad y estabilidad, pero muy prometedora desde el punto de vista de evolución de proyecto. Su velocidad de desarrollo es bestial y es probable que en la próxima release llamada Bexar y programada para febrero de 2011 puedan sacar un framework más estable, desligado del API de Amazon EC2 y con características muy interesantes como soporte para Hyper-V o soporte de discos virtuales con máquinas completas, snapshots de imágenes, etc.

Es habitual ver en las [predicciones para este año que una de las tendencias es OpenStack](http://www.computerworlduk.com/in-depth/cloud-computing/3253266/cloud-computing-2011-predictions/), aunque a día de hoy no hay ni una implantación en el mundo que esté dando servicio real. Puede que sea fruto de esta burbuja del Cloud Computing&#8230; o no. Tal vez realmente estamos ante un proyecto que puede marcar el futuro de una industria.

Y lo mejor de todo, es que lo estamos viviendo y podemos participar.
