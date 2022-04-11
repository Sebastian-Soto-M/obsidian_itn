---
up: [[mod11ITN Module 11 MOC]]
---
# Diseño Estructurado
## Planificación de direcciones de red IPv4

Antes de iniciar la subred, debe desarrollar un esquema de direccionamiento IPv4 para toda la red. Necesitará saber cuántas subredes necesita, cuántos hosts requiere una subred concreta, qué dispositivos forman parte de la subred, qué partes de la red utilizan direcciones privadas y cuáles utilizan público, y muchos otros factores determinantes. Un buen esquema de direccionamiento permite el crecimiento. Un buen esquema de direccionamiento es también el signo de un buen administrador de red.

La planificación de las subredes de la red requiere un análisis tanto de las necesidades de uso de red de la organización como de la forma en que se estructurarán las subredes. El punto de partida consiste en llevar a cabo un estudio de los requisitos de la red. Esto significa mirar toda la red, tanto la intranet como la DMZ, y determinar cómo se segmentará cada área. El plan de direcciones incluye determinar dónde se necesita la conservación de direcciones (generalmente dentro de la DMZ) y dónde hay más flexibilidad (generalmente dentro de la intranet).

Cuando se requiera la conservación de direcciones, el plan debe determinar cuántas subredes se necesitan y cuántos hosts por subred. Como se mencionó anteriormente, esto suele ser necesario para el espacio de direcciones IPv4 público dentro de la DMZ. Esto probablemente incluirá el uso de VLSM.

Dentro de la intranet corporativa, la conservación de direcciones suele ser menos problemática. Esto se debe en gran medida al uso de direcciones IPv4 privadas, incluyendo 10.0.0.0/8, con más de 16 millones de direcciones IPv4 de host.

Para la mayoría de las organizaciones, las direcciones IPv4 privadas permiten más que suficientes direcciones internas (intranet). Para muchas organizaciones e ISP más grandes, incluso el espacio de direcciones IPv4 privado no es lo suficientemente grande como para satisfacer sus necesidades internas. Esta es otra razón por la que las organizaciones están haciendo la transición a IPv6.

Para las intranets que utilizan direcciones IPv4 privadas y DMZs que utilizan direcciones IPv4 públicas, la planificación y asignación de direcciones es importante.

Cuando sea necesario, el plan de direcciones incluye determinar las necesidades de cada subred en términos de tamaño. ¿Cuántos hosts habrá en cada subred? El plan de direcciones también debe incluir cómo se asignarán las direcciones de host, qué hosts requerirán direcciones IPv4 estáticas y qué hosts pueden usar DHCP para obtener su información de direccionamiento. Esto también ayudará a evitar la duplicación de direcciones, al tiempo que permitirá supervisar y administrar direcciones por razones de rendimiento y seguridad.

Conocer los requisitos de direcciones IPv4 determinará el rango, o intervalos, de direcciones de host que implementa y ayudará a garantizar que haya suficientes direcciones para cubrir sus necesidades de red.

## Asignación de direcciones de dispositivo

Dentro de una red, hay diferentes tipos de dispositivos que requieren direcciones:

- **Clientes usuarios finales** - la mayoría de las redes asignan direcciones de manera dinámica con el protocolo de configuración dinámica de host (DHCP). Esto reduce la carga sobre el personal de soporte de red y elimina de manera virtual los errores de entrada. Con DHCP, las direcciones sólo se alquilan durante un período de tiempo y se pueden reutilizar cuando caduque la concesión. Esta es una característica importante para las redes que admiten usuarios transitorios y dispositivos inalámbricos. Cambiar el esquema de subredes significa que el servidor DHCP necesita ser reconfigurado y los clientes deben renovar sus direcciones IPv4. Los clientes IPv6 pueden obtener información de dirección mediante DHCPv6 o SLAAC.
- **Servidores y periféricos** - deben tener una dirección IP estática predecible. Utilice un sistema de numeración coherente para estos dispositivos.
- **Servidores a los que se puede acceder desde Internet** - los servidores que deben estar disponibles públicamente en Internet deben tener una dirección IPv4 pública, a la que se accede con mayor frecuencia mediante NAT. En algunas organizaciones, los servidores internos (no disponibles públicamente) deben ponerse a disposición de los usuarios remotos. En la mayoría de los casos, a estos servidores se les asignan direcciones privadas internamente y se requiere que el usuario cree una conexión de red privada virtual (VPN) para acceder al servidor. Esto tiene el mismo efecto que si el usuario accede al servidor desde un host dentro de la intranet.
- **Dispositivos intermediarios** - estos dispositivos tienen direcciones asignadas para la administración, monitoreo y seguridad de la red. Debido a que es necesario saber cómo comunicarse con dispositivos intermediarios, estos deben tener asignadas direcciones predecibles y estáticas.
- **Puerta de enlace** - los routeres y los dispositivos de firewall tienen una dirección IP asignada a cada interfaz que sirve como puerta de enlace para los hosts en esa red. Normalmente, la interfaz de router utiliza la dirección más baja o más alta de la red.

Al desarrollar un esquema de direccionamiento IP, generalmente se recomienda que tenga un patrón establecido de cómo se asignan las direcciones a cada tipo de dispositivo. Esto beneficia a los administradores a la hora de agregar y quitar dispositivos, ya que filtra el tráfico basado en IP, y también simplifica el registro.

## Packet Tracer - Práctica de Diseño e Implementación de VLSM

- [[11.9.3-packet-tracer---vlsm-design-and-implementation-practice_es-XL.pdf]]
- [[11.9.3-packet-tracer---vlsm-design-and-implementation-practice_es-XL.pka]]
