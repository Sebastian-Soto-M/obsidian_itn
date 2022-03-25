# Secuenciación

La **desventaja** de utilizar **segmentación y multiplexión** para transmitir mensajes a través de la red **es el nivel de complejidad** que se agrega al proceso.

```ad-example
title: Enviar cartas
collapse: closed

Supongamos que tuviera que enviar una carta de 100 páginas, pero en cada sobre solo cabe una. Por lo tanto, se necesitarían 100 sobres y cada sobre tendría que dirigirse individualmente. Es posible que la carta de 100 páginas en 100 sobres diferentes llegue fuera de pedido.

En consecuencia, la información contenida en el sobre tendría que incluir un número de secuencia para garantizar que el receptor pudiera volver a ensamblar las páginas en el orden adecuado.

```

En las comunicaciones de red, cada **segmento** del mensaje debe seguir un proceso similar **para asegurar que llegue al destino correcto y que puede volverse a ensamblar** en el contenido del mensaje original, como se muestra en la figura. [[Transmission Control Protocol|TCP]] es responsable de secuenciar los segmentos individuales.

![[Pasted image 20220305173657.png]]
