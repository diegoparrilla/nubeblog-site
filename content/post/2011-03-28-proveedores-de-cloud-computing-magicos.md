---
author: Diego Parrilla
categories:
- opinion
- saas
date: 2011-03-28T11:04:04Z
dsq_thread_id:
- "264832052"
guid: /?p=2035
id: 2035
tags:
- aws
- carr
- director
- iaas
- saas
- vmware
title: Proveedores de Cloud Computing mágicos
url: /2011/03/28/proveedores-de-cloud-computing-magicos/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="aws,carr,director,iaas,saas,vmware" data-count="vertical" data-url="/2011/03/28/proveedores-de-cloud-computing-magicos/">Tweet</a>
</div>

[<img class="alignright size-medium wp-image-2037" title="mago" src="/wp-content/uploads/mago-252x300.jpg" alt="" width="252" height="300" srcset="/wp-content/uploads/mago-252x300.jpg 252w, /wp-content/uploads/mago.jpg 364w" sizes="(max-width: 252px) 100vw, 252px" />](/wp-content/uploads/mago.jpg)Es sorprendente como empresas que llevan muchos años haciendo software tradicional de repente y de manera mágica resulta que su software está &#8216;En la Nube&#8217;. No solo eso, sino que algunos dicen que fueron ellos los que inventaron el Cloud Computing, pero que como siempre los americanos llegaron y le pusieron un nombre &#8216;chulo&#8217;. Lo del Software as a Service es un auténtico escándalo. Aquí ahora todo es Cloud. Tonto el último.

Pero si en el SaaS lo que te encuentras es con lo que los anglos llaman &#8216;[Cloudwashing](http://blogs.forrester.com/james_staten/09-10-14-cloud_defined_now_stop_cloudwashing)&#8216;, en la parte de Infraestructura como Servicios, la verdad es que no se como clasificarlo. Yo entiendo que vender es muy difícil, estamos en crisis y hay que ganarse la vida&#8230; pero de verdad que hay cosas que claman al cielo.

Por un lado, tenemos a los clientes, que de un día para otro todos quieren &#8216;Cloud&#8217;. El proveedor lo primero que se hace es negar la mayor _&#8216;¿pero tu para que quieres el Cloud Computing, si te puedo proveer todo lo que te ofrecen con nuestro hardware dedicado y nuestra infraestructura?&#8217;_. Desde la perspectiva del proveedor resulta incomprensible que un cliente que (presuntamente) no sabe nada de infraestructura demande una plataforma. Esta es la etapa de la negación del proveedor: se asume que el cliente no sabe y que ha oído la última palabra de moda. Posiblemente muchos clientes se mueven por la moda como ya dijo [Larry Ellison hace mucho tiempo](/2008/10/02/larry-ellison-ceo-oracle-dice-cuatro-verdades-sobre-el-cloud-computing/) (por cierto, este ya está haciendo Cloudwashing a tope), pero otros entienden las teóricas ventajas del modelo y lo quieren probar.

Por otro lado tenemos los proveedores. Su modelo de negocio tradicional está cambiando y los clientes piden cosas que antes nunca pedían. Y lo peor: en un negocio con crecimientos de dos dígitos se encuentran con bajas de clientes también de dos dígitos&#8230; que se van a proveedores de Cloud Computing. ¡Así que hay que ofrecer plataformas de Cloud Computing pero a la de ya! Los comerciales, felices porque ahora no deben convencer a sus clientes de que el Cloud Computing no les vale, sino que pueden usar su plataforma de Cloud Computing.

¿Pero qué plataformas de Infraestructuras como Servicios ofrecen muchos proveedores? Pues&#8230; ninguna&#8230; porque lo que ofrecen son Servicios de Virtualización de Servidores sobre su infraestructura tradicional. ¿Donde queda la elasticidad, el pago por uso, el autoservicio? Pues en ningún sitio. **Y esto no es Cloud Computing.** 

Una plataforma de Cloud Computing es otra cosa. Una IaaS no es un conjunto de servidores virtualizados, un SAN y a correr. Es algo mucho más complejo. **La primera prueba del algodón es esta: ¿puedo contratar el servicio de manera online y no volver a tratar con un técnico de soporte durante todo el ciclo de vida de despliegue de su solución? Si la respuesta es sí, entonces está ante un servicio IaaS, sino, está ante otra cosa**. No se si mejor o peor, pero otra cosa.

Uno de los gurús teóricos del Cloud Computing, [Nicholas Carr lo compara con la electricidad](/2008/11/04/the-big-switch-de-nicholas-carr-el-libro-de-cabecera-del-cloud-computing/). ¿Se imagina usted llamando a su compañía de electricidad cada vez que quiere conectar un nuevo aparato en su casa? No&#8230; simplemente lo enchufas y empieza a funcionar. En **una verdadera plataforma de Cloud Computing el usuario puede levantar una nueva instancia simplemente pidiéndolo a través de una interfaz web, de un API o de una línea de comando. Y es inmediato**. Nada de esperar a que venga alguien y te lo aprovisione (¿se imagina que tenga que venir un técnico de su compañía eléctrica a enchufar un nuevo aparato?).

Al principio, la electricidad que se servía a las fábricas y a los particulares debía producirse ad-hoc. Luego, la llegada de estándares e innovaciones en la distribución (líneas de alta tensión, de media tensión, la corriente alterna, estandarización de los voltajes) permitió que la electricidad se compre y se consuma bajo demanda. Todo el mundo tuvo acceso barato a este recurso. Para poder acceder de manera barata, los dispositivos que se conectan a la red eléctrica necesitan de elementos de transformación. Es decir, un portátil necesita 19 voltios de contínua, un cargador de móvil 9V, un secador tiene otras necesidades&#8230;. es decir, cada elemento tiene diferentes necesidades, pero se conecta a la misma red.

**En el verdadero Cloud Computing, las aplicaciones deben adaptarse a los requisitos de la IaaS. Y aquí tenemos la segunda gran prueba del algodón: Si no necesitas adaptar tus aplicaciones a la nueva IaaS, entonces lo que están haciendo es adaptarse la IaaS a tí.** Y siento decepcionar, pero esto no es mágico. Es muy caro&#8230; tal vez más caro que tener una plataforma dedicada para tí. Puede haber una oferta comercial interesante obviamente&#8230; pero un cliente debe entender que esto no es Cloud. Es otra cosa.

Siento decirles que no existe magia en el Cloud Computing&#8230; Y en el mundo de la empresa lo mágico se asocia  lo barato/gratis o lo inmediato. El Cloud si ofrece inmediatez&#8230; pero hay un precio a pagar: el de migrar tus servicios a las &#8216;interfaces&#8217; de tu proveedor. Puede costar más o menos. Pero es un proceso ineludible. Da igual que sea Amazon Web Services o VMware Director. Hay que hacerlo.

Al igual que ocurrió con la distribución de la electricidad, la estandarización y la innovación en el aprovisionamiento de capacidad de computación y almacenamiento debe acarrear una reducción de costes. Todavía no lo sentimos porque las ventajas del modelo hace que la variable &#8216;coste&#8217; todavía no sea la primordial. Cuando haya diferentes competidores y a posibilidad de migrar de un proveedor a otro (¿entienden ahora mi fijación con las Nubes Abiertas?), entonces veremos brillar las ventajas de las economías de escala en el Cloud Computing.
