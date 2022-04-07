---
up: [[ITN Module 11 MOC]]
---
# Segmentación de La Red
## Dominios de difusión y segmentación
¿Ha recibido alguna vez un correo electrónico dirigido a todas las personas de su trabajo o escuela? Este era un email de transmisión. Con suerte, contenía información que cada uno de ustedes necesitaba saber. Pero a menudo una transmisión no es realmente pertinente para todos en la lista de correo. A veces, sólo un segmento de la población necesita leer esa información.

En una LAN Ethernet, los dispositivos utilizan difusiones y el Protocolo de resolución de direcciones (ARP) para localizar otros dispositivos. ARP envía transmisiones de capa 2 a una dirección IPv4 conocida en la red local para descubrir la dirección MAC asociada. Los dispositivos de LAN Ethernet también localizan otros dispositivos que utilizan servicios. Un host normalmente adquiere su configuración de dirección IPv4 utilizando el Protocolo de configuración dinámica de host (DHCP) que envía transmisiones en la red local para localizar un servidor DHCP.

Los switches propagan las difusiones por todas las interfaces, salvo por aquella en la cual se recibieron. Por ejemplo, si un switch de la ilustración recibiera una difusión, la reenviaría a los demás switches y a otros usuarios conectados en la red.

### Dominios de difusión de segmentos de router
![[Pasted image 20220405203345.png]]

Los routers no propagan difusiones. Cuando un router recibe una difusión, no la reenvía por otras interfaces. Por ejemplo, cuando el R1 recibe una difusión en la interfaz Gigabit Ethernet 0/0, no la reenvía por otra interfaz.

Por lo tanto, cada interfaz de router se conecta a un dominio de transmisión y las transmisiones solo se propagan dentro de ese dominio de transmisión específico.

## Problemas con los dominios de difusión grandes

Un dominio de difusión grande es una red que conecta muchos hosts. Un problema con un dominio de difusión grande es que estos hosts pueden generar difusiones excesivas y afectar la red de manera negativa. En la figura, LAN 1 conecta a 400 usuarios que podrían generar una cantidad excesiva de tráfico de difusión. Esto da como resultado operaciones de red lentas debido a la cantidad significativa de tráfico que puede causar, y operaciones de dispositivo lentas porque un dispositivo debe aceptar y procesar cada paquete de difusión.

### Un dominio de difusión amplio
![[Pasted image 20220405203427.png]]

La solución es reducir el tamaño de la red para crear dominios de difusión más pequeños mediante un proceso que se denomina división en subredes. Estos espacios de red más pequeños se denominan subredes.

En la figura, los 400 usuarios en LAN 1 con la dirección de red 172.16.0.0 / 16 se han dividido en dos subredes de 200 usuarios cada una: 172.16.0.0 / 24 y 172.16.1.0 / 24. Las difusiones solo se propagan dentro de los dominios de difusión más pequeños. Por lo tanto, una transmisión en LAN 1 no se propagaría a LAN 2.

### Comunicación entre redes
![[Pasted image 20220405203500.png]]

Observe cómo la longitud del prefijo ha cambiado de una sola red /16 a dos /24 redes. Esta es la base de la división en subredes: el uso de bits de host para crear subredes adicionales.

> Los términos subred y red a menudo se usan indistintamente. La mayoría de las redes son una subred de un bloque de direcciones más grande.

## Razones para segmentar redes

La división en subredes disminuye el tráfico de red general y mejora su rendimiento. A su vez, le permite a un administrador implementar políticas de seguridad, por ejemplo, qué subredes están habilitadas para comunicarse entre sí y cuáles no lo están. Otra razón es que reduce el número de dispositivos afectados por el tráfico de difusión anormal debido a configuraciones incorrectas, problemas de hardware o software o intenciones malintencionadas.

Existen diversas maneras de usar las subredes para contribuir a administrar los dispositivos de red.

### División en subredes por ubicación
![[Pasted image 20220405203603.png]]

Los administradores de red pueden crear subredes utilizando cualquier otra división que tenga sentido para la red. Observe que, en cada ilustración, las subredes usan longitudes de prefijo más largas para identificar las redes.

Entender cómo dividir redes en subredes es una aptitud fundamental que deben tener todos los administradores de redes. Se desarrollaron diversos métodos que contribuyen a la comprensión de este proceso. Aunque un poco abrumador al principio, preste mucha atención a los detalles y, con práctica, la división en subredes será más fácil.

### Subredes por grupo o función
![[Pasted image 20220405203636.png]]

Los administradores de red pueden crear subredes utilizando cualquier otra división que tenga sentido para la red. Observe que, en cada ilustración, las subredes usan longitudes de prefijo más largas para identificar las redes.

Entender cómo dividir redes en subredes es una aptitud fundamental que deben tener todos los administradores de redes. Se desarrollaron diversos métodos que contribuyen a la comprensión de este proceso. Aunque un poco abrumador al principio, preste mucha atención a los detalles y, con práctica, la división en subredes será más fácil.

### Tipo de dispositivo para Subnetting
![[Pasted image 20220405203716.png]]

Los administradores de red pueden crear subredes utilizando cualquier otra división que tenga sentido para la red. Observe que, en cada ilustración, las subredes usan longitudes de prefijo más largas para identificar las redes.

Entender cómo dividir redes en subredes es una aptitud fundamental que deben tener todos los administradores de redes. Se desarrollaron diversos métodos que contribuyen a la comprensión de este proceso. Aunque un poco abrumador al principio, preste mucha atención a los detalles y, con práctica, la división en subredes será más fácil.
