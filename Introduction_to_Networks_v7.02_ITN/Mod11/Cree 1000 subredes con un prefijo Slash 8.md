---
up: [[División de Subredes Con Prefijos 16 y 8]]
---
# Cree 1000 subredes con un prefijo Slash 8

Es posible que algunas organizaciones, como pequeños proveedores de servicios o grandes empresas, puedan necesitar aún más subredes. Por ejemplo, tome un ISP pequeño que requiera 1000 subredes para sus clientes. Cada cliente necesitará mucho espacio en la parte del host para crear sus propias subredes.

El ISP tiene una dirección de red 10.0.0.0 255.0.0.0 o 10.0.0.0/8. Esto significa que hay 8 bits en la porción de red y 24 bits de host disponibles para tomar prestados a fin de realizar la división en subredes. Por lo tanto, el ISP pequeño dividirá la red 10.0.0.0/8 en subredes.

Para crear subredes, debe tomar prestados bits de la parte del host de la dirección IPv4 de la red existente. Comenzando de izquierda a derecha con el primer bit de host disponible, pida prestado un solo bit a la vez hasta alcanzar el número de bits necesarios para crear 1000 subredes. Como se muestra en la figura, debe tomar prestados 10 bits para crear 1024 subredes (210 = 1024). Esto incluye 8 bits en el segundo octeto y 2 bits adicionales del tercer octeto.

El gráfico muestra cómo calcular el número de subredes creadas al tomar prestados bits del segundo y tercer octetos de una dirección de red IPv4. La fórmula para determinar el número de subredes creadas es 2 a la potencia del número de bits prestados. El gráfico muestra una dirección de 10.0.0.0. Debajo, están las letras nnnnnnnn.hhhhhhhhhhhhhhhhhhh. Comienza tomando prestado el primer bit h en el segundo octeto que resulta en 2 a la potencia de 1 = 2 subredes. Cuando se toman prestados los primeros dos bits h en el segundo octeto, la fórmula es 2 a la potencia de 2 = 4. Esto continúa hasta que los primeros bits de 10 h se toman prestados del segundo y tercer octetos, resultando en 2 a la potencia de 10 = 1024.

## Cantidad de subredes creadas
![[Pasted image 20220406225454.png]]

En la figura 2, se muestra la dirección de red y la máscara de subred resultante, la cual se convierte en 255.255.192.0 o un prefijo /18.

### Red 10.0.0.0/18
![[Pasted image 20220406225645.png]]

Esta figura muestra las subredes resultantes de tomar prestados 10 bits, creando subredes de 10.0.0.0/18 a 10.255.128.0/18.

### Subredes /18 resultantes
![[Pasted image 20220406225631.png]]

Prestar 10 bits para crear las subredes, deja 14 bits host para cada subred. Restar dos hosts por subred (uno para la dirección de red y otro para la dirección de difusión) equivale a 214 - 2 = 16382 hosts por subred. Esto indica que cada una de las 1000subredes puede admitir hasta 16382 hosts.

Esta figura muestra los detalles de la primera subred.

## Intervalo de direcciones para la subred 10.0.0.0/18
![[Pasted image 20220406225712.png]]
