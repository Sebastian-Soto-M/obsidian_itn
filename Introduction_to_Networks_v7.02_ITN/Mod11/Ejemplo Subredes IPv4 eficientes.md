## Ejemplo: Subredes IPv4 eficientes

En este ejemplo, su ISP ha asignado una dirección de red pública de 172.16.0.0/22 (10 bits de host) a su sede central. Como se muestra en la figura, esto proporciona 1022 direcciones de host.

> 172.16.0.0/22 forma parte del espacio de direcciones privadas IPv4. Estamos utilizando esta dirección en lugar de una dirección IPv4 pública real.

### Dirección de red
![[Pasted image 20220409170552.png]]

La sede corporativa cuenta con una DMZ y cuatro sucursales, cada una de las cuales necesita su propio espacio de direcciones IPv4 públicas. Las oficinas centrales corporativas deben aprovechar al máximo su limitado espacio de direcciones IPv4.

La topología mostrada en la figura consta de cinco sitios; una oficina corporativa y cuatro sucursales. Cada sitio requiere conectividad a Internet y, por lo tanto, cinco conexiones a Internet. Esto significa que la organización requiere 10 subredes de la dirección pública 172.16.0.0/22 de la compañía. La subred más grande requiere 40 hosts.

### Topología corporativa con cinco sitios
![[Pasted image 20220409170623.png]]

La dirección de red 172.16.0.0/22 tiene 10 bits de host, como se muestra en la figura. Debido a que la subred más grande requiere 40 hosts, se debe tomar prestado un mínimo de 6 bits de host para proporcionar el direccionamiento de los 40 hosts. Esto se determina utilizando esta fórmula:26 - 2 = 62 hosts.

### Esquema de subredes
![[Pasted image 20220409170713.png]]

La fórmula para determinar subredes da un resultado de 16 subredes: 2^4= 16. Debido a que la interconexión de redes de ejemplo requiere 10 subredes, esto cumplirá con el requisito y permitirá un crecimiento adicional.

Por lo tanto, los primeros 4 bits de host se pueden usar para asignar subredes. Esto significa que se prestarán dos bits del 3er octeto y dos bits del 4to octeto. Cuando se piden prestados 4 bits, la nueva longitud de prefijo es /26, con la máscara de subred 255.255.255.192.

Como se muestra en esta figura, las subredes se pueden asignar a cada ubicación y conexiones de router a ISP.

### Asignaciones de subred a cada sitio e ISP

![[Pasted image 20220409170751.png]]