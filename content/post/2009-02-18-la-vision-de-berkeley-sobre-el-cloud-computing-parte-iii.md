---
author: Diego Parrilla
categories:
- cloud
- estudios
date: 2009-02-18T10:46:46Z
dsq_thread_id:
- "204693425"
guid: /?p=700
id: 700
tags:
- amazon
- berkeley
- estudios
- google
- iaas
- microsoft
- paas
- saas
title: La visión de Berkeley sobre el Cloud Computing. Parte III
url: /2009/02/18/la-vision-de-berkeley-sobre-el-cloud-computing-parte-iii/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,berkeley,estudios,google,iaas,microsoft,paas,saas" data-count="vertical" data-url="/2009/02/18/la-vision-de-berkeley-sobre-el-cloud-computing-parte-iii/">Tweet</a>
</div>

Ir a [La visión de Berkeley sobre el Cloud Computing. Parte I](../2009/02/16/la-vision-de-berkeley-sobre-el-cloud-computing-parte-i/)

Ir a [La visión de Berkeley sobre el Cloud Computing. Parte II](/2009/02/17/la-vision-de-berkeley-sobre-el-cloud-computing-parte-ii/)

La migración a un modelo de Cloud Computing o bien empezar una empresa directamente aprovechando las ventajas de este modelo no solo es una cuestión técnica; es también una cuestión de recursos económicos.

**La elasticidad y la transferencia del riesgo**

Los autores argumentan que la frase &#8220;Convertir [CapEx](http://en.wikipedia.org/wiki/Capital_expenditure) a [OpEx](http://en.wikipedia.org/wiki/Operating_expense)&#8221; se usa habitualmente como argumento de venta del Cloud Computing, &#8220;pay as you go&#8221; (paga por lo que usas no es una traducción exacta, pero nos vale&#8230;) captura mejor la esencia de los beneficios económicos del Cloud Computing. Por lo tanto, aunque Amazon por ejemplo puede ser 1.4 veces más caro que comprar y depreciar servidores del mismo tipo, los beneficios de **elasticidad y transferencia del riesgo** equilibran este sobrecoste. Especialmente cuando hablamos de saturación o falta de utilización de los servicios.

La elasticidad te permite soportar los picos de demanda estacionales, y la transferencia del riesgo es por no perder clientes por una mala calidad del servicio en caso de saturación. Aunque lo nombra de pasada, creo que es también importante señalar que se **reduce de manera significativa el coste de optimización** de las soluciones, por lo que de nuevo transferimos CapEx a OpEx. Recomiendo leer en detalle el capítulo 5.1 ya que está lleno de detalles que no puedo reproducir en el blog como quisiera.

**Comparando costes: ¿Debo irme a La Nube?**

He de confesar que esta parte del documento me parece confusa: no está claro si habla de Cloud Users o Cloud Providers. Cosas como la energía eléctrica consumida, refrigeración y costes de operación de la infraestructura. Creo que este punto por momentos se ponen la gorra de Cloud User y luego la de Cloud Provider, pero no lo hacen de manera rigurosa. Así que si tienes un datacenter y piensas en moverte a la Nube, estos puntos son importantes en su opinión:

  * Paga de manera separada los recursos: Si puedes pagar por ancho de banda consumido, almacenamiento, CPU&#8230; hazlo, ya que la mayoría de las aplicaciones tienen consumos dispares.
  * Ten en cuenta el coste de refrigeración, energía eléctrica y espacio físico: Estos costes duplican los costes del hardware. Para soluciones redundantes, puede ser hasta tres veces el coste.
  * Coste operaciones: El coste de las operaciones hardware ha caido de manera dramática, pero no así el coste de gestión del software de infraestructura, hay que seguir actualizando y poniendo parches. En este caso soluciones como Google AppEngine, Microsoft Azure o Force.com pueden ser interesantes.

Mañana la última parte con las 10 obstáculos para la adopción del Cloud Computing.

Ir a [La visión de Berkeley sobre el Cloud Computing. Parte IV y final
  
](/2009/02/19/la-vision-de-berkeley-sobre-el-cloud-computing-parte-iv-y-final/)
