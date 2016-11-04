---
author: Diego Parrilla
categories:
- cloud
- opensource
date: 2009-01-21T10:01:03Z
dsq_thread_id:
- "204693224"
guid: /?p=603
id: 603
tags:
- api
- gogrid
- opensource
title: GoGrid libera su API de gestión bajo licencia Creative Commons
url: /2009/01/21/gogrid-libera-api-gestion-licencia-creative-commons/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="api,gogrid,opensource" data-count="vertical" data-url="/2009/01/21/gogrid-libera-api-gestion-licencia-creative-commons/">Tweet</a>
</div>

[<img class="aligncenter size-full wp-image-604" title="gogridlogo" src="/wp-content/uploads/gogridlogo.gif" alt="" width="288" height="63" />](/wp-content/uploads/gogridlogo.gif)

[GoGrid](http://www.gogrid.com) es una empresa que ofrece [Infraestructura Como Servicios (IaaS)](/2008/10/15/saas-iaas-y-paas-las-tres-clases-de-cloud-computing/) de manera similar a como hace [Amazon Web Services](http://aws.amazon.com/). Parece que querían eclipsar a Obama en la ceremonia de envestidura anunciando que [liberan la especificación del API de gestión de su CloudCenter](http://blog.gogrid.com/2009/01/20/gogrid-releases-api-specification-to-the-cloud-computing-community-under-creative-commons-license/), la especificación **_GoGrid cloudcenter Application Programming Interface (API)_** bajo una licencia **Creative Common**s. Esto permitirá a desarrolladores, integradores y demás profesionales IT copiar, modificar, distribuir y republicar este API libremente.

Las restricciones de la licencia [**The Creative Commons Attribution Share Alike 3.0**](http://creativecommons.org/licenses/by-sa/3.0/us/), permite lo siguiente:

  * Compartir, distribuir, mostrar y ejecutar la obra
  * Hacer obras derivadas

Y debe cumplir las siguientes condiciones:

  * Debe haber un reconocimiento completo a GoGrid, al autor y al licenciante.
  * No hay ningún respaldo de GoGrid sobre ninguna de las obras derivadas del uso del API o su re-elaboración.
  * Después de cualquier transformación, alteración o creación sobre esta obra, cualquier distribución debe estar bajo la misma licencia, una compatible o similar.
  * Hay que dejar claro a terceros los términos de esta licencia. Lo mejor es enlazar a la Wiki de GoGrid sobre el API: <http://wiki.gogrid.com/wiki/index.php/API>
  * Cualquiera de estas condiciones pueden no ser exigibles con el permiso de GoGrid.

Si echamos un vistazo al API en su [wiki](http://wiki.gogrid.com/wiki/index.php/API) podemos ver que se trata de un API potente, ya que cubre los siguientes puntos:

  * Balanceo de Carga
  * Gestión de Servidores
  * Gestión de imágenes virtuales de servidores
  * Gestión de Red (IPs)
  * Seguridad (passwords)
  * Facturación

Es decir, casi la gestión completa de un Datacenter privado -o CloudCenter- como lo llaman ellos.

Veremos si consiguen que esta especificación abierta triunfe y otros proveedores de Cloud la tomen como referencia para otras implementaciones de Clouds privados -o públicos, ¿por qué no?- en el futuro. Los usuarios finales se beneficiarán por el aumento de la competencia, y aparecerá un ecosistema de empresas alrededor de estas nuevas Nubes que vivan de la competencia entre ellas, y no de [las decisiones que tomen otros](/2009/01/12/nueva-consola-de-gestion-de-amazon-ec2-la-dificil-tarea-de-sobrevivir-en-el-ecosistema-aws/).
