---
author: Diego Parrilla
categories:
- estandares
- opensource
date: 2009-09-04T09:54:42Z
dsq_thread_id:
- "204694047"
guid: /?p=1065
id: 1065
tags:
- api
- deltacloud
- redhat
title: 'RedHat Deltacloud: una API para gobernar todas las nubes'
url: /2009/09/04/redhat-deltacloud-una-api-para-gobernar-todas-las-nubes/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="api,deltacloud,redhat" data-count="vertical" data-url="/2009/09/04/redhat-deltacloud-una-api-para-gobernar-todas-las-nubes/">Tweet</a>
</div>

En esta semana de locos que estamos viviendo, todos los proveedores intentan hacer sombra a larga lista de anuncios realizados en la VMWorld 2009, y RedHat no podía ser menos.

RedHat ha anunciado un nuevo proyecto llamado [Deltacloud](http://deltacloud.org/). Deltacloud es una librería y un pequeño portal con una API que permite gestionar nubes públicas de diferentes proveedores. Y según ellos, protege tus aplicaciones de cambios en el API cloud de tus proveedores debido a cambios e incompatiblidades. Segun ellos, permite gestionar EC2, RHEV-M; VMWare ESX y muy pronto RackSpace.

<img class="aligncenter size-full wp-image-1066" title="diagram-soa" src="/wp-content/uploads/diagram-soa.png" alt="diagram-soa" width="640" height="215" srcset="/wp-content/uploads/diagram-soa.png 640w, /wp-content/uploads/diagram-soa-300x100.png 300w" sizes="(max-width: 640px) 100vw, 640px" />

La verdad es que suena muy prometedor, pero al cabo de un rato te das cuenta que esto esta verde, pero que muy verde, y que además no enfrenta los verdaderos problemas de la interoperabilidad entre nubes públicas.

Para empezar, solo puedes levantar y parar máquinas virtuales. Es decir, todos los servicios asociados que puede necesitar una instancia para que realmente tenga valor no se soportan. Nada de asignación de IPs estáticas, montaje de volúmenes persistentes, zonas de seguridad&#8230; nada.

Además, las imágenes que se despliegan en cada proveedor son diferentes: es decir, **no hay un repositorio común**. Vamos que si quieres desplegar tu imagen en EC2 y luego en Rackspace, olvídate. Necesitas dos imágenes diferentes en dos formatos diferentes en dos repositorios diferentes.

Y eso es todo, no hay más. Nada de migración entre nubes, paso de imágenes virtuales X a Y. Nada. Encender y apagar una instancia. Y se acabó.

Se puede argumentar que es un proyecto en una fase muy semilla. Estoy de acuerdo y creo que evolucionará, pero hay una cosa que afirman que creo no es cierto, y además veo un problema de comprensión del concepto de arquitectura SOA: _&#8220;protege tus aplicaciones de cambios en el API cloud de tus proveedores debido a cambios e incompatiblidades&#8221;._ Y esto no es así, sino todo lo contrario.

Este producto básicamente es un [adaptador](http://en.wikipedia.org/wiki/Adapter_pattern). En Arquitectura Software el patrón adaptador se usa para traducir de un tipo de interfaz a otra. Es muy común en SOA porque es habitual dentro de las empresas encontrarte con este problema. Es un patrón eficaz en entornos donde se puede controlar el cambio de versiones de las interfaces a adaptar. Pero, ¿ocurre esto con un proveedor de una interfaz pública? Es decir, ¿informará VMware, Amazon, Rackspace y compañía a la gente de RedHat Deltacloud de que se producirá un cambio en la interfaz, y que deben liberar una nueva versión que la soporte? Puede que sí, pero probablemente no. Así que RedHat deberá liberar constantemente nuevas versiones que soporten estos cambios para que los clientes sigan teniendo disponibilidad en sus servicios. Ahora, cuantos más proveedores externos de Cloud incorporen, más difícil será mantener el ritmo de cambios. Además, entregar software empaquetado es siempre más lento que el software como servicio. Así que yo tendría mis dudas antes de lanzarme con este API a construir un servicio.
