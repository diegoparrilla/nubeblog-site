---
author: Diego Parrilla
bttc_cache:
- "1283694587:2"
categories:
- vmware
date: 2010-04-06T16:55:13Z
dsq_thread_id:
- "204895396"
guid: /?p=1162
id: 1162
tags:
- licencias
- vmware
title: Los chips de 8 y 12 cores empiezan a dar problemas con las licencias de VMware
url: /2010/04/06/los-chips-de-8-y-12-cores-empiezan-a-dar-problemas-con-las-licencias-de-vmware/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="licencias,vmware" data-count="vertical" data-url="/2010/04/06/los-chips-de-8-y-12-cores-empiezan-a-dar-problemas-con-las-licencias-de-vmware/">Tweet</a>
</div>

Me acaba de llegar una noticia de [SearchServerVirtualization](http://searchservervirtualization.techtarget.com/generic/0,295582,sid94_gci1507974,00.html) en la que se hacen eco de algo que casi todo el mundo se veía venir. El modo de licenciamiento de los productos de VMware choca de frente con el los nuevos modelos de chips de AMD e Intel de 8 y más cores.  En el siguiente pantallazo de la web de VMware podemos apreciar que solo las versiones vSphere Advanced y Enterprise Plus soportan estos nuevos chips. Mientras que la versión estándar está en precio de catálogo a $795, las Advanced y Enterprise Plus están a $2245 y $3495 respectivamente. Más soporte, claro está.

<p style="text-align: center;">
  <img class="size-full wp-image-1163  aligncenter" title="vmware_license_options" src="/wp-content/uploads/vmware_license_options.png" alt="vmware_license_options" width="678" height="421" srcset="/wp-content/uploads/vmware_license_options.png 678w, /wp-content/uploads/vmware_license_options-300x186.png 300w" sizes="(max-width: 678px) 100vw, 678px" />
</p>

Con cualquier cliente de VMware que hables te dirá que está contento con el producto, pero para nada está satisfecho con los cambios, idas y venidas del modo de licenciamiento y los precios de VMware. Vamos, que ponen a parir a la gente de ventas. Este problema ya se veía venir desde hace tiempo, pero las nuevas CPUs lo han acelerado. Me consta que a algunos clientes se les ha tanteado la posibilidad de comprar licencias no por máquinas gestionadas si no por memoria gestionada, por ejemplo. Pero no ha colado.

La solución es sencilla para VMware, saca una nueva lista de precios y otro &#8216;migration path&#8217; para sus clientes, ellos se enfadan, patalean, pero como les tiene cogidos por los &#8220;cores&#8221;, pues a tragar (cómo me recuerda esto a una empresa que hay en Mordor, perdón, en Redmon&#8230;) . Bueno, hay otra, que es armarse de valor y migrar a otro hypervisor: para esto precisamente se ha desarrollado la funcionalidad de Virtual to Virtual (V2V) de Abicloud 1.5.
