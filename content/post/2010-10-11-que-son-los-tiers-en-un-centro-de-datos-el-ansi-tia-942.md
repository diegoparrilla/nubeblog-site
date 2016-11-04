---
author: Diego Parrilla
categories:
- arquitectura
- datacenter
date: 2010-10-11T10:13:11Z
dsq_thread_id:
- "204895105"
guid: /?p=1756
id: 1756
tags:
- arquitectura
- tier
- uptime institute
title: Qué son los &#8216;tiers&#8217; en un Centro de Datos. El ANSI/TIA-942
url: /2010/10/11/que-son-los-tiers-en-un-centro-de-datos-el-ansi-tia-942/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="arquitectura,tier,uptime+institute" data-count="vertical" data-url="/2010/10/11/que-son-los-tiers-en-un-centro-de-datos-el-ansi-tia-942/">Tweet</a>
</div>

[<img class="alignright size-medium wp-image-811" title="abiquomarenostrum3-1024" src="/wp-content/uploads/abiquomarenostrum3-1024-191x300.jpg" alt="" width="191" height="300" srcset="/wp-content/uploads/abiquomarenostrum3-1024-191x300.jpg 191w, /wp-content/uploads/abiquomarenostrum3-1024-653x1024.jpg 653w, /wp-content/uploads/abiquomarenostrum3-1024.jpg 1024w" sizes="(max-width: 191px) 100vw, 191px" />](/wp-content/uploads/abiquomarenostrum3-1024.jpg)Si estás buscando un servicio de alojamiento de servidores, colocación, etc. verás que los diferentes proveedores te ofrecen información de lo más variada sobre sus características y te ofrecen datos interesantes como niveles de redundancia, tamaño del centro de datos, tiempos de respuesta y demás.

Existe un estándar llamado [ANSI/TIA-942 Telecommunications Infrastructure Standard for Data Centers](http://www.tiaonline.org), creado por miembros de la industria, consultores y usuarios, que intenta estandarizar el proceso de diseño de los centros de datos. El estándar está orientado a ingenieros y expertos en la materia. Sin embargo, hay una parte del estándar que vale la pena conocer cuando contratamos servicios de alojamiento en un centro de datos: **Los _Tiers_.** Este sistema de clasificación fue inventado por el [Uptime Institute](http://professionalservices.uptimeinstitute.com/tier_class.htm) para clasificar la fiabilidad (y también para hacer negocio certificando los centros de datos, claro está).

El concepto de _Tier_ nos indica el nivel de fiabilidad de un centro de datos asociados a cuatro niveles de disponibilidad definidos. A mayor número en el _Tier_, mayor disponibilidad, y por lo tanto mayores costes asociados en su construcción y más tiempo para hacerlo. A día de hoy se han definido cuatro _Tier_ diferentes, y ordenados de menor a mayor son:

**Tier 1: Centro de datos Básico: Disponibilidad del 99.671%**.

  * El servicio puede interrumpirse por actividades planeadas o no planeadas.
  * No hay componentes redundantes en la distribución eléctrica y de refrigeración.
  * Puede o no puede tener suelos elevados, generadores auxiliares o UPS.
  * Tiempo medio de implementación, 3 meses.
  * La infraestructura del datacenter deberá estar fuera de servicio al menos una vez al año por razones de mantenimiento y/o reparaciones.

**Tier 2: Centro de datos Redundante: Disponibilidad del 99.741%.**

  * Menos susceptible a interrupciones por actividades planeadas o no planeadas.
  * Componentes redundantes (N+1)
  * Tiene suelos elevados, generadores auxiliares o UPS.
  * Conectados a una única línea de distribución eléctrica y de refrigeración.
  * De 3 a 6 meses para implementar.
  * El mantenimiento de esta línea de distribución o de otras partes de la infraestructura requiere una interrupción de las servicio.

**Tier 3: Centro de datos Concurrentemente Mantenibles: Disponibilidad del 99.982%.**

  * Permite planificar actividades de mantenimiento sin afectar al servicio de computación, pero eventos no planeados pueden causar paradas no planificadas.
  * Componentes redundantes (N+1)
  * Conectados  múltiples líneas de distribución eléctrica y de refrigeración, pero únicamente con una activa.
  * De 15 a 20 meses para implementar.
  * Hay suficiente capacidad y distribución para poder llevar a cabo tareas de mantenimiento en una línea mientras se da servicio por otras.

**Tier 4: Centro de datos Tolerante a fallos: Disponibilidad del 99.995%.**

  * Permite planificar actividades de mantenimiento sin afectar al servicio de computación críticos, y es capaz de soportar por lo menos un evento no planificado del tipo &#8216;peor escenario&#8217; sin impacto crítico en la carga.
  * Conectados múltiples líneas de distribución eléctrica y de refrigeración con múltiples componentes redundantes (2 (N+1) significa 2 UPS con redundancia N+1).
  * De 15 a 20 meses para implementar.

Por ejemplo, si en la publicidad de un proveedor presume de ser _Tier_ 3, lo que nos está diciendo es que su infraestructura no fallará más de 1.6 horas al año, que no hay interrupciones por mantenimientos planificados y que puede haber eventos inesperados que causen interrupciones del servicio. Hay que recalcar que se refiere a la infraestructura del centro de datos, y que otros aspectos como la disponibilidad de los equipos que van dentro del datacenter se gestionan aparte.

Claro está, es lo que dicen en la publicidad. Ahora, ¿podemos exigir en nuestro SLA un _Tier_ determinado? Pues me temo que la cosa no es tan sencilla, ya que el uso de los _Tiers_ se está usando para publicitar capacidades sin que haya una certificación oficial de ello en la mayoría de los casos. De hecho, el Uptime Institute solo [ha certificado unos cuantos Centros de Datos en todo el mundo en los niveles 3 y 4](http://professionalservices.uptimeinstitute.com/tiercert.htm). Por cierto ninguno en España. Así que dudo que un proveedor pueda o quiera realmente garantizar un _Tier_ determinado por contrato. Además, muchos consideran [inflexible esta clasificación](http://searchdatacenter.techtarget.com/news/1348626/Is-Uptime-Institutes-data-center-tier-system-worth-it) por ser demasiado cerrada.
