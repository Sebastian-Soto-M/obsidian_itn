---
tags: concept/itn
---
# Direcciones de host
Las direcciones de host son direcciones que se pueden asignar a un dispositivo, como un equipo host, un portátil, un teléfono inteligente, una cámara web, una impresora, un router, etc. La parte de host de la dirección son los bits indicados por 0 bits en la máscara de subred. Las direcciones de host pueden tener cualquier combinación de bits en la parte del host excepto los 0 bits (esto sería una dirección de red) o los 1 bits (esto sería una dirección de difusión).

Todos los dispositivos dentro de la misma red deben tener la misma máscara de subred y los mismos bits de red. Solo los bits del host serán diferentes y deben ser únicos.

Observe que en la tabla, hay una primera y última dirección de host:

-   **Primera dirección de host** : este primer host dentro de una red tiene todos los 0 bits con el último bit (más a la derecha) como 1 bit. En este ejemplo es 192.168.10.1/24.
-   **Última dirección de host** : este último host dentro de una red tiene los 1 bits con el último bit (más a la derecha) como 0 bit. En este ejemplo es 192.168.10.254/24.

Cualquier dirección entre 192.168.10.1/24 y 192.168.10.254/24 se puede asignar a un dispositivo de la red.