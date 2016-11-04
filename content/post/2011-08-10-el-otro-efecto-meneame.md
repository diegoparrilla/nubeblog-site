---
author: Diego Parrilla
categories:
- amazon
- cloud
- hosting
- iaas
date: 2011-08-10T10:55:37Z
dsq_thread_id:
- "382035352"
guid: /?p=2063
id: 2063
tags:
- amazon
- aws
- ebs
- meneame
- rayo
title: El otro efecto Menéame
url: /2011/08/10/el-otro-efecto-meneame/
image: /wp-content/uploads/503error.png
---
Reconozco que una de mis aficiones favoritas es procrastinar trolleando en los comentarios de las noticias de [Menéame](http://www.meneame.net). Aunque supongo que todo el mundo lo sabe, Menéame es el conocido clon hispano de [Digg](http://www.digg.com), el servicio a enlace de noticias gestionado por los usuarios (envían las que le gustan, y votan otras que les interesan). El pasado domingo intenté conectarme a Menéame después de pasar por varios periódicos online, y me encuentro con el sitio caído. Extraño, Menéame es muy estable&#8230; googleo un poco y veo que [un rayo la lía parda en un centro de datos de Irlanda](http://www.facilware.com/un-rayo-la-lia-parda-en-varios-servicios-y-portales-online.html) donde Amazon Web Services tiene alojada su zona europea. Microsoft, Paypal y otros también les afecta el servicio. Lo primero que me viene a la cabeza es: ¿Ese Datacenter no es un [Tier 4](/2010/10/11/que-son-los-tiers-en-un-centro-de-datos-el-ansi-tia-942/)? Si lo es, no lo parece&#8230;

![Error  503](/wp-content/uploads/503error.png)

El lunes por la mañana mientras desayuno me conecto de nuevo para ver si Menéame ha vuelto, y nada, el sitio sigue caído. A lo largo del día comento con varias personas la situación, y resulta inevitable preguntarse qué carajo les ha pasado, sin más&#8230; El martes por la mañana me conecto y me quedo de piedra: ¿Todavía no han levantado el servicio? Y empiezo a investigar qué ha pasado realmente con Amazon EC2, y qué ha pasado con Menéame.

Antes de empezar con las conclusiones, quisiera contar una intrahistoria que no se si la gente de Menéame son conscientes de ella o no: **Menéame ha sido la mejor propaganda en España del servicio Amazon EC2**. Ese es el otro &#8216;[Efecto Menéame](http://en.wikipedia.org/wiki/Slashdot_effect)&#8216;. Profesionales del hosting reconocen en privado que la decisión de ir a Amazon EC2 fue un golpe para el hosting tradicional en España, y conozco mucha gente que pone como ejemplo de buenas prácticas de despliegue en Amazon EC2 el [famoso post de Ricardo Galli sobre su arquitectura](http://gallir.wordpress.com/2009/12/30/como-montamos-meneame-en-amazon-ec2/). Revisando el post de nuevo, hay dos cosas que me llaman la atención:

  * La arquitectura usa (¿abusa?) de el almacenamiento persistente EBS. Aunque sobre el papel es una solución fantástica, es el servicio de Amazon que más problemas ha dado, con un historial de problemas en otras zonas muy grande, que incluye la pérdida de información. De hecho otro conocido clon de Digg que funciona sobre EC2 [las ha pasado mal precisamente por el uso de EBS](http://blog.reddit.com/2011/03/why-reddit-was-down-for-6-of-last-24.html). De hecho, algunos que también [han aprendido a base de castañazos nos ofrecen alternativas](http://agilesysadmin.net/ec2-outage-lessons).
  * Pero lo que más me sorprende es el tono del documento, donde subyace el mensaje de que Amazon EC2 es indestructible. Todo, absolutamente todo corre en Amazon, por lo tanto se confía ciegamente en la capacidad de Amazon Web Services para correr el servicio. Con frases más propias de un comercial que de un ingeniero: _&#8220;&#8230;(en Amazon está todo monitorizado y es público, **una caída afecta a muchos servidores, así que no tardan nada en resolver**)&#8221;._

<div>
  Este es el problema que ha tenido Menéame: han pensado que Amazon Web Services no puede fallar, y <strong>es precisamente el pensamiento contrario el que debes tener cuando despliegas en una Nube: TODO PUEDE FALLAR</strong>. Y es precisamente lo que ha pasado. Amazon Web Services ha tenido una cadena de fallos que han afectado de manera catastrófica a algunos clientes:
</div>

<div>
  <ul>
    <li>
      Un rayo la lía parda. Terremotos, tormentas, inundaciones&#8230; contra la naturaleza no podemos hacer nada. Todos los servicios de Amazon se vienen abajo en Irlanda.
    </li>
    <li>
      Los servicios tardan en ponerse de nuevo activos.
    </li>
    <li>
      Al intentar levantar los servicios, Amazon Elastic Block Storage (EBS) no se recupera de manera adecuada debido a un bug. Al parecer se eliminaban ciertas partes de los bloques que los volvía inutilizables. Creo que esto no explica todos los problemas con EBS, pero es el típico bug que solo surge en escenarios considerados improbables (¿es rearrancar un servicio como EBS un escenario improbable?)
    </li>
    <li>
      Todos los servicios dependientes de EBS fallan. Amazon Web Services pide a sus clientes que usen EBS de una zona no afectada. Eso implica crear e importar datos e imágenes a otras zonas.
    </li>
  </ul>
  
  <div>
    Estos cuatro pasos y la información correspondiente fue facilitada por Amazon a los clientes de manera abierta antes de las primeras 24 horas. Por lo tanto <strong>todo el tiempo necesario para levantar el servicio de nuevo no es imputable a Amazon, sino a los responsables de las aplicaciones desplegadas, es decir los Menéame, Paypal y compañía</strong>.  Es habitual que las empresas creen planes de contingencia para aquellos servicios que se consideran críticos para el funcionamiento de su negocio.
  </div>
  
  <div>
    Amazon Web Services es un servicio desde el punto de vista de ingeniería sublime, pero no es mágico. Puede fallar y lo hace. Pero además, es mucho menos resistente a fallos que otras soluciones. No porque esté construido de manera deficiente o porque su infraestructura no sea buena: es menos resistente porque está diseñado así. En Amazon Web Services y en gran número de nubes públicas es la aplicación la responsable de mantenerse funcionando pese a los fallos, en contra de lo que ocurre en el despliegue en infraestructura tradicional. Recomiendo este post, &#8216;<a href="http://blogs.gartner.com/lydia_leong/2010/12/03/designing-to-fail/">Designing to fail</a>&#8216;. La razón es clara: hacer que la infraestructura sea resistente a fallos es muy caro. Ofrece los recursos de almacenamiento y computación lo más baratos posible y delega en la aplicación esa gestión.
  </div>
  
  <div>
    Netflix es una empresa que lleva el concepto del &#8216;Diseñado para fallar&#8217; al límite. <a href="/2010/10/28/el-caso-de-exito-de-netflix-como-una-gran-corporacion-migra-a-la-nube-publica/">Netflix tiene su infraestructura en Amazon y Akamai</a>. Y para asegurarse que el servicio siempre está funcionando, creó una aplicación llamada &#8216;<a href="http://techblog.netflix.com/2010/12/5-lessons-weve-learned-using-aws.html">Chaos Monkey</a>&#8216;. Chaos Monkey lo que hace es tratar de interrumpir el servicio de Netflix simulando los errores que pueden ocurrir en Amazon (caída de instancias, desconexión de la red, degradación del servicio&#8230;) de manera aleatoria y no preprogramada. Vamos, como si metes un mono de feria dentro de tus racks en el centro de datos y empieza a tirar de los cables y a apagar y encender los ordenadores. Puede sonar un poco paranoico&#8230; pero cualquiera que haya tenido aplicaciones en producción a veces se pregunta si no hay un <a href="http://www.codinghorror.com/blog/2011/04/working-with-the-chaos-monkey.html">duende en vez de un mono puteando a los servidores</a>.
  </div>
  
  <div>
    Resumiendo, Menéame no estaba diseñado para fallar. Y lo mismo pasa con la gran mayoría de los servicios desplegados en Nubes Públicas. ¿Y por qué no lo están? Pues porque es caro, lleva tiempo y además es complejo. Caro, porque normalmente implica desarrollo adicional y contratar servicios en otro proveedor localizado en otra zona geográfica. Tiempo, porque necesitas dedicar recursos de desarrollo a infraestructura en vez de requisitos de negocio. Y complejo, porque la gran mayoría de los ingenieros software no conocen los intríngulis del desarrollo de sistemas resistentes a fallos. ¿cuando vale la pena invertir en esto? Eso es una decisión que debe hacer cada uno.
  </div>
  
  <div>
    Lo que me pregunto es si la gran propaganda que fue para Amazon la migración de Menéame, podría volverse en su contra tras estos tres días de caída del servicio. Yo si fuera Amazon, les regalaba el servicio durante un tiempo y de paso les enviaba un par de jamones. Y si fuera un proveedor de hosting o cloud español, aprovecharía el cabreo que deben tener ahora mismo Galli y cía. para hacerles una oferta de alojamiento patrocinada 😉
  </div>
</div>

<div>
  <strong>Actualización 11 de Agosto de 2011:</strong> Este post ha sido portada de Menéame (cosas veredes&#8230;) . El Dr. Galli ha publicado un post <a href="http://gallir.wordpress.com/2011/08/10/la-crisis-con-amazon-aws/">explicando lo que ha pasado</a>. Y se confirman mis sospechas: prepararon planes de contingencia para todo menos para ellos mismos, un error muy común, por otra parte. Otra cosa que sospechaba era que la crítica pública al Dr. Galli atraería la ira de script kiddies y demás fauna, como así ha sido 🙁
</div>
