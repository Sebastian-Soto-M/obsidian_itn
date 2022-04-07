---
up: [[División de Subredes de una Red IPv4]]
---
# Subred dentro de un lómite de octeto

Los ejemplos mostrados hasta ahora tomaron prestados bits de host de los prefijos de red comunes /8, /16 y /24. Sin embargo, las subredes pueden tomar prestados bits de cualquier posición de bit de host para crear otras máscaras.

Por ejemplo, una dirección de red /24 se suele dividir en subredes con longitudes de prefijo más extensas al tomar prestados bits del cuarto octeto. Esto le proporciona al administrador mayor flexibilidad al asignar direcciones de red a un número menor de terminales.

Consulte la tabla para ver seis formas de subred una red /24.

## Subnet a /24 Network
| Longitud de prefijo | Máscara de subred | Máscara de subred en binario</br>(n = network, h = host)                    | # de subredes | # de hosts |
| ------------------- | ----------------- | --------------------------------------------------------------------------- | ------------- | ---------- |
| /25                 | 255.255.255.128   | nnnnnnnn.nnnnnnnn.nnnnnnnn.nhhhhhhh</br>11111111.11111111.11111111.10000000 | 2             | 126        |
| /26                 | 255.255.255.192   | nnnnnnnn.nnnnnnnn.nnnnnnnn.nnhhhhhh</br>11111111.11111111.11111111.11000000 | 4             | 62         |
| /27                 | 255.255.255.224   | nnnnnnnn.nnnnnnnn.nnnnnnnn.nnnhhhhh</br>11111111.11111111.11111111.11100000 | 8             | 30         |
| /28                 | 255.255.255.240   | nnnnnnnn.nnnnnnnn.nnnnnnnn.nnnnhhhh</br>11111111.11111111.11111111.11110000 | 16            | 14         |
| /29                 | 255.255.255.248   | nnnnnnnn.nnnnnnnn.nnnnnnnn.nnnnnhhh</br>11111111.11111111.11111111.11111000 | 32            | 6          |
| /30                 | 255.255.255.252   | nnnnnnnn.nnnnnnnn.nnnnnnnn.nnnnnnhh</br>11111111.11111111.11111111.11111100 | 64            | 2          |

Por cada bit que se toma prestado en el cuarto octeto, la cantidad de subredes disponible se duplica, al tiempo que se reduce la cantidad de direcciones de host por subred.

- /25 fila - Tomar prestado 1 bit del cuarto octeto crea 2 subredes que admiten 126 hosts cada una.
- /26 fila - Tomar prestados 2 bits crea 4 subredes que admiten 62 hosts cada una.
- /27 fila - Tomar prestados 3 bits crea 8 subredes que admiten 30 hosts cada una.
- /28 fila - Tomar prestados 4 bits crea 16 subredes que admiten 14 hosts cada una.
- /29 fila - Tomar prestados 5 bits crea 32 subredes que admiten 6 hosts cada una.
- /30 fila - Tomar prestados 6 bits crea 64 subredes que admiten 2 hosts cada una.
