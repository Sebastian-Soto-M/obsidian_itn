---
up: [[ITN Module 9 MOC]]
---
# MAC e IP

## Destino en La Misma Red

A veces, un [[Host|host]] debe enviar un mensaje, pero solo conoce la dirección [[Internet Protocol|IP]] del dispositivo de destino. El host necesita saber la dirección [[Media Access Control|MAC]] de ese dispositivo, pero ¿cómo se puede descubrir? Ahí es donde la resolución de direcciones se vuelve crítica.

Hay dos direcciones primarias asignadas a un dispositivo en una [[Local Area Network|LAN]] [[Ethernet]]:

- **Dirección física (la dirección [[Media Access Control|MAC]])** – Se utiliza para comunicaciones [[Network Interface Card|NIC]] a NIC en la misma red [[Ethernet]].
- **Dirección lógica (la dirección [[Internet Protocol|IP]])** – Se utiliza para enviar el paquete desde el dispositivo de origen al dispositivo de destino. La dirección [[Internet Protocol|IP]] de destino puede estar en la misma red IP que la de origen o en una red remota.

Las direcciones físicas de [[Capa de enlace de datos|capa 2]] (es decir, las direcciones [[Media Access Control|MAC]] de [[Ethernet]]) se utilizan para entregar la trama de enlace de datos con el paquete [[Internet Protocol|IP]] encapsulado de una [[Network Interface Card|NIC]] a otra NIC que está en la misma red. Si la dirección IP de destino está en la misma red, la dirección MAC de destino es la del dispositivo de destino.

Considere el siguiente ejemplo utilizando representaciones de direcciones [[Media Access Control|MAC]] simplificadas.

La imagen es un diagrama de red con PC 1 en IP 192.168.10.10/24 con MAC simplificado aa-aa-aa, conectado a un switch en IP 192.168.10.0/24, conectado a PC 2 en IP 192.168.10.11/24 con MAC simplificado 55-55. Debajo del diagrama hay cuatro cuadros que leen de izquierda a derecha: Destino MAC 55-55, MAC de origen aa-aa-aa, IPv4 192.168.10.10 y Destino IPv4 192.168.10.11.

![[Pasted image 20220329175449.png]]

En este ejemplo, PC1 desea enviar un paquete a PC2. La figura muestra las direcciones [[Media Access Control|MAC]] de origen y destino de [[Capa de enlace de datos|capa 2]] y el direccionamiento [[IP versión 4|IPv4]] de [[Capa de red|capa 3]] que se incluirían en el paquete enviado desde PC1.

La [[Trama de Red|Trama]] Ethernet de [[Capa de enlace de datos|capa 2]] contiene lo siguiente:

- **Dirección [[Media Access Control|MAC]] de destino**: esta es la dirección MAC simplificada de PC2, 55-55.
- **Dirección [[Media Access Control|MAC]] de origen**: es la dirección MAC simplificada de la NIC Ethernet en PC1, aa-aa-aa.

El paquete IP de capa 3 contiene lo siguiente:

- **Dirección [[IP versión 4|IPv4]] de origen**: esta es la dirección IPv4 de PC1, 192.168.10.10.
- **Dirección [[IP versión 4|IPv4]] de destino**: esta es la dirección IPv4 de PC2, 192.168.10.11.

## Destino en una Red Remota

Cuando la dirección [[Internet Protocol|IP]] de destino ([[IP versión 4|IPv4]] o [[IP versión 6|IPv6]]) está en una red remota, la dirección [[Media Access Control|MAC]] de destino será la dirección de gateway predeterminada del [[Host|host]] (es decir, la interfaz del router).

Considere el siguiente ejemplo utilizando una representación de dirección [[Media Access Control|MAC]] simplificada.

![[Pasted image 20220329175700.png]]

En este ejemplo, PC1 desea enviar un paquete a PC2. PC2 se encuentra en una red remota. Dado que la dirección IPv4 de destino no está en la misma red local que PC1, la dirección [[Media Access Control|MAC]] de destino es la del gateway predeterminado local en el router.

Los routers examinan la dirección [[IP versión 4|IPv4]] de destino para determinar la mejor ruta para reenviar el paquete [[IP versión 4|IPv4]]. Cuando el router recibe una trama de [[Ethernet]], desencapsula la información de [[Capa de enlace de datos|capa 2]]. Por medio de la dirección [[Internet Protocol|IP]] de destino, determina el dispositivo del siguiente salto y desencapsula el paquete IP en una nueva trama de enlace de datos para la interfaz de salida.

En nuestro ejemplo, R1 ahora encapsularía el paquete con la nueva información de dirección de [[Capa de enlace de datos|capa 2]] como se muestra en la figura.

![[Pasted image 20220329175719.png]]

La nueva dirección [[Media Access Control|MAC]] de destino sería la de la interfaz R2 G0/0/1 y la nueva dirección [[Media Access Control|MAC]] de origen sería la de la interfaz R1 G0/0/1.

A lo largo de cada enlace de una ruta, un paquete [[Internet Protocol|IP]] se encapsula en una trama. El [[Trama de Red|trama]] es específico de la tecnología de enlace de datos asociada a ese vínculo, como [[Ethernet]]. Si el dispositivo del siguiente salto es el destino final, la dirección [[Media Access Control|MAC]] de destino será la del [[Network Interface Card|NIC]] de [[Ethernet]] del dispositivo, como se muestra en la figura.

![[Pasted image 20220329175845.png]]

¿Cómo se asocian las direcciones IP de los paquetes IP en un flujo de datos con las direcciones [[Media Access Control|MAC]] en cada enlace a lo largo de la ruta hacia el destino? Para los paquetes [[IP versión 4|IPv4]], esto se realiza a través de un proceso llamado Protocolo de resolución de direcciones ([[Address Resolution Protocol|ARP]]). Para los paquetes [[IP versión 6|IPv6]], el proceso es [[Protocolo de Descubrimiento de Vecinos versión 6|ICMPv6 ND]].

## Packet Tracer: Identificación de direcciones MAC y direcciones IP

- [[9.1.3-packet-tracer---identify-mac-and-ip-addresses_es-XL.pdf]]
- [[9.1.3-packet-tracer---identify-mac-and-ip-addresses_es-XL.pka]]