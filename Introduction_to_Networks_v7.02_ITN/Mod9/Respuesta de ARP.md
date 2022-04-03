## Respuesta de ARP

Solo el dispositivo con la dirección [[IP versión 4|IPv4]] de destino asociada con la solicitud ARP responderá con una respuesta ARP. La respuesta de ARP se encapsula en una trama de [[Ethernet]] con la siguiente información de encabezado:

- **Dirección [[Media Access Control|MAC]] de destino** – Es la dirección [[Media Access Control|MAC]] del remitente de la solicitud de ARP.
- **Dirección [[Media Access Control|MAC]] de origen** – Esta es la dirección [[Media Access Control|MAC]] del remitente de la respuesta ARP.
- **Tipo** - Los mensajes ARP tienen un campo de tipo de 0x806. Esto informa a la [[Network Interface Card|NIC]] receptora que la porción de datos de la trama se debe enviar al proceso ARP.

Solamente el dispositivo que envió inicialmente la solicitud de ARP recibe la respuesta de ARP de unicast. Una vez que recibe la respuesta de ARP, el dispositivo agrega la dirección [[IP versión 4|IPv4]] y la dirección [[Media Access Control|MAC]] correspondiente a su tabla ARP. A partir de ese momento, los paquetes destinados para esa dirección [[IP versión 4|IPv4]] se pueden encapsular en las tramas con su dirección [[Media Access Control|MAC]] correspondiente.

Si ningún dispositivo responde a la solicitud de ARP, el paquete se descarta porque no se puede crear una trama.

Las entradas de la tabla ARP tienen marcas de tiempo. Si un dispositivo no recibe una trama de un dispositivo en particular antes de que caduque la marca de tiempo, la entrada para este dispositivo se elimina de la tabla ARP.

Además, se pueden introducir entradas estáticas de asignaciones en una tabla ARP, pero esto no sucede con frecuencia. Las entradas estáticas de la tabla ARP no caducan con el tiempo y se deben eliminar de forma manual.

**Nota**: IPv6 utiliza un proceso similar a ARP para [[IP versión 4|IPv4]], conocido como ICMPv6 Neighbour Discovery (ND). IPv6 utiliza mensajes de solicitud de vecino y de anuncio de vecino similares a las solicitudes y respuestas de ARP de [[IP versión 4|IPv4]].

For a video explaining the process, see [this](https://contenthub.netacad.com/itn-dl/9.2.4) link.