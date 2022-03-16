---
up: [[3.5 Modelos de referencia]]
---
## Comparación del modelo [[Protocolos de interconexión de sistemas abiertos|OSI]] y el modelo [[Internet Protocol Suite|TCP/IP]]

![[modelos de referencia.png]]

Los protocolos que forman la suite de protocolos [[Internet Protocol Suite|TCP/IP]] pueden describirse en términos del modelo de referencia [[Protocolos de interconexión de sistemas abiertos|OSI]].

En el modelo OSI, la [[Capa de acceso a la red]] y la [[Capa de aplicación]] del modelo [[Internet Protocol Suite|TCP/IP]] están subdivididas para describir funciones discretas que deben producirse en estas capas.

En la *capa de acceso a la red*, la suite de protocolos TCP/IP ==no especifica cuáles protocolos utilizar cuando se transmite por un medio físico== solo ==describe la transferencia desde la capa de Internet a los protocolos de red física==.
capa Las capas [[Protocolos de interconexión de sistemas abiertos|OSI]] [[Capa Física|1]] y [[Capa de Enlace de datos|2]] tratan los procedimientos necesarios para acceder a los medios y las maneras físicas de enviar datos por la red

Las **similitudes clave** se encuentran en la [[Capa de transporte]] y en [[Capa de red]]. Sin embargo, los dos modelos se
diferencian en el modo en que se relacionan con las capas que están por encima y por debajo de cada capa.

- La capa OSI 3, la [[Capa de red]], asigna **directamente** a la capa de Internet [[Internet Protocol Suite|TCP/IP]].
	- Esta capa se utiliza para describir protocolos que abordan y dirigen mensajes a través de una internetwork.
	
- La capa OSI 4, [[Capa de transporte]], asigna **directamente** a la capa de transporte [[Internet Protocol Suite|TCP/IP]].
	- Esta capa describe los servicios y las funciones generales que proporcionan la entrega ordenada y confiable de datos entre los hosts de origen y de destino.
	
- La [[Capa de aplicación]] [[Internet Protocol Suite|TCP/IP]] incluye un número de protocolos que proporciona funcionalidad específica a una variedad de aplicaciones de usuario final.
	- Las capas 5, 6 y 7 del modelo [[Protocolos de interconexión de sistemas abiertos|OSI]] se utilizan como referencias para proveedores y desarrolladores de software de aplicación para fabricar productos que funcionan en redes.
	
- Tanto el modelo [[Internet Protocol Suite|TCP/IP]] como el modelo [[Protocolos de interconexión de sistemas abiertos|OSI]] se utilizan comúnmente en la referencia a protocolos en varias capas.
	- Dado que el modelo ==OSI separa la capa de enlace de datos de la capa física==, se suele utilizar cuando se refiere a esas capas inferiores.