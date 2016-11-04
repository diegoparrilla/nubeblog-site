---
author: Diego Parrilla
categories:
- cloud
- Uncategorized
date: 2008-11-17T09:11:50Z
dsq_thread_id:
- "204692910"
guid: /?p=291
id: 291
tags:
- caroline
- paas
- sun
title: 'Project Caroline: El Cloud Computing según Sun Microsystems'
url: /2008/11/17/project-caroline-el-cloud-computing-segun-sun-microsystems/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="caroline,paas,sun" data-count="vertical" data-url="/2008/11/17/project-caroline-el-cloud-computing-segun-sun-microsystems/">Tweet</a>
</div>

<p style="text-align: center;">
  <a href="/wp-content/uploads/sun-logo.jpg"><img class="aligncenter size-full wp-image-302" title="sun-logo" src="/wp-content/uploads/sun-logo.jpg" alt="" width="350" height="187" srcset="/wp-content/uploads/sun-logo.jpg 501w, /wp-content/uploads/sun-logo-300x160.jpg 300w" sizes="(max-width: 350px) 100vw, 350px" /></a>
</p>

El viernes leí la noticia de [nuevos despidos en Sun](http://www.theinquirer.es/2008/11/16/sun-microsystem-despidos-reestructuracion-y-software-libre.html). Esto no es nuevo, cada 2 años hacen lo mismo. Me acordé de un chiste malo que me contaron hace unos años sobre Sun y Microsoft:

> &#8211; Tio, no se si hacer este proyecto con Java o con C#&#8230;
> 
> &#8211; Vamos a ver&#8230;¿Tu has visto **Armageddon**?
> 
> &#8211; ¿La de Bruce Willis y el asteroide? Sí, la he visto&#8230;
> 
> &#8211; Pues figúrate que en vez de llamar a Bruce Willis y su banda, tienes que llamar a la mejor empresa de ingeniería informática del mundo: ¿A quién llamarías, a Sun o a Microsoft?
> 
> &#8211; Nos ha jodido, ¡A Sun! ¡A los de Microsoft igual les da un pantallazo azul taladrando el asteroide y se va el planeta al carajo!
> 
> &#8211; Ok. Entonces&#8230; ¿qué vas a elegir para tu proyecto: Java, no?
> 
> &#8211; Pues no lo tengo claro, yo no tengo que salvar el planeta: no necesito tecnología aeroespacial para mi proyecto&#8230;

<p style="text-align: left;">
  Y es que este es el problema de Sun: Han sido cojonudos, pero no todo el mundo necesita de Sun para sacar sus proyectos adelante. Los creadores del &#8216;The network is the computer&#8217; no han hecho mucho ruido en La Nube. Así que me acordé de su proyecto de Cloud Computing: <a href="https://www.projectcaroline.net">Project Caroline</a>. Hay una mastodóntica presentación de ¡2 horas! colgada en la web de Sun de Abril de 2008 que cuenta en detalle la plataforma y las razones para este producto.
</p>

<p style="text-align: center;">
</p>

Aquí va un pequeño resumen:

  * Es una [PaaS](/2008/10/15/saas-iaas-y-paas-las-tres-clases-de-cloud-computing/) completa: Ofrece una virtualización completa de red, computación y almacenamiento.
  * Viene a ofrecer un conjunto de servicios para el despliegue de Servicios Web complejos. Podríamos decir que en este aspecto se parece bastante a [Windows Azure](/2008/11/01/windows-azure-que-es-real-y-que-es-vapor/). Pensado para construir SaaS, usando lenguajes de alto nivel. Es una nueva plataforma, necesitará un nuevo tipo de aplicaciones (pero no es necesario empezar desde cero).
  * Su verdadero fuerte es la virtualización de la computación a nivel de lenguajes: Java, Python, JRuby, PERL&#8230;fuertemente Java Virtual Machine .
  * El equipo de trabajo es de unas 20 personas (atención startups: no hace falta un equipo grande para construir un gran producto).
  * Es un proyecto de investigación y **todo el código es abierto**. Te lo puedes [descargar aquí](https://www.projectcaroline.net/main/index.php?q=node/8). Existe de todos modos el llamado &#8216;Grid de Servicio&#8217; para pruebas.
  * Control programático (gracias a unas APIs) de todos los servicios distribuidos: computación, almacenamiento y redes. Es posible configurar el uso de los recursos en tiempo real. No hay ficheros de configuración. **Los Servicios construyen su propio entorno de ejecución en vez de ser insertados en uno existente.**
  * La virtualización no se hace a nivel de &#8216;hypervisor&#8217; en el Sistema Operativo. Se hace a un nivel superior: por lo tanto, los programas son independientes del hardware, del SSOO y su localización. Lo mismo pasa para las bases de datos y el sistema de ficheros (desarrolladores J2EE, ¿esto no os suena?). **El control de los recursos se delega al desarrollador, en vez de al administrador**.
  * PostgreSQL es la base de datos de la plataforma. Aunque anuncian soporte para MySQL muy pronto (lógico&#8230;).
  * Las redes son ciudadanos de primera por fín en la Nube: hay balanceadores, firewalls, NAT, VPN, DNSs&#8230;
  * Entornos completamentes aislados: no se comparten recursos, excepto a través de internet (la red es privada a cada cuenta). Configuración independiente en cada nodo. No es posible ejecutar librerías nativas. No es posible hacer un fork o un exec. Métricas a nivel de proceso y de hilo.
  * Caroline Tunnels: Depuración en local de recursos remotos. Excelente idea para depurar aplicaciones en la Nube.

Como resumen a la presentación, el sitio [www.projectcaroline.net](http://www.projectcaroline.net) que aloja el proyecto corre sobre la plataforma, pero lo más curioso es que el CMS que usan es Drupal, que está escrito en PHP. Usan [Quercus](http://www.caucho.com/resin-3.0/quercus/) sobre un Apache Tomcat para interpretar el PHP en un servidor Java. Curioso.

La primera impresión es muy interesante. Voy a dedicar más tiempo y otro post a dar mi opinión de lo que he visto, pero necesitaré tiempo&#8230; ese bien tan escaso&#8230;
