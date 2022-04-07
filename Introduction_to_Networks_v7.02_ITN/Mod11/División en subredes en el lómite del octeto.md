---
up: [[División de Subredes de una Red IPv4]]
---
# División en subredes en el lómite del octeto

En el tema anterior aprendiste varias buenas razones para segmentar una red. También ha aprendido que la segmentación de una red se denomina subred. La subred es una habilidad crítica a tener al administrar una red IPv4. Es un poco desalentador al principio, pero se hace mucho más fácil con la práctica.

Las subredes IPv4 se crean utilizando uno o más de los bits de host como bits de red. Esto se realiza por medio de la ampliación de la máscara de subred para que tome prestados algunos de los bits de la porción de host de la dirección a fin de crear bits de red adicionales. Cuantos más bits de host se tomen prestados, mayor será la cantidad de subredes que puedan definirse. Cuantos más bits se prestan para aumentar el número de subredes reduce el número de hosts por subred.

Las redes se subdividen con más facilidad en el límite del octeto de /8 /16 y /24. La tabla identifica estas longitudes de prefijo. Observe que el uso de longitudes de prefijo más extensas disminuye la cantidad de hosts por subred.

## Subnet Masks on Octet Boundaries

| Longitud de prefijo | Máscara de subred |                Máscara de subred en sistema binario (n=red, h=host)                 | # de hosts |
|:-------------------:|:-----------------:|:-----------------------------------------------------------------------------------:|:----------:|
|       **/8**        |   **255**.0.0.0   | **nnnnnnnn**.hhhhhhhh.hhhhhhhh.hhhhhhhh</br>**11111111**.00000000.00000000.00000000 |  16777214  |
|       **/16**       |  **255.255**.0.0  | **nnnnnnnn.nnnnnnnn**.hhhhhhhh.hhhhhhhh</br>**11111111.11111111**.00000000.00000000 |   65534    |
|       **/24**       | **255.255.255**.0 | **nnnnnnnn.nnnnnnnn**.nnnnnnnn.hhhhhhhh</br>**11111111.11111111.11111111**.00000000 |    254     |

Comprender cómo ocurre la división en subredes en el límite del octeto puede ser de utilidad. En el siguiente ejemplo, se muestra este proceso. Suponga que una empresa eligió como su dirección de red interna la dirección privada 10.0.0.0/8. Dicha dirección de red puede conectar 16777214 hosts en un dominio de difusión. Obviamente, tener más de 16 millones de hosts en una sola subred no es ideal.

La empresa podría subdividir aún más la dirección 10.0.0.0/8 en el límite de octeto de / 16 como se muestra en la tabla. Esto proporcionaría a la empresa la capacidad de definir hasta 256 subredes (es decir, 10.0.0.0/16 - 10.255.0.0/16) con cada subred capaz de conectar 65.534 hosts Observe cómo los primeros dos octetos identifican la porción de red de la dirección, mientras que los dos últimos octetos son para direcciones IP de host.

## Subnetting Network 10.0.0.0/8 using a /16

| Dirección de subred</br>(256 subredes posibles) | Rango de host</br>(65.534 posibles hosts por subred) |     Dirección      |
|:-----------------------------------------------:|:----------------------------------------------------:|:------------------:|
|               **10.0**.0.0**/16**               |           **10.0**.0.1 - **10.0**.255.254            |  **10.0**.255.255  |
|               **10.1.**0,0**/16**               |           **10.1**.0.1 - **10.1**.255.254            |  **10.1**.255.255  |
|               **10.2**.0.0**/16**               |           **10.2**.0.1 - **10.2**.255.254            |  **10.2**.255.255  |
|               **10,3**,0.0**/16**               |            **10,3**0,1 - **10,3**.255.254            |  **10.3**.255.255  |
|               **10,4**,0.0**/16**               |           **10,4**,0,1 - **10,4**,255,254            |  **10.4**.255.255  |
|               **10,5**,0.0**/16**               |           **10,5**,0,1 - **10,5**,255,254            |  **10.5**.255.255  |
|               **10,6**,0.0**/16**               |           **10,6**,0,1 - **10,6**.255.254            |  **10.6**.255.255  |
|               **10,7**,0.0**/16**               |           **10,7**,0,1 - **10,7**,255,254            |  **10.7**.255.255  |
|                        …                        |                          …                           |         …          |
|              **10.255**.0.0**/16**              |         **10.255**.0.1 - **10.255**.255.254          | **10.255**.255.255 |

Alternativamente, la empresa podría elegir subred la red 10.0.0.0/8 en el límite de / 24 octetos, como se muestra en la tabla. Esto le permitiría a la empresa definir 65536 subredes, cada una capaz de conectar 254 hosts. El uso del límite /24 está muy difundido en la división en subredes debido a que admite una cantidad razonable de hosts y permite dividir en subredes en el límite del octeto de manera conveniente.

## Subnetting Network 10.0.0.0/8 using a /24 Prefix

Dirección de subred (65.536 posibles subredes) Rango de host (254 hosts posibles por subred) Broadcast10.0.0.0/2410.0.0.1 - 10.0.0.25410.0.0.25510.0.1.0/2410.0.1.1 - 10.0.1.25410.0.1.25510.0.2.0/2410.0.2.1 - 10.0.2.25410.0.2.255 10.0.255.0/2410.0.255.1 - 10.0.255.25410.0.255.25510.1.0.0/2410.1.0.1 - 10.1.0.25410.1.0.25510.1.1.0/2410.1.1.1 - 10.1.1.25410.1.1.25510.1.2.0/2410.1.2.1 - 10.1.2.25410.1.2.255 10.100.0.0/2410.100.0.1 - 10.100.0.25410.100.0.255… 10.255.255.0/2410.255.255.1 - 10.2255.255.25410.255.255.255

| Dirección de subred</br>(65,536 subredes posibles) | Rango de host</br>(254 posibles hosts por subred) |     Dirección      |
|:--------------------------------------------------:|:-------------------------------------------------:|:------------------:|
|                **10.0.0**.0**/24**                 |           **10.0.0**.1 - **10.0.0**.254           |   **10.0.0**.255   |
|                **10.0.1**.0**/24**                 |           **10.0.1**.1 - **10.0.1**.254           |   **10.0.1**.255   |
|                **10.0.2**.0**/24**                 |           **10.0.2**.1 - **10.0.2**.254           |   **10.0.2**.255   |
|                         …                          |                         …                         |         …          |
|               **10.0.255**.0**/24**                |         **10.0.255**.1 - **10.0.255**.254         |  **10.0.255**.255  |
|                **10.1.0**.0**/24**                 |           **10.1.0**.1 - **10.1.0**.254           |   **10.1.0**.255   |
|                **10.1.1**.0**/24**                 |           **10.1.1**.1 - **10.1.1**.254           |   **10.1.1**.255   |
|                **10.1.2**.0**/24**                 |           **10.1.2**.1 - **10.1.2**254            |   **10.1.2**.255   |
|                         …                          |                         …                         |         …          |
|               **10.100,0**.0**/24**                |          **10,100,0**,1 - 10,100,0 ,254           |  **10.100,0**.255  |
|                         …                          |                         …                         |         …          |
|              **10.255.255**.0**/24**               |      **10.255.255**.1 - **10.2255.255**.254       | **10.255.255**.255 |
