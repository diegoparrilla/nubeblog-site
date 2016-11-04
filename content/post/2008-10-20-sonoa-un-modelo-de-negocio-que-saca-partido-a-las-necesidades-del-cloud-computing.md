---
author: Diego Parrilla
categories:
- cloud
date: 2008-10-20T10:07:11Z
dsq_thread_id:
- "204894383"
guid: /?p=130
id: 130
tags:
- esb
- sonoa
title: 'Sonoa: un modelo de negocio que saca partido a las necesidades del Cloud Computing'
url: /2008/10/20/sonoa-un-modelo-de-negocio-que-saca-partido-a-las-necesidades-del-cloud-computing/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="esb,sonoa" data-count="vertical" data-url="/2008/10/20/sonoa-un-modelo-de-negocio-que-saca-partido-a-las-necesidades-del-cloud-computing/">Tweet</a>
</div>

[<img class="alignright" title="Sonoa systems logo" src="http://www.sonoasystems.com/sites/all/themes/zen/sonoa/images/sonoa-logo.gif" alt="" width="160" height="90" />](http://www.sonoasystems.com/sites/all/themes/zen/sonoa/images/sonoa-logo.gif)Desde hace tiempo viendo dándole vueltas a qué modelos de negocio pueden surgir alrededor del Cloud Computing, y que no sean los ya conocidos relacionados con la Virtualización, Facturación, Provisión, etc&#8230; Dado que me ha tocado lidiar con la implantación de [Enterprise Services Bus (ESB)](http://en.wikipedia.org/wiki/Enterprise_service_bus) para la adopción de SOA dentro de alguna gran organización, la idea de que existiese un ESB específico para las necesidades del Cloud Computing me rondaba la cabeza.

Vía [TechcrunchIT](http://www.techcrunchit.com) descubro una compañía que no solo [ha tenido una idea similar, sino que además ha levantado 25 millones de dólares para llevarla a cabo](http://www.techcrunchit.com/2008/10/15/sonoa-appliance-knits-apis-and-cloud-together/). La empresa se llama [Sonoa Systems](http://www.sonoasystems.com/), y su propuesta puede sonar similar a la de un ESB clásico, aunque no lo es.Su producto ServiceNet Appliance permite añadir una capa extra virtual que permite:

  * gestionar el control de acceso a los recursos,
  * habilitar cierta interoperabilidad entre protocolos
  * monitoriza el rendimiento y disponibilidad de los servicios de cara a establecer y garantizar los Acuerdos de Nivel de Servicio
  * controlar de manera proactiva el acceso los servicios Web expuestos a los clientes.
  * forzar el uso de políticas de manera no intrusiva a los servicios
  * unificar en un único punto todas las políticas para reducir el trabajo de gestión
  * priorización de tráfico en función de los servicios demandados
  * ayudar a controlar el gasto realizado sobre servicios externos

Puede que este producto sólo sea un ESB al que le han puesto la etiqueta &#8216;Cloud&#8217; para tratar de venderlo mejor -todo lo que ofrecen lo tienen los ESBs mayoritarios-, pero esto me plantea varias cuestiones, y estoy seguro que son cuestiones que también tienen los clientes que se enchufan a la Nube.

Si quiero contratar uno o varios servicios en la nube&#8230;

  * ¿Cómo controlo yo que el SLA de mi proveedor se está cumpliendo?
  * ¿Cómo puedo restringir el uso de mi proveedor en la nube para no hacer gasto innecesario?
  * ¿Puedo evitar el &#8216;casarme&#8217; con el API de un proveedor?
  * ¿Cómo se yo que la información que está almacenando el proveedor está bien cuidada?

Y si quiero vender servicios en la nube, pues me surgen muchos más:

  * ¿Cómo puedo controlar el acceso de un cliente a un recurso o varios?
  * ¿Cómo integro el sistema de facturación elegido con mi sistema provisión?
  * ¿Cómo controlo el SLA de mis servicios de manera individualizada por cliente?
  * ¿Cómo puedo garantizar legalmente que mis métricas para el SLA son reales?
  * ¿Cómo realizo un control de cuota de grano fino por recurso y cliente?
  * &#8230;

Vamos, que creo que en la gestión de los servicios a alojar en La Nube puede haber hueco para el desarrollo de plataformas que resuelvan todos estos problemas.
