---
author: Diego Parrilla
categories:
- cloud
- opinion
date: 2009-02-06T17:03:05Z
dsq_thread_id:
- "206188364"
guid: /?p=677
id: 677
tags:
- arquitectura
title: Arquitecturas Software para el Cloud Computing
url: /2009/02/06/arquitecturas-software-para-el-cloud-computing/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="arquitectura" data-count="vertical" data-url="/2009/02/06/arquitecturas-software-para-el-cloud-computing/">Tweet</a>
</div>

Los viernes son un día para cerrar cosas en el trabajo. No dejar cosas abiertas ayuda a planificar las nuevas tareas que se abrirán con el próximo lunes. Además, esta semana ha sido especial porque hay cambios, cambios que anunciaré próximamente.

Llevo semanas reflexionando sobre cómo afecta a los equipos de desarrollo las nuevas plataformas de escalado dinámico que tenemos en La Nube. No debemos olvidar que una plataforma tiene éxito si es adoptada por los desarrolladores. Los ejemplos son claros en las plataformas tradicionales como **J2EE,** **.NET** o **RoR**. Pero en el mundo de las **PaaS** y las **IaaS** la cosa no está tan clara.

Las [**Platform as a Service** o](/2008/10/15/saas-iaas-y-paas-las-tres-clases-de-cloud-computing/) [PaaS](/2008/10/15/saas-iaas-y-paas-las-tres-clases-de-cloud-computing/) tipo **Google AppEngine**, **Microsoft Azure** y **Sun Caroline** son una raza completamente nueva de plataformas, y por lo tanto necesitan de un nuevo tipo de Arquitectura. Lo cierto es que no tengo claro cual es el modelo a seguir, seguramente porque son plataformas muy verdes todavía y su planteamiento de Arquitectura Software probablemente romperá con lo conocido en la actualidad.

Sin embargo, creo que las [**Infrastructure as a Service o IaaS**](/2008/10/15/saas-iaas-y-paas-las-tres-clases-de-cloud-computing/) como **Amazon Web Services** o **GoGrid**, se aprovecharán de las arquitecturas software de referencia existentes en el mundo enterprise. En [HighScalability.com](http://highscalability.com) -un blog de referencia si estás metidos en temas de arquitectura- hay un articulo interesante en el que se describe lo que ellos llaman una [Arquitectura de Referencia Canónica](http://highscalability.com/canonical-cloud-architecture) [para el Cloud Computing](http://highscalability.com/canonical-cloud-architecture). En esta arquitectura no se describe nada revolucionario, ni falta que hace. Lo que se describe es una arquitectura típica enterprise altamente desacoplada, casi abusando de los procesos asíncronos. Añaden componentes imprescindibles en un entorno que se auto ajusta (me gusta más _self-healing_ en inglés, pero en español suena fatal), y hecho en falta decir de manera explícita que en cualquier sistema escalable el **Estado es el Infierno** ([State is Hell](http://www.artima.com/intv/distrib4.html)) y que las soluciones sin estado son las más escalables -en La Nube o en tu casa&#8230;-.

Una lectura interesante para el fin de semana.
