---
author: Diego Parrilla
categories:
- amazon
date: 2009-08-26T08:02:18Z
dsq_thread_id:
- "204693784"
guid: /?p=1024
id: 1024
tags:
- amazon
title: Amazon anuncia su Virtual Private Cloud, o como decir Privada cuando debería
  decir Pública
url: /2009/08/26/amazon-anuncia-su-virtual-private-cloud-o-como-decir-privada-cuando-deberia-decir-publica/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon" data-count="vertical" data-url="/2009/08/26/amazon-anuncia-su-virtual-private-cloud-o-como-decir-privada-cuando-deberia-decir-publica/">Tweet</a>
</div>

<p style="text-align: center;">
  <img class="size-full wp-image-121 aligncenter" title="logo_aws" src="/wp-content/uploads/logo_aws.gif" alt="logo_aws" width="164" height="60" />
</p>

Reconozco que esta noticia la conocía desde Abril, así que no me ha sorprendido. Tampoco voy a decir que tenía preparado un post al respecto, pero casi. Hoy Amazon ha anunciado un nuevo servicio llamado [Amazon Virtual Private Cloud](http://aws.amazon.com/vpc/). Y por ese nombre cualquiera diría que Amazon va a vender su software de infrastructure para que cada uno de nosotros montemos nuestro Cloud Privado en nuestro datacenter. Pero no, no es eso&#8230; aunque quieren que lo parezca.

En [el blog de Werner Wogels, el CTO de Amazon](http://www.allthingsdistributed.com/2009/08/amazon_virtual_private_cloud.html) hace una interesante disertación sobre los pros y sobre todo los contras de las Nubes Privadas. Resumiendo, viene a decir que una Nube Privada no es Cloud Computing  porque:

  * No es verdaderamente elástico (recursos ilimitados)
  * No te ahorras Capex (Pay-as-you-go)

Es cierto que desde el punto de vista teórico puedo estar de acuerdo,  pero aterrizando en el mundo real, se olvida de algo muy importante: en la Nube Privada el departamento de IT se convierte en el proveedor del servicio (el Amazon de turno), y los departamentos o líneas de negocio se convierten en sus clientes. Es en ese modelo donde encaja la Nube Privada que la gran mayoría proponemos, y que Amazon no quiere porque va en contra de sus intereses.

Volviendo a la propuesta de Amazon, lo que ofrecen no es por lo tanto una Nube Privada, es una **Nube Pública securizada**: como dice uno de sus [evangelistas](http://twitter.com/jeffbarr/status/3551774791) **&#8220;Amazon VPS es una red interna aislada con subredes&#8221;**. ¡Qué grande es Twitter ofreciendo capacidad de síntesis! ¿Y qué es lo que ofrece?

  * Creación de un Virtual Private Cloud sobre la infrastructura existente de AWS
  * Especificar el rango de direcciones IP que se desee, del bloque que se desee.
  * Creación de subredes de ese rango.
  * Conexión securizada a la infrastructura con una VPN IPSec.
  * Acceder a instancias de Amazon EC2 desde tu VPC.
  * Salida a internet a través de la VPN, para su monitorización por parte del cliente (WTF?)

Es decir, lo que vende Amazon es la posibilidad de **poner una valla a las instancias EC2** que uses. Nada más. Se que ya hay gente que ha hecho esto, e incluso hay productos [que lo promocionan](http://www.cohesiveft.com/vpncubed/). De hecho, muchos proveedores con infrastructura elástica (cloud?) ofrecen accesos securizados con VPNs a esa infrastructura, y no lo llaman Cloud Privado.

Resumiendo, Amazon aprovechando el boom alrededor de las Nubes Privadas -porque es donde está el negocio- ha querido apropiarse del término y asociarlo a una funcionalidad de su producto. Una muy buena estrategia de marketing, sin duda. Pero no nos engañemos: siguen siendo un proveedor de Nube Pública.
