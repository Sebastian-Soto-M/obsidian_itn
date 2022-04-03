# Rol de Acceso a Datos de Las Direcciones de Capa de vínculo de Datos: Diferentes Redes [[Internet Protocol|IP]]

Cuando el emisor y el receptor del paquete IP se encuentran en redes diferentes, la trama de enlace de datos de Ethernet no se puede enviar directamente al host de destino, debido a que en la red del emisor no se puede tener acceso directamente al host. La trama de Ethernet se debe enviar a otro dispositivo conocido como router o gateway predeterminado. En nuestro ejemplo, el gateway predeterminado es R1. R1 tiene una dirección de enlace de datos de Ethernet que se encuentra en la misma red que PC1. Esto permite que PC1 alcance el router directamente.

- Dirección [[Media Access Control|MAC]] de origen
	- La dirección [[Media Access Control|MAC]] de [[Ethernet]] del dispositivo emisor, PC1.
	- La dirección [[Media Access Control|MAC]] de la interfaz [[Ethernet]] de PC1 es AA-AA-AA-AA-AA-AA.
- Dirección MAC de destino
	- Cuando el dispositivo receptor, la dirección [[Internet Protocol|IP]] de destino, está en una red distinta de la del dispositivo emisor, este utiliza la dirección [[Media Access Control|MAC]] de [[Ethernet]] del gateway predeterminado o el router.
	- En este ejemplo, la dirección MAC de destino es la dirección [[Media Access Control|MAC]] de la interfaz [[Ethernet]] de R1, 11-11-11-11-11-11.
		- Esta es la interfaz que está conectada a la misma red que PC1, como se muestra en la figura.

```ad-seealso
title: Observe en la figura...
collapse: open

![[Pasted image 20220308211308.png]]

- La trama de [[Ethernet]] con el paquete [[Internet Protocol|IP]] [[3.6 Encapsulamiento de datos|encapsulado]] ahora se puede transmitir a R1.
- R1 reenvía el paquete al destino, el servidor web.
	- Esto puede significar que R1 reenvía el paquete a otro router o directamente al servidor web si el destino se encuentra en una red conectada a R1.

```

Es importante que en la dirección [[Internet Protocol|IP]] del gateway predeterminado esté configurada en cada host de la red local.

Todos los paquetes que tienen como destino redes remotas se envían al gateway predeterminado.
