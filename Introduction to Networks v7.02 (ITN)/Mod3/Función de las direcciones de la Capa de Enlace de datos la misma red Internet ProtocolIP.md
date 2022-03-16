## Función de las direcciones de la [[Capa de Enlace de datos]]: la misma red [[Internet Protocol|IP]]

Cuando el **emisor y el receptor** del paquete [[Internet Protocol|IP]] están **en la misma red**, la **[[Trama de Red|Trama]]** de enlace de datos **se envía directamente al dispositivo receptor**.

```ad-seealso
title: Observe en la figura...
collapse: open

![[Pasted image 20220308210436.png]]

Las direcciones [[Media Access Control|MAC]] están integradas físicamente a la [[Network Interface Card|NIC]] [[Ethernet]].

-   Dirección MAC de **origen**
	- La dirección de enlace de datos, o la dirección [[Media Access Control|MAC]] de [[Ethernet]], del dispositivo que envía la trama de enlace de datos con el paquete IP encapsulado.
	- La dirección [[Media Access Control|MAC]] de la [[Network Interface Card|NIC]] [[Ethernet]] de PC1 es AA-AA-AA-AA-AA-AA, redactada en notación hexadecimal.
-   Dirección MAC de **destino**
	- Cuando el dispositivo receptor está en la misma red que el dispositivo emisor, la dirección [[Media Access Control|MAC]] de destino es la dirección de enlace de datos del dispositivo receptor.
	- En este ejemplo, la dirección MAC de destino es la dirección MAC del servidor FTP: CC-CC-CC-CC-CC-CC, escrito en notación hexadecimal.

> La trama con el paquete IP encapsulado ahora se puede transmitir desde PC1 directamente hasta el servidor FTP.
```