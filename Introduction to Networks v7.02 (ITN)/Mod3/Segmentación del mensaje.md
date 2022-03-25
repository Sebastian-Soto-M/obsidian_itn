# Segmentación Del Mensaje

- Es el proceso de dividir un flujo de datos en unidades más pequeñas para transmisiones a través de la red.
- Es necesaria porque las redes de datos utilizan el conjunto de protocolos [[Internet Protocol Suite|TCP/IP]] para enviar datos en **paquetes** [[Internet Protocol|IP]] individuales.
	- Cada paquete se **envía por separado**, similar al envío de una carta larga como una serie de postales individuales.
	- Los **paquetes** que contienen segmentos para el mismo destino se pueden **enviar a través de diferentes rutas**.

La segmentación de mensajes tiene dos beneficios principales.

| Beneficio de la segmentación | Justificación                                                                                              |
| ---------------------------- | ---------------------------------------------------------------------------------------------------------- |
| Aumenta la velocidad         | Se pueden enviar muchos datos sin *atar un enlace de comunicaciones* lo cual permite la multiplexación[^1] |
| Aumenta la eficiencia        | Si un segmento no llega, no es necesario volver a solicitar todos los otros segmentos                      |

[^1]: Cuando muchas conversaciones diferentes se intercalen en la red.
