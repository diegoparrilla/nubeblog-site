---
author: Diego Parrilla
categories:
- cloud
- grid
date: 2010-12-24T16:12:11Z
dsq_thread_id:
- "204892916"
guid: /?p=1928
id: 1928
tags:
- amplia
- caida
- cloud
- grid
- skype
title: Aprendiendo de las caídas de servicio de Skype
url: /2010/12/24/aprendiendo-de-las-caidas-de-servicio-de-skype/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amplia,caida,cloud,grid,skype" data-count="vertical" data-url="/2010/12/24/aprendiendo-de-las-caidas-de-servicio-de-skype/">Tweet</a>
</div>

[<img class="size-full wp-image-1930 alignright" title="skype" src="/wp-content/uploads/skype.jpg" alt="" width="280" height="280" srcset="/wp-content/uploads/skype.jpg 400w, /wp-content/uploads/skype-150x150.jpg 150w, /wp-content/uploads/skype-300x300.jpg 300w" sizes="(max-width: 280px) 100vw, 280px" />](/wp-content/uploads/skype.jpg)Skype ha sido noticia de nuevo [tres años después de su última caída del servicio](/2007/08/17/skype-outage-has-cost-more-than-11000-per-second-to-ebay/). Y en un momento horrible, ya que están preparando su salida a bolsa&#8230;

Hace unos años me tocó hacer un análisis de la arquitectura de Skype para una operadora que estaba interesada en conocer su funcionamiento sobre las emergentes redes de datos 3G. Las operadoras ya intuían hace años que Skype era una seria amenaza para sus intereses, y de ahí su interés. Aprendí mucho sobre el funcionamiento de la red P2P subyacente, y muchas cosas sorprendentes. Recomiendo esta magnífica presentación del [Black Hat Europe 2006](http://www.blackhat.com/presentations/bh-europe-06/bh-eu-06-biondi/bh-eu-06-biondi-up.pdf). Canela fina.

Desde el punto de vista de arquitectura software el producto es simplemente acojonante. Sus diseñadores se adelantaron 10 años a los problemas que hoy conocemos como &#8216;Neutralidad de la Red&#8217; y construyeron su software con [los principios que hoy asumimos para las soluciones Grid y Cloud](http://blogs.gartner.com/lydia_leong/2010/12/03/designing-to-fail/). Su software está diseñado para seguir funcionando ante fallos y cualquier eventualidad en su red P2P&#8230; ¿Entonces qué ha pasado? Bueno&#8230; desde el punto de vista de arquitectura de sistemas, trabajaron con una pre-requisito muy arriesgado: no queremos tener que gestionar y administrar nuestra infraestructura. Y este es el truco: el precio que pagan los usuarios por usar Skype es que &#8216;ceden&#8217; su hardware a la Red de Skype para dar servicio.

Desde el punto de vista económico parece un negocio redondo: &#8220;podemos ofrecer servicios a cientos de millones de personas de manera gratuita gracias a un software resiliente a fallos, los ordenadores de los usuarios donde se ejecuta, y la red de banda ancha que empezaba a cubrir el globo&#8221;. El coste del servicio tiende a cero, y Skype se puede mantener gracias a otros servicios de valor añadido como SkypeIn o SkypeOut que sí usan la infraestructura y por lo tanto pagan por ella. Brillante&#8230; ¿no? Bueno, las cosas no son siempre tan bonitas&#8230;

Skype no es una red pura P2P, ya que necesita de servicios de autenticación y autorización de usuarios que se encuentran centralizados y gestionados por Skype Inc. Creo que tienen más de 250 millones de usuarios registrados, y es fácil ver conectados diariamente a varias decenas de millones. Estos servicios son los que nos identifican en la red de manera única y nos permiten acceder a los servicios premium (con estos no voy a meterme). Durante la caída del año 2007, [una actualización de Microsoft Windows](http://techcrunch.com/2007/08/20/windows-users-caused-skype-outage/) que hizo reiniciar de manera masiva a ordenadores de todo el mundo hizo que estos servicios colapsaran por no estar dimensionados para soportar tal avalancha de peticiones de autenticación y autorización concurrentes. Es decir, todos los clientes skype del mundo empezaron a logarse en la red al mismo tiempo. Y Skype no pudo con ello. También hace 3 años la red tardó en recuperarse.

Para que Skype funcione es necesario que haya un número suficiente de lo que ellos llaman &#8216;supernodos&#8217;. En realidad un supernodo no es mas que un ordenador cualquiera que se conecta a internet de manera directa, sin un firewall. Estos nodos hacen de &#8216;intermediarios&#8217; entre los clientes que se encuentran detrás de los firewalls de empresas y particulares. Los supernodos mantienen el &#8216;directorio&#8217; de usuarios de Skype y su localización de manera distribuida. Hay una buena [explicación de su funcionamiento en este blog](http://www.disruptivetelephony.com/2010/12/understanding-todays-skype-outage-explaining-supernodes.html). La caída de servicio esta vez se achaca a un fallo en el software que hace que los supernodos &#8216;casquen&#8217; al cabo de unos minutos de funcionamiento. Es decir, Skype se quedó huérfano de intermediarios que gestionaran su infraestructura: Skype dejó de existir. Rápidamente se solucionó el problema software, se distribuyó y los ingenieros de sistemas levantaron &#8216;meganodos&#8217; que hicieron las labores de los supernodos.

En 2007 esto nos hizo reflexionar sobre el impacto de las actualizaciones Over The Air (OTA) en dispositivos móviles y especialmente en los M2M y los procedimientos a seguir, ya que se trata de un problema similar. Una de las diferencias de una arquitectura Grid sobre una Cloud es precisamente que los recursos están garantizados en esta última. **Skype tiene una arquitectura donde es imposible garantizar un Nivel de Servicio, ya que no se tiene control sobre la arquitectura que la soporta**. Y esta es una de las causas para el fracaso del Grid y el éxito del Cloud. **En el Cloud Computing es posible definir Niveles de Servicios ya que se tiene control de la infraestructura**.

¿Y ahora qué hará Skype? Lo primero es mandar un mensaje de confianza&#8230; que tiene que salir a Bolsa. Luego, debería plantearse realmente si debe invertir en construir una capa de &#8216;supernodos&#8217; en una nube pública que le permita mantener un nivel mínimo de servicio de manera permanente: el impacto económico no creo que sea muy grande, y seguro que es menor que el coste en imagen que está sufriendo.
