## Unidades de datos de protocolo
Mientras los datos de la aplicación bajan a la pila del protocolo y se transmiten por los medios de la red, se agrega diversa información de protocolos en cada nivel. Esto comúnmente se conoce como proceso de encapsulamiento.
```ad-note
title: Datagramas
Aunque la [[Protocol Data Unit|PDU]] [[User Datagram Protocol|UDP]] se denomina datagrama, los paquetes [[Internet Protocol|IP]] a veces también se conocen como datagramas IP.
```

- Durante el encapsulamiento, cada capa encapsula las [[Protocol Data Unit|PDU]] que recibe de la capa inferior de acuerdo con el protocolo que se utiliza.
- En **cada etapa** del proceso, una [[Protocol Data Unit|PDU]] tiene un **nombre distinto** para reflejar sus funciones nuevas.
- Aunque no existe una convención universal de **nombres para las [[Protocol Data Unit|PDU]]**, en este curso se denominan **de acuerdo** con los protocolos de la suite **[[Internet Protocol Suite|TCP/IP]]**. Las [[Protocol Data Unit|PDU]] de cada tipo de datos se muestran en la figura.

![[Pasted image 20220305175209.png]]
- Datos: término general que se utiliza en la capa de aplicación para la PDU
- Segmento: PDU de la capa de transporte
- Paquete: PDU de la capa de red
- Trama: PDU de la capa de enlace de datos
- Bits: PDU de capa física que se utiliza cuando se transmiten datos físicamente por el medio
```ad-note
title: Si el encabezado de transporte es...

- TCP = segmento
- UDP = datagrama


```
