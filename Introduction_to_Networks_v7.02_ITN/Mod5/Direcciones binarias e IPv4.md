# Direcciones Binarias E IPv4

Las direcciones IPv4 comienzan como binarias, una serie de solo 1 y 0. Estos son difíciles de administrar, por lo que los administradores de red deben convertirlos a decimales. En este tema se muestran algunas formas de hacerlo.

Binario es un sistema de numeración que consta de los dígitos 0 y 1 llamados bits. En contraste, el sistema de numeración decimal consta de 10 dígitos que consisten en los dígitos desde el 0 al 9.

Es importante que comprendamos el sistema binario, ya que los hosts, los servidores y los dispositivos de red usan el direccionamiento binario. Específicamente, usan direcciones IPv4 binarias, como se muestra en la figura, para identificarse entre sí.

Hay un router central con dos LAN conectadas directamente y una WAN conectada a una nube. Cada LAN tiene un switch y una PC. La WAN tiene una PC. Cada dispositivo tiene una dirección IPv4 que está en notación binaria punteada en lugar de notación decimal punteada.

PC1PC211000000.10101000.00001010.0000101011000000.10101000.00001011.0000101011000000.10101000.00001010.0000000111000000.10101000.00001011.00000001G0/0/0G0/0/111010001.10100101.11001000.11100001PC1R1PC2

**Dirección de red LAN A**
11000000.10101000.00001010.00000000 /24**Dirección de red LAN B**
11000000.10101000.00001011.00000000 /24

Cada dirección consta de una cadena de 32 bits, divididos en cuatro secciones denominadas octetos. Cada octeto contiene 8 bits (o 1 byte) separados por un punto. Por ejemplo, a la PC1 de la ilustración se le asignó la dirección IPv4 11000000.10101000.00001010.00001010. La dirección de gateway predeterminado sería la de la interfaz Gigabit Ethernet del R1, 11000000.10101000.00001010.00000001.

Binario funciona bien con hosts y dispositivos de red. Sin embargo, es muy difícil para los humanos trabajar con ellos.

Para facilitar el uso por parte de las personas, las direcciones IPv4 se expresan comúnmente en notación decimal con puntos. A la PC1 se le asigna la dirección IPv4 192.168.10.10, y su dirección de puerta de enlace predeterminada es 192.168.10.1, como se muestra en la figura.

Este diagrama es el mismo que el primero, un router central con dos LAN y una WAN conectada a una nube. Esto tiene los mismos dispositivos que el primer diagrama; sin embargo, en lugar de tener el direccionamiento IPv4 en binario, está en notación decimal con puntos.

PC1PC2192.168.10.10192.168.11.10192.168.10.1192.168.11.1G0/0/0G0/0/1209.165.200.225PC1R1PC2

**Dirección de red LAN A**
192.168.10.0 /24**Dirección de red LAN B**
192.168.11.0 /24

Para tener una buena comprensión del direccionamiento de red, es necesario comprender el direccionamiento binario y obtener habilidades prácticas en la conversión entre direcciones IPv4 binarias y decimales punteadas. Esta sección cubrirá cómo convertir entre sistemas de numeración de base dos (binario) y base 10 (decimal).
