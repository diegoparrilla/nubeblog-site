---
author: Diego Parrilla
bttc_cache:
- "1283694588:11"
categories:
- iaas
date: 2010-03-29T11:38:00Z
dsq_thread_id:
- "204895349"
guid: /?p=1156
id: 1156
tags:
- cloud
- opensolaris
- solaris
title: Solaris puede dejar de ser gratuito y nadie sabe que será de OpenSolaris
url: /2010/03/29/solaris-puede-dejar-de-ser-gratuito-y-nadie-sabe-que-sera-de-opensolaris/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="cloud,opensolaris,solaris" data-count="vertical" data-url="/2010/03/29/solaris-puede-dejar-de-ser-gratuito-y-nadie-sabe-que-sera-de-opensolaris/">Tweet</a>
</div>

<img class="aligncenter size-full wp-image-1154" title="sun_oracle_logo" src="/wp-content/uploads/sun_oracle_logo.jpg" alt="sun_oracle_logo" width="500" height="375" srcset="/wp-content/uploads/sun_oracle_logo.jpg 500w, /wp-content/uploads/sun_oracle_logo-300x225.jpg 300w" sizes="(max-width: 500px) 100vw, 500px" />

Si te preguntas a qué viene esta entrada en un blog de Cloud Computing, lee un poquito más y te enterarás. Acaba de aparecer la siguiente noticia en InfoWorld: &#8216;[Los cambios en la licencia de Sun Solaris deja a los usuarios en una encrucijada](http://www.infoworld.com/d/open-source/license-change-leaves-sun-solaris-users-crossroads-858)&#8216;. Hasta ahora, para usar Solaris solo había que registrarse en la web de Sun, descargarse el Solaris 10 y recibir el documento que acredita que puedes usar el Sistema Operativo sin soporte por tiempo indefinido. Pero al parecer, Oracle ha añadido las siguientes frases al documento de licencia:

> Please remember, your right to use Solaris acquired as a download is limited to a trial of 90 days, unless you acquire a service contract for the downloaded Software.

El movimiento es claro: quieren aumentar el ratio de conversión de usuarios de Solaris gratuitos a Solaris de pago. ¿Pero lo van a conseguir con un contrato de prueba de 90 días? Red Hat anunció que en el último cuarto que una de sus 18 últimos contratos con más de un $1M fueron por convertir usuarios gratuitos a usuarios de pago. Supongo que este movimiento Oracle lo habrá estudiado con cuidado y sabrá lo que hace, pero parece cuando menos arriesgado: quitar a un usuario un privilegio es el camino más rápido para cabrearle (aunque sea un usuario gratuito).

¿Y qué pasa con OpenSolaris? Pues la cosa no parece muy clara tampoco la verdad. En el blog de Ben Rockwood (se hace eco de la noticia) comenta lo que es un secreto a voces: [Oracle no está apoyando OpenSolaris](http://www.cuddletech.com/blog/pivot/entry.php?id=1120).  La anunciada OpenSolaris 2010.03 no llega y se acaba el mes de Marzo y dicen que nadie se atreve a decir nada al respecto. Por ahora, no hay cambio de licencia en OpenSolaris (sigue siendo CDDL).

¿Y esto cómo afecta a la Nube? Pues bastante, ya que OpenSolaris es probablemente el mejor sistema operativo pensado para convertir las Infrestructuras en Servicios. De hecho, es el sistema operativo base de unos cuantos proveedores Públicos como [Joyent](http://www.joyent.com) y [DAAS](http://www.daas.com), y es usado por unos cuantos proveedores de Nube Privada como [VMOps](http://www.vmops.com), [A-Serve](http://www.a-server.com)r y la propia Joyent. Y en [Abiquo](http://www.abiquo.com) lo usamos como uno de nuestros sistemas de almacenamiento (ZFS). Estas empresas han creado soluciones completas (virtualización, almacenamiento, redes) sobre OpenSolaris, una pila de servicios. Esto es un gran ahorro de costes en desarrollo de las soluciones y en su mantenimiento, sin duda, pero se puede correr el riesgo quedarse fuera de juego si OpenSolaris no evoluciona. Esta es una ventaja competitiva de Abiquo respecto al resto: no nos hemos casado con ninguna plataforma.

La razón principal por la que OpenSolaris y Solaris encajan tan bien en las arquitecturas altamente virtualizadas viene de lejos y tiene que ver con el compromiso de los ingenieros de Sun. Si se deja de soportar OpenSolaris estos productos pueden perder esta ventaja tecnológica frente al resto. La comunidad OpenSolaris es fuerte y con mucha presencia, pero lo estamos viendo en Linux: son las grandes empresas las que sostienen a Linux metiendo mucho dinero en su mantenimiento y constante actualización. Y esa era exactamente la labor de Sun, y de la que no sabemos nada en Oracle.
