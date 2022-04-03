---
up: [[ITN Module 11 MOC]]
---
# Unidifusión, difusión y multidifusión de IPv4
## Unidifusión

En el tema anterior, aprendió acerca de la estructura de una dirección IPv4; cada una tiene una parte de red y una parte de host. Existen diferentes formas de enviar un paquete desde un dispositivo de origen, y estas diferentes transmisiones afectan a las direcciones IPv4 de destino.

La transmisión unidifusión se refiere a un dispositivo que envía un mensaje a otro dispositivo en comunicaciones uno a uno.

Un paquete de unidifusión tiene una dirección IP de destino que es una dirección de unidifusión que va a un único destinatario. Una dirección IP de origen sólo puede ser una dirección de unidifusión, ya que el paquete sólo puede originarse de un único origen. Esto es independientemente de si la dirección IP de destino es una unidifusión, difusión o multidifusión.

Reproduzca la animación para ver un ejemplo de transmisión de unidifusión.

![[Pasted image 20220402203142.png]]
![[Pasted image 20220402203155.png]]

> En este curso, toda la comunicación entre dispositivos es unidifusión a menos que se indique lo contrario.

Las direcciones de host de unidifusión IPv4 están en el rango de direcciones de 1.1.1.1 a 223.255.255.255. Sin embargo, dentro de este intervalo existen muchas direcciones reservadas para fines específicos. Estas direcciones de propósito especial se discutirán más adelante en este módulo.

## Dirección

Transmisión de transmisión hace referencia a un dispositivo que envía un mensaje a todos los dispositivos de una red en comunicaciones unipersonales.

Los paquetes de difusión tienen una dirección IPv4 de destino que contiene solo números uno (1) en la porción de host.

**Nota:** IPv4 usa paquetes de difusión. Sin embargo, no hay paquetes de difusión con IPv6.

Todos los dispositivos del mismo dominio de difusión deben procesar un paquete de difusión. Un dominio de difusión identifica todos los hosts del mismo segmento de red. Una transmisión puede ser dirigida o limitada. Una difusión dirigida se envía a todos los hosts de una red específica. Por ejemplo, un host de la red 172.16.4.0/24 envía un paquete a la dirección 172.16.4.255. Se envía una difusión limitada a 255.255.255.255. De manera predeterminada, los routers no reenvían transmisiones por difusión.

Reproduzca la animación para ver un ejemplo de transmisión de difusión limitada.

![[Pasted image 20220402231232.png]]
![[Pasted image 20220402231245.png]]

Los paquetes de difusión usan recursos en la red y hacen que cada host receptor en la red procese el paquete. Por lo tanto, se debe limitar el tráfico de difusión para que no afecte negativamente el rendimiento de la red o de los dispositivos. Debido a que los routers separan los dominios de difusión, la subdivisión de redes puede mejorar el rendimiento de la red al eliminar el exceso de tráfico de difusión.

**Difusiones dirigidas por IP**

Además de la dirección de difusión 255.255.255.255, hay una dirección IPv4 de difusión para cada red, llamada difusión dirigida. Esta dirección utiliza la dirección más alta de la red, que es la dirección donde todos los bits de host son 1s. Por ejemplo, la dirección de difusión dirigida para 192.168.1.0/24 es 192.168.1.255. Esta dirección permite la comunicación con todos los hosts de esa red. Para enviar datos a todos los hosts de una red, un host puede enviar un solo paquete dirigido a la dirección de difusión de la red.

Un dispositivo que no está conectado directamente a la red de destino reenvía una difusión dirigida IP de la misma manera que reenvía paquetes IP de unidifusión destinados a un host de esa red. Cuando un paquete de difusión dirigida llega a un router que está conectado directamente a la red de destino, ese paquete se transmite en la red de destino.

**Nota**: Debido a problemas de seguridad y abuso previo de usuarios malintencionados, las transmisiones dirigidas se desactivan de forma predeterminada a partir de Cisco IOS Release 12.0 con el comando de configuración global **no ip directed-broadcasts**.

## Multidifusión

La transmisión de multidifusión reduce el tráfico al permitir que un host envíe un único paquete a un grupo seleccionado de hosts que estén suscritos a un grupo de multidifusión.

Un paquete de multidifusión es un paquete con una dirección IP de destino que es una dirección de multidifusión. IPv4 reservó las direcciones de 224.0.0.0 a 239.255.255.255 como rango de multidifusión.

Los hosts que reciben paquetes de multidifusión particulares se denominan clientes de multidifusión. Los clientes de multidifusión utilizan servicios solicitados por un programa cliente para subscribirse al grupo de multidifusión.

Cada grupo de multidifusión está representado por una sola dirección IPv4 de destino de multidifusión. Cuando un host IPv4 se suscribe a un grupo de multidifusión, el host procesa los paquetes dirigidos a esta dirección de multidifusión y los paquetes dirigidos a la dirección de unidifusión asignada exclusivamente.

Los protocolos de enrutamiento como OSPF utilizan transmisiones de multidifusión. Por ejemplo, los routeres habilitados con OSPF se comunican entre sí mediante la dirección de multidifusión OSPF reservada 224.0.0.5. Sólo los dispositivos habilitados con OSPF procesarán estos paquetes con 224.0.0.5 como dirección IPv4 de destino. Todos los demás dispositivos ignorarán estos paquetes.

En la animación, se muestran clientes que aceptan paquetes de multidifusión.

![[Pasted image 20220402231419.png]]
![[Pasted image 20220402231430.png]]

## Activity - Unicast, Broadcast, or Multicast
![[Pasted image 20220402231554.png]]