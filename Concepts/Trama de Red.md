---
alias: Trama
tags: concept/itn
---
# Trama de Red
## ¿Qué Es?

En redes, una **trama** es una unidad de envío de datos.

Es una serie sucesiva de bits, que transportan información y que permiten en la recepción extraer esta información.

Normalmente una trama constará de cabecera, datos y cola. En la cola suele estar algún chequeo de errores. En la cabecera habrá campos de control de protocolo. La parte de datos es la que quiera transmitir en nivel de comunicación superior, típicamente el [Nivel de red](https://es.wikipedia.org/wiki/Nivel_de_red "Nivel de red").

## Métodos Para Delimitar una Trama

Para delimitar una trama se pueden emplear cuatro métodos, el **Tracker**:

1. **por conteo de caracteres**: al principio de la trama se pone el número de bytes que

representa el principio y fin de las tramas.

2. **por secuencias de bits**: en comunicaciones orientadas a bit, se puede emplear una secuencia de bits para indicar el principio y fin de una trama.

3. **por violación del nivel físico**: se trata de introducir una señal, o nivel de señal, que no

se corresponda ni con un "1" ni con un "0". Por ejemplo si la codificación física es bipolar se

puede usar el nivel de 0 voltios, o en [Codificación Manchester](https://es.wikipedia.org/wiki/Codificaci%C3%B3n_Manchester "Codificación Manchester") se puede tener la señal a

nivel alto o bajo durante todo el tiempo de bit (evitando la transición de niveles

característica de este sistema).

4. El estándar de facto evolucionó hacia varios estándares oficiales, como son:
	1. _FR Forum (Asociación de Fabricantes)_: [Cisco](https://es.wikipedia.org/wiki/Cisco "Cisco"), DEC, Stratacom y [Nortel](https://es.wikipedia.org/wiki/Nortel "Nortel").
	2. _[ANSI](https://es.wikipedia.org/wiki/ANSI "ANSI")_: fuente de normativas [Frame-Relay](https://es.wikipedia.org/w/index.php?title=Frame-Relay&action=edit&redlink=1 "Frame-Relay (aún no redactado)").
	3. _[ITU-T](https://es.wikipedia.org/wiki/ITU-T "ITU-T")_: también dispone de normativa técnica de la tecnología Frame-Relay.
