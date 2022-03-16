## Dirección lógica de capa 3
Una dirección lógica de la [[Capa de red]], o capa 3, se utiliza para enviar el paquete [[Internet Protocol|IP]] desde el dispositivo de origen hasta el dispositivo de destino, como se muestra en la figura.
![[Pasted image 20220308210304.png]]

Los paquetes IP contienen dos direcciones IP:

-   Dirección IP de origen
	- La dirección IP del dispositivo emisor
	- La fuente de origen del paquete
-   Dirección IP de destino
	- La dirección IP del dispositivo receptor, es decir, el destino final del paquete

Las direcciones de la capa de red, o direcciones IP, indican el origen y el destino final. Esto es cierto si el origen y el destino están en la misma red IP o redes IP diferentes.

Un paquete IP contiene dos partes:

-   Porción de red ([[IP versión 4|IPv4]]) o Prefijo ([[IP versión 6|IPv6]])
	- La sección más a la izquierda de la dirección que indica la red de la que es miembro la dirección IP
	- Todos los dispositivos de la misma red tienen la misma porción de red de la dirección.
-   Porción de host ([[IP versión 4|IPv4]]) o ID de interfaz ([[IP versión 6|IPv6]])
	- La parte restante de la dirección que identifica un dispositivo específico de la red
	- La sección de host es única para cada dispositivo o interfaz en la red
```ad-note
La máscara de subred ([[IP versión 4|IPv4]]) o la longitud del prefijo ([[IP versión 6|IPv6]]) se utiliza para identifica la porción de red de una dirección [[Internet Protocol|IP]] de la porción del host.
```