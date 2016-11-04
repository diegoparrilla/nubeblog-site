---
author: Diego Parrilla
categories:
- cloud
date: 2008-11-01T00:18:25Z
dsq_thread_id:
- "238862305"
guid: /?p=218
id: 218
tags:
- azure
title: 'Windows Azure: qué es real y qué es vapor'
url: /2008/11/01/windows-azure-que-es-real-y-que-es-vapor/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="azure" data-count="vertical" data-url="/2008/11/01/windows-azure-que-es-real-y-que-es-vapor/">Tweet</a>
</div>

[<img class="aligncenter size-full wp-image-200" title="windowsazure" src="/wp-content/uploads/windowsazure.jpg" alt="" width="244" height="145" />](/wp-content/uploads/windowsazure.jpg)Parece que Microsoft ha inventado el Cloud Computing. Esta semana [todo el mundo se ha dedicado a hablar de &#8216;La Nube&#8217;](http://www.publico.es/ciencias/169577/apuntan/cloud/computing). Hay que reconocer que una vez más, Microsoft ha sabido mover su enorme maquinaria de marketing. Por cierto, hace unos años me comentaron que el porcentaje que Microsoft invertía en publicidad era igual porcentaje que BEA Systems invertía en I+D, y viceversa. Igual no es cierto, pero da que pensar.

Lo cierto es que la visión de alto nivel del producto no creo que sea buena: es perfecta. Todas las herramientas necesarias para construir aplicaciones en La Nube perfectamente integradas (¿y acopladas?) para dar gustazo a los desarrolladores y productividad a los directores de los departamentos de IT.

Demasiado bueno para ser verdad&#8230;

Los que llevamos un tiempo en esto sabemos que Microsoft lo hace así: vende humo, tu lo compras, y luego esperas a que el producto madure&#8230; o bien te pasas a otras tecnologías harto de que te vendan la moto una y otra vez.La sensación que hay en La Red es que [Microsoft vuelve a las andadas](http://www.informationweek.com/blog/main/archives/2008/10/is_the_cloud_th.html). Se ha dado prisa en ofrecer algo para no perder comba. **[Es decir, Windows Azure está a medio hacer](http://news.cnet.com/8301-13860_3-10076588-56.html)** ¿Pero qué es exactamente Windows Azure?

Windows Azure es el nombre comercial de un proyecto llamado [&#8216;Red Dog&#8217;](http://www.liveside.net/main/archive/2008/04/09/red-dog-ray-ozzie-s-answer-to-the-google-app-engine.aspx). Es un sistema operativo diseñado por un equipo de expertos en SSOO liderado por [Amitabh Srivastava](http://www.microsoft.com/presspass/exec/srivastava/default.aspx). En este equipo está [Dave Cutler](http://en.wikipedia.org/wiki/Dave_Cutler_(software_engineer)), padre de VMS y de Windows NT liderando equipos de desarrollo centrados en las tecnologías de virtualización. Por cierto, Microsoft no está usando su tecnología de virtualización <a href="http://en.wikipedia.org/wiki/Hyper-V" target="_blank">Hyper-V</a> de Windows Server. Se ha desarrollado un hypervisor completamente nuevo que está pensado para un entorno de Datacenter completamente heterogéneo.

Azure ha sido diseñado desde el principio para que sea simple, rápido y modular. Por eso, Windows Azure sólo es el núcleo de la suite de Servicios de Microsoft Azure. Los desarrolladores interactuarán con los servicios de manera directa, y no con Windows Azure. Podrán elegir que conjunto de servicios desean usar para sus aplicaciones.

Red Dog está compuesto de cuatro pilares:

  * Almacenamiento: El sistema de ficheros en La Nube. No tengo claro si se refieren a un sistema de ficheros estándar o bien algo tipo S3.
  * Fabric Controller: Sistema de gestión para modelar, desplegar y provisionar.
  * Virtualización
  * Entorno de desarrollo accesible desde los entornos de escritorio.

Por debajo de Windows Azure y entre él y el hardware se encuentra el Global Foundational Services. Al parecer GFS es como el HAL (Hardware Abstraction Layer) de Windows. No hay mucha información al respecto.

Sobre los diversos servicios que se ofrecen [ya he hablado en otro post](/2008/10/29/microsoft-azure-services-platform-la-apuesta-paas-de-microsoft/), pero la pregunta que nos hacemos todos es ¿qué tipo de código podemos ejecutar en La Nube?

Azure nos permite ejecutar código gestionado (managed code) .NET. Han dicho que se puede ejecutar ASP.NET, que podrán correrse procesos batch (esto es una diferencia importante con Google AppEngine) y al parecer los ejemplo usaban LINQ como método de acceso a datos. Se ha dejado claro que por ahora no se podrá ejecutar código nativo, lo cual hasta cierto punto es natural.

Lo que por ahora nadie sabe son las limitaciones que puede tener el entorno. Por su similitud con Google AppEngine podemos presumir que estos puntos serán críticos:

  * Tiempos máximos por petición
  * Tamaños de ficheros
  * Hilos
  * TCP-UDP/IP capado
  * APIs &#8216;capadas&#8217; para su uso en La Nube
  * &#8230;

Para terminar una reflexión. En los últimos años, Microsoft perdió la guerra de los sitios web. La guerra del navegador la está perdiendo lentamente. Vista ha sido un fiasco. Durante un tiempo fueron el &#8216;Imperio malvado&#8217; que quería destruir Java y el software libre, pero ahora simplemente los desarrolladores los ignoran&#8230; Lo único que le ha funcionado bien ha sido la Xbox gracias a lo mal que lo ha hecho Sony. Creo que esta puede ser su última oportunidad para reinventarse como empresa. Así que pondrán todo en el asador.
