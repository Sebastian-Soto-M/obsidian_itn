---
up: [[División de Subredes Con Prefijos 16 y 8]]
---
# Cree 100 subredes con un prefijo Slash 16

Imagine una gran empresa que requiere, como mínimo, 100 subredes y eligió la dirección privada 172.16.0.0/16 como su dirección de red interna.

Al tomar prestados bits de una dirección /16, comience a tomarlos del tercer octeto, de izquierda a derecha. Tome prestado un solo bit por vez hasta que se alcance la cantidad de bits necesarios para crear 100 subredes.

La figura muestra el número de subredes que se pueden crear al tomar prestados bits del tercer octeto y el cuarto octeto. Observe que ahora hay hasta 14 bits de host que pueden ser prestados.

El gráfico muestra cómo calcular el número de subredes creadas al tomar prestados bits del tercer y cuarto octetos de una dirección de red IPv4. La fórmula para determinar el número de subredes creadas es 2 a la potencia del número de bits prestados. El gráfico muestra una dirección de 172.16.0.0. Debajo, están las letras nnnnnnnnnnnnnnn.hhhhhhhhhhhhh. Comienza tomando prestado el primer bit h en el tercer octeto que resulta en 2 a la potencia de 1 = 2 subredes. Cuando se toman prestados los primeros dos bits h en el tercer octeto, la fórmula es 2 a la potencia de 2 = 4. Esto continúa hasta que los primeros 14 bits h se toman prestados del tercer y cuarto octetos resultando en 2 a la potencia de 14 = 16384. Los últimos dos bits h en el cuarto octeto siguen siendo los mismos.

## Cantidad de subredes creadas

![[Pasted image 20220406225238.png]]

Para satisfacer el requisito de 100 subredes para la empresa, se necesitarían prestar 7 bits (es decir, 27 = 128 subredes) (para un total de 128 subredes), como se muestra en la figura.

## Red 172.16.0.0/23

![[Pasted image 20220406225314.png]]

Recuerde que la máscara de subred debe modificarse para que se muestren los bits que se tomaron prestados. En este ejemplo, cuando se toman prestados 7 bits, la máscara se extiende 7 bits en el tercer octeto. En formato decimal, la máscara se representa como 255.255.254.0, o como el prefijo /23, debido a que, en formato binario, el tercer octeto es 11111110 y el cuarto octeto es 00000000.

En la figura 3, se muestran las subredes resultantes desde 172.16.0.0 /23 hasta 172.16.254.0 /23.

## Resultado: subredes de /23

![[Pasted image 20220406225336.png]]

Después de tomar prestados 7 bits para la subred, queda un bit de host en el tercer octeto y 8 bits de host en el cuarto octeto, para un total de 9 bits que no fueron prestados. 29 resultados en 512 direcciones de host totales. La primera dirección está reservada para la dirección de red y la última para la dirección de difusión, por lo que restar para estas dos direcciones (29 - 2) equivale a 510 direcciones de host disponibles para cada /23 subred.

Como se muestra en la figura, la primera dirección de host para la primera subred es 172.16.0.1, y la última dirección de host es 172.16.1.254.

## Intervalo de direcciones para la subred 172.16.0.0/23

![[Pasted image 20220406225402.png]]
