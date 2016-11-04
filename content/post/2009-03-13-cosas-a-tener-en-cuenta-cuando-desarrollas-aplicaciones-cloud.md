---
author: Diego Parrilla
categories:
- arquitectura
date: 2009-03-13T00:12:55Z
dsq_thread_id:
- "204693569"
guid: /?p=773
id: 773
tags:
- arquitectura
- desarrollo
title: Cosas a tener en cuenta cuando desarrollas aplicaciones Cloud
url: /2009/03/13/cosas-a-tener-en-cuenta-cuando-desarrollas-aplicaciones-cloud/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="arquitectura,desarrollo" data-count="vertical" data-url="/2009/03/13/cosas-a-tener-en-cuenta-cuando-desarrollas-aplicaciones-cloud/">Tweet</a>
</div>

No es habitual encontrar gente que hable sobre los desarrolladores en el mundo del Cloud Computing. Estamos tan cegados por las facilidades que nos ofrece, que nos olvidamos que no todas las aplicaciones están preparadas para aprovechar sus ventajas.

No lo entiendo.

La única explicación que encuentro a esto es la inmadurez del paradigma. Vamos, que todavía no hay mucha gente que se haya dedicado a desarrollar aplicaciones que aprovechen al máximo la potencia del Cloud Computing. Y los que lo han hecho, son todavia los visionarios y los &#8216;early adopters&#8217;.

[Paul Krill en Infoworld enumera algunas de las cosas a tener en cuenta](http://www.infoworld.com/archives/emailPrint.jsp?R=printThis&A=/article/09/03/11/10NF-cloud-app-dev_1.html). Resumiendo:

  * **Evita almacenar el estado o estados de tu aplicacion en cualquier sitio que no sea la base de datos**. La vieja cantinela del &#8216;El estado es el infierno&#8217; que casi todos los desarrolladores web que han tenido que desplegar en cluster ya conocen. Si un nodo falla, debe poderse recuperar el estado con facilidad.
  * **Diseña tu aplicación para que autoaprovisione sus recursos**. Las aplicaciones solicitarán los recursos que necesiten bajo demanda, cuando lo necesiten. Es un cambio fundamental respecto a las aplicaciones enterprise tradicionales, y único del Cloud Computing.
  * **Usa las bases de datos en La Nube adaptándote a sus características**. Las bases de datos en La Nube no siguen el modelo relacional. Así que hay que diseñar las aplicaciones teniendo en cuenta las nuevas formas de acceso a datos. Especialmente importante es por ejemplo que la propiedad de Consistencia [ACID](http://databases.about.com/od/specificproducts/a/acid.htm) no se garantiza en algunos proveedores Cloud, como Amazon SimpleDB, que implementa &#8216;[Consistencia Eventual](http://peat.wordpress.com/2007/12/20/eventual-consistency-explained/)&#8216;, en mi opinión una fuente potencial de problemas enorme.
  * **Las aplicaciones en la Nube cambian más rápido**. Parece que es un hecho esto; es más fácil incorporar cambios en aplicaciones tipo SaaS. Si te basas en ellas, debes tener en cuenta que pueden cambiar y mucho. Y tus aplicaciones también pueden cambiar más. Y es que una característica del Cloud Computing como la autogestión de los entornos tiene como efecto secundario la subida más frecuente de cambios a los entornos de producción.
  * **Cuidado con los modelos de precios y licencias**. Cada proveedor de Cloud tiene su propio esquema de precios, así que haz tus cuentas antes de desarrollar, para que no haya sorpresas. Por ejemplo, en una aplicación desarrollada que usaba Amazon SimpleDB fui capaz de reducir la factura mensual en más de un 90% implementando una caché de nivel 2 en la aplicación.

¿Qué otras cosas debemos considerar en el diseño de nuestras aplicaciones?
