---
author: Diego Parrilla
categories:
- cloud
- seguridad
date: 2009-01-27T00:08:10Z
dsq_thread_id:
- "204693265"
guid: /?p=638
id: 638
tags:
- amazon
- edos
- securidad
title: 'Los riesgos del escalado automático: EDoS (Economic Denial of Sustainability)'
url: /2009/01/27/los-riesgos-del-escalado-automatico-edos-economic-denial-of-sustainability/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,edos,securidad" data-count="vertical" data-url="/2009/01/27/los-riesgos-del-escalado-automatico-edos-economic-denial-of-sustainability/">Tweet</a>
</div>

[<img class="aligncenter size-full wp-image-170" title="bankrupt" src="/wp-content/uploads/bankrupt.jpg" alt="" width="500" height="334" srcset="/wp-content/uploads/bankrupt.jpg 500w, /wp-content/uploads/bankrupt-300x200.jpg 300w" sizes="(max-width: 500px) 100vw, 500px" />](/wp-content/uploads/bankrupt.jpg)

Hace unos meses leí un artículo (que no he podido encontrar) sobre un pobre tipo que había montado una startup y utilizaba Amazon S3 para servir contenido estático. Todo le iba de maravilla hasta que un mes le llegó una factura absolutamente descomunal por el servicio. Tan grande era que tuvo que cerrar el sitio. Investigando qué había pasado, descubrió que alguien se había dedicado a hacer peticiones a sus ficheros alojados en S3 de manera continuada y masiva, sin hacer uso real de su servicio. El resultado fue que Amazon sirvió el contenido solicitado, aunque esas peticiones fueran falsas y maliciosas.

Exactamente esto es un [ataque de tipo EDoS](http://rationalsecurity.typepad.com/blog/2009/01/a-couple-of-followups-on-my-edos-economic-denial-of-sustainability-concept.html) (Economic Denial of Sustainibility). En un ataque tipo DDoS (Distributed Denial of Service), un tio con muy mala leche ataca una aplicación o una web cualquiera con la intención de colapsarla, lanzando peticiones desde múltiples computadoras de manera concurrente y masiva. Al final, el servicio cae ya que no es capaz de copar todas las peticiones solicitadas. El EDoS es una manera más sutil de tirar el servicio abajo. Su objetivo no es la caida física de los servidores que soportan el servicio, sino la rendición de los propietarios del servicio al no poder hacer frente las facturas de uso de los recursos en La Nube.

El ataque DDoS asume que un servicio puede escalar hasta un límite fijo. Este límite lo marca la cantidad de hardware instalado y la capacidad del software para aprovecharlo. En cambio, en el Cloud Computing este límite es variable si el software es capaz de aprovecharlo de manera dinámica. Es el tan famoso escalado dinámico. Un Controlador/Agente implementa un conjunto de políticas que permite solicitar a La Nube más recursos en caso de ser necesarios, o de liberarlos si ya no lo son. En teoría (y en la práctica también) esto permite optimizar el gasto en infraestructura. El ataque EDoS aprovecha la facilidad para escalar de manera dinámica para pedir de manera alocada más y más recursos a La Nube. El servicio sigue funcionando sin que nadie se de cuenta de lo que pasa, pero la factura por el uso de recursos sube y sube hasta que se hace evidente y es cuando se toman medidas, ya tarde.

[En una arquitectura Cloud es necesario este Controlador o Agente](/2009/01/14/seran-los-humanos-irrelevantes-monitorizando-aplicaciones-cloud/) que gestione el escalado dinámico, pero no hay que olvidarse de políticas que limiten el uso de recursos para evitar abusos de este tipo. Es decir, no solo indicar cuando debe escalar con más o menos recursos, sino limitar el gasto máximo de los recursos para evitar desagradables sorpresas. Es decir, [no delegar todo en el escalado dinámico, sino realizar una Planificación de la Capacidad (Capacity Planning)](http://broadcast.oreilly.com/2008/12/why-i-dont-like-cloud-auto-scaling.html) en la que introduzcamos como variables el límite de consumo en La Nube.
