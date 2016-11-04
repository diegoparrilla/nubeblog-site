---
author: Diego Parrilla
categories:
- cloud
date: 2008-10-01T03:56:15Z
dsq_thread_id:
- "216796500"
guid: /?p=3
id: 886
tags:
- amazon
- ec2
- windows
title: Microsoft Windows Server correrá sobre Amazon EC2
url: /2008/10/01/microsoft-windows-server-correra-sobre-amazon-ec2/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,ec2,windows" data-count="vertical" data-url="/2008/10/01/microsoft-windows-server-correra-sobre-amazon-ec2/">Tweet</a>
</div>

[<img class="size-full wp-image-6 alignright" style="border: 0px initial initial;" title="Windows Server on Amazon Web Services EC2" src="/wp-content/uploads/windowsserver2008onawsec2.jpg" alt="" width="200" height="148" />](/wp-content/uploads/windowsserver2008onawsec2.jpg)

Al final tenía que pasar. En el blog del CTO de Amazon, Werner Wogels, se anuncia que [será posible lanzar instancias de Amazon EC2 que soporten Windows Server](http://www.allthingsdistributed.com/2008/09/amazon_ec2_with_microsoft_wind.html). Resulta curioso que uno de los principales argumentos para correr Windows en la nube es que facilitaría la conversión de los contenidos a formatos propietarios de Microsoft (¿No sería más facil usar formatos abiertos?). 

No hay mucha información sobre qué tipo de virtualización se va a usar, aunque creo que XEN no es lo más adecuado para correr Windows (aunque hay gente que lo hace, es un poco rebuscado y con mal rendimiento). Tampoco se dice nada sobre el coste del servicio y lo que yo considero fundamental cómo se licenciará el uso de Windows: ¿se usarán licencias que ya posea el usuario o bien Amazon te &#8216;alquilará&#8217; las licencias en función de uso?

Muchas dudas, pero seguro que poco a poco tendremos más información sobre el tema. Por ahora la beta es privada, pero se puede intentar solicitar la entrada en el grupo de beta testers [aquí](http://aws.amazon.com/windows/).
