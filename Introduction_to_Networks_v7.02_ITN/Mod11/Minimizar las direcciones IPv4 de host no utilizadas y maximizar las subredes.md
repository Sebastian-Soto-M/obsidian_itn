## Minimizar las direcciones IPv4 de host no utilizadas y maximizar las subredes

Para minimizar el número de direcciones IPv4 de host no utilizadas y maximizar el número de subredes disponibles, hay dos consideraciones al planificar subredes: el número de direcciones de host necesarias para cada red y el número de subredes individuales necesarias.

La tabla muestra los detalles para subredes a una red / 24. Observe que existe una relación inversa entre la cantidad de subredes y la cantidad de hosts. Cuantos más bits se toman prestados para crear subredes, menor es la cantidad de bits de host disponibles. Si se necesitan más direcciones de host, se requieren más bits de host, lo que tiene como resultado menos subredes.

La cantidad de direcciones de host que se requieren en la subred más grande determina cuántos bits se deben dejar en la porción de host. Recuerde que no se pueden usar dos de las direcciones, por lo que el número de direcciones utilizables se puede calcular como 2n \ -2.

### Subnetting a /24 Network

| Longitud de prefijo | Máscara de subred |              Máscara de subred en binario</br>(n = network, h = host)               | # de subredes | # hosts por subred |
|:-------------------:|:-----------------:|:-----------------------------------------------------------------------------------:|:-------------:|:------------------:|
|         /25         |  255.255.255.128  | nnnnnnnn.nnnnnnnn.nnnnnnnn.**n**hhhhhhh</br>11111111.11111111.11111111.**1**0000000 |     **2**     |        126         |
|         /26         |  255.255.255.192  | nnnnnnnn.nnnnnnnn.nnnnnnnn.**nn**hhhhhh</br>11111111.11111111.11111111.**11**000000 |     **4**     |         62         |
|         /27         |  255.255.255.224  | nnnnnnnn.nnnnnnnn.nnnnnnnn.**nnn**hhhhh</br>11111111.11111111.11111111.**111**00000 |     **8**     |         30         |
|         /28         |  255.255.255.240  | nnnnnnnn.nnnnnnnn.nnnnnnnn.**nnnn**hhhh</br>11111111.11111111.11111111.**1111**0000 |    **16**     |         14         |
|         /29         |  255.255.255.248  | nnnnnnnn.nnnnnnnn.nnnnnnnn.**nnnnn**hhh</br>11111111.11111111.11111111.**11111**000 |    **32**     |         6          |
|         /30         |  255.255.255.252  | nnnnnnnn.nnnnnnnn.nnnnnnnn.**nnnnnn**hh</br>11111111.11111111.11111111.**111111**00 |    **64**     |         2          |

Los administradores de redes deben diseñar un esquema de direccionamiento de red que admita la cantidad máxima de hosts para cada red y la cantidad de subredes. El esquema de direccionamiento debe permitir el crecimiento tanto de la cantidad de direcciones de host por subred como de la cantidad total de subredes.