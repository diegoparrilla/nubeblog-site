---
author: Diego Parrilla
categories:
- amazon
- empresas
date: 2009-03-17T11:10:33Z
dsq_thread_id:
- "204693576"
guid: /?p=781
id: 781
tags:
- amazon
- hosting
title: Amazon y su nuevo servicio de reserva de instancias para EC2
url: /2009/03/17/amazon-y-su-nuevo-servicio-de-reserva-de-instancias-para-ec2/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,hosting" data-count="vertical" data-url="/2009/03/17/amazon-y-su-nuevo-servicio-de-reserva-de-instancias-para-ec2/">Tweet</a>
</div>

[<img class="aligncenter size-full wp-image-121" title="logo_aws" src="/wp-content/uploads/logo_aws.gif" alt="" width="164" height="60" />](/wp-content/uploads/logo_aws.gif)

Ya se que han pasado unos cuantos días [de esta noticia](http://www.elasticvapor.com/2009/03/amazon-reserves-right-to-host-your.html), pero quería escribir un poco sobre ella ya que implica un cambio radical en el posicionamiento de Amazon Web Services, y creo que vale la pena analizarlo.

La semana pasada Amazon Web Services anunció que permitirá reservar instancias de su servicio Elastic Computing Cloud (EC2 para los amigos) mediante prepagos por período de uno y tres años. La newsletter dice: &#8220;Es una opción para hacer un pago único más barato para reservar capacidad y por lo tanto reducir los cargos por hora de uso. Como las instancias &#8216;on-demand&#8217;, solo vas a pagar por la capacidad que realmente vas a consumir, y cuando no usas la instancia, no se cargará por su uso&#8221;.

Es decir, tu pagas por adelantado la reserva por uno o tres años, y ellos te aplican una tarifa especial. El servicio es realmente intersante si tienes sistemas funcionando 24&#215;7. Los descuentos son realmente interesantes:

<table class="tan-table" style="padding: 0px; height: 132px;" border="0" cellspacing="0" cellpadding="0" width="452">
  <tr bgcolor="#eeeecc">
    <td style="border-left: 1px solid #eeeecc; font-size: 12px; vertical-align: bottom;" valign="bottom">
      <strong>Standard Reserved Instances</strong>
    </td>
    
    <td style="vertical-align: middle;" width="125" valign="bottom">
      <strong>1 yr Term</strong>
    </td>
    
    <td style="vertical-align: middle;" width="125" valign="bottom">
      <strong>3 yr Term</strong>
    </td>
    
    <td style="border-right: 1px solid #eeeecc; vertical-align: middle;" width="150" valign="bottom">
      <strong>Usage</strong>
    </td>
  </tr>
  
  <tr>
    <td style="border-left: 1px solid #eeeecc;" width="250">
      Small (Default)
    </td>
    
    <td>
      $325
    </td>
    
    <td width="125">
      $500
    </td>
    
    <td style="border-right: 1px solid #eeeecc;" width="150">
      $0.03 per hour
    </td>
  </tr>
  
  <tr>
    <td style="border-left: 1px solid #eeeecc;" width="250">
      Large
    </td>
    
    <td>
      $1300
    </td>
    
    <td width="125">
      $2000
    </td>
    
    <td style="border-right: 1px solid #eeeecc;" width="150">
      $0.12 per hour
    </td>
  </tr>
  
  <tr>
    <td style="border-left: 1px solid #eeeecc;" width="250">
      Extra Large
    </td>
    
    <td>
      $2600
    </td>
    
    <td width="125">
      $4000
    </td>
    
    <td style="border-right: 1px solid #eeeecc;" width="150">
      $0.24 per hour
    </td>
  </tr>
  
  <tr bgcolor="#eeeecc">
    <td style="border-left: 1px solid #eeeecc; font-size: 12px; vertical-align: bottom;" width="250">
      <strong>High CPU Reserved Instances</strong>
    </td>
    
    <td style="vertical-align: middle;" valign="bottom">
      <strong>1 yr Term</strong>
    </td>
    
    <td style="vertical-align: middle;" width="125" valign="bottom">
      <strong>3 yr Term</strong>
    </td>
    
    <td style="border-right: 1px solid #eeeecc; vertical-align: middle;" width="150">
      <strong>Usage</strong>
    </td>
  </tr>
  
  <tr>
    <td style="border-left: 1px solid #eeeecc;" width="250">
      Medium
    </td>
    
    <td>
      $650
    </td>
    
    <td width="125">
      $1000
    </td>
    
    <td style="border-right: 1px solid #eeeecc;" width="150">
      $0.06 per hour
    </td>
  </tr>
  
  <tr>
    <td style="border-left: 1px solid #eeeecc;" width="250">
      Extra Large
    </td>
    
    <td>
      $2600
    </td>
    
    <td width="125">
      $4000
    </td>
    
    <td style="border-right: 1px solid #eeeecc;" width="150">
      $0.24 per hour
    </td>
  </tr>
</table>

Para el caso de una instancia funcionando 24&#215;7, el coste mensual es de unos $72 (sin contar almacenamiento ni ancho de banda). Por lo tanto al año son $864 aproximadamente. Si compramos este servicio, a $0.03 la hora tenemos que al mes pagaríamos unos $22, y al año $264. A esto le sumamos los $325 de reserva y nos quedan $589 al año. Una ahorro de más del 30%.

Cuando leí la noticia lo primero que pensé es cómo Amazon Web Services está ocupando espacios de otros de manera lenta y silenciosa. Y ahora va a por el espacio del **Virtual Private Server** (VPS). Se ha alineado en precio con ellos (incluso más barato que ellos), **pero ofrece lo que ellos no dan: servicios Cloud como autoescalado y autogestión muy poderosa**.  Esto viene a corroborar otra tendencia que veo, y es la progresiva comoditización de los servicios de virtualización de servidores. Ya da igual que tecnología de virtualización me ofrezcas, lo que quiero es tener un valor añadido para gestionarlas.

¿Qué van a hacer los proveedores de VPS? Mi opinión es que el VPS pasará a ser Cloud Hosting, los proveedores de hosting ofrecerán servicios similares a los de Amazon Web Services. La cuestión aquí es cual encontrará un servicio de valor añadido de bajo coste que permita atraer clientes y retenerlos.
