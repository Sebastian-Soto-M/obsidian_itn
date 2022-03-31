---
up: [[Introduction to Networks v7.02 (ITN) Index]]
tags: quiz/netacad
---
# Exam Mod 1-3

```ad-question
title: ¿Qué término describe una red donde un equipo puede ser tanto cliente como servidor?
- [x]   Entre pares
- [ ]   calidad de servicio
- [ ]   nube
- [ ]   BYOD

```

```ad-question
title: Después de realizar cambios de configuración en un switch Cisco, un administrador de redes emite el comando copy running-config startup-config . ¿Qué sucede al emitir este comando?

- [ ] La nueva configuración se almacena en la memoria flash.
- [x] Si se reinicia el switch, se carga la nueva configuración.
- [ ] El archivo de IOS actual se reemplaza por el archivo configurado recientemente.
- [ ] Se eliminan los cambios de configuración y se restaura la configuración original.

```ad-info
title: Explique
collapse: closed
Con el comando copy running-config startup-config , el contenido de la configuración operativa actual reemplaza el archivo de configuración de inicio almacenado en la NVRAM. El archivo de configuración guardado en la NVRAM se carga cuando se reinicia el dispositivo.

```

```ad-question
title: Un administrador está configurando la contraseña del puerto de consola de un switch. ¿En qué orden debe el administrador atravesar los modos de operación de IOS para llegar al modo en el que introducirá los comandos de configuración? No se utilizan todas las opciones.

1. Modo EXEC del usuario
2. Modo EXEC privilegiado
3. Modo de configuración global
4. Modo de configuración de linea
```

```ad-question
title: ¿Cuáles son los dos nombres de host que cumplen las pautas de convenciones de nomenclatura en dispositivos con Cisco IOS? Elija dos opciones.

- [x]   SwBranch799
- [x]   RM-3-Switch-2A4
- [ ]   Branch2!
- [ ]   HO Floor 17
- [ ]   Floor(15)

```

```ad-question
title: ¿Qué comando se utiliza para verificar el estado de las interfaces del switch, incluido el estado de las interfaces y una dirección IP configurada?

- [ ]   ipconfig
- [x]   show ip interface brief
- [ ]   traceroute
- [ ]   ping

```

```ad-question
title: ¿Cuál de los siguientes comandos o combinaciones de teclas le permite a un usuario regresar al nivel anterior en la jerarquía de comandos?

- [x] exit
- [ ] Ctrl-Z
- [ ] end
- [ ] Ctrl-C

```

```ad-question
title: Se pueden usar contraseñas para restringir el acceso a todo o parte del Cisco IOS. Seleccione los modos e interfaces que se pueden proteger con contraseñas. (Elija tres).

- [ ] Modo de configuración del router
- [x] Interfaz de consola
- [ ] Interfaz Ethernet
- [x] Interfaz VTY
- [x] Modo EXEC privilegiado
- [ ] Modo de arranque de IOS

```

```ad-question
title: Una la descripción con el modo de IOS relacionado. (No se utilizan todas las opciones).
collapse: closed

![[Pasted image 20220317095727.png]]

```

```ad-question
title: ¿Cuáles de las siguientes son dos características de la RAM en un dispositivo Cisco? Elija dos opciones.

- [ ] La RAM es un componente de los switches Cisco, pero no de los routers Cisco.
- [x] La configuración que está activamente en ejecución en el dispositivo se almacena en la RAM.
- [x] El contenido de la RAM se pierde al apagar y volver a encender el dispositivo.
- [ ] La RAM puede almacenar varias versiones de IOS y de archivos de configuración.
- [ ] La RAM proporciona almacenamiento no volátil.

```

```ad-question
title: Un administrador de red ingresa el comando service password-encryption en el modo de configuración de un router. ¿Qué logra este comando?

- [ ] Este comando cifra automáticamente las contraseñas en los archivos de configuración que se almacenan actualmente en NVRAM.
- [x] Este comando impide que alguien vea las contraseñas de configuración en ejecución.
- [ ] Este comando proporciona una contraseña cifrada exclusiva para el personal de servicio externo que debe realizar el mantenimiento del enrutador.
- [ ] Este comando habilita un algoritmo de cifrado seguro para el comando enable secret password .
- [ ] Este comando cifra las contraseñas a medida que se transmiten a través de vínculos WAN serie.

```

```ad-question
title: Consulte la ilustración. Un administrador de redes está configurando el control de acceso al switch SW1. Si el administrador utiliza una conexión de consola para conectarse al switch, ¿cuál de las siguientes contraseñas se necesita para acceder al modo EXEC del usuario?
![[Pasted image 20220317100036.png]]
- [ ] letmein
- [ ] secretin
- [x] lineconin
- [ ] linevtyin

```

```ad-question
title: Una las definiciones con los respectivos métodos abreviados y teclas de acceso rápido de la CLI. No se utilizan todas las opciones.
collapse: closed

![[Pasted image 20220317100205.png]]

```

```ad-question
title: Un técnico configura un switch con los siguientes comandos

¿Qué configura el técnico?
- [ ] Acceso físico al puerto de switch
- [ ] Cifrado de contraseñas
- [ ] Acceso por Telnet
- [x] SVI

```sh
SwitchA(config)# **interface vlan 1**  
SwitchA(config-if)# **ip address 192.168.1.1 255.255.255.0**  
SwitchA(config-if)# **no shutdown**
```

```ad-question
title: ¿En qué se diferencian SSH y Telnet?

- [ ] SSH se debe configurar en una conexión de red activa, mientras que Telnet se usa para conectarse a un dispositivo mediante una conexión de consola.
- [x] SSH proporciona seguridad a las sesiones remotas al cifrar los mensajes y solicitar la autenticación de usuarios. Telnet se considera inseguro y envía mensajes en texto sin formato.
- [ ] SSH requiere el uso del programa de emulación de terminal PuTTY. Para conectarse a los dispositivos mediante Telnet, se debe usar Tera Term.
- [ ] SSH conexiones a través de la red, mientras que Telnet se usa para el acceso fuera de banda.

```

```ad-question
title: ¿En qué capa OSI se agrega una dirección IP de origen a una PDU durante el proceso de encapsulación?

- [ ] Capa de enlace de datos
- [ ] Capa de transporte
- [x] Capa de red
- [ ] Capa de aplicación

```

```ad-question
title: Una cada característica con el tipo de conectividad a Internet correspondiente. No se utilizan todas las opciones.
collapse: closed

![[Pasted image 20220317101740.png]]

```

```ad-question
title: ¿Qué tipo de tráfico de red requiere QoS?

- [ ] Correo electrónico
- [ ] Compras en línea
- [ ] Wiki
- [x] Videoconferencia

```

```ad-question
title: Un técnico de redes está trabajando en la red inalámbrica en una clínica médica. El técnico configura accidentalmente la red inalámbrica para que los pacientes puedan ver los datos de los registros médicos de otros pacientes. ¿Cuál de las cuatro características de la red se ha violado en esta situación?

- [ ] Escalabilidad
- [x] Seguridad
- [ ] Confiabilidad
- [ ] Calidad de servicio (QoS)
- [ ] Tolerancia a fallas

```

```ad-question
title: Consulte la ilustración. Un administrador intenta configurar el switch pero recibe el mensaje de error que se muestra en la ilustración. ¿Cuál es el problema?

![[Pasted image 20220317102137.png]]
- [x] El administrador primero debe ingresar al modo EXEC privilegiado antes de emitir el comando.
- [ ] El administrador ya se encuentra en el modo de configuración global.
- [ ] Se debe utilizar el comando completo **configure terminal** .
- [ ] El administrador se debe conectar a través del puerto de consola para acceder al modo de configuración global.

```

```ad-question
title: ¿Por qué un switch de capa 2 necesitaría una dirección IP?

- [x] Para habilitar el switch de modo que se administre de forma remota.
- [ ] Para habilitar el switch para que envíe tramas de broadcast a las PC conectadas.
- [ ] Para habilitar el switch para que reciba tramas de las PC conectadas.
- [ ] Para habilitar el switch para que funcione como un gateway predeterminado.

```

```ad-question
title: ¿Cuál de estos dispositivos cumple la función de determinar la ruta que los mensajes deben tomar a través de las internetworks?

- [x] Un router
- [ ] Un firewall
- [ ] Un módem DSL
- [ ] Un servidor Web

```

```ad-question
title: ¿Cual es la dirección IP de la interfaz virtual del switch (SVI), en el Switch0?

- [ ] 192.168.10.1
- [ ] 192.168.5.0
- [x] 192.168.5.10
- [ ] 192.168.10.5

```

```ad-question
title: Una la descripción con la organización. No se utilizan todas las opciones.
collapse: closed

![[Pasted image 20220317102718.png]]

```

```ad-question
title: ¿Qué formato de PDU se utiliza cuando la NIC de un host recibe bits del medio de red?

- [ ] Archivo
- [ ] Segmento
- [x] Trama
- [ ] Paquete

```

```ad-question
title: ¿Qué tres protocolos de la capa de aplicación forman parte del paquete del protocolo TCP/IP? Elija tres opciones.

- [ ] RP
- [x] FTP
- [ ] NAT
- [ ] PPP
- [x] DHCP
- [x] DNS

```

```ad-question
title: ¿Cuál de estas afirmaciones describe de forma precisa un proceso de encapsulación TCP/IP cuando una PC envía datos a la red?

- [ ] Los paquetes se envían de la capa de acceso a la red a la capa de transporte.
- [x] Los segmentos se envían de la capa de transporte a la capa de Internet.
- [ ] Las tramas se envían de la capa de acceso a la red a la capa de Internet.
- [ ] Los datos se envían de la capa de Internet a la capa de acceso a la red.

```

```ad-question
title: ¿Cuál de estos métodos pueden utilizar dos PC para asegurar que no se descarten los paquetes debido a que se envían demasiados datos demasiado rápido?

- [ ] Tiempo de espera de respuesta
- [ ] Método de acceso
- [x] Control del flujo
- [ ] Encapsulación

```

```ad-question
title: ¿Cuál es la capa responsable de enrutar los mensajes en una interconexión de redes en el modelo TCP/IP?

- [ ] Acceso a la red
- [x] Internet
- [ ] Transporte
- [ ] Sesión

```

```ad-question
title: Observe la ilustración. El ServidorB está intentando ponerse en contacto con HostA. ¿Qué dos instrucciones identifican correctamente el direccionamiento que ServidorB generará en el proceso? (Escoja dos opciones).

![[Pasted image 20220317103404.png]]

- [x] ServidorB generará un paquete con la dirección IP de destino de HostA.
- [x] ServidorB generará una trama con la dirección MAC de destino del RouterB.
- [ ] ServidorB generará un paquete con la dirección IP de destino de RouterA.
- [ ] ServidorB generará una trama con la dirección MAC de destino del SwitchB.
- [ ] ServidorB generará una trama con la dirección MAC de destino de RouterA.
- [ ] ServidorB generará un paquete con la dirección IP de destino del RouterB.

```

```ad-question
title: Un cliente Web está recibiendo una respuesta para una página Web de un servidor Web. Desde la perspectiva del cliente, ¿cuál es el orden correcto de la pila de protocolos que se usa para decodificar la transmisión recibida?

- [x]   Ethernet, IP, TCP, HTTP
- [ ]   HTTP, Ethernet, IP, TCP
- [ ]   HTTP, TCP, IP, Ethernet
- [ ]   Ethernet, TCP, IP, HTTP
```

```ad-question

title: ¿En cuál de estas capas del modelo OSI se agregaría una dirección lógica durante el encapsulamiento?

- [x] Capa de red
- [ ] Capa física
- [ ] Capa de enlace de datos
- [ ] Capa de transporte

```

```ad-question
title: ¿Qué método permite que un equipo reaccione en consecuencia cuando solicita datos de un servidor y el servidor tarda demasiado en responder?

- [ ] método de acceso
- [x] tiempo de espera de respuesta
- [ ] Encapsulamiento
- [ ] Control del flujo

```

```ad-question
title: ¿Cuál de las siguientes es una característica de los mensajes multidifusión?

- [ ] Se envían a un destino único.
- [ ] Se envían a todos los hosts de una red.
- [x] Se envían a un grupo seleccionado de hosts.
- [ ] Debe acusarse su recibo.

```
