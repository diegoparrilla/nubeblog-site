---
author: Diego Parrilla
categories:
- cloud
- negocios
- opinion
date: 2008-11-25T09:05:25Z
dsq_thread_id:
- "204692949"
guid: /?p=365
id: 365
tags:
- amazon
- datasets
- ec2
- negocios
- opinion
title: 'Amazon Hosted Public Datasets: Vislumbrando nuevos modelos de negocio'
url: /2008/11/25/amazon-hosted-public-datasets-vislumbrando-nuevos-modelos-de-negocio/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,datasets,ec2,negocios,opinion" data-count="vertical" data-url="/2008/11/25/amazon-hosted-public-datasets-vislumbrando-nuevos-modelos-de-negocio/">Tweet</a>
</div>

Amazon ha anunciado la [publicación de repositorios públicos de datos](http://aws.amazon.com/publicdatasets/), accesibles únicamente desde sus entornos EC2. Es decir, puedes montar estos datos en su &#8216;Nube&#8217; y usarlos como quieras sin pagar nada, únicamente el tiempo de uso de las instancias EC2. Según dicen:

> Nuestra meta es proveer un acceso sencillo a datos de datos públicos y comunes como el genoma humano, astronomía y al censo de los USA.

Además si tienes un conjunto de datos interesante, puedes solicitar su publicación y donar los datos a la comunidad. Como podéis ver, todo muy bonito y&#8230; ¿altruista? Bueno, todo lo altruista que debe ser una empresa: evidentemente Amazon espera recuperar el dinero invertido cobrando por el uso de EC2.

La pasada semana tuve una [agradable reunión con un defensor del SaaS](http://josempelaez.wordpress.com/), y uno de los temas que han salido es el de la captura y explotación de datos de y en La Nube. Y casualmente va Amazon y saca a la luz este proyecto&#8230;

Cuando pienso en explotación de datos pienso en Business Intelligence, Datawarehouses y Datamining: lo que he visto en la empresa. Recuerdo una asignatura llamada &#8216;Bases de datos avanzadas&#8217; (nosotros la llamábamos &#8216;Bases de datos Avanzadísimas&#8217;&#8230;). En ella se estudiaba un par de conceptos nuevos llamados &#8216;Datawarehouse&#8217; y &#8216;Datamining&#8217;. Fascinantes conceptos en aquella época, pero nuestros profesores se empeñaban en darle más importancia a los conceptos teóricos formales que a la verdadera razón por la que explotaron los DW y los DM a mediados de los noventa: **El coste de proceso y el coste de almacenamiento bajó de manera drástica, permitiendo el manejo de datos en tiempos más reducidos y por lo tanto, ajustados a la velocidad que necesitan las diferentes Unidades de Negocio para tomar decisiones**. ¡Por fín era rentable explotar estos datos! Una característica fundamental de estos almacenes de datos es que trabajan con información interna de la empresa. Es decir, su ámbito es el de la corporación X o corporación Y (departamento X o departamento Y&#8230; datamarts). Resulta impensable que una corporación X ponga a disposición de sus competidores su Datawarehouse&#8230;¿o no?

Estamos a finales de la década y la situación es muy diferente: el coste de almacenamiento tiende a cero, la computación se compra por tiempo de uso, el ancho de banda aumenta y el precio se congela&#8230; El coste de proceso y almacenamiento pueden llegar a ser irrelevantes cuando manejamos grandes cantidades de datos. Y en la parte software, algoritmos como Map/Reduce surgen como alternativa a los modelos relacionales clásicos, menos eficientes para grandes volúmenes. **Estamos ante el nacimiento de una Nueva Generación de Data Warehouses**.

¿Pero con qué datos vamos a alimentar a esta Nueva Generación? Veo tres fuentes básicas:

  1. **Las propias organizaciones**. No todos los datos entraban en el data warehouse, pero ahora **empieza a ser factible almacenar todos y cada uno de los datos manejados en las organizaciones**. Aquí entraría el [almacenamiento &#8216;crudo&#8217; de información recogida de las arquitecturas M2M](http://josempelaez.wordpress.com/2008/11/20/captura-datos-nube/), por ejemplo.
  2. **Los proveedores**. De igual manera que se acuerdan niveles de calidad de servicio a proveedores clave, se podrán demandar datos &#8216;crudos&#8217; a éstos. Ya se hace, pero normalmente ligado a las métricas de calidad.
  3. **Proveedores de Bancos de Datos**: Como Amazon. Cobrando de modo directo o indirecto por el acceso a estos bancos públicos de datos. Con el tiempo, este tipo de proveedores ofrecerían datos menos genéricos y más orientados a segmentos de negocio. Posiblemente, estos proveedores de bancos de datos serán &#8216;Brokers&#8217; entre organizaciones afines. Ya sea mediante la forma de consorcios o fundaciones que garanticen la &#8216;neutralidad&#8217; de estos datos, o bien mediante mercadeo de datos como si fuese otra mercancia.

Lo cierto es que esta nueva generación de Data Warehouses **ya existe**. Hace unos años, una empresa con un novedoso software de reconocimiento de textos nos comentó cómo una importante empresa americana de tarjetas de crédito no sólo estaba digitalizando todo su almacén de datos en papel, sino que **compraba bases de datos en cualquier formato con la esperanza de poder cruzarlas en el futuro**. Sabían que sólo era cuestión de tiempo que el coste de cruzar estos datos compensase sus esfuerzos por calcular el riesgo de sus clientes de manera más avanzada. Y en muchas ocasiones [el problema no era de costes, sino de acceso a los recursos](http://brigomp.blogspot.com/2007/10/alto-rendimiento-en-wall-street.html), por sorprendente que parezca.

**Actualización 9:30am:** Via twitter.com me llega esta empresa que parece que intentan mover este negocio usando Amazon AWS: <http://datamarket.net/>

 
