---
author: Diego Parrilla
categories:
- almacenamiento
date: 2009-10-14T15:01:01Z
dsq_thread_id:
- "204694063"
guid: /?p=1082
id: 1082
tags:
- almacenamiento
title: Sidekick y cómo suicidarte en La Nube
url: /2009/10/14/sidekick-y-como-suicidarte-en-la-nube/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="almacenamiento" data-count="vertical" data-url="/2009/10/14/sidekick-y-como-suicidarte-en-la-nube/">Tweet</a>
</div>

Ha sido una de las noticias más comentadas de los últimos tiempos alrededor del Cloud Computing: [Los usuarios de Sidekick, un dispositivo similar a la Blackberry muy popular en los USA han perdido todos sus datos y hay muy pocas posibildades de recuperarlos](http://www.underpc.com/articulos/general/1526-los-usuarios-de-sidekick-pierden-sus-datos-por-culpa-de-microsoft).  <span style="text-decoration: line-through;">Acojonante</span> Acongojante.  Sidekick almacenaba los datos en local y en &#8216;La Nube&#8217;, es decir, en almacenamiento en sus Centros Datos donde se suponía que gestionaban los datos de sus usuarios.

La historia de esta empresa es curiosa. Hace cosa de un año [Danger](http://www.danger.com) fue comprada por [Microsoft](http://blogs.zdnet.com/hardware/?p=5820) por unos $500M.  No quiero imaginarme qué puede haber pasado dentro de esta empresa para que ocurra una cosa así. Se supone que Microsoft sabe de servidores y estas cosas&#8230;

Los agoreros de la Nube ya han llegado diciendo que lo de la Nube no funciona y todo esto a lo que ya estamos acostumbrados. Sin intentar disculpar a la gente de Danger, creo que la única diferencia entre lo que ha pasado con Danger y cosas que han pasado internamente en las empresas es precisamente la **visibilidad**. En un servicio público en la Nube, no puedes fallar, ya que tus clientes lo que hacen es **confiar** en ti. Te contratan tu servicio por confianza. Las críticas a Microsoft y Danger han sido feroces, pero son absolutamente merecidas.

En los últimos años me he encontrado con mucha gente que se centra en dar niveles de disponibilidad de 4, 5 y hasta seis nueves, pero se olvidan de otro tipo de servicios necesarios para el correcto funcionamiento de un sistema que se ejecutan cada semana, mes, cuatrimestre o año. Y son los que suelen fallar. Se ha hablado mucho sobre Sidekick comentando que no tenían redundancia de datos. Me cuesta creer que una empresa que vale tanto dinero no tenga redundancia. Probablemente tendrían procesos mal implementados y que no se probaban con frecuencia (recuerda que se ha perdido TODO, sin posibilidad de recuperar un backup antiguo).

Dentro de los departamentos de IT hay ciertas  &#8216;líneas rojas&#8217; que son muy peligrosas de cruzar. Una de ellas es restringir el coste de las operaciones de respaldo de datos. Viví una situación en la que una Forbes 500 perdió hasta el 50% de su valor en bolsa por culpa de un recorte desmesurado en el departemento de IT de una subsidiaria que afectó a los sistemas de respaldo. No pudieron recuperar datos, vino un auditor&#8230; y ¡ay! los datos no eran correctos en los sistemas por culpa de ese fallo&#8230; Y costó miles de millones de dólares a los accionistas. Y recuerdo perfectamente cómo el director de IT puso  su cargo a disposición del CIO cuando le dijeron que debía cruzar esas &#8216;líneas rojas&#8217; para ahorrar costes. Y se fué, porque sospechaba que podía ocurrir algo como lo que pasó. Ética del trabajo, se llama esto.

No hace falta irse a una Forbes 500, todos conocemos de casos de servidores que llevan meses funcionando, se rearrancan y dejan de funcionar&#8230; fuentes de alimentación que fallan cuando se apaga el servidor después de meses de funcionamiento&#8230; descubrir con horror que el backup de los datos de tu empresa hace meses que no se hacen y nadie se ha dado cuenta&#8230; Y es que los nueves nos ciegan, y no nos acordamos de esas otras tareas que hacen que todo esto gire y funcione.

Esperemos que no me toque nunca algo así.
