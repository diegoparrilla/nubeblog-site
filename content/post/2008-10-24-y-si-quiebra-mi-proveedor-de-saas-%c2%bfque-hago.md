---
author: Diego Parrilla
categories:
- saas
date: 2008-10-24T09:41:56Z
dsq_thread_id:
- "204894496"
guid: /?p=166
id: 166
tags:
- negocios
- opinion
- saas
title: Y si quiebra mi proveedor de SaaS, ¿qué hago?
url: /2008/10/24/y-si-quiebra-mi-proveedor-de-saas-%c2%bfque-hago/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="negocios,opinion,saas" data-count="vertical" data-url="/2008/10/24/y-si-quiebra-mi-proveedor-de-saas-%c2%bfque-hago/">Tweet</a>
</div>

[<img class="alignright size-medium wp-image-170" title="bankrupt" src="/wp-content/uploads/bankrupt.jpg" alt="" width="300" height="200" srcset="/wp-content/uploads/bankrupt.jpg 500w, /wp-content/uploads/bankrupt-300x200.jpg 300w" sizes="(max-width: 300px) 100vw, 300px" />](/wp-content/uploads/bankrupt.jpg)Me ha surgido esta duda cuando me han comentado hoy que hay algún ministerio y/o administración que está usando Google Maps -además sustituyendo a software propietario de primer nivel-. Y me he preguntado, ¿qué pasa si quiebra Google?

Evidentemente Google no va a quebrar a corto plazo (ni a medio, ni a largo), pero esto me sirve para sacar un tema recurrente en el mundo del IaaS y SaaS: ¿Qué pasa si mi proveedor por cualquier causa ajena a mi voluntad deja de darme el servicio?

La respuesta es clara: **estás jodido**. Vale, creo que en esto estamos todos de acuerdo, ¿pero y ahora qué hacemos? Ojalá tuviera una respuesta satisfactoria a esto, pero me temo que no la hay y probablemente no la haya. Si tu proveedor de Servicios desaparece porque un tsunami arrasa Alcobendas, o habían invertido todo en bonos de Lehman Brothers bien aconsejados por su banco de confianza, necesitas tener un Plan B que te permita continuar con ti negocio: tu propio y personal Plan de Continuidad del Negocio.

Si estamos hablando de SaaS, entonces lo primero y fundamental es no perder los datos que tienes en tu proveedor. Así que implementa una política de backups adecuada, o bien contrata el servicio de backup de datos a otros soportes que algunos servicios ya ofrecen. Con esto no hemos solucionado el problema de la Continuidad del Negocio, pero por lo menos tienes los datos en tus manos.

Si tu proveedor SaaS es crítico para tus servicios, entonces tienes que buscar una alternativa que te permita replicar el servicio que te daba el proveedor. Si lo que tenías era el SugarCRM como SaaS, entonces puedes montar de nuevo el servicio localmente e importar los datos. Pero no creo que todos los proveedores quieran abrir su código y liberarlo.

Hay otras opciones para el código cerrado. Hace unos años trabajé en una empresa que usaba un producto software extremadamente caro y &#8216;raro&#8217;. La empresa desarrolladora del paquete era muy pequeña y mi empresa muy grande (más de 50000 empleados). Sin embargo, mi empresa consideró que ese software podía darle ventaja sobre los competidores así que adquirió licencias, y esto es lo importante, contrató un servicio de custodia del código fuente del producto ([source code escrow](http://en.wikipedia.org/wiki/Source_code_escrow)).

¿Qué es un servicio de custodia del código fuente del producto? Pues un servicio que dan ciertas empresas para asegurar que, en caso de que un proveedor de software no pueda seguir con su negocio, sus clientes puedan recuperar el código fuente de sus productos mediante el pago de una tarifa periódica. Así, cada año o cada nueva versión del producto, el fabricante de software entrega el código fuente al custodio. El custodio sólo entregará el código fuente cuando se cumplan las condiciones del contrato entre las partes, normalmente la desaparición del fabricante por la causa que sea.

Hace poco [he descubierto que ya existen estos servicios para SaaS](http://www.escroweurope.com). Así que es una opción interesante a tener en cuenta, tanto por los clientes como por los proveedores, ya que elimina una de las trabas de entrada de SaaS en las empresas.
