## Solicitud de ARP

Se envía una solicitud ARP cuando un dispositivo necesita determinar la dirección [[Media Access Control|MAC]] que está asociada con una dirección [[IP versión 4|IPv4]], y no tiene una entrada para la dirección [[IP versión 4|IPv4]] en su tabla ARP.

Los mensajes de ARP se encapsulan directamente dentro de una trama de Ethernet. No se utiliza un encabezado de [[IP versión 4|IPv4]]. La solicitud de ARP se encapsula en una trama de [[Ethernet]] con la siguiente información de encabezado:

- **Dirección [[Media Access Control|MAC]] de destino** – esta es una dirección broadcast que requiere que todas las [[Network Interface Card|NIC]] [[Ethernet]] de la LAN acepten y procesen la solicitud de ARP.
- **Dirección [[Media Access Control|MAC]] de origen** – Esta es la dirección [[Media Access Control|MAC]] del remitente de la solicitud ARP.
- **Tipo** - Los mensajes ARP tienen un campo de tipo de 0x806. Esto informa a la [[Network Interface Card|NIC]] receptora que la porción de datos de la trama se debe enviar al proceso ARP.

Como las solicitudes de ARP son de broadcast, el switch las envía por todos los puertos, excepto el de recepción. Todas las [[Network Interface Card|NIC]] [[Ethernet]] de la LAN procesan transmisiones y deben entregar la solicitud ARP a su sistema operativo para su procesamiento. Cada dispositivo debe procesar la solicitud de ARP para ver si la dirección [[IP versión 4|IPv4]] objetivo coincide con la suya. Un router no reenvía broadcasts por otras interfaces.

Solo un dispositivo de la LAN tiene la dirección [[IP versión 4|IPv4]] que coincide con la dirección [[IP versión 4|IPv4]] objetivo de la solicitud de ARP. Todos los demás dispositivos no envían una respuesta.

For a video explaining the process, see [this](https://contenthub.netacad.com/itn-dl/9.2.3) link.