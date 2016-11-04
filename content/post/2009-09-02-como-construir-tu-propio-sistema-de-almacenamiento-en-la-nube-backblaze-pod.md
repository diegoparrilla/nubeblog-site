---
author: Diego Parrilla
categories:
- almacenamiento
date: 2009-09-02T11:26:20Z
dsq_thread_id:
- "204694032"
guid: /?p=1052
id: 1052
tags:
- almacenamiento
title: 'Cómo construir tu propio sistema de almacenamiento en la Nube: Backblaze Pod'
url: /2009/09/02/como-construir-tu-propio-sistema-de-almacenamiento-en-la-nube-backblaze-pod/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="almacenamiento" data-count="vertical" data-url="/2009/09/02/como-construir-tu-propio-sistema-de-almacenamiento-en-la-nube-backblaze-pod/">Tweet</a>
</div>

<img class="aligncenter size-full wp-image-1054" title="backblaze-cheap-cloud-server-storage2" src="/wp-content/uploads/backblaze-cheap-cloud-server-storage2.jpg" alt="backblaze-cheap-cloud-server-storage2" width="560" height="188" srcset="/wp-content/uploads/backblaze-cheap-cloud-server-storage2.jpg 560w, /wp-content/uploads/backblaze-cheap-cloud-server-storage2-300x100.jpg 300w" sizes="(max-width: 560px) 100vw, 560px" />A través de [highscalability.com](http://highscalability.com) me encuentro con un artículo que puede interesar a todos aquellos que están pensando en dar servicios de Almacenamiento en La Nube (Cloud Storage) y quieren un diseño abierto. La gente de Backblaze.com nos muestran cómo diseñaron y construyeron sus propios appliances para gestionar hasta 67 Teras en un 4U. E incluso te puedes descargar el fichero con el modelo en 3D para que lo puedas encargar.

[Backblaze.com](http://www.backblaze.com) es un servicio de backup online, ahora llamado Cloud Storage (sigh!). La información almacenada se mide en Petabytes, por lo que no había nada en el mercado que fuera capaz de dar un precio por gigabyte almacenado alrededor de los 30 céntimos de euro.

Me he &#8216;apropiado&#8217; de esta interesante tabla mostrando el coste por petabyte entre proveedores:

<img class="aligncenter size-full wp-image-1055" title="cost-of-a-petabyte-chart" src="/wp-content/uploads/cost-of-a-petabyte-chart.jpg" alt="cost-of-a-petabyte-chart" width="560" height="642" srcset="/wp-content/uploads/cost-of-a-petabyte-chart.jpg 560w, /wp-content/uploads/cost-of-a-petabyte-chart-261x300.jpg 261w" sizes="(max-width: 560px) 100vw, 560px" />Los datos se han calculado asumiendo un tiempo de amortización de 3 años. Ellos han conseguido un precio por appliance de $7867 (unos 5600€ al cambio actual). Una pasada.

Desde el punto de vista software, lo que han montado es una Debian con JFS y una interfaz web que permite subir y bajar ficheros. Nada muy espectacular en este aspecto. La verdad es que con un monstruo así probablemente les hubiera ido mejor usar ZFS con Opensolaris: la gestión es muy eficiente y compites directamente con el SUN X4550 a nivel de prestaciones, sobre todo por el [Thin Provisioning](http://en.wikipedia.org/wiki/Thin_provisioning).

Veo en este tipo de productos sinergias con nuestro producto [Abicloud](http://www.abiquo.com/en/products/abicloud): con una arquitectura completamente automatizada, un sistema de almacenamiento para archivado que complemente al <span style="text-decoration: line-through;">NAS</span> SAN de almacenamiento es lo lógico, más que un sistema en cintas, en mi opinión. La sensación de disponibilidad inmediata que dan las infraestructuras como servicios queda mermada por el acceso a las cintas. Lo que no quiere decir que no sea necesario realizar copias de respaldo en cintas, pero de manera transparente al usuario cloud.

Asi que, si alguno se anima a montar algo parecido por aquí, nosotros encantados en probar nuestro software sobre él.

El post completo está [aquí](http://blog.backblaze.com/2009/09/01/petabytes-on-a-budget-how-to-build-cheap-cloud-storage/).
