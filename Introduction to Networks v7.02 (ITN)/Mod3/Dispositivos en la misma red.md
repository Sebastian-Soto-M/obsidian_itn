# Dispositivos En La Misma Red

En este ejemplo, tenemos un equipo cliente, PC1, que se comunica con un servidor FTP, en la misma red IP.

- Dirección [[IP versión 4|IPv4]] de origen
	- La dirección [[IP versión 4|IPv4]] del dispositivo emisor, es decir, el equipo cliente PC1: 192.168.1.110.
- Dirección [[IP versión 4|IPv4]] de destino
	- La dirección [[IP versión 4|IPv4]] del dispositivo receptor, el servidor FTP: 192.168.1.9.

```ad-seealso
title: Observe en la figura...
collapse: open

![[Pasted image 20220308210402.png]]

- La porción de red de las direcciones [[Internet Protocol|IP]] de origen y de destino se encuentran en la misma red.
- La parte de red de la dirección [[IP versión 4|IPv4]] de **origen** y la **parte de red** de la dirección [[IP versión 4|IPv4]] de **destino son iguales** y, por tanto, ==el origen y el destino están en la misma red==.
- La figura muestra el encabezado de [[Trama de Red|Trama]] [[Ethernet]] de enlace de datos y el encabezado de paquete [[Internet Protocol|IP]] de capa de red para la información que fluye desde un origen a un destino en la misma red.
- En la parte inferior hay una topología de red.
	- Comenzando por la izquierda, consta de PC1 con dirección IP 192.168.1.110 y dirección [[Media Access Control|MAC]] AA-AA-AA-AA-AA, un servidor FTP con dirección IP 192.168.1.9 y dirección [[Media Access Control|MAC]] CC-CC-CC-CC-CC-CC-CC, y otro PC, todos conectados al mismo conmutador.
- En el medio de la topología hay una cadena de tres routeres a los que está conectado el conmutador.
- A la derecha hay otro conmutador conectado a un servidor.
- Por encima de la topología está el mensaje dividido en sus diversos componentes.
- Comienza a la izquierda con el encabezado de trama [[Ethernet]] de enlace de datos que muestra un destino de CC-CC-CC-CC-CC-CC y una fuente de AA-AA-AA-AA.
- A continuación se muestra el encabezado de paquete [[Internet Protocol|IP]] de [[Capa de red]] que muestra un origen de 192.168.1 (red) 110 (host) y un destino de 192.168.1 (red) 9 (host).
- Por último, los datos.

```
