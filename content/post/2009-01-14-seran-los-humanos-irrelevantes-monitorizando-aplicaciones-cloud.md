---
author: Diego Parrilla
categories:
- cloud
- opinion
date: 2009-01-14T10:27:22Z
dsq_thread_id:
- "204693193"
guid: /?p=565
id: 565
tags:
- arquitectura
- monitorizacion
- opinion
title: ¿Serán los humanos irrelevantes monitorizando aplicaciones Cloud?
url: /2009/01/14/seran-los-humanos-irrelevantes-monitorizando-aplicaciones-cloud/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="arquitectura,monitorizacion,opinion" data-count="vertical" data-url="/2009/01/14/seran-los-humanos-irrelevantes-monitorizando-aplicaciones-cloud/">Tweet</a>
</div>

> <div>
>   &#8220;&#8230;se aprobara el presupuesto del Skynet. El sistema se conectara el 4 de agosto de 1997, se eliminaran las decisiones humanas en la defensa estrategica, Skynet aprendera en progresion geometrica. Tendra conciencia de si mismo a las 2 y 14 de la madrugada, del 29 de agosto. Los humanos aterrados intentaran desconectarlo.&#8221;<br /> -Pero Skynet se defendera&#8230;
> </div>
> 
> <div style="text-align: right;">
>   Terminator 2.
> </div>

<div style="text-align: left;">
  Este <a href="http://cloudcomputing.sys-con.com/node/804549">post en Cloud Computing Journal</a> me ha hecho recordar dos cosas: a <a href="http://www.imdb.com/title/tt0103064/">Terminator</a> y al difunto<a href="http://www.google.es/url?sa=t&source=web&ct=res&cd=3&url=http%3A%2F%2Fbooks.google.es%2Fbooks%3Fid%3DimoDH0HnNv8C%26pg%3DPR8%26lpg%3DPR8%26dq%3D%2522jose%2Bcuena%2522%2Bobituary%26source%3Dbl%26ots%3Da0RJ3e1X0l%26sig%3D9LqF96B1bSU6vWZuy4yduRtoUtA%26hl%3Den%26sa%3DX%26oi%3Dbook_result%26resnum%3D3%26ct%3Dresult&ei=Ug9tSaqnE9TIjAfNw5CjDA&usg=AFQjCNGioBuElI9l2DJUrQLb-TPJJjozxA&sig2=lYAlVETeLZRz2AMaYjEbTA"> Profesor José Cuena</a>. Tras el provocador título &#8216;¿Son los humanos realmente necesarios para mantener un SLA en La Nube?&#8217;, el artículo trata sobre lo complicado que es monitorizar los servicios en La Nube cuando están cambiando de manera constante. Se lanzan más servidores para gestionar más carga, se quitan servidores cuando ya no son necesarios. Pero&#8230; ¿cómo se detecta si hay más o menos carga? ¿Qué políticas hay que implementar? En esto estoy de acuerdo, son políticas complicadas y diferentes a las que existen en un Centro de Datos tradicional.
</div>

<div style="text-align: left;">
  El Profesor Cuena era una personalidad a nivel mundial en el campo de los Sistemas Expertos. Aunque nunca llegué a interesarme por este campo, muchas de sus clases podían considerarse Clases Maestras. Se sentaba, y empezaba a hablar sobre lo que él pensaba de la materia. Consideraba que un Sistema Experto que tomaba decisiones por si mismo era un Sistema Experto Paleto. Tal cual. <strong>Los Sistemas Expertos deben ayudar a la decisión del humano, pero no deben tomar decisiones por si mismos</strong>. Claro, probablemente también había visto Terminator, como yo.
</div>

<div style="text-align: left;">
  Hace unos días <a href="http://blogs.smugmug.com/don/2008/06/03/skynet-lives-aka-ec2-smugmug/">revisé un post en el Blog de SmugSmug</a> recopilando información sobre Arquitecturas para el Cloud Computing. Y planteaban el mismo escenario: dado que es muy complicado controlar manualmente el escalado de una aplicación en La Nube, lo mejor es implementar un servicio que se encargue de ello de manera automática. Este proceso Controlador lo llamaron <a href="http://es.wikipedia.org/wiki/Skynet_(Terminator)">Skynet</a>, que cachondos. En un amago de toma de conciencia de si mismo, levantó más de 250 máquinas virtuales tamaño XL de Amazon EC2 sin que fuera necesario. Una &#8216;paletada&#8217;. Por suerte la factura no fue muy alta. La gente de SmugSmug asume que la única manera de ser eficiente y flexible es delegando esta tarea completamente a este controlador &#8216;Skynet&#8217; (aun a riesgo de que comience la primera guerra hombres contra máquinas 😉 )
</div>

<div style="text-align: left;">
  Estoy llegando a la conclusión de que una Arquitectura Orientada al Cloud Computing debe incluir este controlador/skynet <em>de serie</em>. Es decir, aunque no me guste, debemos ceder el control del escalado de manera absoluta a este proceso controlador. Habrá que implementar restricciones para que la lógica de este servicio sea la correcta (siguiendo con el juego de las películas, como <a href="http://es.wikipedia.org/wiki/RoboCop">las directivas primarias de Robocop</a>) pero desgraciadamente los humanos somos un recurso demasiado caro como para estar dedicados a monitorizar las necesidades de escalado de una aplicación en tiempo de ejecución. Para confirmar un poco más esta afirmación, la arquitectura que han implementado la gente de <a href="https://scalr.net/login.php">Scalr </a>es muy similar a la de SmugSmug, o la que yo tengo en mente.
</div>
