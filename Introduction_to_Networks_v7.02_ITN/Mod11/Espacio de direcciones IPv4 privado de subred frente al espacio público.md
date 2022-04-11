## Espacio de direcciones IPv4 privado de subred frente al espacio público

Aunque es bueno segmentar rápidamente una red en subredes, la red de su organización puede usar direcciones IPv4 públicas y privadas. Esto afecta a la forma en que va a subred la red.

La figura muestra una red empresarial típica:

- **Intranet -** Esta es la parte interna de la red de una empresa, accesible sólo dentro de la organización. Los dispositivos de la intranet utilizan direcciones IPv4 privadas.
- **DMZ -** Esto es parte de la red de la compañía que contiene recursos disponibles para Internet, como un servidor web. Los dispositivos de la DMZ utilizan direcciones IPv4 públicas.

### Espacio de direcciones IPv4 público y privado
![[Pasted image 20220409165105.png]]

Tanto la intranet como la DMZ tienen sus propios requisitos y desafíos de subredes.

La intranet utiliza espacio de direcciones IPv4 privado. Esto permite a una organización utilizar cualquiera de las direcciones de red IPv4 privadas, incluido el prefijo 10.0.0.0/8 con 24 bits de host y más de 16 millones de hosts. El uso de una dirección de red con 24 bits de host hace que la subred sea más fácil y flexible. Esto incluye la subred en un límite de octetos utilizando un /16 o /24.

Por ejemplo, la dirección de red IPv4 privada 10.0.0.0/8 se puede subred utilizando una máscara /16. Como se muestra en la tabla, esto da como resultado 256 subredes, con 65.534 hosts por subred. Si una organización necesita menos de 200 subredes, lo que permite cierto crecimiento, esto da a cada subred más que suficientes direcciones de host.

### Subnetting Network 10.0.0.0/8 using a /16

| Dirección de subred</br>(256 subredes posibles) | Rango de host</br>(65,534 posibles hosts por subred) |     Dirección      |
|:-----------------------------------------------:|:----------------------------------------------------:|:------------------:|
|               **10.0**.0.0**/16**               |           **10.0**.0.1 - **10.0**.255.254            |  **10.0**.255.255  |
|               **10.1**.0.0**/16**               |           **10.1**.0.1 - **10.1**.255.254            |  **10.1**.255.255  |
|                 **10.2**.0.0/16                 |           **10.2**.0.1 - **10.2**.255.254            |  **10.2**.255.255  |
|               **10,3**,0.0**/16**               |            **10,3**0,1 - **10,3**.255.254            |  **10.3**.255.255  |
|               **10,4**,0.0**/16**               |           **10,4**,0,1 - **10,4**,255,254            |  **10.4**.255.255  |
|               **10,5**,0.0**/16**               |           **10,5**,0,1 - **10,5**,255,254            |  **10.5**.255.255  |
|               **10,6**,0.0**/16**               |            **10,6**0,1 - **10,6.**255.254            |  **10.6**.255.255  |
|               **10,7**,0.0**/16**               |           **10,7**,0,1 - **10,7**,255,254            |  **10.7**.255.255  |
|                        …                        |                          …                           |         …          |
|              **10.255**.0.0**/16**              |         **10.255**.0.1 - **10.255**.255.254          | **10.255**.255.255 |

Otra opción que utiliza la dirección de red privada IPv4 10.0.0.0/8 es subred usando una máscara /24. Como se muestra en la tabla, esto da como resultado 65.536 subredes, con 254 hosts por subred. Si una organización necesita más de 256 subredes, se puede utilizar un /24 con 254 hosts por subred.

### Subnetting Network 10.0.0.0/8 using a /24

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

El 10.0.0.0/8 también se puede subred usando cualquier otro número de longitudes de prefijo, como /12, /18, /20, etc. Esto daría al administrador de red una amplia variedad de opciones. El uso de una dirección de red IPv4 privada 10.0.0.0/8 facilita la planificación e implementación de subredes.

**¿Qué pasa con la DMZ?**

Debido a que estos dispositivos deben ser accesibles públicamente desde Internet, los dispositivos de la DMZ requieren direcciones IPv4 públicas. El agotamiento del espacio público de direcciones IPv4 se convirtió en un problema a partir de mediados de la década de 1990. Desde 2011, IANA y cuatro de cada cinco RIR se han quedado sin espacio de direcciones IPv4. Aunque las organizaciones están realizando la transición a IPv6, el espacio de direcciones IPv4 restante sigue siendo muy limitado. Esto significa que una organización debe maximizar su propio número limitado de direcciones IPv4 públicas. Esto requiere que el administrador de red subred su espacio de direcciones públicas en subredes con diferentes máscaras de subred, a fin de minimizar el número de direcciones de host no utilizadas por subred. Esto se conoce como máscara de longitud de subred variable (VLSM).