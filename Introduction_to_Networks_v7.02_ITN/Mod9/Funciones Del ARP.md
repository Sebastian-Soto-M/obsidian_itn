## Funciones Del ARP

Cuando se envía un paquete a la capa de enlace de datos para encapsularlo en una trama de Ethernet, el dispositivo consulta una tabla en su memoria para encontrar la dirección [[Media Access Control|MAC]] que está asignada a la dirección [[IP versión 4|IPv4]]. Esta tabla se almacena temporalmente en la memoria RAM y se denomina tabla ARP o caché ARP.

El dispositivo emisor busca en su tabla ARP la dirección [[IP versión 4|IPv4]] de destino y la dirección [[Media Access Control|MAC]] correspondiente.

- Si la dirección [[IP versión 4|IPv4]] de destino del paquete está en la misma red que la dirección [[IP versión 4|IPv4]] de origen, el dispositivo busca la dirección [[IP versión 4|IPv4]] de destino en la tabla ARP.
- Si la dirección [[IP versión 4|IPv4]] de destino está en una red diferente que la dirección [[IP versión 4|IPv4]] de origen, el dispositivo busca la dirección [[IP versión 4|IPv4]] del gateway predeterminado.

En ambos casos, se realiza una búsqueda de la dirección [[IP versión 4|IPv4]] y la dirección [[Media Access Control|MAC]] correspondiente para el dispositivo.

En cada entrada o fila de la tabla ARP, se enlaza una dirección [[IP versión 4|IPv4]] con una dirección [[Media Access Control|MAC]]. Llamamos a la relación entre los dos valores un mapa. Esto solamente significa que es posible buscar una dirección [[IP versión 4|IPv4]] en la tabla y encontrar la dirección [[Media Access Control|MAC]] correspondiente. La tabla ARP almacena temporalmente (en caché) la asignación para los dispositivos de la LAN.

Si el dispositivo localiza la dirección [[IP versión 4|IPv4]], se utiliza la dirección [[Media Access Control|MAC]] correspondiente como la dirección [[Media Access Control|MAC]] de destino de la trama. Si no se encuentra ninguna entrada, el dispositivo envía una solicitud de ARP.

```ad-example
title: Función ARP
collapse: closed

![[Pasted image 20220330215348.png]]
![[Pasted image 20220330215409.png]]
![[Pasted image 20220330215422.png]]
![[Pasted image 20220330215439.png]]
![[Pasted image 20220330215500.png]]

```