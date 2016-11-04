---
author: Diego Parrilla
categories:
- cloud
- estudios
date: 2009-02-17T00:05:10Z
dsq_thread_id:
- "204693408"
guid: /?p=692
id: 692
tags:
- amazon
- berkeley
- estudios
- google
- iaas
- microsoft
- paas
- saas
title: La visión de Berkeley sobre el Cloud Computing. Parte II
url: /2009/02/17/la-vision-de-berkeley-sobre-el-cloud-computing-parte-ii/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,berkeley,estudios,google,iaas,microsoft,paas,saas" data-count="vertical" data-url="/2009/02/17/la-vision-de-berkeley-sobre-el-cloud-computing-parte-ii/">Tweet</a>
</div>

Ir a [La visión de Berkeley sobre el Cloud Computing. Parte I](/2009/02/16/la-vision-de-berkeley-sobre-el-cloud-computing-parte-i/)

Los siguientes capítulos del documento tratan un asunto que suele salir en conversaciones informales pero que normalmente pasamos por alto: Por qué despega ahora el Cloud Computing, y por qué fallo antes.

**¿Por qué ahora Cloud Computing y antes no?
  
** 

Para los autores la razón está detras de algo que según ellos acompaña a los modelos de negocio Web 2.0: el paso de un modelo de &#8216;cercanía al cliente, margenes altos y compromisos altos&#8217; a un modelo de &#8216;distanciamiento del cliente, márgenes bajos y compromiso bajo&#8217;. Es decir, **pasar de un modelo donde es necesario definir contratos y marcos de relación entre empresas pesados a un modelo donde el autoservicio (self-service) es el que manda.** Como ejemplo Paypal y Amazon Web Services, donde no es necesario firmar un contrato para trabajar con ellos, basta con dar tu tarjeta de crédito.

**Las nuevas aplicaciones
  
** 

Los autores sostienen que el driver actual fundamental para la adopción de una arquitectura de aplicaciones en la Nube es el elevado coste actual para acceder a datos en una red WAN comparado con una red LAN. Aunque me parece una aproximación un poco simplista, se la compro. Los tipos de aplicaciones que proponen son:

  * Aplicaciones móviles interactivas: Estas aplicaciones normalmente necesitan alta disponibilidad en la parte servidora y capacidad de almacenamiento masiva. Lo que me parece una chorrada monumental es que sean interactivas. El mundo M2M (machine-to-machine) genera muchísimos más datos que las aplicaciones interactivas.
  * Procesado Batch en paralelo: La posibilidad de poder trabajar con cientos de máquinas en paralelo es algo desconocido hasta ahora para la gran mayoría de desarrolladores. Soluciones con MapReduce pensadas para gestionar esta complejidad emergerán.
  * Aplicaciones analíticas: El procesado de datos está en auge frente a las aplicaciones transaccionales. Cada vez es más importante analizar los datos que manejan las empresas.
  * Extensión de la capacidad de computación de los ordenadores personales: Herramientas de cálculo que lanzan sus cálculos contra los servidores en La Nube. Matlab y Mathematica como ejemplo de soluciones existentes.

**Las clases existentes de utility computing**

Los autores sostienen que las diferentes ofertas de utility computing se distinguirán en función del nivel de abstracción presentada al programador y el nivel de gestión de los recursos virtualizados. Cualquier aplicación necesita un modelo de computación, un modelo de almacenamiento y un modelo de comunicación entre procesos. Para conseguir la ilusión de capacidad infinita es necesario virtualizar estos recursos para poder multiplexarlos y ocultarlos al programador.

A un lado del espectro está Amazon EC2. Una instancia EC2 es como hardware físico, y los usuarios tienen control sobre todo el software de kernel hacia arriba. El API disponible es ligero. Puede ejecutarse casi cualquier cosa en las instancias. Debido a su bajo nivel de abstracción, es complicado ofrecer escalabilidad automática y tolerancia a fallos a este nivel. Esto se suele gestionar a nivel de aplicación.

En el otro extremo se encuentran las Plataformas de aplicaciones específicas para un dominio como Google AppEngine y Force.com. AppEngine está pensada para aplicaciones web y modelos petición-respuesta, por lo que se raciona el uso de la CPU en las peticiones de servicios. Force.com está pensada únicamente para trabajar con las bases de datos de Salesforce.com. Por lo tanto, no sirven como plataformas de computación de propósito general.

Microsoft Azure se encuentra a medio camino entre la flexibilidad y la facilidad para el programador. Las aplicaciones se escriben usando librerías .NET y soporta computación de propósito general. Los usuarios pueden usar el lenguaje que prefieran (mientras sea soportado por .NET), pero no pueden controlar el sistema operativo debajo o la plataforma de ejecución de .NET. Las librerías permiten configurar redes, y parámetros de escalabilidad y tolerancia a fallos, pero debe hacerlo el programador de manera declarativa.

Los autores se preguntan si un modelo podrá batir a otro en el espacio del Cloud Computing. Al igual que hay lenguajes de programación especializados en el manejo de recursos hardware como el C, y otros se especializan en el desarrollo de aplicaciones Web (olvidándose del metal) como Ruby (on Rails), lo mismo pasará con las ofertas de Cloud Computing.

Por hoy es suficiente, mañana seguiré con la Economía del Cloud Computing.

Ir a [La visión de Berkeley sobre el Cloud Computing. Parte III](/2009/02/18/la-vision-de-berkeley-sobre-el-cloud-computing-parte-iii/)

Ir a [La visión de Berkeley sobre el Cloud Computing. Parte IV y final](/2009/02/19/la-vision-de-berkeley-sobre-el-cloud-computing-parte-iv-y-final/)
