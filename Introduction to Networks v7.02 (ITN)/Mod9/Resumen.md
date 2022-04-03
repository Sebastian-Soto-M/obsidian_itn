---
up: [[ITN Module 9 MOC]]
---
# Resumen

## [[Media Access Control|MAC]] e IP

Las direcciones físicas de capa 2 (es decir, las direcciones [[Media Access Control|MAC]] de [[Ethernet]]) se utilizan para entregar la trama de enlace de datos con el paquete [[Internet Protocol|IP]] encapsulado de una [[Network Interface Card]] a otra [[Network Interface Card]] que está en la misma red. Si la dirección [[Internet Protocol|IP]] de destino está en la misma red, la dirección [[Media Access Control|MAC]] de destino es la del dispositivo de destino. Cuando la dirección [[Internet Protocol|IP]] de destino ([[IP versión 4|IPv4]] o [[IP versión 6|IPv6]]) está en una red remota, la dirección [[Media Access Control|MAC]] de destino será la dirección de gateway predeterminada del host (es decir, la interfaz del router). A lo largo de cada enlace de una ruta, un paquete [[Internet Protocol|IP]] se encapsula en una trama. El trama es específico de la tecnología de enlace de datos asociada a ese vínculo, como [[Ethernet]]. Si el dispositivo del siguiente salto es el destino final, la dirección [[Media Access Control|MAC]] de destino es la de la [[Network Interface Card]] [[Ethernet]] del dispositivo. ¿Cómo se asocian las direcciones [[Internet Protocol|IP]] de los paquetes [[Internet Protocol|IP]] en un flujo de datos con las direcciones [[Media Access Control|MAC]] en cada enlace a lo largo de la ruta hacia el destino? Para los paquetes IPv4, esto se realiza a través de un proceso llamado ARP. Para los paquetes [[IP versión 6|IPv6]], el proceso es [[Protocolo de Descubrimiento de Vecinos versión 6|ICMPv6 ND]].

## ARP

Cada dispositivo [[Internet Protocol|IP]] de una red [[Ethernet]] tiene una dirección [[Media Access Control|MAC]] [[Ethernet]] única. Cuando un dispositivo envía una trama de capa 2 de [[Ethernet]], contiene estas dos direcciones: dirección [[Media Access Control|MAC]] de destino y dirección [[Media Access Control|MAC]] de origen. Un dispositivo utiliza ARP para determinar la dirección [[Media Access Control|MAC]] de destino de un dispositivo local cuando conoce su dirección IPv4. ARP proporciona dos funciones básicas: resolver direcciones [[IP versión 4|IPv4]] a direcciones [[Media Access Control|MAC]] y mantener una tabla de asignaciones de direcciones [[IP versión 4|IPv4]] a MAC. La solicitud ARP se encapsula en una trama [[Ethernet]] utilizando esta información de encabezado: direcciones [[Media Access Control|MAC]] de origen y destino y tipo. Solo un dispositivo de la [[Local Area Network|LAN]] tiene la dirección [[IP versión 4|IPv4]] que coincide con la dirección [[IP versión 4|IPv4]] objetivo de la solicitud de ARP. Todos los demás dispositivos no envían una respuesta. La respuesta ARP contiene los mismos campos de encabezado que la solicitud. Solamente el dispositivo que envió inicialmente la solicitud de ARP recibe la respuesta de ARP de unicast. Una vez que recibe la respuesta de ARP, el dispositivo agrega la dirección [[IP versión 4|IPv4]] y la dirección [[Media Access Control|MAC]] correspondiente a su tabla ARP. Cuando la dirección [[IP versión 4|IPv4]] de destino no está en la misma red que la dirección [[IP versión 4|IPv4]] de origen, el dispositivo de origen debe enviar la trama al gateway predeterminado. Esta es la interfaz del router local. Para cada dispositivo, un temporizador de memoria caché ARP elimina las entradas de ARP que no se hayan utilizado durante un período especificado. Los comandos también se pueden usar para eliminar manualmente algunas o todas las entradas de la tabla ARP. Como una trama de difusión, todos los dispositivos de la red local reciben y procesan una solicitud ARP, lo que podría hacer que la red se desacelere. Un atacante puede usar la ARP spoofing para realizar un ataque de ARP poisoning.

## Detección de Vecinos

IPv6 no utiliza ARP, utiliza el protocolo ND para resolver direcciones MAC. ND proporciona servicios de resolución de direcciones, detección de routers y redirección para [[IP versión 6|IPv6]] mediante ICMPv6. [[Protocolo de Descubrimiento de Vecinos versión 6|ICMPv6 ND]] utiliza cinco mensajes ICMPv6 para realizar estos servicios: solicitud de vecino, anuncio de vecino, solicitud de router, anuncio de router y redirección. Al igual que ARP para IPv4, los dispositivos [[IP versión 6|IPv6]] utilizan [[IP versión 6|IPv6]] ND para resolver la dirección [[Media Access Control|MAC]] de un dispositivo en una dirección [[IP versión 6|IPv6]] conocida.