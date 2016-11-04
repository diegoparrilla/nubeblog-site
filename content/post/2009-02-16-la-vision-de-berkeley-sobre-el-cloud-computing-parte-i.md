---
author: Diego Parrilla
categories:
- cloud
- estudios
date: 2009-02-16T11:27:27Z
dsq_thread_id:
- "204693380"
guid: /?p=690
id: 690
tags:
- amazon
- berkeley
- estudios
- google
- iaas
- microsoft
- paas
- saas
title: La visión de Berkeley sobre el Cloud Computing. Parte I
url: /2009/02/16/la-vision-de-berkeley-sobre-el-cloud-computing-parte-i/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,berkeley,estudios,google,iaas,microsoft,paas,saas" data-count="vertical" data-url="/2009/02/16/la-vision-de-berkeley-sobre-el-cloud-computing-parte-i/">Tweet</a>
</div>

Hace unos días recibí un correo indicándome que debía comentar un estudio que circula por la red hecho por la Universidad de Berkeley sobre el estado actual del Cloud Computing. Al leerlo me di cuenta que era un documento que necesita un análisis más detallado que mis habituales 300-500 palabras por post. Por suerte, muchos de los temas tratados ya han sido comentados en el blog, pero merece la pena dar un repaso.

El documento es el resultado de un estudio del [UC Berkeley Reliable Adaptive Distributed Systems Laboratory,](http://radlab.cs.berkeley.edu) y viene a responder a varias cuestiones fundamentales en el estado actual del Cloud Computing:

  * ¿Qué es Cloud Computing y en qué se diferencia de otros cambios de paradigma como el Software as a Service (SaaS)?
  * ¿Por qué puede el Cloud Computing despegar ahora, cuando ha fallado en los intentos anteriores?
  * ¿Qué se necesita para llegar a ser un proveedor de Cloud Computing, y por qué una compañía consideraría convertirse en uno?
  * ¿Cuales son las oportunidades que se abren o los potenciales &#8216;drivers&#8217; (de adopción, entiendo) del Cloud Computing?
  * ¿Cómo podríamos clasificar la oferta actual de Cloud Computing en el espectro, y cómo difieren los retos técnicos y de negocio dependiendo de qué lugar del espectro del producto?
  * ¿Cuales son los nuevos modelos económicos facilitados por el Cloud Computing, y cómo un operador de servicios decide si moverse a La Nube o quedarse en un Datacenter?
  * ¿Cuales son los diez obstáculos más importantes para la adopción del Cloud Computing, y las correspondientes 10 oportunidades disponibles para superar estos obstáculos?
  * ¿Qué cambios deberían hacer los diseñadores de futuras aplicaciones software, infraestructura software y hardware para aprovechar las necesidadesy oportunidades del Cloud Computing?

**¿Qué es el Cloud Computing?
  
** 

El comienzo del documento intenta explicar con una metáfora una de las razones del Cloud Computing, el acceso a recursos bajo demanda con menores costes debido a las economías de escala de los super datacenters. De igual manera que los fabricantes de chips -y yo añado que los fabricantes de casi todo- ya no tienen fábricas físicas para sus productos, sino que contratan la producción a empresas que únicamente tienen líneas de producción adaptables, ocurre lo mismo en el mundo de la operación de aplicaciones software.

Según ellos, **el Cloud Computing es la suma del SaaS y del Utility Computing**. Me ha llamado la atención cómo se desmarcan con celeridad del Software as a Service (SaaS) desde el punto de vista del usuario (_Saas User_). Todo el mundo conoce sus ventajas y se ha tratado ampliamente en múltiples sitios. Sin embargo el documento se centra sobre todo en lo que ellos llaman _SaaS Provider/Cloud User y Cloud Provider_.

El Cloud Computing desde el punto de vista de la infraestructura hardware ofrece cosas nuevas:

  * Ilusión de recursos de computación infinitos disponibles bajo demanda. Esto significa que los **Cloud Users no necesitan hacer planificaciones lejanas en el tiempo**. _(Y yo me pregunto, ¿Significa esto que desaparece el Capacity Planning? Yo creo que no&#8230;)_
  * La eliminación de compromisos tempranos de los Cloud Users, lo que **permite que las empresas empiecen con poco e incrementen sus necesidades hardware solo cuando hay un incremento de sus necesidades**, y
  * Poder pagar por el uso de recursos de computación por períodos cortos de tiempo (por ejemplo pagar por procesadores a la hora o almacenamiento por día), y liberándolos cuando no se necesitan.

Está claro que las ventajas para los Cloud Users son evidentes, pero ¿quién quiere convertirse en un Cloud Provider? ¿Qué necesidad tiene?

Una condición necesaria pero no suficiente para que una compañía se conviertan en proveedor de Cloud Computing es que ya debe haber realizado inversiones importantes no solo en grandes datacenters, sino también en sotfware de infraestructura a gran escala, además de los conocimientos para mantenerlos. Una vez que se dan estas condiciones, hay una gran cantidad de factores que pueden influir en que se conviertan en proveedores o no:

  1. Ganar mucho dinero: Las **economías de escala de los superdatacenters pueden ofrecer costes bastante por debajo de los datacenters medianos y pequeños** (ver el documento).
  2. Aprovechar inversiones ya realizadas: **Añadir Servicios de Cloud Computing sobre infraestructura ya existente** permite tener un nuevo flujo de benificios a cambio de costes bajos.
  3. Defender una franquicia: Microsoft quiere defender sus productos ofreciendo soluciones en la Nube, evitando su fuga a otros proveedores.
  4. Ser cabeza de playa: Si una compañía **ya tiene el software y un datacenter que cumpla los requisitos**, puede querer tomar la playa antes de que lleguen los Google, Microsoft y demás.
  5. Aprovechar las relaciones con clientes: Hay empresas de servicios que pueden **aprovechar su oferta de servicios para reducir la ansiedad** que produce a los clientes el camino hasta migrar a la Nube.
  6. Convertirse en una plataforma: Al estilo de Facebook, ofrecer la posibilidad de **integrar aplicaciones dentro de la plataforma** encaja con el modelo Cloud Computing.

Esta es la primera parte de mi análisis del estudio. Mañana más.

Ir a [La visión de Berkeley sobre el Cloud Computing. Parte II](/2009/02/17/la-vision-de-berkeley-sobre-el-cloud-computing-parte-ii/)

Ir a [La visión de Berkeley sobre el Cloud Computing. Parte III](/2009/02/18/la-vision-de-berkeley-sobre-el-cloud-computing-parte-iii/)

Ir a [La visión de Berkeley sobre el Cloud Computing. Parte IV y final](/2009/02/19/la-vision-de-berkeley-sobre-el-cloud-computing-parte-iv-y-final/)
