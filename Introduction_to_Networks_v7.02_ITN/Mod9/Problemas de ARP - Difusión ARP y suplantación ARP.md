## Problemas de ARP - Difusión ARP y suplantación ARP

Todos los dispositivos de la red local reciben y procesan una solicitud de ARP debido a que es una trama de difusión. En una red comercial típica, estas difusiones tendrían, probablemente, un efecto mínimo en el rendimiento de la red. Sin embargo, si se encendiera una gran cantidad de dispositivos que comenzaran a acceder a los servicios de red al mismo tiempo, el rendimiento podría disminuir durante un breve período, como se muestra en la figura. Después que los dispositivos envían las solicitudes de difusión ARP iniciales y obtienen las direcciones [[Media Access Control|MAC]] necesarias, se minimiza cualquier efecto en la red.

![[Pasted image 20220330235421.png]]

En algunos casos, el uso de ARP puede conducir a un riesgo potencial de seguridad. Un atacante puede usar la suplantación ARP para realizar un ataque de envenenamiento ARP. Esta es una técnica utilizada por un atacante para responder a una solicitud de ARP de una dirección [[IP versión 4|IPv4]] que pertenece a otro dispositivo, como la puerta de enlace predeterminada, tal como se muestra en la ilustración. El atacante envía una respuesta de ARP con su propia dirección [[Media Access Control|MAC]]. El receptor de la respuesta de ARP agrega la dirección [[Media Access Control|MAC]] incorrecta a la tabla ARP y envía estos paquetes al atacante. Los switches de nivel empresarial incluyen técnicas de mitigación conocidas como “inspección dinámica de ARP (DAI)”. DAI está más allá del alcance de este curso.

![[Pasted image 20220330235443.png]]