---
author: Diego Parrilla
categories:
- cloud
- paas
date: 2008-11-19T10:02:14Z
dsq_thread_id:
- "216820014"
guid: /?p=327
id: 327
tags:
- amazon
- cloudfront
title: 'Por fin llegó: CloudFront, la Content Delivery Network de Amazon'
url: /2008/11/19/por-fin-llego-cloudfront-la-content-delivery-network-de-amazon/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,cloudfront" data-count="vertical" data-url="/2008/11/19/por-fin-llego-cloudfront-la-content-delivery-network-de-amazon/">Tweet</a>
</div>

[<img class="size-full wp-image-121 alignright" title="logo_aws" src="/wp-content/uploads/logo_aws.gif" alt="" width="164" height="60" />](/wp-content/uploads/logo_aws.gif)El servicio ya se había anunciado hace tiempo, pero ya está aquí la [versión Beta de CloudFront](http://aws.amazon.com/cloudfront/), la [Content Delivery Network](http://en.wikipedia.org/wiki/Content_Delivery_Network) (CDN) de Amazon. Es casi transparente para los usuarios actuales de Amazon S3, y permite distribuir contenido con tasas muy altas de transferencia a través de una red global de servidores de contenido en redes extremo. Siguiendo el esquema de otros servicios Amazon, el modelo es un puro pago por uso, sin desembolso inicial.

CloudFront funciona así: las peticiones se originan desde cualquier lugar del mundo, y se enrutan a alguna de los 14 servidores de contenido en los extremos de la red. Si el contenido no está presente en alguna de estos servidores, entonces se coge la información de S3 y se cachea en los extremos. Los extremos se encuentran localizados en:

  * Estados Unidos: Ashburn (VA), Dallas/Fort Worth, Los Angeles, Miami, Newark, Palo Alto, Seattle y St. Louis
  * _<span style="font-style: normal;">Europa</span>_: Amsterdam, Dublin, Frankfurt y Londres
  * _<span style="font-style: normal;">Asia</span>_: Hong Kong y Tokyo

<div>
  Se cobra por el número de peticiones que se hacen y la cantidad de datos transferidos. El coste varía según la localización: fuera de los Estados Unidos los precios varían y son ligeramente más altos. También se paga por la petición inicial y la transferencia entre el repositorio S3 y el extremo que sirve el contenido.
</div>

<div>
  Los precios por zonas son estos:
</div>

<div>
  <blockquote>
    <h4>
      United States Edge Locations
    </h4>
    
    <h5>
      Data Transfer
    </h5>
    
    <p>
      $0.170 per GB – first 10 TB / month data transfer out<br /> $0.120 per GB – next 40 TB / month data transfer out<br /> $0.100 per GB – next 100 TB / month data transfer out<br /> $0.090 per GB – data transfer out / month over 150 TB
    </p>
    
    <h5>
      Requests
    </h5>
    
    <p>
      $0.010 per 10,000 GET requests
    </p>
    
    <h4>
      European Edge Locations
    </h4>
    
    <h5>
      Data Transfer
    </h5>
    
    <p>
      $0.170 per GB – first 10 TB / month data transfer out<br /> $0.120 per GB – next 40 TB / month data transfer out<br /> $0.100 per GB – next 100 TB / month data transfer out<br /> $0.090 per GB – data transfer out / month over 150 TB
    </p>
    
    <h5>
      Requests
    </h5>
    
    <p>
      $0.012 per 10,000 GET requests
    </p>
    
    <h4>
      Hong Kong Edge Locations
    </h4>
    
    <h5>
      Data Transfer
    </h5>
    
    <p>
      $0.210 per GB – first 10 TB / month data transfer out<br /> $0.160 per GB – next 40 TB / month data transfer out<br /> $0.140 per GB – next 100 TB / month data transfer out<br /> $0.130 per GB – data transfer out / month over 150 TB
    </p>
    
    <h5>
      Requests
    </h5>
    
    <p>
      $0.012 per 10,000 GET requests
    </p>
    
    <h4>
      Japan Edge Locations
    </h4>
    
    <h5>
      Data Transfer
    </h5>
    
    <p>
      $0.220 per GB – first 10 TB / month data transfer out<br /> $0.168 per GB – next 40 TB / month data transfer out<br /> $0.147 per GB – next 100 TB / month data transfer out<br /> $0.137 per GB – data transfer out / month over 150 TB
    </p>
    
    <h5>
      Requests
    </h5>
    
    <p>
      $0.013 per 10,000 GET requests
    </p>
  </blockquote>
</div>

<div>
  A destacar la cantidad de herramientas que arropan el producto nada mas salir:
</div>

  * [Guía de inicio](http://docs.amazonwebservices.com/AmazonCloudFront/latest/GettingStartedGuide/)
  * [Guía para el desarrollador](http://docs.amazonwebservices.com/AmazonCloudFront/2008-06-30/DeveloperGuide/)
  * [FAQ](http://aws.amazon.com/cloudfront/faqs)
  * [Guía de Referencia Rápida](http://s3.amazonaws.com/awsdocs/CF/20080630/cf_qrc_20080630.pdf)
  * [S3 Fox Organizer](http://www.suchisoft.com/ext/s3fox.php), el addon para Firefox

Otra característica interesante es que se puede integrar con Amazon EC2. Puedes configurar un servidor web en EC2 que sirva el contenido dinámico, y delegar el contenido estático a CloudFront. La verdad es que esto no tiene mucho misterio con un servidor Apache y URL rewrite, pero seguro que algo de magia meten por debajo&#8230;

Solo una pega: ¿Por qué no han colocado servidores en Australia y Nueva Zelanda? ¡Allí si que se nota el uso de un CDN!
