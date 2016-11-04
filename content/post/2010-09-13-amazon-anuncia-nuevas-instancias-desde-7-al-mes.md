---
author: Diego Parrilla
categories:
- amazon
- iaas
date: 2010-09-13T00:00:32Z
dsq_thread_id:
- "204831532"
guid: /?p=1318
id: 1318
tags:
- amazon
- aws
- microinstancia
- vps
title: Amazon anuncia nuevas instancias desde $7 al mes
url: /2010/09/13/amazon-anuncia-nuevas-instancias-desde-7-al-mes/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,aws,microinstancia,vps" data-count="vertical" data-url="/2010/09/13/amazon-anuncia-nuevas-instancias-desde-7-al-mes/">Tweet</a>
</div>

[<img class="alignright size-full wp-image-121" title="logo_aws" src="/wp-content/uploads/logo_aws.gif" alt="" width="164" height="60" />](/wp-content/uploads/logo_aws.gif)

La semana pasada Amazon [anunció unas nuevas instancias denominadas &#8216;microinstancias&#8217;](http://aws.amazon.com/about-aws/whats-new/2010/09/09/announcing-micro-instances-for-amazon-ec2/) en su servicio de computación en la nube Amazon EC2. Estas nuevas instancias ofrecen 613MB de RAM por un precio $0.02 la hora. Es decir, unos $14 al mes, unos €11 mensuales.
  
¿Pero cómo consiguen esta gente ofrecer un precio como este? Bueno, hay letra pequeña y no tan pequeña. Se puede hacer porque este servicio tiene ciertas características que lo diferencian de una instancia tradicional EC2:

  * **No se permiten instancias &#8216;efímeras&#8217;. La instancia solo funciona en modo &#8216;persistente&#8217;.** Es decir, la instancia necesita un disco basado en EBS (Elastic Block Storage) con el sistema operativo. Tampoco hay disco temporal, una característica de las instancias tradicionales de EC2.
  * **Hay sobresubscripción de CPUs. Y esta es la gran novedad de este tipo de instancias** ya que rompe una regla del servicio de Amazon EC2 seguida hasta ahora: no usar sobresubscripción de memoria o de CPUs. Según dice la información del servicio, permite el uso de hasta 2 ECUs durante ráfagas cortas de tiempo (curiosa manera de disimular la sobresubscripción).

Estas microinstancias están optimizadas para aplicaciones que requieren un rendimiento bajo, pero que necesiten consumir picos de recursos de manera ocasional. Las microinstancias permiten tener un nivel de CPU bajo pero consistente, y nos permite acceder a mayor capacidad en ráfagas.

La verdad es que este es el servicio Amazon EC2 que más se parece a unVirtual Private Hosting. De hecho, hay mucha gente que piensa que este tipo de instancias es el Cloud Computing (pobrecitos&#8230;).

Para comparar manzanas con manzanas, he cogido la información que ofrece [Linode.com](http://www.linode.com), uno de los proveedores de VPS más importantes del mundo de su plan Linode 512 y lo he comparado con una microinstancia. El Linode 512 tiene lo siguiente:

  * 512MB de RAM
  * 16GB de disco duro
  * 200GB de transferencia
  * No hay información de Ghz disponibles, así que tendremos que asumir que son comparables&#8230;

El precio de este servicio es de $19.95. Ahora vamos a calcular el coste de una microinstancia similar:

  * 613MB de RAM y 2ECU sobresubscripta a $14,4
  * 16GB de disco EBS son unos $5,76 ([100GB de un disco con unos 100 IO por segundo son $36](http://aws.amazon.com/ebs/))
  * 200GB de transferencia es gratis hasta noviembre, pero en ningún caso el tráfico de entrada costará más de $1.

Las cifras confirman lo dicho anteriormente: La nueva micro instancia de Amazon es un ataque directo al modelo de negocio de los VPS basado en servidores sobresubscriptos hasta las trancas, ya que está perfectamente alineado en coste. Si ya contratamos planes de prepago a 1 o a 3 años, entonces los ahorros pueden llegar al 50%.
