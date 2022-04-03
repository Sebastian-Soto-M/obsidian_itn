# Direcciones de Enlace de Datos

La dirección física de la [[Capa de enlace de datos]], o capa 2, tiene una función distinta.

Su **propósito** es **enviar la [[Trama de Red|Trama]]** de enlace de datos desde una interfaz de red hasta otra interfaz de red en la misma red.

Antes de que un paquete [[Internet Protocol|IP]] pueda enviarse a través de una red conectada por cable o inalámbrica, se debe [[3.6 Encapsulamiento de datos|encapsular]] en una [[Trama de Red|trama]] de enlace de datos de modo que **pueda transmitirse a través del medio físico**.

A medida que el paquete [[Internet Protocol|IP]] se mueve de host a router, de router a router y, finalmente, de router a host, es encapsulado en una nueva trama de enlace de datos, en cada punto del recorrido.

Cada [[Trama de Red|trama]] de enlace de datos contiene la dirección de origen de enlace de datos de la tarjeta [[Network Interface Card|NIC]] que envía la [[Trama de Red|trama]] y la dirección de destino de enlace de datos de la tarjeta [[Network Interface Card|NIC]] que recibe la [[Trama de Red|trama]].

El protocolo de enlace de datos de capa 2 solo se utiliza para enviar el paquete de NIC a NIC en la misma red.

El **router elimina la información de la capa 2** a medida que una [[Network Interface Card|NIC]] la recibe y agrega nueva información de enlace de datos antes de reenviarla a la [[Network Interface Card|NIC]] de salida en su recorrido hacia el dispositivo de destino final.

El paquete [[Internet Protocol|IP]] se encapsula en una trama de enlace de datos que contiene información de enlace de datos, como la siguiente:

- Dirección de enlace de datos de origen
	- La dirección física de la [[Network Interface Card|NIC]] del dispositivo que envía la trama de enlace de datos.
- Dirección de enlace de datos de destino
	- La dirección física de la [[Network Interface Card|NIC]] que recibe la trama de enlace de datos. Esta dirección es el router del salto siguiente o el dispositivo de destino final.

```ad-hint
title: Host a router
collapse: closed
![[Pasted image 20220308211403.png]]
```

```ad-hint
title: Router a router
collapse: closed
![[Pasted image 20220308211431.png]]
```

```ad-hint
title: Router a servidor
collapse: closed
![[Pasted image 20220308211502.png]]
```
