---
author: Diego Parrilla
categories:
- grid
date: 2008-10-06T23:54:18Z
dsq_thread_id:
- "206896399"
guid: /?p=54
id: 54
tags:
- grid
- lhc
- oracle
title: 'LCG: Esto es un Grid y lo demás tonterías'
url: /2008/10/06/lcg-esto-es-un-grid-y-lo-demas-tonterias/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="grid,lhc,oracle" data-count="vertical" data-url="/2008/10/06/lcg-esto-es-un-grid-y-lo-demas-tonterias/">Tweet</a>
</div>

Supongo que si estás leyendo este blog probablemente hayas recibido multitud de información sobre el [proyecto Worldwide LHC Computing Grid (LCG)](http://lcg.web.cern.ch/LCG/Default.htm). Si aún no te has enterado de lo que es, es la infraestructura de análisis y almacenamiento de los datos que toda la comunidad de Física de Alta Energía que use el LHC ([El Gran Colisionador de Hadrones](http://es.wikipedia.org/wiki/Gran_colisionador_de_hadrones)) va a utilizar.

El LCG fue diseñado para soportar la inmensa cantidad de datos que los experimentos generarán. Se habla de unos 15 petabytes accesibles a miles de científicos en todo el mundo. Cuando se empezó a gestar el proyecto del LHC, ya se vio que era inviable crear un gran supercentro de cálculo que centralizase el almacenamiento y el procesado de los datos. Inviable económicamente, quiero decir. Así que se pensó en algo que aprovechase la capacidad de almacenamiento y de procesado al que sí tenían acceso los centros de investigación locales de cada pais. La arquitectura está distribuida en 3 capas de procesado de la siguiente manera:

  * Tier-0: Es el CERN Computing Centre. Todos los datos pasan por aquí, pero la capacidad de procesado es del 20% del total.
  * Tier-1: En total siete centros de datos repartidos en varios países. Aproximadamente 30% de procesado.
  * Tier-2: En total 140 sitios agrupados en 38 federaciones que proveerán del 50% de la capacidad e procesado.

Hace unos años tuve acceso a información de Oracle relativa al proyecto. Era realmente espectacular lo que estaban haciendo. He intentado encontrar esa información pero no la he podido localizar (sic), aunque probablemente fuese información sensible. El manejo de un conjunto de datos tan enorme alrededor de una arquitectura con Oracle 10g RAC era impresionante. Creo que es el único producto de código no-abierto de la arquitectura, lo cual dice mucho a favor de Oracle y su capacidad de cálculo. Por lo que me contaron MySQL también participaba de la arquitectura, pero no era el gestor que llevaba el peso del almacenamiento (bueno, lo contaban gente de Oracle, así que tampoco me fio mucho de lo que me contaron&#8230;).

He encontrado [una bonita presentación sobre la arquitectura multicapa del LCG con Oracle](http://www.nesc.ac.uk/talks/608/Day2/3D_talk_Edinburgh_Nov-2005.ppt), que aunque no es la que pude disfrutar, es interesante.
