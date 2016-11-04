---
author: Diego Parrilla
categories:
- cloud
- grid
date: 2008-10-09T10:31:19Z
dsq_thread_id:
- "205483423"
guid: /?p=72
id: 72
tags:
- gigaspaces
- gogrid
- grid
title: Gigaspaces y GoGrid lanzan un servicio de Cloud Computing de nivel Empresarial
url: /2008/10/09/gigaspaces-y-gogrid-lanzan-un-servicio-de-cloud-computing-de-nivel-empresarial/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="gigaspaces,gogrid,grid" data-count="vertical" data-url="/2008/10/09/gigaspaces-y-gogrid-lanzan-un-servicio-de-cloud-computing-de-nivel-empresarial/">Tweet</a>
</div>

<img class="alignright" title="GoGrid logo" src="http://www.gogrid.com/images/logo.gif" alt="" width="202" height="44" /><img class="alignright size-medium wp-image-73" title="gigaspaces_logo" src="/wp-content/uploads/gigaspaces_logo.gif" alt="" width="210" height="59" srcset="/wp-content/uploads/gigaspaces_logo.gif 480w, /wp-content/uploads/gigaspaces_logo-300x85.gif 300w" sizes="(max-width: 210px) 100vw, 210px" />No todo el Cloud Computing va a ser Amazon Web Services. Existen otras propuestas interesantes, y creo [GoGrid](http://www.gogrid.com) es una de las que parece más profesional. Por poner un ejemplo, ofrecen balanceadores F5 dentro de su infraestructura, lo que en mi opinión es fundamental para poner en marcha tolerante a fallos. También el servicio de monitorización y soporte 24&#215;7 es algo fundamental a la hora de establecer los niveles de servicio. 

Y dentro del mundo de las empresas de software que desarrollan software de infraestructura para el Cloud Computing uno de mis favoritos es [GigaSpaces](http://www.gigaspaces.com). Su producto [eXtreme Application Platform (XAP)](http://www.gigaspaces.com/xap) es una de las soluciones de Grid Computing para empresas que más implantación tiene. Simplificando su propuesta, ellos plantean que el modelo de separación de capas clásico propuesto en arquitecturas empresariales de presentación-negocio-datos no es válido si quieres implementar soluciones de alto rendimiento y altamente escalables. Ellos plantean otra arquitectura en la que cada nodo es autocontenido y por lo tanto escalar es sencillo ya que simplemente hay que añadir más nodos. Resumiendo, computación distribuida y Grid de datos de nivel empresarial. Por cierto que se basa en un standar Java muy olvidado como es [JavaSpaces](http://java.sun.com/developer/technicalArticles/tools/JavaSpaces/).

En esta [nota de prensa](http://www.earthtimes.org/articles/show/gigaspaces-and-gogrid-launch-enterprise-grade-cloud-computing-solution,567646.shtml) anuncian que han unido sus fuerzas para ofrecer el &#8216;Santo Grial de las TI&#8217;: Si hay un pico de demanda importante, la combinación de ambas propuestas te permitirá soportarlo. Se me ocurren varios casos en los que puede ser interesante el uso de este tipo de soluciones elásticas, pero por ejemplo aquellos que necesiten realizar operaciones de liquidación y conciliación al cierre de un mercado o en fechas muy señaladas y con slots de tiempo muy reducidos que pueden beneficiarse de este tipo de soluciones. Tu sistema funciona unas pocas horas pero necesitas muchos ciclos de CPU para hacerlo. Si el mercado ha estado loco ese día y hay mucho volumen, pues más nodos del Cloud, que es Agosto y no hay moviento, pues solo contratas lo imprescindible.

¿Qué se os ocurre a vosotros?
