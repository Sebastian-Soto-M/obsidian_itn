---
up: [[ITN Module 9 MOC]]
---
# Detección de Vecinos IPv6
## Video - Detección de vecinos IPv6
Si su red utiliza el protocolo de comunicaciones IPv6, el protocolo de detección de vecinos o ND es lo que necesita para hacer coincidir las direcciones [[IP versión 6|IPv6]] con las direcciones [[Media Access Control|MAC]] . En este tema se explica cómo funciona ND.

Haga clic en Reproducir en la figura para ver una demostración de Descubrimiento de vecinos IPv6.

To watch the video, go [here](https://contenthub.netacad.com/itn-dl/9.3.1).

## Mensajes de descubrimiento de vecinos IPv6

El protocolo [[IP versión 6|IPv6]] descubrimiento de vecinos se conoce a veces como ND o NDP. En este curso, nos referiremos a él como ND. ND proporciona servicios de resolución de direcciones, detección de routers y redirección para [[IP versión 6|IPv6]] mediante ICMPv6. ICMPv6 ND utiliza cinco mensajes ICMPv6 para realizar estos servicios:

-   NS: Mensajes de solicitud de vecinos.
-   NA: Mensaje de anuncio de vecino
-   RS: Mensaje de solicitud del router
-   RA: Mensajes de anuncio del router. Mensaje de* redirección

Los mensajes de solicitud de vecino y anuncio de vecino se utilizan para la mensajería de dispositivo a dispositivo, como la resolución de direcciones (similar a ARP para [[IP versión 4|IPv4]] ). Los dispositivos incluyen tanto equipos host como routers.

![[Pasted image 20220331101517.png]]

Los mensajes de solicitud de router y anuncio de router son para mensajes entre dispositivos y routers. Normalmente, la detección de routers se utiliza para la asignación dinámica de direcciones y la configuración automática de direcciones sin estado (SLAAC).

![[Pasted image 20220331101609.png]]

> El quinto mensaje ICMPv6 ND es un mensaje de redirección que se utiliza para una mejor selección de siguiente salto. Esto está fuera del alcance de este curso.

IPv6 ND se define en IETF RFC 4861.

## Descubrimiento de vecinos IPv6: resolución de direcciones

Al igual que ARP para [[IP versión 4|IPv4]] , los dispositivos [[IP versión 6|IPv6]] utilizan [[IP versión 6|IPv6]] ND para determinar la dirección [[Media Access Control|MAC]]  de un dispositivo que tiene una dirección [[IP versión 6|IPv6]] conocida.

Los mensajes ICMPv6 Solicitud de vecino y Anuncio de vecino se utilizan para la resolución de la dirección [[Media Access Control|MAC]] . Esto es similar a las solicitudes ARP y las respuestas ARP utilizadas por ARP para [[IP versión 4|IPv4]] . Por ejemplo, supongamos que PC1 desea hacer ping a PC2 en la dirección [[IP versión 6|IPv6]] 2001:db8:acad: :11. Para determinar la dirección [[Media Access Control|MAC]]  de la dirección [[IP versión 6|IPv6]] conocida, PC1 envía un mensaje de solicitud de vecino ICMPv6 como se ilustra en la figura.

![[Pasted image 20220331102036.png]]

Los mensajes de solicitud de vecinos ICMPv6 se envían utilizando direcciones multibroadcast Ethernet e [[IP versión 6|IPv6]] especiales. Esto permite que la NIC Ethernet del dispositivo receptor determine si el mensaje de solicitud de vecino es para sí mismo sin tener que enviarlo al sistema operativo para su procesamiento.

PC2 responde a la solicitud con un mensaje ICMPv6 Neighbor Advertisement que incluye su dirección [[Media Access Control|MAC]] .

## Packet Tracer - Detección de vecinos IPv6
- [[9.3.4-packet-tracer---ipv6-neighbor-discovery_es-XL.pdf]]
- [[9.3.4-packet-tracer---ipv6-neighbor-discovery_es-XL.pka]]