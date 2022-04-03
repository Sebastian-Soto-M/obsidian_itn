# Estructura de La dirección IPv4
## Porciones de red y de host
![[IP versión 4|IPv4]]

Los bits dentro de la porción de red de la dirección deben ser idénticos para todos los dispositivos que residen en la misma red. Los bits dentro de la porción de host de la dirección deben ser únicos para identificar un host específico dentro de una red. Si dos hosts tienen el mismo patrón de bits en la porción de red especificada de la secuencia de 32 bits, esos dos hosts residen en la misma red.

¿Pero cómo saben los hosts qué porción de los 32 bits identifica la red y qué porción identifica el host? El rol de la máscara de subred
## La máscara de subred

Como se muestra en la figura, asignar una dirección IPv4 a un host requiere lo siguiente:

- **Dirección IPv4** - Esta es ladirección IPv4única del host.
- **Máscara de subred** - se usa para identificar la parte de red/host de la dirección IPv4.

```ad-seealso
title: Configuración IPv4 en Windows
collapse: closed
![[Pasted image 20220402085726.png]]

```

> Se requiere una dirección IPv4 de puerta de enlace predeterminada para llegar a redes remotas y se requieren direcciones IPv4 del servidor DNS para traducir nombres de dominio a direcciones IPv4.

La máscara de subred IPv4 se usa para diferenciar la porción de red de la porción de host de una dirección IPv4. Cuando se asigna una dirección IPv4 a un dispositivo, la máscara de subred se usa para determinar la dirección de red del dispositivo. La dirección de red representa todos los dispositivos de la misma red.

La siguiente figura muestra la máscara de subred de 32 bits en formato decimal y binario punteado.

### Máscara de subred

![[Pasted image 20220402090005.png]]

Observe cómo la máscara de subred es una secuencia consecutiva de 1 bits seguida de una secuencia consecutiva de 0 bits.

Para identificar las porciones de red y host de una dirección IPv4, la máscara de subred se compara con la dirección IPv4 bit por bit, de izquierda a derecha como se muestra en la figura.

### Asociación de una dirección IPv4 con su máscara de subred

![[Pasted image 20220402090129.png]]

Tenga en cuenta que la máscara de subred en realidad no contiene la porción de red o host de una dirección IPv4, solo le dice a la computadora dónde buscar la parte de la dirección IPv4 que es la porción de red y qué parte es la porción de host.

El proceso real que se usa para identificar la porción de red y la porción de host se denomina AND.

## La longitud del prefijo

Puede ser difícil expresar direcciones de red y de host con la dirección de la máscara de subred decimal punteada. Afortunadamente, hay un método alternativo para identificar una máscara de subred, un método llamado longitud del prefijo.

La longitud del prefijo es el número de bits establecido en 1 en la máscara de subred. Está escrito en "notación de barra", que se observa mediante una barra diagonal (/) seguida del número de bits establecido en 1. Por lo tanto, cuente el número de bits en la máscara de subred y anteponga una barra diagonal.

Consulte la tabla para ver ejemplos. En la primera columna, se enumeran varias máscaras de subred que se pueden usar con una dirección de host. En la segunda columna, se muestra la dirección binaria de 32 bits convertida. En la última columna, se muestra la longitud de prefijo resultante.

### Comparando la máscara de subred y la longitud del prefijo
| Máscara de subred | Dirección de 32 bits                | Longitud de prefijo |
| ----------------- | ----------------------------------- | ------------------- |
| 255.0.0.0         | 11111111.00000000.00000000.00000000 | /8                  |
| 255.255.0.0       | 11111111.11111111.00000000.00000000 | /16                 |
| 255.255.255.0     | 11111111.11111111.11111111.00000000 | /24                 |
| 255.255.255.128   | 11111111.11111111.11111111.10000000 | /25                 |
| 255.255.255.192   | 11111111.11111111.11111111.11000000 | /26                 |
| 255.255.255.224   | 11111111.11111111.11111111.11100000 | /27                 |
| 255.255.255.240   | 11111111.11111111.11111111.11110000 | /28                 |
| 255.255.255.248   | 11111111.11111111.11111111.11111000 | /29                 |
| 255.255.255.252   | 11111111.11111111.11111111.11111100 | /30                 |

> Una dirección de red también se conoce como prefijo o prefijo de red. Por lo tanto, la longitud del prefijo es el número de 1 bits en la máscara de subred.

Al representar una dirección IPv4 utilizando una longitud de prefijo, la dirección IPv4 se escribe seguida de la longitud del prefijo sin espacios. Por ejemplo, 192.168.10.10 255.255.255.0 se escribiría como 192.168.10.10/24. Más adelante se analiza el uso de varios tipos de longitudes de prefijo. Por ahora, el foco estará en el prefijo / 24 (es decir, 255.255.255.0)

## Determinación de la red: lógica AND

Un AND lógico es una de las tres operaciones booleanas utilizadas en la lógica booleana o digital. Las otras dos son OR y NOT. La operación AND se usa para determinar la dirección de red.

Y lógico es la comparación de dos bits que producen los resultados que se muestran a continuación. Observe que solo mediante 1 AND 1 se obtiene 1. Cualquier otra combinación da como resultado un 0.

- 1 Y 1 = 1
- 0 Y 1 = 0
- 1 Y 0 = 0
- 0 Y 0 = 0

> En la lógica digital, 1 representa True y 0 representa False. Cuando se utiliza una operación AND, ambos valores de entrada deben ser True (1) para que el resultado sea True (1).

Para identificar la dirección de red de un host IPv4, se recurre a la operación lógica AND para la dirección IPv4, bit por bit, con la máscara de subred. El uso de la operación AND entre la dirección y la máscara de subred produce la dirección de red.

Para ilustrar cómo se usa AND para descubrir una dirección de red, considere un host con dirección IPv4 192.168.10.10 y una máscara de subred de 255.255.255.0, como se muestra en la figura:

- **Dirección de host IPv4 (192.168.10.10)** - La dirección IPv4 del host en formato decimal y binario con puntos.
- **Máscara de subred (255.255.255.0)** - La máscara de subred del host en formatos decimales y binarios punteados.
- **Dirección de red (192.168.10.0)** - la operación AND lógica entre la dirección IPv4 y la máscara de subred da como resultado una dirección de red IPv4 que se muestra en formato decimal y binario con puntos.

![[Pasted image 20220402162820.png]]

Utilizando la primera secuencia de bits como ejemplo, observe que la operación AND se realiza en el 1 bit de la dirección del host con el 1 bit de la máscara de subred. Esto da como resultado un bit de 1 para la dirección de red. 1 AND 1 = 1.

La operación AND entre una dirección de host IPv4 y una máscara de subred da como resultado la dirección de red IPv4 para este host. En este ejemplo, la operación AND entre la dirección host 192.168.10.10 y la máscara de subred 255.255.255.0 (/24) da como resultado la dirección de red IPv4 192.168.10.0/24. Esta es una operación IPv4 importante, ya que le dice al host a qué red pertenece.

## Video - Direcciones de red, host y Broadcast
 El [video](https://contenthub.netacad.com/itn-dl/11.1.5) es una demostración de cómo se determinan las direcciones de red, host y de difusión para una dirección IPv4 y una máscara de subred.

## Direcciones de red, de host y de difusión

Dentro de cada red hay tres tipos de direcciones IP:

- [[Dirección de red]]
- [[Direcciones de host]]
- [[Dirección de broadcast]]

Usando la topología de la figura, se examinarán estos tres tipos de direcciones.

![[Pasted image 20220402163009.png]]

![[Direcciones de host]]

![[Direcciones de broadcast]]

![[Dirección de red]]

Un host determina su dirección de red realizando una operación AND entre su dirección IPv4 y su máscara de subred.

Como se muestra en la tabla, la dirección de red tiene todos los 0 bits en la parte del host, según lo determinado por la máscara de subred. En este ejemplo, la dirección de red es 192.168.10.0/24. No se puede asignar una dirección de red a un dispositivo.

### Network, Host and Broadcast Addresses
|                                                    |                Porción de red                 | Porción de host | Bits de host        |
| -------------------------------------------------- |:---------------------------------------------:|:---------------:| ------------------- |
| Máscara de subred **255.255.255.**0 o **/24**      | 255, 255, 255<br>11111111, 11111111, 11111111 |  0<br>00000000  |                     |
| La dirección de red es **192.168.10.**0 o **/24**  | 192, 168, 10<br>11000000, 10100000, 00001010  |  0<br>00000000  | Todos los 0         |
| Primera dirección **192.168.10**.1 ó **/24**       | 192, 168, 10<br>11000000, 10100000, 00001010  |   1, 00000001   | Todos los 0s y un 1 |
| Última dirección **192.168.10**.254 or **/24**     | 192, 168, 10<br>11000000, 10100000, 00001010  |  254, 11111110  | Todos los 1s y un 0 |
| Dirección de difusión **192.168.10**.255 ó **/24** | 192, 168, 10<br>11000000, 10100000, 00001010  |  255, 11111111  | Todos los 1s        |

## Actividad: Uso de la operación AND para determinar la dirección de red
|                                      | 1        | 2        | 3        | 4        |
| ------------------------------------:| -------- | -------- | -------- | -------- |
|                    Dirección de host | 10       | 20       | 130      | 238      |
|                    Máscara de subred | 255      | 255      | 255      | 252      |
| Dirección de host en formato binario | 00001010 | 00010100 | 10000010 | 11101110 |
| Máscara de subred en formato binario | 11111111 | 11111111 | 11111111 | 11111100 |
|  Dirección de red en formato binario | 00001010 | 00010100 | 10000010 | 11101100 |
|  Dirección de red en formato decimal | 10       | 20       | 130      | 236      |
