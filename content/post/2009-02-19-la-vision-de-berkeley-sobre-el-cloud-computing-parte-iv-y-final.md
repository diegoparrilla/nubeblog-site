---
author: Diego Parrilla
categories:
- cloud
- estudios
date: 2009-02-19T13:54:06Z
dsq_thread_id:
- "204693433"
guid: /?p=716
id: 716
tags:
- amazon
- berkeley
- estudios
- google
- iaas
- microsoft
- paas
- saas
title: La visión de Berkeley sobre el Cloud Computing. Parte IV y final
url: /2009/02/19/la-vision-de-berkeley-sobre-el-cloud-computing-parte-iv-y-final/
---

<div style="float: right; margin-left: 10px;">
  <a href="https://twitter.com/share" class="twitter-share-button" data-via="nubeblog" data-hashtags="amazon,berkeley,estudios,google,iaas,microsoft,paas,saas" data-count="vertical" data-url="/2009/02/19/la-vision-de-berkeley-sobre-el-cloud-computing-parte-iv-y-final/">Tweet</a>
</div>

Ir a [La visión de Berkeley sobre el Cloud Computing. Parte I](../2009/02/16/la-vision-de-berkeley-sobre-el-cloud-computing-parte-i/)

Ir a [La visión de Berkeley sobre el Cloud Computing. Parte II](/2009/02/17/la-vision-de-berkeley-sobre-el-cloud-computing-parte-ii/)

Ir a [La visión de Berkeley sobre el Cloud Computing. Parte III](/2009/02/18/la-vision-de-b…ting-parte-iiila-vision-de-berkeley-sobre-el-cloud-computing-parte-iii/)

Para concluir, los autores nos muestran el &#8216;Top Ten&#8217; de los impedimentos para la adopción del Cloud Computing, tanto tecnológicos como de negocio:

**1.- Disponibilidad del Servicio**

Según los autores, los clientes tienen miedo a no tener un nivel de servicio adecuado. Creo que están equivocados, esto es algo que ahora mismo es secundario. Es importante, pero no es la primera preocupación, hay otras. **Se empieza a asumir que la disponibilidad de los servicios en La Nube es alta.** 

Una ventaja que argumentan es que los servicios en una Nube tienen **mayor capacidad de defensa ante un DDoS** (Distributed Denial of Service). Cierto, pero debes tener un bolsillo muy profundo para soportar un ataque así, ya que por otro lado tenemos EDoS (Economical Denial Of Service). Más información en [este otro post sobre el tema](/2009/01/27/los-riesgos-del-escalado-automatico-edos-economic-denial-of-sustainability/).

**2.- Clientes cautivos de un proveedor(Vendor Lock-in)**

Este si que es un problema interesante. La naturaleza actual de las soluciones de Cloud Computing son cerradas. Hay multitud de APIs propietarios, pero al final eres cautivo de tu proveedor.

La solución sería estandarizar los APIs y formatos de los objetos, para poder transitar cómodamente de un proveedor a otro. **Evidentemente, los proveedores ya asentados no les interesa seguir este camino**. Pero hay muchos actores que para entrar en este negocio sí les puede interesar apostar por la estandarización. Y aquí es donde el opensource puede ser la llave que permita implantar soluciones estándar que beneficien a los Cloud Users.

**3.- Confidencialidad de la información y auditabilidad**

Los almacenes de datos deben regirse bajo diferentes legislaciones en diferentes países o regiones. Y esto va en contra de la naturaleza del Cloud Computing, que es ubiquo. Seguro que encriptando los datos y garantizando su trazabilidad conseguimos cumplir las más exigentes legislaciones, pero es complicado cumplirlas todas en todos los casos.

En mi opinión, el nacimiento de Clouds geolocalizadas es inminente, y no va a ser por requisitos técnicos, sino púramente legislativos.

**4.- Cuellos de botella en la transferencia de datos**

Los requisitos de almacenamiento de datos para algunas aplicaciones puede ser gigantesco. Por ello, el coste de transferencia puede dispararse, y el coste de contratación de ancho de banda puede ser gigantesco.

No lo veo como un impedimento, sino como una restricción de la tecnología actual. Es cuestión de tiempo que los costes bajen y sea más barato transferir un disco duro entero entre Nubes que enviarlo por un mensajero.

**5.- Rendimiento impredecible**

La virtualización ha conseguido una separación entre máquinas virtuales fantástica cuando hablamos de CPU y de memoria RAM, pero sin embargo la Entrada/Salida (I/O) sigue siendo un problema. Lo cierto es que una máquina virtual que haga uso intensivo de la entrada salida afecta al resto de las máquinas virtuales.

De nuevo nos encontramos con un problema propio de la inmadurez de la tecnología. Los proveedores de hardware empiezan a diseñar sistemas pensando en ser virtualizados. Estos sistemas deberán tener en cuenta el problema de la entrada y salida y actuar en consecuencia.

**6.-Almacenamiento escalable**

Mientras que el almacenamiento escala hacia arriba, no se ha encontrado un modelo que sea capaz de soportar escalado hacia abajo de los datos, o de &#8216;envejecimiento&#8217;. Es decir, pagar por los datos que usas más recientemente y no por todos los que tienes almacenados.

Esto es un reto. Hay proveedores que [dicen haber conseguido esto](/2008/11/11/emc-atmos-nueva-solucion-de-almacenamiento-cloud-optimized-storage/), pero bueno, hay que verlo funcionando.

**7.-Bugs en sistema altamente escalables**

Por la naturaleza de las soluciones masivas altamente escalables, reproducir un error en un entorno local es complicado, y si el bug tiene que ver con la naturaleza de la infraestructura subyacente que soporta la aplicación entonces será más complicado.

La solución a este problema es complicada, y puede que no tenga solución. Los que llevamos trabajando en el mundo Java unos cuantos años hemos visto como las soluciones opensource que han cogido suficiente tracción y que tienen muchos usuarios tienen menos bugs que las soluciones propietarias. Aprovecho aquí para dar un enorme tirón de orejas a Oracle/BEA, Sun e IBM. Espero que aprendan de JBoss. Por eso, una solución opensource puede ayudar a encontrar problemas más fácilmente.

**8.-Escalado (suficientemente) rápido**

Las demandas de picos a veces pueden predecirse y otras veces no (digged, meneado, slashdotted&#8230;). El escalado puede necesitarse de manera instantánea debido a esta demanda inesperada. El no poder escalar a tiempo puede hacer que duranto unos minutos el sistema no responda como espera el cliente y perdamos la oportunidad. Soluciones como EC2 son más sensible a este problema, pero Google AppEngine parece que es transparente.

Otra cuestión es la fracción de pago del escalado. Si tu pico ha durado unos pocos minutos, pagarás por la fracción de tiempo contratada. En el caso de EC2, por horas.

Los autores no han visto Terminator y por eso proponen máquinas que escalen solas y que aprendan, para poder reaccionar a tiempo a la demanda. [Ya sabéis mi opinión al respecto](/2009/01/14/seran-los-humanos-irrelevantes-monitorizando-aplicaciones-cloud/).

**9.-Reputación compartida entre Cloud Users y Cloud Providers
  
** 

La mala práxis de un Cloud User (por ejemplo un spammer) puede afectar al resto de los usuarios y a un proveedor de Cloud. Pongamos el caso de un spammer que usa IPs de EC2 y son puestas en listas negras de antispammers. En ese caso un cliente puede poner en riesgo la reputación de Amazon.

Creo que este argumento es igual de válido para cualquier proveedor de hosting o de housing, o un ISP. Deben tener especial cuidado con las IPs que se asignan a sus clientes, para evitar que se metan en este tipo de listas. No es un argumento propio del Cloud Computing, por lo tanto.

**10.-Licencias de software**

El modelo de compra de licencias o de alquiler perpetuo ya no valen. Se debe pasar a un modelo donde se paguen por el tiempo que se usan las licencias. Una de las razones del éxito de los productos opensource en La Nube es que no tienes que preocuparte por esto. Los modelos posibles son variados, pero deben adaptarse al &#8216;pay as you go&#8217;. Microsoft Windows en Amazon EC2 tiene un sobrecoste de $0.05 por hora, e IBM está trabajando en una tabla de conversión de pago por CPU a pago por uso sobre Amazon EC2. Una sugerencia hecha por los autores es pasar a un modelo de &#8216;prepago&#8217; de uso de CPU. Es decir, pagar por adelantado el uso aproximado del sistema durante uno, dos o tres años, al mismo tiempo que se negocian los contratos de mantenimiento. Una buena idea.

**Conclusiones**

Finalmente el Cloud Computing está emergiendo. Se han dado la combinación de factores que ha hecho que empiece a despegar. Aún quedan muchas incógnitas que resolver, especialmente cual será el papel de los medianos y pequeños proveedores de hosting contra los grandes proveedores.

La otra gran cuestión es qué características arquitectónicas deberán tener las aplicaciones que aprovechen el Cloud Computing, que pueden correr sobre cientos o miles de máquinas virtuales iguales:

  * La aplicación debe poder escalar hacia arriba y hacia abajo de manera sencilla y rápida.
  * El software de infraestructura debe estar pensado para correr sobre máquinas virtuales y no sobre el metal.
  * Los sistemas hardware deben pasar de diseñarse para racks a diseñarse para containers. Además, el hardware debe ser energéticamente eficiente cuando el sistema esté ocioso. Otra cuestión importante es que el hardware deberá tener en cuenta la virtualización y sus características (cuellos de botella de entrada/salida, por ejemplo)
