---
author: Diego Parrilla
categories:
- arquitectura
- cloud
- iaas
- virtualización
date: 2010-09-16T01:39:55Z
dsq_thread_id:
- "204732492"
guid: /?p=1333
id: 1333
tags:
- cloud
- sobresubscripcion
- virtualización
title: Qué es la sobresuscripción en el Cloud Computing
url: /2010/09/16/que-es-la-sobresuscripcion-en-el-cloud-computing/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="cloud,sobresubscripcion,virtualizaci%C3%B3n" data-count="vertical" data-url="/2010/09/16/que-es-la-sobresuscripcion-en-el-cloud-computing/">Tweet</a>
</div>

[<img class="alignright size-full wp-image-1337" title="glass_full" src="/wp-content/uploads/glass_full.jpg" alt="" width="240" height="352" srcset="/wp-content/uploads/glass_full.jpg 240w, /wp-content/uploads/glass_full-204x300.jpg 204w" sizes="(max-width: 240px) 100vw, 240px" />](/wp-content/uploads/glass_full.jpg)Hace un par de días escribí un [post](/2010/09/13/amazon-anuncia-nuevas-instancias-desde-7-al-mes/) sobre las nuevas instancias de Amazon EC2 con sobresuscripción de CPU y tal vez de memoria. Este concepto, el de &#8216;sobresubscripción&#8217;, pensé que era un concepto usado con normalidad por tecnólogos, pero parece ser que no.

¿Qué es esto de la sobresuscripción de recursos? Bueno, esto no es nuevo en absoluto. La sobresuscripción no es mas que el compromiso por parte de un proveedor a ofrecer un recurso a sus clientes a sabiendas de que puede que en algún momento no pueda atender toda la demanda solicitada. ¿Les suena? Claro que sí. Si tienen una línea ADSL o cable en casa que a veces llega a sus 10MB y otras no, no es por las características físicas del enlace: es que tus vecinos también se bajan películas al mismo tiempo que tu&#8230;

Aunque creo que la sobresuscripción no es algo único del mundo de las Telecomunicaciones (supongo que los antiguos coeficientes de caja y los famosos tier-N de Basilea de la banca siguen algún patrón similar), son ellos los que han basado su crecimiento en ese concepto: vendo más recursos de los que tengo, y luego hago firmar un acuerdo de nivel de servicio (SLA) a mi cliente para protegerme cuando no pueda darle el servicio demandado. Como ocurre en el Cloud Computing, el modelo de servicio se basa en la experiencia anterior en las empresas de Telecomunicaciones.

El Cloud Computing también se usa la sobresuscripción. Y mucho. Y si vas a buscar un proveedor de Cloud o de Virtualización es MUY importante que preguntes y que tengas claros estos conceptos antes de contratar el servicio. Veamos primero qué recursos se usan en una IaaS típica:

  * CPU: Ciclos de CPU que te vende tu proveedor.
  * Memoria: La memoria RAM disponible para tu servidor virtual.
  * Almacenamiento Local: Disco duro &#8216;local&#8217; usado por el servidor. Hay proveedores que no lo usan.
  * Almacenamiento remoto: Volumen remotos creados en un almacenamiento tipo SAN (puede ser un NAS, pero por simplificar pensemos en un almacenamiento de bloque).
  * Entrada y Salida a disco: Es decir, los famosos IOs del Sistema Operativo hacia los dispositivos de almacenamiento.
  * Tráfico entre servidores:  Ancho de banda permitido entre servidores en la misma infraestructura.
  * Tráfico externo: Ancho de banda permitido entre los servidores e internet.

Todos estos recursos pueden ser sobresuscritos. Todos. El parámetro que se usa para conocer el nivel de sobresuscripción de cada recurso se llama _ratio de concentración_.

Sin embargo, no todos los proveedores sobresuscriben todos los recursos. Casi todos hacen sobresuscripción del ancho de banda disponible desde/hacia internet. Casi todos aprovechan las capacidades de las cabinas de almacenamiento SAN de thin provisioning y deduplicación, con ratios de concentración muy altos. Sin embargo, no todos sobresuscriben CPU, memoria e IOs de sus servidores. ¿Por qué?

Mientras que en el caso del ancho de banda es algo que se conoce desde hace tiempo y los departamentos de TI están acostumbrados a trabajar con ello, en el caso de las cabinas de almacenamiento lo que ocurre es que el cliente realmente no tiene reducción en la calidad de su servicio (a no ser que haya un problema de sobrecapacidad en la cabina, pero de eso ya hablaré otro día). Sin embargo la sobresuscripción de CPU y memoria tiene un impacto muy importante en la calidad de servicio ofrecida y por lo tanto en sus Acuerdos de Nivel de Servicio.  Por decirlo a las claras, definir un SLA sobre una plataforma altamente sobresuscrita en CPU y Memoria es un infierno.

Sin embargo, se hace. Pero no en el Cloud Computing, sino con plataformas virtualizadas de hosting gestionadas. Los administradores de estas plataformas distribuyen los servidores virtuales de tal manera que se aproveche la máquina de la mejor manera posible sin afectar a los &#8216;vecinos&#8217; que comparten máquina. Es decir, hacen un balanceo de la carga basada en su experiencia como administradores.

Por desgracia esto no puede hacerse en el Cloud Computing ya que es una premisa fundamental en una plataforma altamente automatizada que la elección del servidor físico donde se hace el despliegue de la máquina virtual se haga con un algoritmo que implementa políticas para ello. Y los algoritmos por ahora no son muy listos. Así que ante esta situación lo mejor es simplemente simplificar el problema y no sobresuscribir recursos. Este es (bueno, era) el caso de Amazon EC2.

Amazon EC2 no sobresuscribe ni memoria ni CPUs. Lo que hace es un particionamiento exacto de los recursos entre los &#8216;inquilinos&#8217; de sus máquinas físicas. O tan exacto como las tecnologías de virtualización que usa lo permite (Xen paravirtualizado y parece ser que KVM con virtualización completa para correr Windows). Muchos proveedores de hosting con los que he hablado se llevan las manos a la cabeza cuando les cuento esto, ya que la mayoría de los servidores en los centros de datos se encuentran infrautilizados. Sin embargo, el modelo de Amazon no se centra (o se centraba, ahora tengo mis dudas) en el bajo coste de sus servicios, sino en que el coste es razonable para el servicio ofrecido. Y su estrategia de optimización de la plataforma se basa en prescindir de los humanos ([Skynet de nuevo](/2009/01/14/seran-los-humanos-irrelevantes-monitorizando-aplicaciones-cloud/)&#8230;) en las tareas de provisión y operación, por lo que el balanceo de la carga que hace un administrador experto debe sustituirse con un algoritmo sencillo y eficiente.
