---
author: Diego Parrilla
bttc_cache:
- "1283694588:7"
categories:
- virtualización
date: 2010-03-09T07:53:09Z
dsq_thread_id:
- "204895312"
guid: /?p=1148
id: 1148
tags:
- hypervisor
- oracle
- sun
title: ¿Puede ser Oracle un actor importante en el mundo de la virtualización?
url: /2010/03/09/puede-ser-oracle-un-actor-importante-en-el-mundo-de-la-virtualizacion/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="hypervisor,oracle,sun" data-count="vertical" data-url="/2010/03/09/puede-ser-oracle-un-actor-importante-en-el-mundo-de-la-virtualizacion/">Tweet</a>
</div>

<img class="aligncenter size-full wp-image-1154" title="sun_oracle_logo" src="/wp-content/uploads/sun_oracle_logo.jpg" alt="sun_oracle_logo" width="500" height="375" srcset="/wp-content/uploads/sun_oracle_logo.jpg 500w, /wp-content/uploads/sun_oracle_logo-300x225.jpg 300w" sizes="(max-width: 500px) 100vw, 500px" />

Una de las preguntas recurrentes en el mundillo de IT empresarial es cual es la estrategia de Oracle respecto a la virtualización y el Cloud Computing. Pese al esfuerzo que han hecho en explicar su estrategia, el consenso general es que tienen una pequeña empanada mental, y lo peor, los clientes se están dando cuenta.

Pero antes de nada, vamos a hacer un pequeño inventario de qué tiene Oracle en el catálogo-que no es poco- y para qué sirve cada cosa:

  * **Oracle VM:** Este hypervisor es otro sabor más del archiconocido Xen. Al estilo de Citrix con XenServer, Oracle VM ha recubierto el Xen con sus propias (y escasas) herramientas de gestión y lo ha ofrecido como la mejor herramienta posible para correr sus aplicaciones, especialmente su gestor de base de datos sobre su propia versión del Linux, Unbreakeable Linux. No tengo datos de penetración de este hypervisor, pero el sentimiento general es que no lo usa ni Dios, y que el vendor lock-in es tan salvaje (hypervisor+Sistema Opearativo+Base de Datos) que echa para atrás. Además, la presencia de VMware en el campo de batalla natural de Oracle hace que su adopción sea más difícil todavía. De hecho, aunque Oracle se resiste a certificar soluciones sobre VMware, es sin duda la opción preferida para montar soluciones de Oracle Virtualizadas.
  * **VirtualIron:** En 2009 Oracle adquirió esta compañía y después se cepilló su actividad comercial y de soporte, provocando la ira de sus clientes. Dejar a los clientes sin opciones reales de migración hizo que otros ofrecieran actualizaciones competitivas a esos clientes, que con lentitud han pasado a usar VMware e Hyper-V, por ejemplo. Aunque no está claro cual es el futuro de los productos de VirtualIron, parece que el futuro pasa por integrarlos como capa de gestión de Oracle VM.
  * **VirtualBox:** Este hypervisor comprado a Innotek por Sun Microsystems es la estrella opensource de la virtualización en el escritorio. Sin embargo, es el producto elegido por Q-layer y A-Server en la capa de virtualización de sus servidores. También en abiCloud lo usamos como hypervisor para pruebas, pero no lo vemos para producción.
  * **xVM:** El hypervisor de servidor de Sun Microsystems basado en Xen, muy similar a lo que ofrece Oracle VM. De nuevo es un producto que no consiguó toda la tracción que debía tener un producto de servidor de Sun, y tiene todas las papeletas para ser abandona o integrado en el Oracle VM, que parece será la estrella de Oracle.
  * **Solaris Containers:** Es la tecnología de virtualización propia de Solaris. Es una tecnología de virtualización de servidor que aprovecha las magníficas posibilidades de Solaris y OpenSolaris. Sin embargo, su declive frente a Linux principalmente ha evitado la adopción de esta tecnología. Pese a ello, es la opción de virtualización más importante sobre Solaris, y dado que está soportada en OpenSolaris es muy difícil que sea abandona a su suerte.

No he incluido las herramientas de gestión asociadas a cada hypervisor, por no aburrir. Es decir tenemos hasta 5 diferentes hypervisores en el catálogo de productos de la empresa. A todas luces, esto no es sostenible ni por Oracle. Es más que probable que la gran apuesta para competir contra VMware y no quedarse fuera definitivamente de la carrera por la virtualización del centro de datos sea una combinación de Oracle VM, VirtualIron y posiblemente algo de xVM (xVM ops), en un único producto. El futuro de VirtualBox es incierto, como todo proyecto opensource dentro de Oracle, pero dudo que el proyecto muera si Oracle decide cancelarlo: hacer un _fork_ y seguir manteniéndolo siempre sería posible.

El gran problema que tiene Oracle es la percepción que tienen los clientes de su solución: es una solución donde la posibilidad de caer cautivo es mucho mayor que con otras soluciones. Y dado que hay otras soluciones con niveles inferiores de cautividad y sin embargo mayor capacidad y funcionalidad, sin duda estas soluciones le ganarán la batalla. Además, el camino tomado por Oracle poniendo trabas a la certificación de las soluciones de VMware para Oracle no ayuda a mejorar este percepción, sino que la empeora.

La ventaja que tiene Oracle es que dado que su flujo de ingresos viene por la venta de licencias de sus productos enterprise, puede vender (o incluso regalar) las licencias de su futura pila integrada de productos con precios más competitivos que la competencia, que sí depende de la venta de licencias como VMware o Citrix. Pero no es el caso de Microsoft, cuyos ingresos vienen por la venta de licencias del Windows Server. Pero para que un cliente decida optar por la opción de mejor precio primero tiene que demostrar que ofrece un conjunto de funcionalidades y capacidades suficientemente válidas para las necesidades de un centro de datos, y eso todavía Oracle VM no lo hace.

Mañana hablaré de Oracle y el Cloud Computing.
