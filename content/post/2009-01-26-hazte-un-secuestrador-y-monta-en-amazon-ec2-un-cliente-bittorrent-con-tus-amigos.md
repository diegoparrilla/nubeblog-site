---
author: Diego Parrilla
categories:
- cloud
date: 2009-01-26T08:00:04Z
dsq_thread_id:
- "204693253"
guid: /?p=628
id: 628
tags:
- amazon
- bittorrent
- cloud
- ec2
title: Hazte un secuestrador y monta en Amazon EC2 un cliente bittorrent con tus amigos
url: /2009/01/26/hazte-un-secuestrador-y-monta-en-amazon-ec2-un-cliente-bittorrent-con-tus-amigos/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,bittorrent,cloud,ec2" data-count="vertical" data-url="/2009/01/26/hazte-un-secuestrador-y-monta-en-amazon-ec2-un-cliente-bittorrent-con-tus-amigos/">Tweet</a>
</div>

[<img class="alignright size-full wp-image-632" title="sellers_pinkpanther7" src="/wp-content/uploads/sellers_pinkpanther7.jpg" alt="" width="187" height="300" />](/wp-content/uploads/sellers_pinkpanther7.jpg)Cual [Inspector Clouseau](http://en.wikipedia.org/wiki/Inspector_Clouseau), llega un tio y suelta esto en ComputerWorld.com en plan profeta del Apocalipsis: [&#8220;Amazon cloud could be hijacked to harvest BitTorrent files, researcher says&#8221;](http://www.computerworld.com/action/article.do?command=viewArticleBasic&articleId=9126722) (La Nube de Amazon podría ser secuestrada para cultivar ficheros BitTorrent, dice un investigador). Tras leer esto todas mis alertas se encendieron y puse la máxima atención ya que si efectivamente &#8216;alguien&#8217; puede &#8216;secuestrar&#8217; La Nube de Amazon, eso es muy serio. Pero no se preocupen, mis queridos lectores, que aquí nadie secuestra, ni cultiva, ni nada&#8230; Aquí lo que hay es una falta de rigor que asusta.

Empecemos por el principio: [hace unos días apareció este post en un blog en el que se detalla cómo instalar Torrentflux en una instancia Amazon EC2](http://negatendo.net/blog/2009/01/17/howto-use-amazon-ec2-for-bittorrent/). En este pequeño tutorial se nos explica cómo instalar la AMI adecuada para poder ejecutarla, y cómo instalar [Torrentflux](http://www.torrentflux.com/index.php). Para el que no lo sepa, Torrentflux no es mas que una interfaz web escrita en PHP y MySQL que permite gestionar las descargas bittorrent en un servidor. Tiene alguna funcionalidad chula, como poder administrar múltiples cuentas de usuario (más luego). El blogger nos dice que por unos $75 al mes podemos tener acceso a un cliente bittorrent con velocidades de subida y bajada de órdago. Sin embargo, se olvida decir que en EC2 se paga por ancho de banda consumido, por lo que si abusas del ancho de banda tendrás una bonita factura cada mes. También apunta que tienes 120Gb de espacio disponible en el servidor, pero este espacio se borra cada vez que reinicias la instancia. Así que como almacenamiento persistente de descargas, es una mala idea. Por último, Amazon prohibe expresamente el uso de sus instancias para la compartición de archivos no autorizados.

Así que de una amenaza a la seguridad de Amazon EC2 hemos pasado a un tutorial explicando cómo montar torrentflux en un Linux. Cosa que puedes hacer en cualquier empresa de hosting del mundo, y probablemente más barato que en EC2. Por el camino, [una empresa de seguridad](http://www.gss.co.uk/) se monta una película y una publicación seria se lo traga todo. Impresionante.

Hay una cosa cierta en todo esto: pagar $75 (mínimo) al mes por tener un cliente bittorrent funcionando es una gilipollez. Lo siento, pero pagar casi $1000 al año por descargarte contenido que luego tienes que bajarte a tu entorno local me parece un sinsentido. Puede que haya ISPs que reduzcan el ancho de banda para clientes P2P, pero lo mismo podría hacer Amazon.

Hay una cosa que no comenta el artículo que es interesante: la posibilidad de crear cuentas de usuario en Torrentflux y que cada uno pueda descargar los contenidos que quiera sin interferir en los demas. Se puede configurar el número de descargas máxima por usuario, profundidad de la cola, ancho de banda de subida y de bajada&#8230; Así que si tienes un grupo de amigos que quiera compartir gastos, igual lo de los $1000 no es para tanto. Y digo lo de grupo de amigos ya que en el momento en que alguien se lucre compartiendo contenido protegido por copyright estará cometiendo un delito.

Así que no veo razón para montar Torrentflux en La Nube&#8230; ¿o si?
