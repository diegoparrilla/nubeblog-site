---
author: Diego Parrilla
categories:
- cloud
- Uncategorized
date: 2008-11-11T09:04:06Z
dsq_thread_id:
- "205636374"
guid: /?p=256
id: 256
tags:
- almacenamiento
- emc
title: EMC Atmos, nueva solución de almacenamiento Cloud Optimized Storage
url: /2008/11/11/emc-atmos-nueva-solucion-de-almacenamiento-cloud-optimized-storage/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="almacenamiento,emc" data-count="vertical" data-url="/2008/11/11/emc-atmos-nueva-solucion-de-almacenamiento-cloud-optimized-storage/">Tweet</a>
</div>

<p style="text-align: center;">
  <a href="/wp-content/uploads/emcatmosideas.jpg"><img class="aligncenter size-medium wp-image-259" title="emcatmosideas" src="/wp-content/uploads/emcatmosideas.jpg" alt="" width="861" height="541" srcset="/wp-content/uploads/emcatmosideas.jpg 861w, /wp-content/uploads/emcatmosideas-300x188.jpg 300w" sizes="(max-width: 861px) 100vw, 861px" /></a><a href="http://www.emc.com"></a>
</p>

<p style="text-align: left;">
  <a href="http://www.emc.com">EMC</a> acaba de anunciar su nueva linea de productos <a href="http://www.emc.com/products/detail/software/atmos.htm">Atmos</a>. Se trata de una solución de infraestructura de almacenamiento (como no podía ser de otra manera viniendo de EMC) en La Nube o <a href="http://www.emc.com/products/category/subcategory/cloud-optimized-storage.htm">Cloud Storage</a>. Este sistema construido sobre hardware commodity permite alcanzar niveles de almacenamiento de hasta 360Petabytes, está dirigido a aquellos que necesitas optimizar la distribución de información rica y no estructurada, permitiendo a proveedores Web 2.0, proveedores de internet, telcos, empresas de media y entretenimiento construir y servir de manera segura servicios de entrega de información basados en La Nube, así como aplicaciones con necesidades de escalado masivo.
</p>

<p style="text-align: left;">
  EMC ha descrito este producto como Cloud Optimized Storage (COS), que es:
</p>

> La capacidad de acceder a aplicaciones e información desde un proveedor externo -como una gran compañía de telecomunicaciones- que ha construido a una gran infraestructura en La Nube. Esta infraestructura tendrá ingentes cantidades de información no estructurada en la Web, y requerirá de una política que disperse la información de manera eficiente por todo el mundo.

Algunas características relevantes del producto son:

  * No existe el concepto de Gigabyte o Terabyte, son unidades demasiado pequeñas. Está diseñado para despliegues multi-Petabyte. Solo se manejan objetos y metadata.
  * No es un cluster de sistema de ficheros ni nada parecido. Se ha construido desde cero pensando en las necesidades de La Nube.
  * La información se almacena como objetos. Se aplican políticas sobre estos objetos, permitiendo aplicar diferente funcionalidad y niveles de servicio diferentes tipos de usuarios y datos.
  * Espacio de nombres unificado. No se agrupa la información en silos independientes, sino que hay un único repositorio independientemente del número de Petabytes o cuantos miles de millones de objetos se encuentren distribuidos por cualquier número de lugares e independientemente del número de usuarios.
  * Una única consola de gestión, da igual el número de lugares donde haya repositorios de objetos
  * Es un sistema autónomo que reacciona de manera automática a los cambios en la carga y a los fallos para asegurar la disponibilidad global del sistema.
  * Servicios avanzados de gestión de la información: replicado, versionado, compresión, deduplicación y parada de la rotación de los discos (disk drive spin-down).
  * APIs Web Services REST y SOAP. También es posible usar acceso por fichero.

La solución es tan potente que es posible que los objetos que se usan más frecuentemente tengan más copias en más sitios, y la que es más vieja y/o se acceda con menos frecuencia se encuentra en menos sitios y además comprimida. Es posible también implementar servicios de acceso seguro y de pago-por-uso.

No se ha dado ningún precio al producto, aunque al parecer el precio del producto es bastante inferior a una solución similar basada en [NAS](http://es.wikipedia.org/wiki/Network-attached_storage), donde el precio por Gigabyte es de docenas de euros. A esto hay que sumar el precio de los Servicios profesionales que pongan en marcha la solución, por supuesto.

Por lo que se, hay Telcos en España que están muy interesadas en ofrecer servicios de almacenamiento virtual masivo al estilo de Amazon S3 o los repositorios de fotos Picassa o Flickr como valor añadido a sus líneas ADSL. Sin embargo, el precio de poner en marcha una solución de este tipo usando tecnología tradicional es absolutamente prohibitivo. Este es el tipo de mercado al que va enfocado este producto de alta gama. Y cuando los usuarios tengamos acceso a este servicio al contratar nuestra línea con ADSL, ya no tendremos que almacenar en nuestros equipos la música y las películas que honradamente hemos comprado, lo haremos en el espacio que pagamos a nuestro operador. Aunque todos los honrados nos perderemos la posibilidad de ejecutar Bittorrent o Emule en una instancia en La Nube alojada en centros de datos al lado de estos repositorios de datos, con velocidades de descarga de gigabytes&#8230; ¡Películas en formato Blu-Ray descargadas en menos de un minuto!
