---
author: Diego Parrilla
categories:
- arquitectura
- cloud
- datacenter
- empresas
- opensource
- openstack
- stackops
date: 2011-03-23T13:33:49Z
dsq_thread_id:
- "261062969"
guid: /?p=2021
id: 2021
tags:
- distro
- nova
- openstack
- stackops
title: 'Stackops Distro &#038; Smart Installer: despliega Openstack en tu centro de
  datos'
url: /2011/03/23/stackops-distro-smart-installer-despliega-openstack-en-tu-centro-de-datos/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="distro,nova,openstack,stackops" data-count="vertical" data-url="/2011/03/23/stackops-distro-smart-installer-despliega-openstack-en-tu-centro-de-datos/">Tweet</a>
</div>

<img class="alignright" title="Stackops Distro" src="http://stackops.s3.amazonaws.com/STACKOPSLOGO-SMALL.png" alt="" width="320" height="132" />Durante estas últimas semanas nos hemos reunido con unas cuantas empresas interesadas en Infraestructuras como Servicios, y a todas les encantaba lo que Openstack Nova promete. La idea de tener una plataforma verdaderamente abierta y que haya un ecosistema de empresas a su alrededor es muy atractivo. Los participantes en Openstack son empresas con una reputación más que consolidada y reconocida por los profesionales. Todo parece perfecto&#8230; ¿Todo? No&#8230;

En un momento dado de la conversación, siempre sale la siguiente pregunta:

> **¿Cómo despliego Openstack en mi centro de datos?**

Y entonces es cuando empezábamos con los juegos florales, el chauchaubulebú y otras artimañas más propias de vendedores de humo que de tecnología&#8230; porque montar Openstack Nova no es (bueno, era) trivial ni mucho menos. Puedes pasarte días consultando su documentación y lo más probable es que no pases mas allá de una instalación en un servidor de toda la arquitectura. Ideal para hacer alguna prueba rápida, pero muy lejos de lo que es una Infraestructura como Servicio.

Recientemente han aparecido interesantes herramientas que automatizan el despliegue de los nodos. Eso está genial, pero se olvidan de algo que es básico en el despliegue de Openstack Nova: no es un conjunto de servidores, es una plataforma en la que **los servicios se encuentran entrelazados a un nivel superior al del sistema operativo**, por lo que es necesario algo o alguien que &#8216;orqueste&#8217; ese despliegue.

Nos dimos cuenta que la mayoría de la gente pasa por tres etapas básicas en la puesta en marcha de una _solución tipo_ con Openstack Nova: **Toma de Contacto, Prueba de Concepto y Piloto,** más una etapa final que es la **Puesta en Producción**. El número de empresas que empieza una toma de contacto es muy alto, sin embargo por razones obvias quienes llegan a Producción son los menos. El mercado potencial de empresas que acabarán poniendo en Producción (y que serán por tanto clientes) puede ser menos del 1% de las que instalan una Toma de Contacto, menos de un 10% de las que despliegan una Prueba de Concepto, y menos de un 50% de las que montan un Piloto con sus clientes. Es imposible dimensionar una startup para que atienda de manera directa a los potenciales clientes, especialmente en las dos primeras fases.  Por lo tanto, si quieres llegar a una audiencia muy alta y poder escalar globalmente debíamos ser capaces de **definir arquitecturas de despliegue que pudieran satisfacer las demandas de cada etapa** con un soporte por nuestra parte mínimo, de modo desatendido y automático.

Y por supuesto&#8230; debía funcionar. Un Administrador de Sistemas debía encontrar una **dificultad similar a la que hay instalando un VMware ESXi o un Citrix XenServer**. Ni más ni menos.

<img class="alignright size-medium wp-image-2023" title="distro-1" src="/wp-content/uploads/distro-1-300x225.png" alt="" width="300" height="225" srcset="/wp-content/uploads/distro-1-300x225.png 300w, /wp-content/uploads/distro-1.png 640w" sizes="(max-width: 300px) 100vw, 300px" />
  
Y así es como nos lanzamos a construir la **Stackops Openstack Nova Distro**. Una distribución basada en Ubuntu 10.04 LTS Server que contiene todo lo necesario para desplegar una solución Openstack Nova. Solo aquello que es necesario para que funcione Openstack. La distribución puede configurarse para que pueda tomar diferentes roles de la arquitectura: Controller, Volume, Network y Compute.

[<img class="alignright size-medium wp-image-2024" title="smart-installer-4" src="/wp-content/uploads/smart-installer-4-300x223.png" alt="" width="300" height="223" srcset="/wp-content/uploads/smart-installer-4-300x223.png 300w, /wp-content/uploads/smart-installer-4-1024x764.png 1024w, /wp-content/uploads/smart-installer-4.png 1053w" sizes="(max-width: 300px) 100vw, 300px" />](/wp-content/uploads/smart-installer-4.png)
  
[<img class="alignright size-medium wp-image-2026" title="smart-installer-5" src="/wp-content/uploads/smart-installer-5-300x176.png" alt="" width="300" height="176" srcset="/wp-content/uploads/smart-installer-5-300x176.png 300w, /wp-content/uploads/smart-installer-5-1024x603.png 1024w, /wp-content/uploads/smart-installer-5.png 1074w" sizes="(max-width: 300px) 100vw, 300px" />](/wp-content/uploads/smart-installer-5.png)
  
Pero una distribución bare-metal no soluciona el problema de la configuración de un despliegue: se necesita algo más. Y por eso desarrollamos el Stackops Smart Installer. **El Smart Installer es un agente embebido en la distro que habla con una aplicación web hosteada por nosotros y que ayuda al administrador a desplegar alguna de las arquitecturas de despliegue de referencia anteriormente mostradas**. ¿Quieres desplegar en una máquina virtual para hacer una prueba rápida? Ok, no hay problema. ¿Quieres una arquitectura con múltiples nodos? Tampoco hay problema: el Smart Installer guarda aquellos parámetros globales a la arquitectura y los inyecta cuando es necesario. Se acabó el infierno de parámetros globales y locales a los componentes. El Asistente se encarga de llevar el control de éstos.

Pero lo mejor es que la Distro y el Smart Installer son gratuitos. [Podéis bajar la ISO y probar desde ya sobre una máquina virtual](http://www.stackops.org), o si tienes una granja de servidores hacer un despliegue complejo asistido. Y claro, si necesitas una personalización, [contactar con nosotros](http://www.stackops.com/contact-us/) 😉

¡Disfrutadlo!
