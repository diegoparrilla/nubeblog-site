---
author: Diego Parrilla
categories:
- almacenamiento
- cloud
- virtualización
date: 2010-09-06T09:35:33Z
dsq_thread_id:
- "204894981"
guid: /?p=1286
id: 1286
tags:
- 3par
- almacenamiento
- dell
- hp
- virtualización
title: ¿Qué tiene 3PAR que Dell y HP se pelean por ella?
url: /2010/09/06/que-tiene-3par-que-hp-dell-todos-se-pelean-por-ella/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="3par,almacenamiento,dell,hp,virtualizaci%C3%B3n" data-count="vertical" data-url="/2010/09/06/que-tiene-3par-que-hp-dell-todos-se-pelean-por-ella/">Tweet</a>
</div>

[<img class="aligncenter size-full wp-image-1291" title="3par-dell-hp" src="/wp-content/uploads/3par-dell-hp.jpg" alt="" width="480" height="313" srcset="/wp-content/uploads/3par-dell-hp.jpg 480w, /wp-content/uploads/3par-dell-hp-300x195.jpg 300w" sizes="(max-width: 480px) 100vw, 480px" />](/wp-content/uploads/3par-dell-hp.jpg)

Estas últimas semanas ha ocurrido algo que hacía muchos años que no se veía, y  que algunos han identificado como [la llegada de una nueva burbuja](http://www.elblogsalmon.com/sectores/estamos-ante-otra-burbuja-punto-com): [Dell](http://www.dell.com) y [HP](http://www.hp.com) han peleado por una empresa mucho más pequeña que ellas, [3PAR](http://www.3par.com).

Pero vamos por partes: hace unas semanas Dell hace una oferta por una &#8220;pequeña&#8221; empresa llamada 3PAR ($600M) dedicada a fabricar software y cabinas de almacenamiento. La oferta ofrece una prima por encima del 80% de su valor en el mercado. Los analistas critican a Dell por hacer una oferta que consideran muy alta.

Días después, una descabezada Hewlett-Packard (se habían quedado sin CEO por sus líos de faldas) hace un ejercicio de músculo financiero y aumenta la oferta por 3PAR de $18 por accion a $24,3. Todos absortos. Dell iguala la  oferta, pero HP sube hasta los $27. Es una prima del 200% sobre el valor de mercado en julio de la compañía. Dell vuelve a igualar. Nuevo envite de HP a $30 por acción. Dell ya no solo iguala la oferta, sino que ofrece $32, todo un órdago. Finalmente  HP ofrece $33 por acción, $2.4 miles de millones. Dell se rinde, no ve el envite, 3PAR pagará a Dell por romper el acuerdo de compra unos $90 millones de dólares y pasará a manos de HP ([más detalles en Gurusblog](http://www.gurusblog.com/archives/hp-mejora-oferta-dell-3par/02/09/2010/)).

Se especula cual es la razón por la que HP ha puesto tanto encima de la mesa para adquirir 3PAR. La realidad de fondo es que su ex-CEO, además de [tener relaciones inapropiadas con esta señora](http://www.boingboing.net/2010/08/08/actress-jodie-fisher.html), se había cepillado multitud de departamentos de I+D y había dejado una empresa tradicionalmente innovadora en una empresa centrada en los servicios [sin capacidad de crear cosas nuevas](http://techcrunch.com/2010/08/29/behind-the-bidding-war-the-real-reasons-why-hp-and-dell-are-so-desperate-for-3par/). Escándalos sexuales y falsa moral aparte, la situación es similar para Dell, pero por otras razones. Dell siempre ha trabajado en mercados de poco margen y mucho volumen, pero necesita &#8216;reinventarse&#8217; ofreciendo valor añadido sobre hardware que cada vez deja menos margen.

3PAR ha puesto las vergüenzas de estas empresas al descubierto por una razón muy simple: tiene un producto innovador que es atractivo para las grandes empresas y proveedores de servicios que han puesto sus ojos en el Cloud Computing y en el uso de soluciones que permiten el aprovechamiento máximo de su infraestructura.

La tecnología estrella de 3PAR es el modo en que ellos hacen el &#8216;thin provisioning&#8217;: Zero-detection thin provisioning. ¿Qué es el thin provisioning? Es la capacidad de algunas soluciones de almacenamiento de ofrecer a los usuarios la cantidad de almacenamiento que realmente necesitan, y no el que reservan. Por ejemplo: tu contratas con tu proveedor de hosting 2TB de almacenamiento, pero en realidad ellos no te reservan 2TB en sus cabinas, sino que hacen un reserva &#8216;virtual&#8217; de espacio, y la cabina te va dando más capacidad de almacenamiento según lo necesitas. Así, el aprovechamiento de las unidades de almacenamiento es mucho mayor, con el consiguiente ahorro.

Pero el &#8216;thin provisioning&#8217; no es nuevo ni único de 3PAR. Otros proveedores de soluciones cerradas e incluso de soluciones abiertas ya lo tienen. ¿qué lo hace especial? Más que el &#8216;thin provisioning&#8217; lo que hace especial la solución es el &#8216;unthin provisioning&#8217;. Esto es, la capacidad de poder meter dentro de las cabinas de 3PAR datos importados de almacenamientos externos.

Uno de los grandes problemas de las soluciones de &#8216;thin provisioning&#8217; es optimizar el almacenamiento por ejemplo de un disco del que se han borrado en múltiples ocasiones datos o bien se ha usado como almacenamiento temporal. Pongamos este caso: estás migrando tu base de datos desde una fuente externa. El proceso de importado usa mucho espacio temporal, aumentado el tamaño del disco pongamos a 400GB. Pero al final del proceso de importado, la base de datos solo ocupa 50GB. Sin embargo, una solución de thin provisioning tradicional reservará 400GB de disco, **pero no sabrá como &#8216;reducir&#8217; su tamaño hasta los 50GB reales al final del proceso de importado**. Ahí está la verdadera potencia de 3PAR. La tecnología &#8216;zero-detection&#8217; de 3PAR lo que hace es buscar los bloques en el disco que están a cero y los &#8216;recupera&#8217; y desprovisiona.

Cualquiera que sepa un poco de Sistemas Operativos podrá argumentarme que realmente cuando se borra un fichero no se ponen &#8216;a cero&#8217; donde se encontraba, sino que simplemente se elimina el puntero a ese grupo de sectores en el disco. Precisamente por eso y porque hay sistemas de ficheros que no &#8216;ponen a cero&#8217; (NTFS) 3PAR no es mágico, pero lo parece.

Por supuesto, estas no son las únicas ventajas de 3PAR [como bien me apuntan](http://twitter.com/vfernandezg/status/22886849329), pero es lo que la hace &#8216;diferente&#8217;. Los Proveedores de Servicios son especialmente sensibles al Coste Total de Propiedad de las soluciones de almacenamiento, y por eso por apuestan por 3PAR, como se puede ver en esta diapositiva supuestamente confidencial y que se puede encontrar buscando imágenes de 3PAR en Google:

<img class="aligncenter size-full wp-image-1294" title="3PAR_Penetration_into_CSPs" src="/wp-content/uploads/3PAR_Penetration_into_CSPs.jpg" alt="" width="480" height="360" srcset="/wp-content/uploads/3PAR_Penetration_into_CSPs.jpg 480w, /wp-content/uploads/3PAR_Penetration_into_CSPs-300x225.jpg 300w" sizes="(max-width: 480px) 100vw, 480px" />

&nbsp;
