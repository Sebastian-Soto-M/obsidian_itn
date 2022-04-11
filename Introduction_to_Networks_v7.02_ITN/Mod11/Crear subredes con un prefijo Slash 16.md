---
up: [[División de Subredes Con Prefijos 16 y 8]]
---
# Crear subredes con un prefijo Slash 16

Algunas subredes son más fáciles que otras subredes. En este tema se explica cómo crear subredes que tengan el mismo número de hosts.

En una situación en la que se necesita una mayor cantidad de subredes, se requiere una red IPv4 con más bits de host para tomar prestados. Por ejemplo, la dirección de red 172.16.0.0 tiene una máscara predeterminada de 255.255.0.0 o /16. Esta dirección tiene 16 bits en la porción de red y 16 bits en la porción de host. Estos 16 bits en la porción de host se pueden tomar prestados para crear subredes. La tabla resalta todos los escenarios posibles para dividir en subredes un prefijo /16.

## Subnet a /16 Network

| Longitud de prefijo | Máscara de subred |                Dirección de red</br>(n = network, h = host)                 | # de subredes | # de hosts |
|:-------------------:|:-----------------:|:---------------------------------------------------------------------------:|:-------------:|:----------:|
|         /17         |   255.255.128.0   | nnnnnnnn.nnnnnnnn.nhhhhhhh.hhhhhhhh</br>11111111.11111111.10000000.00000000 |       2       |   32766    |
|         /18         |   255.255.192.0   | nnnnnnnn.nnnnnnnn.nnhhhhhh.hhhhhhhh</br>11111111.11111111.11000000.00000000 |       4       |   16382    |
|         /19         |   255.255.224.0   | nnnnnnnn.nnnnnnnn.nnnhhhhh.hhhhhhhh</br>11111111.11111111.11100000.00000000 |       8       |    8190    |
|         /20         |   255.255.240.0   | nnnnnnnn.nnnnnnnn.nnnnhhhh.hhhhhhhh</br>11111111.11111111.11110000.00000000 |      16       |    4094    |
|         /21         |   255.255.248.0   | nnnnnnnn.nnnnnnnn.nnnnnhhh.hhhhhhhh</br>11111111.11111111.11111000.00000000 |      32       |    2046    |
|         /22         |   255.255.252.0   | nnnnnnnn.nnnnnnnn.nnnnnnhh.hhhhhhhh</br>11111111.11111111.11111100.00000000 |      64       |    1022    |
|         /23         |   255.255.254.0   | nnnnnnnn.nnnnnnnn.nnnnnnnh.hhhhhhhh</br>11111111.11111111.11111110.00000000 |      128      |    510     |
|         /24         |   255.255.255.0   | nnnnnnnn.nnnnnnnn.nnnnnnnn.hhhhhhhh</br>11111111.11111111.11111111.00000000 |      256      |    254     |
|         /25         |  255.255.255.128  | nnnnnnnn.nnnnnnnn.nnnnnnnn.nhhhhhhh</br>11111111.11111111.11111111.10000000 |      512      |    126     |
|         /26         |  255.255.255.192  | nnnnnnnn.nnnnnnnn.nnnnnnnn.nnhhhhhh</br>11111111.11111111.11111111.11000000 |     1024      |     62     |
|         /27         |  255.255.255.224  | nnnnnnnn.nnnnnnnn.nnnnnnnn.nnnhhhhh</br>11111111.11111111.11111111.11100000 |     2048      |     30     |
|         /28         |  255.255.255.240  | nnnnnnnn.nnnnnnnn.nnnnnnnn.nnnnhhhh</br>11111111.11111111.11111111.11110000 |     4096      |     14     |
|         /29         |  255.255.255.248  | nnnnnnnn.nnnnnnnn.nnnnnnnn.nnnnnhhh</br>11111111.11111111.11111111.11111000 |     8192      |     6      |
|         /30         |  255.255.255.252  | nnnnnnnn.nnnnnnnn.nnnnnnnn.nnnnnnhh</br>11111111.11111111.11111111.11111100 |     16384     |     2      |

Aunque no es necesario memorizar esta tabla, todavía necesita una buena comprensión de cómo se genera cada valor de la tabla. No se deje intimidar por el tamaño de la tabla. La razón por la que es grande es que tiene 8 bits adicionales que se pueden pedir prestados y, por lo tanto, el número de subredes y hosts es simplemente mayor.
