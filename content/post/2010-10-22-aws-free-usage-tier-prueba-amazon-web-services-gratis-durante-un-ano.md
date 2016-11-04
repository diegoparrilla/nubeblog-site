---
author: Diego Parrilla
categories:
- amazon
date: 2010-10-22T11:18:21Z
dsq_thread_id:
- "204723869"
guid: /?p=1797
id: 1797
tags:
- aws
- free usage tier
- marketing
title: AWS Free Usage Tier, prueba Amazon Web Services gratis durante un año
url: /2010/10/22/aws-free-usage-tier-prueba-amazon-web-services-gratis-durante-un-ano/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="aws,free+usage+tier,marketing" data-count="vertical" data-url="/2010/10/22/aws-free-usage-tier-prueba-amazon-web-services-gratis-durante-un-ano/">Tweet</a>
</div>

[<img class="size-full wp-image-121 alignright" title="logo_aws" src="/wp-content/uploads/logo_aws.gif" alt="" width="164" height="60" />](/wp-content/uploads/logo_aws.gif)

Menudo revuelo que ha causado la nueva estrategia de marketing de [Amazon Web Services](http://aws.amazon.com). Sí, he escrito bien: Marketing. Ayer anunció un &#8216;menú degustación&#8217; de sus servicios en la nube llamado [AWS Free Usage Tier](http://aws.amazon.com/free/) durante un año.

En un cambio de política por sorpresa (y tal vez sorprendente), Amazon ofrece los nuevos clientes creados a partir del 20 de octubre de 2010 la posibilidad de usar uno conjunto de recursos de manera gratuita. Los recursos se pueden empezar a consumir a partir del 1 de Noviembre e 2010, y tendrán una duración máxima de un año.

Los recursos gratuitos ofrecidos para los nuevos clientes son los siguientes:

  * 750 horas de una Micro instancia Linux de 32 y 64 bits ([hablé sobre ella en el blog](/2010/09/13/amazon-anuncia-nuevas-instancias-desde-7-al-mes/)).
  * 750 horas de Elastic Load Balancer además de 15G de datos. Es el balanceador de carga de su nube.
  * 10G de Elastic Block Storage, incluyendo 1 millon de IOs, 1G de espacio para snapshots y 10.000 peticiones GET y 1000 peticiones PUT. Un disco persistente de 10GB (poca cosa) y solo 1G para snapshots (vamos, nada&#8230;). Sobre el millon de IOs, un MySQL se lo ceptilla relativamente rápido.
  * 5GB de almacenamiento en S3 con 20.000 peticiones GET y 2000 peticiones PUT.
  * 30GB de transferencia de datos desde y hacia internet en todos los servicios.

Y para los nuevos y antiguos, tenemos los siguientes:

  * 25 horas de uso de Amazon SimpleDB y 1GB de Almacenamiento. Parece poco, pero no lo es.
  * 100.000 peticiones a Simple Queue Service.
  * 100.000 peticiones, 100.000 notificaciones HTTP y 1000 emails para el servicio de Simple Notification Service.

Hay que destacar que en el alta del servicio se debe registrar una tarjeta de crédito, y en caso de superar los límites de la banda freemium o que pase el año de validez del contrato empezarán a facturar mensualmente por el servicio. La oferta no tiene fecha de terminación, y será a discreción del proveedor. El servicio se ofrece en todas las regiones AWS.

Resulta curioso  que una empresa que ha destacado por no hacer ningún tipo de marketing empiece ahora a hacerlo. Todo el foco de AWS iba encaminado a &#8216;evangelizar&#8217; sobre su producto mediante un grupo muy bueno de profesionales que mostraban las virtudes del producto. Lo que me pregunto es qué parte de culpa tiene en este nuevo modelo la necesidad de captar nuevos clientes, o la necesidad de ofrecer una cuenta tipo &#8216;menú degustación&#8217; más barata todavía para desarrolladores. Y me explico: como desarrollador que ha usado desde el principio Amazon Web Services te das cuenta muy pronto que el coste de mantener un entorno de pruebas en su nube es realmente barato y la mayoría de las veces muy por debajo de los $100 mensuales. Hablo de desarrollo. Si este coste es asumible para un desarrollador o micro-startup, para una empresa más todavía. Entonces, ¿a qué viene subvencionar mediante una acción de marketing precisamente ese segmento del mercado?

Puede que haya varias razones&#8230; Tal vez han llegado ya a una &#8216;meseta de crecimiento&#8217;, a una resistencia en el crecimiento de clientes que no pueden romper. Yo sigo insistiendo que el modelo de Cloud es igual que el de las operadoras de telefonía: para romper esas resistencias ellas te subvencionan el terminal para que te cambies. O bien la razón es tratar de ganar la mayor cuota de mercado posible ahora que empiezan a surgir alternativas reales a la hegemonía de Amazon. Amazon Web Services es un servicio que puede llegar a ser terriblemente cautivo. Estoy seguro que su &#8216;[churn rate](http://en.wikipedia.org/wiki/Churn_rate)&#8216; es bajísimo y quieren asegurarse que así sea.

Algo de lo que no se suele hablar es que la posibilidad de portar e interoperar servicios cloud construidos sobre Amazon a otro proveedor Cloud es a día de hoy prácticamente inexistente. Pero las [nuevas iniciativas que están surgiendo sobre las Cloud utilities puras](http://openstack.org/) van a facilitar la portabilidad. Tampoco se dice de estas plataformas que conocemos el coste de entrada, pero existe un coste oculto de salida. Los nuevos estándares y las nuevas plataformas de otros proveedores harán que caiga ese coste oculto de salida, pero no desaparecerá. Volviendo a las operadoras, la manera de &#8216;forzar&#8217; al cliente para que cambie de proveedor es subvencionándolo, es decir, pagando ese coste de salida. Amazon está &#8216;ensayando&#8217; este modelo, sin duda.
