---
author: Diego Parrilla
categories:
- google
date: 2009-04-08T08:34:57Z
dsq_thread_id:
- "204693636"
guid: /?p=837
id: 837
tags:
- appengine
- google
- java
title: Google AppEngine para Java. Ya está aquí
url: /2009/04/08/google-appengine-para-java-ya-esta-aqui/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="appengine,google,java" data-count="vertical" data-url="/2009/04/08/google-appengine-para-java-ya-esta-aqui/">Tweet</a>
</div>

<img class="aligncenter size-full wp-image-838" title="appengine_java" src="/wp-content/uploads/appengine_java.png" alt="appengine_java" width="320" height="247" srcset="/wp-content/uploads/appengine_java.png 320w, /wp-content/uploads/appengine_java-300x231.png 300w" sizes="(max-width: 320px) 100vw, 320px" />

Si hubo una petición que se repitió hasta la saciedad en el último Google Developers Day en Madrid fue que Google AppEngine soportara Java. Bueno, pues ya está. En [el blog de Google App Engine podemos leer que ahora va en serio:  Tenemos Java dentro del Google AppEngine](http://googleappengine.blogspot.com/2009/04/seriously-this-time-new-language-on-app.html).

Dicen que Java ha sido el lenguaje que más se ha solicitado. Hay otros, pero está claro que el Rey de los lenguajes es Java desde hace unos 10 años. C sigue vivo, pero la presencia de Java es aplastante. Hay muchas razones para entender que estamos ante el lenguaje de programación de toda una generación de ingenieros, pero creo que la más importante es que su comunidad de desarrolladores ha evitado el &#8216;casarse&#8217; con nadie (Que se lo digan a Sun Microsystems&#8230;).

Las malas lenguas me han contado que Google tenía miedo a liberar Google AppEngine para Java ya que la avalancha de peticiones en su plataforma iba a ser tan brutal que ni ellos tenían recursos para atender la demanda. Por eso empezaron con un lenguaje elitista como Python. Parece que han superado esos problemas de capacidad.

No dan muchos detalles de la implementación dentro de AppEngine, pero comentan que soportará el API de Servlets, JDO (¿cómo?) y JPA (ah&#8230;), javax.cache y javax.mail. No dicen nada de ningún framework de desarrollo tipo Spring, o un MVC tipo Struts&#8230; ¿vamos tener que tirar de Servlets? ¡Espero que no! ¿Usaremos GWT? Creo que sí&#8230; Además hay un [Google Plugin para Eclipse](http://code.google.com/eclipse) que ayudará en el desarrollo ydespliegue.

Una de las restricciones de la plataforma es que corre dentro de un &#8216;sandbox&#8217; que controla lo que se puede hacer dentro de los servidores de Google. Así que seguro que no es coger tu código y desplegar tal cual. Habrá que currarse la adaptación a su plataforma. Por ahora, hay 10.000 cuentas disponibles para pruebas. Así que corre a pedir tu cuenta de pruebas [aquí](http://appengine.google.com/promo/java_runtime).

Está claro que Google sigue trabajando duro en su apuesta de Platform as a Service (PaaS), y abrir la plataforma a Java es acceder a un mercado de millones de desarrolladores y prácticamente la totalidad de los estudiantes de Ingeniería Informática (o Ciencias de la Computación fuera de España). Creo que como solución enterprise todavía es muy limitada, pero el Cloud Computing sigue bajando los gastos necesarios para montar una startup gracias a soluciones de este tipo. ¡Enhorabuena Google!

**Actualización**: Me ha pasado Pedro Navarro de Abiquo este un video con una demostración de la plataforma y su integración con eclipse
