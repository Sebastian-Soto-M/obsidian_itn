---
up: [[ITN Module 11 MOC]]
---

# Tipos de Direcciones IPv4
## Direcciones IPv4 públicas y privadas

Del mismo modo que hay diferentes formas de transmitir un paquete IPv4, también hay diferentes tipos de direcciones IPv4. Algunas direcciones IPv4 no se pueden usar para salir a Internet, y otras se asignan específicamente para enrutar a Internet. Algunos se utilizan para verificar una conexión y otros se autoasignan. Como administrador de red, eventualmente se familiarizará con los tipos de direcciones IPv4, pero por ahora, al menos debe saber qué son y cuándo usarlas.

Las direcciones IPv4 públicas son direcciones que se enrutan globalmente entre routeres de proveedores de servicios de Internet (ISP). Sin embargo, no todas las direcciones IPv4 disponibles pueden usarse en Internet. Existen bloques de direcciones denominadas direcciones privadas que la mayoría de las organizaciones usan para asignar direcciones IPv4 a los hosts internos.

A mediados de la década de 1990, con la introducción de la World Wide Web (WWW), se introdujeron direcciones IPv4 privadas debido al agotamiento del espacio de direcciones IPv4. Las direcciones IPv4 privadas no son exclusivas y cualquier red interna puede usarlas.

 > La solución a largo plazo para el agotamiento de direcciones IPv4 fue IPv6.

 ### The Private Address Blocks

| Dirección de red y prefijo | Rango de direcciones privadas de RFC 1918 |
| -------------------------- | ----------------------------------------- |
| 10.0.0.0/8                 | 10.0.0.0 a 10.255.255.255                 |
| 172.16.0.0/12              | 172.16.0.0 a 172.31.255.255               |
| 192.168.0.0/16             | 192.168.0.0 a 192.168.255.255             |

 Las direcciones privadas se definen en RFC 1918 y a veces se denomina espacio de direcciones RFC 1918.

## Enrutamiento en Internet

La mayoría de las redes internas, desde grandes empresas hasta redes domésticas, utilizan direcciones IPv4 privadas para dirigirse a todos los dispositivos internos (intranet), incluidos los hosts y routeres. Sin embargo, las direcciones privadas no son enrutables globalmente.

En la figura, las redes de clientes 1, 2 y 3 están enviando paquetes fuera de sus redes internas. Estos paquetes tienen una dirección IPv4 de origen que es una dirección privada y una dirección IPv4 de destino que es pública (enrutable globalmente). Los paquetes con una dirección privada deben filtrarse (descartarse) o traducirse a una dirección pública antes de reenviar el paquete a un ISP.

### Private IPv4 Addresses and Network Address Translation (NAT)
![[Pasted image 20220405201938.png]]

Antes de que el ISP pueda reenviar este paquete, debe traducir la dirección IPv4 de origen, que es una dirección privada, a una dirección IPv4 pública mediante la traducción de direcciones de red (NAT). Se usa la traducción de direcciones de red (NAT) para traducir entre direcciones IPv4 privadas y públicas. Esto generalmente se realiza en el router que conecta la red interna a la red ISP. Las direcciones IPv4 privadas de la intranet de la organización se traducirán a direcciones IPv4 públicas antes de enrutar a Internet.

> Aunque no se puede acceder directamente a un dispositivo con una dirección IPv4 privada desde otro dispositivo a través de Internet, el IETF no considera las direcciones IPv4 privadas o NAT como medidas de seguridad efectivas.

Las organizaciones que tienen recursos disponibles para Internet, como un servidor web, también tendrán dispositivos que tengan direcciones IPv4 públicas. Como se muestra en la figura, esta parte de la red se conoce como DMZ (zona desmilitarizada). El router en la figura no solo realiza enrutamiento, sino que también realiza NAT y actúa como un firewall para la seguridad.

![[Pasted image 20220405202020.png]]

> Las direcciones IPv4 privadas se utilizan comúnmente con fines educativos en lugar de utilizar una dirección IPv4 pública que probablemente pertenezca a una organización.

## Direcciones IPv4 de uso especial

Existen ciertas direcciones, como la dirección de red y la dirección de difusión, que no se pueden asignar a los hosts. También hay direcciones especiales que pueden asignarse a los hosts, pero con restricciones respecto de la forma en que dichos hosts pueden interactuar dentro de la red.

### Direcciones de Loopback

Direcciones de Loopback (127.0.0.0 /8 or 127.0.0.1 to 127.255.255.254) generalmente identificadas solo como 127.0.0.1, son direcciones especiales que usa un host para dirigir el tráfico hacia sí mismo. Por ejemplo, se puede usar en un host para probar si la configuración TCP/IP funciona, como se muestra en la ilustración. Observe cómo la dirección de loopback 127.0.0.1 responde al comando **ping** También observe cómo todas las direcciones de este bloque realizan un bucle invertido hacia el host local, como se muestra con el segundo **ping** de la ilustración.

#### Ping a la interfaz de bucle invertido

```sh
C:\Users\NetAcad> **ping 127.0.0.1**
Pinging 127.0.0.1 with 32 bytes of data:
Reply from 127.0.0.1: bytes=32 time<1ms TTL=128 
Reply from 127.0.0.1: bytes=32 time<1ms TTL=128 
Reply from 127.0.0.1: bytes=32 time<1ms TTL=128 
Reply from 127.0.0.1: bytes=32 time<1ms TTL=128 
Ping statistics for 127.0.0.1: 
	Packets: Sent = 4, Received = 4, Lost = 0 (0% loss), 
Approximate round trip times in milli-seconds: 
	Minimum = 0ms, Maximum = 0ms, Average = 0ms 
C:\Users\NetAcad> **ping 127.1.1.1** 
Pinging 127.1.1.1 with 32 bytes of data: 
Reply from 127.1.1.1: bytes=32 time<1ms TTL=128 
Reply from 127.1.1.1: bytes=32 time<1ms TTL=128 
Reply from 127.1.1.1: bytes=32 time<1ms TTL=128 
Reply from 127.1.1.1: bytes=32 time<1ms TTL=128 
Ping statistics for 127.1.1.1: 
	Packets: Sent = 4, Received = 4, Lost = 0 (0% loss), 
Approximate round trip times in milli-seconds: 
	Minimum = 0ms, Maximum = 0ms, Average = 0ms C:\Users\NetAcad>
```

### Direcciones link-local

Direcciones link-local o direcciones IP privadas automáticas (APIPA) 169.254.0.0/16o 169.254.0.1 a 169.254.255.254 Los utiliza un cliente DHCP de Windows para autoconfigurarse en caso de que no haya servidores DHCP disponibles. Las direcciones locales de vínculo se pueden utilizar en una conexión de punto a punto, pero no se utilizan comúnmente para este propósito.

## Direccionamiento con clase antigua

En 1981, las direcciones IPv4 de Internet se asignaban mediante el direccionamiento con clase, según se define en RFC 790 ([https://tools.ietf.org/html/rfc790](https://tools.ietf.org/html/rfc790)), Números asignados. A los clientes se les asignaba una dirección de red basada en una de tres clases: A, B o C. RFC dividía los rangos de unidifusión en las siguientes clases específicas:

- **Clase A (0.0.0.0/8 a 127.0.0.0/8)** - diseñada para admitir redes extremadamente grandes, con más de 16 millones de direcciones de host. La clase A utilizó un prefijo fijo / 8 con el primer octeto para indicar la dirección de red y los tres octetos restantes para las direcciones de host (más de 16 millones de direcciones de host por red).
- **Clase B (128.0.0.0 /16 - 191.255.0.0 /16)** - iseñada para satisfacer las necesidades de redes de tamaño moderado a grande, con hasta 65000 direcciones de host. La clase B utilizó un prefijo fijo / 16 con los dos octetos de alto orden para indicar la dirección de red y los dos octetos restantes para las direcciones de host (más de 65,000 direcciones de host por red).
- **Clase C (192.0.0.0 /24 - 223.255.255.0 /24)** - diseñada para admitir redes pequeñas con un máximo de 254 hosts. La clase C utilizó un prefijo fijo / 24 con los primeros tres octetos para indicar la red y el octeto restante para las direcciones de host (solo 254 direcciones de host por red).

**Nota**: También existe un bloque de multidifusión de clase D que va de 224.0.0.0 a 239.0.0.0, y un bloque de direcciones experimentales de clase E que va de 240.0.0.0 a 255.0.0.0.

En ese momento, con un número limitado de computadoras que utilizan Internet, el direccionamiento con clase era un medio eficaz para asignar direcciones. Como se muestra en la figura, las redes de clase A y B tienen un número muy grande de direcciones de host y la clase C tiene muy pocas. Las redes de clase A representaron el 50% de las redes IPv4. Esto hizo que la mayoría de las direcciones IPv4 disponibles no se utilizaran.

![[Pasted image 20220405202446.png]]

A mediados de la década de 1990, con la introducción de la World Wide Web (WWW), el direccionamiento de clase fue obsoleto para asignar de manera más eficiente el limitado espacio de direcciones IPv4. La asignación de direcciones con clase se reemplazó con direcciones sin clase, que se usa hoy en día. El direccionamiento sin clases ignora las reglas de las clases (A, B, C). Las direcciones de red IPv4 públicas (direcciones de red y máscaras de subred) se asignan en función del número de direcciones que se pueden justificar.

## Asignación de direcciones IP

Las direcciones IPv4 públicas son direcciones en las que se realiza routing globalmente entre los routers ISP. Las direcciones IPv4 públicas deben ser únicas.

Tanto las direcciones IPv4 como las IPv6 son administradas por la Autoridad de Números Asignados a Internet (Internet Assigned Numbers Authority, IANA) ( La IANA administra y asigna bloques de direcciones IP a los Registros Regionales de Internet (RIR). Los cinco RIR se muestran en la figura.

Los RIR se encargan de asignar direcciones IP a los ISP, quienes a su vez proporcionan bloques de direcciones IPv4 a las organizaciones y a los ISP más pequeños. Las organizaciones pueden obtener sus direcciones directamente de un RIR, según las políticas de ese RIR.

### Regional Internet Registries
![[Pasted image 20220405202529.png]]

- AfriNIC (African Network Information Centre) - Africa Region
- APNIC (Asia Pacific Network Information Centre) - Asia/Pacific Region
- ARIN (American Registry for Internet Numbers) - North America Region
- LACNIC (Regional Latin-American and Caribbean IP Adress Registry) - Latin America and some Caribbean Islands
- RIPE NCC (Réseaux IP Européens Network Coordination Centre) - Europa, Medio Oriente, Asia Central

## Activity - Public or Private IPv4 Address
![[Pasted image 20220405202939.png]]
