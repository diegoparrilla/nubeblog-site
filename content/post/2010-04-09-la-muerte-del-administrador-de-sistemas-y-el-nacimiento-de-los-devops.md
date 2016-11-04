---
author: Diego Parrilla
bttc_cache:
- "1283694587:16"
categories:
- administracion
date: 2010-04-09T10:46:13Z
dsq_thread_id:
- "204895413"
guid: /?p=1165
id: 1165
tags:
- arquitectura
- devops
- sysadmins
title: La muerte del Administrador de Sistemas y el nacimiento de los &#8216;Devops&#8217;
url: /2010/04/09/la-muerte-del-administrador-de-sistemas-y-el-nacimiento-de-los-devops/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="arquitectura,devops,sysadmins" data-count="vertical" data-url="/2010/04/09/la-muerte-del-administrador-de-sistemas-y-el-nacimiento-de-los-devops/">Tweet</a>
</div>

[<img class="size-full wp-image-458 alignleft" title="cola-del-paro" src="/wp-content/uploads/cola-del-paro.jpg" alt="" width="248" height="248" srcset="/wp-content/uploads/cola-del-paro.jpg 248w, /wp-content/uploads/cola-del-paro-150x150.jpg 150w" sizes="(max-width: 248px) 100vw, 248px" />](/wp-content/uploads/cola-del-paro.jpg)

He comentado en varias ocasiones que sigo a [James Urquhart en su blog](http://news.cnet.com/wisdom-of-clouds/). Es un tío interesante, un visionario de verdad. Vale la pena seguirle.

Hace cosa de un mes empezó una serie de artículos sobre la evolución que se está dando en el perfil de los Administradores de Sistemas, los [&#8216;grandes damnificados&#8217;](http://www.itproportal.com/portal/news/article/2010/4/8/ca-set-pink-slip-1000-employees/) de la evolución a las Infraestructuras como Servicios. Para ello, introduce un nuevo perfil llamado &#8216;[Devops](http://www.slideshare.net/jurquhart/the-new-devops-designers-cloud-and-the-big-rethink)&#8216;. Este término fue introducido por Jesse Robins, el CEO de [Opscode](http://www.opscode.com/). Opscode son los creadores de [Chef](http://wiki.opscode.com/display/chef/Home), un framework para traer de manera programática los beneficios de la Gestión de la Configuración a la infraestructura. Devops es la combinación de &#8216;developer&#8217; y &#8216;operations&#8217;, ya que la tendencia es a que las operaciones sean programadas usando este tipo de herramientas. Es decir, pasamos de unas operaciones reactivas, centradas en los procesos, a unas más ágiles y automatizadas.

La aparición de este nuevo rol viene dada por los cambios que la automatización y la virtualización (servidores, almacenamiento, redes) conllevan: que las operaciones sobre los sistemas se pueden desacoplar de la parte física. Los sistemas operativos ya no están en servidores físicos, los volúmenes no están asociados a los discos duros, y las conexiones entre máquinas no tienen que pasar por puertos físicos en el switch.

Ahora, en la era del Cloud Computing, es posible desplegar soluciones que casi ignoren la necesidad de operaciones sobre la infraestructura física. Casi, porque todavía hay cosas como la seguridad que no están bien resueltas. Así, la infraestructura pasa a ser &#8216;el problema de otro&#8217;, y de ahí la importancia de las grandes nubes en el futuro y el outsourcing de la infraestructura en los próximos años.

En el Cloud Computing la unidad de despliegue es la &#8216;Aplicación&#8217; (a mi me gusta más llamarlo la &#8216;Solución&#8217;, ya que estamos hablando de unir hardware -virtual- y software en un mismo paquete). Ahora mismo casi todas las soluciones están centradas en la máquina virtual más que en la &#8216;Aplicación&#8217;. Dado que la &#8216;Aplicación&#8217; pasa a ser el principal centro de atención ya que describe sus necesidades hardware, su arquitectura y políticas que se deben aplicar a la aplicación (en Alta Disponibilidad, Ancho de banda reservado de XMb, etc&#8230;), **la Aplicación dicta sus propias necesidades**.

Esta situación genera tensión entre los equipos de desarrollo y los equipos de operaciones. Los equipos de desarrollo hacen la arquitectura mínima para asegurar el despliegue, y &#8216;le pasan el marrón&#8217; a los de operaciones. A su vez, los equipos de operaciones toman actitudes defensivas definiendo restricciones, normas y reglas para los despliegues.

En los despliegues en las nuevas plataformas de Cloud, los equipos de desarrollo y sistemas tienen que trabajar juntos para que la &#8216;Aplicación&#8217; cuando se despliegue gestione tantas necesidades operativas como sea posible. **Para conseguir esto, todo el ecosistema de la aplicación debe poderse gestionar a través del software.**

Hacer esto dentro del código es posible, pero no es portable. La solución propuesta por Urquhart es el uso de Políticas de Aplicación. Definición de reglas, parámetros y trozos de (pseudo?)código para decirle a la infraestructura qué hacer en nombre de la aplicación. Estas políticas se le enchufan al Proveedor Cloud por medio de un API y listo.

La manera de estandarizar esto es definiendo un estándar para las políticas y otro para comunicarse con las plataformas (API). Pero la cosa está muy verde y hay muchos intereses. Llevará años. Mientras tanto, los proveedores de infraestructura nos tenemos que poner las pilas y permitir que las soluciones permitan configuraciones muy dinámicas.

Tras leer esto, ¿un Administrador de Sistemas se debe echar a temblar? Todo el poder pasa a los desarrolladores? Donde queda la infraestructura física?, alguien la tiene que gestionar! Mi opinión personal es que los desarrolladores SÍ tendrán más poder, y entraran en partes del diseño de la solución que antes no entraban. Bueno, esto ya está pasando por ejemplo cuando construyen soluciones para Amazon EC2. Los Administradores de Sistemas tal y como los conocemos seguirán gestionando el hardware con un ratio administrador/máquina gestionada mucho mayor (por la automatización). Aunque las necesidades de computación aumentan cada vez más rápidamente, creo que muchos administradores pasarán a tomar este nuevo rol.

Este nuevo perfil, el de Devops, es intrigante.  Mientras que el trabajo de desarrollador es un trabajo necesariamente monohilo (no más de una tarea al mismo tiempo), con ciclos de trabajo largos (una historia, un caso de uso, un Sprint&#8230;), un administrador es justo lo contrario, multihilo y con ciclos cortos. Por lo que he visto en Abiquo con Chef, el trabajo de administrador se parece más al de un desarrollador. Me imagino que un Devop hará sobre un Virtual Datacenter lo mismo que hace ahora mismo sobre un servidor, más la gestión de políticas de servicio, por ejemplo. El uso de un lenguaje de script parece necesario, pero una GUI que haga esas tareas por tí y luego cree las &#8216;Aplicaciones&#8217; tambien suena atractivo. Esto último se acerca a la visión de Abiquo para el diseño de las soluciones.
