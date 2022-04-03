## Descripción General de ARP

Si su red utiliza el protocolo de comunicaciones [[IP versión 4|IPv4]], el protocolo de resolución de direcciones o ARP es lo que necesita para asignar direcciones [[IP versión 4|IPv4]] a direcciones [[Media Access Control|MAC]]. En este tema se explica cómo funciona ARP.

Cada dispositivo [[Internet Protocol|IP]] de una red [[Ethernet]] tiene una dirección [[Media Access Control|MAC]] [[Ethernet]] única. Cuando un dispositivo envía una trama de capa 2 de Ethernet, contiene estas dos direcciones:

- **Dirección [[Media Access Control|MAC]] de destino** - La dirección [[Media Access Control|MAC]] [[Ethernet]] del dispositivo de destino en el mismo segmento de red local. Si el host de destino está en otra red, entonces la dirección de destino en el trama sería la del gateway predeterminado (es decir, router).
- **Dirección [[Media Access Control|MAC]] de origen** - La dirección [[Media Access Control|MAC]] de la [[Network Interface Card|NIC]] de [[Ethernet]] en el host de origen.

La figura ilustra el problema al enviar una trama a otro host en el mismo segmento en una red [[IP versión 4|IPv4]].

Cuatro hosts, H1, H2, H3 y H4, están conectados al mismo switch. H1 tiene una [[Internet Protocol|IP]] de 192.168.1.5/24, H2 tiene una [[Internet Protocol|IP]] de 192.168.1.6/24, H3 tiene una [[Internet Protocol|IP]] de 192.168.1.8/24 y H4 tiene una [[Internet Protocol|IP]] de 192.168.1.7/24. H1 tiene un enunciado que dice: Necesito enviar información a 192.168.1.7, pero solo tengo la dirección IP. No conozco la dirección [[Media Access Control|MAC]] del dispositivo que tiene esa dirección IP.

![[Pasted image 20220330215132.png]]

Para enviar un paquete a otro host en la misma red [[IP versión 4|IPv4]] local, un host debe conocer la dirección [[IP versión 4|IPv4]] y la dirección [[Media Access Control|MAC]] del dispositivo de destino. Las direcciones [[IP versión 4|IPv4]] de destino del dispositivo se conocen o se resuelven por el nombre del dispositivo. Sin embargo, las direcciones [[Media Access Control|MAC]] deben ser descubiertas.

Un dispositivo utiliza el Protocolo de resolución de direcciones (ARP) para determinar la dirección [[Media Access Control|MAC]] de destino de un dispositivo local cuando conoce su dirección [[IP versión 4|IPv4]].

ARP proporciona dos funciones básicas:

- Resolución de direcciones [[IP versión 4|IPv4]] a direcciones [[Media Access Control|MAC]]
- Mantener una tabla de asignaciones de direcciones [[IP versión 4|IPv4]] a [[Media Access Control|MAC]]