---
up: [[ITN Module 11 MOC]]
---
# VLSM
[Video: Aspectos básicos de VLSM](https://contenthub.netacad.com/itn-dl/11.8.1)
[Video: Ejemplo de VLSM](https://contenthub.netacad.com/itn-dl/11.8.2)
## Conservación de direcciones IPv4

Debido al agotamiento del espacio de direcciones IPv4 público, sacar el máximo partido a las direcciones de host disponibles es una preocupación primordial cuando se subredes de redes IPv4.

> La dirección IPv6 más grande permite una planificación y asignación de direcciones mucho más fáciles de lo que permite IPv4. Conservar direcciones IPv6 no es un problema. Esta es una de las fuerzas impulsoras para la transición a IPv6.

Mediante la división en subredes tradicional, se asigna la misma cantidad de direcciones a cada subred. Si todas las subredes tienen los mismos requisitos para la cantidad de hosts, o si la conservación del espacio de direcciones IPv4 no es un problema, estos bloques de direcciones de tamaño fijo serían eficientes. Normalmente, con direcciones IPv4 públicas, ese no es el caso.

Por ejemplo, la topología que se muestra en la figura requiere siete subredes, una para cada una de las cuatro LAN y una para cada una de las tres conexiones WAN entre los routers.

![[Pasted image 20220409193430.png]]

Utilizando la división en subredes tradicional con la dirección dada de 192.168.20.0/24, se pueden tomar prestados tres bits de la parte del host en el último octeto para cumplir con el requisito de subred de siete subredes. Como se muestra en la figura, tomar prestados 3 bits crea 8 subredes y deja 5 bits de host con 30 hosts utilizables por subred. Mediante este esquema, se crean las subredes necesarias y se cumplen los requisitos de host de la LAN más grande.

### Esquema de subredes básico
![[Pasted image 20220409193506.png]]

Estas siete subredes podrían asignarse a las redes LAN y WAN, como se muestra en la figura.

![[Pasted image 20220409193537.png]]

Si bien la división en subredes tradicional satisface las necesidades de la LAN más grande y divide el espacio de direcciones en una cantidad adecuada de subredes, da como resultado un desperdicio significativo de direcciones sin utilizar.

Por ejemplo, solo se necesitan dos direcciones en cada subred para los tres enlaces WAN. Dado que cada subred tiene 30 direcciones utilizables, hay 28 direcciones sin utilizar en cada una de estas subredes. Como se muestra en la figura, esto da como resultado 84 direcciones no utilizadas (28x3).

### Direcciones sin utilizar en subredes WAN
![[Pasted image 20220409193558.png]]

Además, de esta forma se limita el crecimiento futuro al reducir el número total de subredes disponibles. Este uso ineficiente de las direcciones es característico de la división en subredes tradicional. La aplicación de un esquema de división en subredes tradicional a esta situación no resulta muy eficiente y genera desperdicio.

La máscara de subred de longitud variable (VLSM) se desarrolló para evitar el desperdicio de direcciones al permitirnos subred una subred.

## VLSM

En todos los ejemplos de división en subredes anteriores, se aplicó la misma máscara de subred en todas las subredes. Esto significa que cada subred tiene la misma cantidad de direcciones de host disponibles. Como se ilustra en la figura, mediante la división en subredes tradicional se crean subredes de igual tamaño. Cada subred en un esquema tradicional utiliza la misma máscara de subred. Como se muestra en la figura, VLSM permite dividir un espacio de red en partes desiguales. Con VLSM, la máscara de subred varía según la cantidad de bits que se toman prestados para una subred específica, de lo cual deriva la parte “variable” de la VLSM.

![[Pasted image 20220409193646.png]]

VLSM simplemente subdivide una subred. La misma topología utilizada anteriormente se muestra en la figura. Nuevamente, usaremos la red 192.168.20.0/24 y la subred para siete subredes, una para cada una de las cuatro LAN, y una para cada una de las tres conexiones entre los routeres.

![[Pasted image 20220410164401.png]]

La figura muestra cómo la red 192.168.20.0/24 se subredes en ocho subredes de igual tamaño con 30 direcciones de host utilizables por subred. Se usan cuatro subredes para las LAN y tres subredes para las conexiones entre los routers.

### Esquema Básico de Subredes
![[Pasted image 20220410164435.png]]

Sin embargo, las conexiones entre los routeres requieren sólo dos direcciones de host por subred (una dirección de host para cada interfaz del router). Actualmente todas las subredes tienen 30 direcciones de host utilizables por subred. Para evitar desperdiciar 28 direcciones por subred, VLSM puede usarse para crear subredes más pequeñas para las conexiones entre routeres.

Para crear subredes más pequeñas para los enlaces WAN, se dividirá una de las subredes. En este ejemplo, la última subred, 192.168.20.224/27, puede subdividirse aún más. La figura muestra que la última subred se ha subred utilizando la máscara de subred 255.255.255.252 o /30.

### Esquema de división en subredes de VLSM

![[Pasted image 20220410164504.png]]

¿Por qué /30? Recuerde que cuando se conoce el número de direcciones de host necesarias, se puede usar la fórmula 2n \ -2 (donde n es igual al número de bits de host restantes). Para proporcionar dos direcciones utilizables, se deben dejar dos bits de host en la parte del host.

Debido a que hay cinco bits de host en el espacio de direcciones subred 192.168.20.224/27, se pueden pedir prestados tres bits más, dejando dos bits en la porción de host. Los cálculos que se realizan llegado este punto son exactamente los mismos que se utilizan para la división en subredes tradicional: Se toman prestados los bits, y se determinan los rangos de subred. La figura muestra cómo las cuatro subredes /27 se han asignado a las LAN y tres de las subredes /30 se han asignado a los enlaces entre routeres.

![[Pasted image 20220410164542.png]]

Este esquema de subredes VLSM reduce el número de direcciones por subred a un tamaño apropiado para las redes que requieren menos subredes. La subred subred 7 para enlaces entre routeres permite que las subredes 4, 5 y 6 estén disponibles para redes futuras, así como cinco subredes adicionales disponibles para conexiones entre routeres.

> Cuando use VLSM, siempre comience por satisfacer los requisitos de host de la subred más grande. Siga con la división en subredes hasta que se cumplan los requisitos de host de la subred más pequeña.

## Asignación de direcciones de topologóa VLSM

Usando las subredes VLSM, las redes LAN y entre routeres se pueden abordar sin desperdicio innecesario.

La figura muestra las asignaciones de direcciones de red y las direcciones IPv4 asignadas a cada interfaz de router.

![[Pasted image 20220410164623.png]]

Mediante un esquema de direccionamiento común, la primera dirección IPv4 de host para cada subred se asigna a la interfaz de la red LAN del router. Los hosts en cada subred tendrán una dirección IPv4 de host del intervalo de direcciones de host para esa subred y una máscara adecuada. Los hosts utilizarán la dirección de la interfaz de la red LAN del router conectada como dirección de gateway predeterminado.

La tabla muestra las direcciones de red y el intervalo de direcciones de host para cada red. Se muestra la dirección de puerta de enlace predeterminada para las cuatro LAN.

|            | Dirección de red  | Intervalo de direcciones de host       | Dirección de puerta de enlace predeterminada |
| ---------- | ----------------- | -------------------------------------- | -------------------------------------------- |
| Edificio A | 192.168.20.0/27   | 192.168.20.1/27 to 192.168.20.30/27    | 192.168.20.1/27                              |
| Edificio B | 192.168.20.32/27  | 192.168.20.33/27 to 192.168.20.62/27   | 192.168.20.33/27                             |
| Edificio C | 192.168.20.64/27  | 192.168.20.65/27 to 192.168.20.94/27   | 192.168.20.65/27                             |
| Edificio D | 192.168.20.96/27  | 192.168.20.97/27 to 192.168.20.126/27  | 192.168.20.97/27                             |
| R1-R2      | 192.168.20.224/30 | 192.168.20.225/30 to 192.168.20.226/30 |                                              |
| R2-R3      | 192.168.20.228/30 | 192.168.20.229/30 to 192.168.20.230/30 |                                              |
| R3-R4      | 192.168.20.232/30 | 192.168.20.233/30 to 192.168.20.234/30 |                                              |
