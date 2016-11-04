---
author: Diego Parrilla
categories:
- cloud
- grid
date: 2008-12-23T09:44:19Z
dsq_thread_id:
- "204693054"
guid: /?p=486
id: 486
tags:
- grid
title: Un ejemplo de Cloud-as-a-Feature con GigaSpaces XAP
url: /2008/12/23/un-ejemplo-de-cloud-as-a-feature-con-gigaspaces-xap/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="grid" data-count="vertical" data-url="/2008/12/23/un-ejemplo-de-cloud-as-a-feature-con-gigaspaces-xap/">Tweet</a>
</div>

[<img class="aligncenter size-full wp-image-73" title="gigaspaces_logo" src="/wp-content/uploads/gigaspaces_logo.gif" alt="" width="480" height="137" srcset="/wp-content/uploads/gigaspaces_logo.gif 480w, /wp-content/uploads/gigaspaces_logo-300x85.gif 300w" sizes="(max-width: 480px) 100vw, 480px" />](/wp-content/uploads/gigaspaces_logo.gif)

[Cloud-as-a-Feature (CaaF)](http://www.roughtype.com/archives/2008/11/the_cloud_as_a.php) es el último palabro que ha nacido del Cloud Computing. El padre de la criatura es [Nicholas Carr (el de Big Switch)](/2008/11/04/the-big-switch-de-nicholas-carr-el-libro-de-cabecera-del-cloud-computing/) y según él significa la _mezcla del software tradicional que corre en un PC con software que corre en La Nube_. Un ejemplo muy claro de CaaF sería Google Earth, donde la aplicación visualiza la información en un PC, pero todo el procesado se hace en los servidores de Google.

[Gigaspaces XAP](http://www.gigaspaces.com/xap) es un producto creado por una compañía Israelí [del mismo nombre](http://www.gigaspaces.com) que sigue dentro del mundo Java un paradigma diferente al archiconocido J2EE (o JEE como se llama ahora). Plantean que el modelo de separación de capas clásico propuesto en arquitecturas empresariales de presentación-negocio-datos no es válido si quieres implementar soluciones de alto rendimiento y altamente escalables. Ellos plantean otra arquitectura en la que cada nodo es autocontenido y por lo tanto escalar es sencillo ya que simplemente hay que añadir más nodos. Resumiendo, computación distribuida y Grid de datos de nivel empresarial. Por cierto que se basa en un standar Java muy olvidado: <a onclick="javascript:pageTracker._trackPageview ('/outbound/java.sun.com');" href="http://java.sun.com/developer/technicalArticles/tools/JavaSpaces/">JavaSpaces</a>.

[Nati Shalom](http://natishalom.typepad.com/about.html) (CTO de Gigaspaces) [nos muestra en su blog otro ejemplo de Cloud-as-a-Feature para el mundo financiero](http://natishalom.typepad.com/nati_shaloms_blog/2008/12/risk-analysis-as-a-service-using-excel-and-gigaspaces.html) y especialmente para el cálculo y análisis de riesgos. En el ejemplo que muestra en el blog, ellos introducen directamente la información en una hoja Excel (el frontal), y la información se pasa a los nodos que corren la aplicación sobre GigaSpaces XAP.Net (el backend), que realiza los cálculos necesarios en una Nube de nodos que corren GigaSpaces.

Probablemente alguno me podrá decir que esto mismo ya se hace en muchos proveedores de servicios financieros, pero él sugiere que la verdadera potencia de esta solución es la posibilidad de delegar a Nubes públicas o privadas este servicio, y cobrar por él mediante un modelo de pago por uso. Además -y esta es una característica que debería tener una solución CaaF- si los usuarios pueden seguir usando su herramienta favorita -Excel- y no tienen que migrar a una aplicación cliente que no les da la flexibilidad de la hoja de cálculo, las posibilidades de adopción de estas soluciones serán mayores.

La verdad es que el post lo acabé en el párrafo anterior, pero pensando en la características sistémicas del Cloud-as-a-Feature, veo que una de las más importantes es el uso de un estilo arquitectónico orientado a servicios (SOA, vamos). Y me pregunto si el Cloud Computing ha explotado por la adopción de este estilo de desarrollar servicios, o es una casualidad. Ya sea casual o causal, lo que veo claro es que las arquitecturas SOA ayudan a mover servicios a La Nube. Creo que ahora mismo convergen muchas ideas y propuestas tecnológicas. Da la sensación de que nos encontramos en el paso anterior a una gran &#8216;toma de concencia&#8217;, es decir, una revolución tecnológica. Es como cuando estabas estudiando Física, Algebra o Cálculo y no entendías nada&#8230; pero de repente las piezas encajan y todo pasa a tener sentido.

Demasiado denso para estas fechas, ¿no?
