---
author: Diego Parrilla
categories:
- amazon
- arquitectura
- cloud
date: 2010-10-28T09:32:33Z
dsq_thread_id:
- "204895159"
guid: /?p=1804
id: 1804
tags:
- arquitectura
- caso de exito
- imagenio
- netflix
title: 'El caso de éxito de Netflix: cómo una gran corporación migra a la Nube Pública'
url: /2010/10/28/el-caso-de-exito-de-netflix-como-una-gran-corporacion-migra-a-la-nube-publica/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="arquitectura,caso+de+exito,imagenio,netflix" data-count="vertical" data-url="/2010/10/28/el-caso-de-exito-de-netflix-como-una-gran-corporacion-migra-a-la-nube-publica/">Tweet</a>
</div>

[<img class="alignright size-full wp-image-1807" title="netflix-logo" src="/wp-content/uploads/netflix-logo.jpg" alt="" width="315" height="140" srcset="/wp-content/uploads/netflix-logo.jpg 450w, /wp-content/uploads/netflix-logo-300x133.jpg 300w" sizes="(max-width: 315px) 100vw, 315px" />](/wp-content/uploads/netflix-logo.jpg)[Netflix](http://www.netflix.com/) es una empresa que nació prestando DVDs por correo ordinario, y [ha evolucionado hacia los servicios de streaming](http://www.todotvnews.com/scripts/templates/estilo_nota.asp?tipo=ultima%20semana&nota=nuevo/Newmedia/Web%20TV/2010/10_octubre/22_Netflix_convierte_streaming&idioma=). Hoy presume de tener 15 millones de subscriptores offline y online en los EEUU y Canadá. Por decirlo de alguna manera, es similar lo que sería [Imagenio](www.imageniotelevision.com) en España en la parte de alquiler de contenidos, pero sin nada que ver con el servicio de Internet. La diferencia es que puede servir contenidos a un conjunto bastante importante de dispositivos: TiVo, AppleTV, PlayStation 3, Wii y XBox entre otros.

Para entender la dimensión de Netflix, unas estadísticas recientes de tráfico de internet en los EEUU nos indican que [el 20% del tráfico de bajada (desde los proveedores al cliente final) lo consumen los protocolos de Netflix](http://seekingalpha.com/article/231480-netflix-s-bandwidth-squeeze). Únicamente todo el protocolo HTTP junto en los EEUU es capaz de superar al tráfico de bajada de Netflix. Bestial.

Netflix es un caso claro de cómo una [gran corporación](http://www.google.com/finance?q=NASDAQ:NFLX) puede delegar sus servicios &#8216;core&#8217; a una Nube Pública. Netflix decidió que no quería ni tener ni operar sus centros de datos. No es su negocio. Además, los usuarios hacen uso de sus servicios de modo estacionario: grandes picos en las horas de mayor consumo televisivo y cuando se producen grandes lanzamientos. Por eso empezó a mover sus servicios a Amazon Web Services en 2009, y está completando la migración a lo largo de este 2010.

En esta magnífica presentación Adrian Cockcroft, Cloud Architect en Netflix explica cómo han &#8216;reconstruido&#8217; los servicios de Netflix sobre la Nube de Amazon y los CDNs de Akamai para soportar la tremenda carga que necesitan. La conferencia dura una hora, es en inglés y el nivel del auditorio está a la altura del ponente.



Lo que más me ha llamado la atención es cómo han adaptado sus servicios a las características de Amazon Web Services, aprovechando todo el conjunto de servicios que tienen. Es decir, a ellos les vale la pena &#8216;atarse&#8217; a Amazon porque los beneficios que reciben les compensa. Migraron de Oracle a SimpleDB, por ejemplo. Uno de los asistentes le pregunta si es cierto que la Nube es barata para las empresas pequeñas, pero es cara para las grandes. Es decir, una gran corporación tiene la capacidad financiera para afrontar un gran proyecto de construcción de un centro de datos, por lo que a largo plazo el Centro de Datos es un activo de la empresa. Sin embargo, Neflix decició no construir Centros de Datos, ellos invierten todo el dinero en licenciar las películas que alquilan, no en IT.

También asumen que muchas de sus necesidades no las puede cubrir Amazon Web Services, por lo que deben implementar sus propios servicios de infraestructura (Balanceo en middle-tier, Encritpación y Caching), así como desplegar en sus propios Centros de Datos el procesamiento de pagos online. El streaming principal lo delegan a CDNs de Akamai (dice que son uno de sus mayores clientes).

Un caso de éxito potente, sin duda alguna. Que la disfrutéis.
