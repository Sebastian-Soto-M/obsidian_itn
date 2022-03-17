---
tags: quiz/university
---

# Exam Mod 4-7

```ad-question
title: ¿Cuáles de las siguientes son dos características de un cable de fibra óptica? Elija dos opciones.

- [x] Es más caro que el cable UTP.
- [ ] Combina las técnicas de anulación, protección y trenzado para proteger los datos.
- [x] No lo afectan la EMI ni la RFI.
- [ ] Cada par de cables se encuentra envuelto en papel metálico.
- [ ] Típicamente, contiene cuatro pares de hilos de fibra óptica.

**Explique:** El cableado de fibra óptica admite un mayor ancho de banda que el UTP para distancias más grandes. La fibra es inmune a la EMI y a la RFI, pero es más costosa, es más difícil de instalar y requiere más precauciones de seguridad.
```

```ad-question
title: Con el uso del cable de cobre de par trenzado sin blindaje en una red, ¿qué causa croostalk dentro de los pares de cables?

- [ ] el uso de alambre trenzado para proteger los pares de cables adyacentes
- [x] el campo magnético alrededor de los pares adyacentes de alambre
- [ ] la colisión causada por dos nodos que intentan usar los medios simultáneamente
- [ ] el reflejo de la onda eléctrica de vuelta desde el extremo lejano del cable

**Explique:** Crosstalk es un tipo de ruido o interferencia que se produce cuando la transmisión de la señal en un cable interfiere con otro cable. Cuando la corriente fluye a través de un cable, se produce un campo magnético. El campo magnético producido interconectará la señal transportada en el cable adyacente.
```

```ad-question
title: Consulte el gráfico. ¿Qué tipo de cableado se muestra?

![[Pasted image 20220317105320.png]]
- [ ] Coaxial
- [x] Fibra
- [ ] UTP
- [ ] STP

**Explique:** El cableado de red incluye diferentes tipos de cables:
Consta de cuatro pares de hilos codificados por colores que están trenzados entre sí y recubiertos con un revestimiento de plástico flexible.
STP utiliza cuatro pares de hilos. Cada uno de estos pares está empaquetado primero con un blindaje de hoja metálica y, luego, el conjunto se empaqueta con una malla tejida o una hoja metálica.
El cable coaxial utiliza un conductor de cobre y una capa de aislamiento plástico flexible rodea el conductor de cobre.
El cable de fibra es una un vidrio flexible, extremadamente delgado y transparente rodeada de aislamiento de plástico.
```

```ad-question
title: Además de la longitud del cable, ¿cuáles son los otros dos factores que podrían interferir en la comunicación por cables UTP? Elija dos opciones.

- [x] Interferencia electromagnética
- [ ] Tamaño de la red
- [ ] Ancho de banda
- [x] Crosstalk
- [ ] Técnica de modulación de señal

**Explique:** Los medios de cobre se utilizan de manera extensiva en las comunicaciones de red. Sin embargo, estos medios están limitados por la distancia y la interferencia de señal. Los datos se transmiten por cables de cobre como impulsos eléctricos, que son susceptibles a la interferencia de dos orígenes:
Interferencia electromagnética (EMI) o interferencia de radiofrecuencia (RFI): las señales de EMI y RFI pueden distorsionar y dañar las señales de datos que transportan los medios de cobre.
Crosstalk: se trata de una perturbación causada por los campos eléctricos o magnéticos de una señal de un hilo a la señal de un hilo adyacente.
```

```ad-question
title: Consulte el gráfico. ¿Qué tipo de cableado se muestra?**
![[Pasted image 20220317105724.png]]
- [ ] Fibra
- [ ] Coaxial
- [x] UTP
- [ ] STP

**Explique:** El cableado de red incluye diferentes tipos de cables:
UTP Consta de cuatro pares de hilos codificados por colores que están trenzados entre sí y recubiertos con un revestimiento de plástico flexible.
STP utiliza cuatro pares de hilos. Cada uno de estos pares está empaquetado primero con un blindaje de hoja metálica y, luego, el conjunto se empaqueta con una malla tejida o una hoja metálica.
El cable coaxial utiliza un conductor de cobre y una capa de aislamiento plástico flexible rodea el conductor de cobre.
El cable de fibra es un vidrio flexible, extremadamente delgado y transparente rodeada de aislamiento de plástico.
```

```ad-question
title: ¿Cuáles son los dos dispositivos que comúnmente afectan las redes inalámbricas? (Elija dos opciones).

- [ ] Lámparas incandescentes
- [ ] Centros de entretenimiento
- [x] Microondas
- [ ] Discos duros externos
- [x] Teléfonos inalámbricos
- [ ] Reproductores de Blu-ray

**Explique:** La interferencia de radiofrecuencia (RFI, Radio Frequency Interference) es la interferencia causada por los trasmisores de radio y otros dispositivos que transmiten la misma frecuencia.
```

```ad-question
title: ¿Cuáles dos instrucciones describen los servicios proporcionados por la capa de enlace de datos? (Escoja dos opciones).

- [ ] Define el esquema de direccionamiento de entrega de extremo a extremo.
- [x] Gestiona el acceso de tramas a los medios de red.
- [ ] Mantiene la ruta entre los dispositivos de origen y destino durante la transmisión de datos.
- [ ] Garantiza que los datos de la aplicación se transmitan de acuerdo con la priorización.
- [ ] Proporciona una entrega fiable a través del establecimiento de enlaces y el control de flujo.
- [x] Empaque varias PDU de capa 3 en un formato de trama que es compatible con la interfaz de red.

**Explique:** La capa de enlace de datos del modelo OSI se divide en dos subcapas: la subcapa de control de acceso al medio (MAC) y la subcapa de control de enlace lógico (LLC). LLC forma una trama de la PDU de capa de red en un formato que se ajusta a los requisitos de la interfaz de red y los medios. Una PDU de capa de red puede ser para IPv4 o IPv6. La sub-capa MAC he MAC define los procesos de acceso al medio que realiza el hardware. Gestiona el acceso de trama a los medios de red de acuerdo con los requisitos de señalización física (cable de cobre, fibra óptica, inalámbrica, etc.)
```

```ad-question
title: ¿Cuál es la función del valor CRC que se encuentra en el campo FCS de una trama?

- [ ] Verificar la dirección física que se encuentra en la trama.
- [x] Verificar la integridad de la trama recibida.
- [ ] Calcular el encabezado checksum para el campo de datos de la trama.
- [ ] Verificar la dirección lógica que se encuentra en la trama.

**Explique:** El valor CRC del campo FCS de la trama recibida se compara con el valor CRC calculado para verificar la integridad de dicha trama. Si los dos valores no coinciden, se descarta la trama.
```

```ad-question
title: ¿Qué contiene el tráiler de una trama de enlace de datos?

- [ ] DATA
- [x] Detección de errores
- [ ] Dirección lógica
- [ ] Dirección física

**Explique:** El tráiler de una trama de enlace de datos contiene la información de detección de errores pertinente a la trama incluida en el campo FCS. El encabezado contiene información de control, como el direccionamiento, mientras que el área que indica la palabra “data” (datos) incluye los datos, la PDU de la capa de transporte y el encabezado IP.
```

```ad-question
title: ¿Cuál de estas afirmaciones describe una característica de los campos de encabezado de la trama de la capa de enlace de datos?

- [ ] Los campos de encabezado de la trama de Ethernet contienen las direcciones de origen y destino de la capa 3.
- [ ] Incluyen información sobre las aplicaciones de usuario.
- [x] Varían según los protocolos.
- [ ] Todos incluyen los campos de control del flujo y de conexión lógica.

**Explique:** Todos los protocolos de capa de enlace de datos encapsulan la PDU de la capa 3 dentro del campo de datos de la trama. Sin embargo, la estructura de la trama y los campos contenidos en el encabezado varían de acuerdo con el protocolo. Los distintos protocolos de capa de enlace de datos pueden utilizar campos distintos, como prioridad/calidad de servicio, control de conexión lógica, control de enlace físico, control del flujo y control de congestión.
```

```ad-question
title: Un equipo de redes compara las topologías físicas WAN para la conexión de sitios remotos al edificio de una oficina central. ¿Qué topología proporciona alta disponibilidad y conecta algunos sitios remotos, pero no todos?

- [x] Malla parcial
- [ ] Hub-and-spoke
- [ ] Malla
- [ ] Punto a punto

**Explique:** Las topologías de malla parcial proporcionan alta disponibilidad porque interconectan varios sitios remotos, pero no requieren una conexión entre todos los sitios remotos. Las topologías de malla requieren enlaces punto a punto, donde cada sistema esté conectado a todos los demás sistemas. Una topología punto a punto se da cuando cada dispositivo está conectado a un dispositivo. Las topologías hub-and-spoke utilizan un dispositivo central en una topología en estrella que se conecta a otros dispositivos punto a punto.
```

```ad-question
title: ¿Qué dos campos o características examina Ethernet para determinar si una trama recibida es pasada a la capa de enlace de datos o descartada por la NIC? (Escoja dos opciones).

- [ ] Dirección MAC de origen
- [x] Secuencia de verificación de trama
- [x] tamaño mínimo de trama
- [ ] CEF
- [ ] MDIX automático

**Explique:** Una trama Ethernet no se procesa y se descarta si es menor que el mínimo (64 bytes) o si el valor de la secuencia de comprobación de trama calculada (FCS) no coincide con el valor FCS recibido. Auto-MDIX (cruce automático de interfaz dependiente del medio) es tecnología de capa 1 que detecta los tipos de cable directo o cruzado. La dirección MAC de origen no se utiliza para determinar cómo se recibe la trama. CEF (Cisco Express Forwarding) es una tecnología utilizada para acelerar switching a nivel 3.
```

```ad-question
title: ¿Qué tipo de comunicación de medios no requiere arbitraje en la capa de enlace de datos?

- [ ] Acceso controlado
- [ ] Semidúplex
- [x] Dúplex completo
- [ ] determinante

**Explique:** Comunicación half-duplex: los dos dispositivos pueden transmitir y recibir en los medios pero no pueden hacerlo simultáneamente. Comunicación full-dúplex: los dos dispositivos pueden transmitir y recibir en los medios al mismo tiempo. La comunicación semidúplex suele basarse en la contencion, mientras que el acceso controlado (determinista) se aplica en tecnologías donde los dispositivos se turnan para acceder al medio.
```

```ad-question
title: ¿Cuál de las siguientes es una característica de la subcapa LLC?

- [ ] Proporciona la delimitación de datos según los requisitos de señalización física del medio.
- [ ] Proporciona el direccionamiento lógico requerido que identifica el dispositivo.
- [x] Coloca en la trama información que permite que varios protocolos de capa 3 utilicen la misma interfaz y los mismos medios de red.
- [ ] Define los procesos de software que proporcionan servicios a la capa física.

**Explique:** El control de enlace lógico (LLC) define los procesos de software que proporcionan servicios a los protocolos de capa de red. El LLC coloca información en la trama e identifica qué protocolo de capa de red se utiliza para ella. Esta información permite que varios protocolos de capa 3, tales como IPv4 e IPv6, utilicen la misma interfaz y los mismos medios de red.
```

```ad-question
title: ¿Qué tres partes básicas son comunes a todos los tipos de trama admitidos por la capa de enlace de datos? (Escoja tres opciones).

- [x] data
- [ ] MTU size
- [ ] type field
- [ ] Valor CRC
- [x] header
- [x] trailer

**Explique:** La capa de enlace de datos implica una comunicación de NIC a NIC dentro de la misma red. Si bien existen muchos protocolos de capa de enlace de datos diferentes que describen las tramas de la capa de enlace de datos, cada tipo de trama tiene tres partes básicas:
Header
Data
Trailer
```

```ad-question
title: Consulte la ilustración. ¿Cuál es la dirección MAC de destino de la trama de Ethernet al salir del servidor web si el destino final es la PC1?

![[Pasted image 20220317105751.png]]
- [ ] 00-60-2F-3A-07-BB
- [x] 00-60-2F-3A-07-CC
- [ ] 00-60-2F-3A-07-AA
- [ ] 00-60-2F-3A-07-DD

**Explique:** La dirección MAC de destino se utiliza para la entrega local de tramas de Ethernet. La dirección MAC (capa 2) cambia en cada segmento de red a lo largo de la ruta. Cuando la trama sale del servidor web, se entrega utilizando la dirección MAC del gateway predeterminado.
```

```ad-question
title: Un switch de capa 2 se utiliza para conmutar las tramas entrantes desde un puerto 1000BASE-T a un puerto conectado a una red 100Base-T. ¿Qué método de almacenamiento en búfer de memoria sería el más adecuado para esta tarea?

- [ ] Almacenamiento en búfer basado en puerto
- [ ] Almacenamiento en búfer de caché de nivel 1
- [ ] Almacenamiento en búfer de configuración fija
- [x] Almacenamiento en búfer de memoria compartida

**Explique:** Mediante el almacenamiento en búfer de memoria compartida, la cantidad de tramas almacenadas en el búfer solo se encuentra limitada por el tamaño del búfer de memoria en su totalidad y no se limita al búfer de un solo puerto. Esto permite la transmisión de tramas más amplias y que se descarte una menor cantidad de ellas. Esto es importante para la conmutación asimétrica, la cual se aplica a esta situación, donde las tramas se intercambian entre puertos con distintas velocidades. Con el almacenamiento en búfer de memoria basado en puerto, las tramas se almacenan en colas vinculadas a puertos de entrada y de salida específicos, lo que permite que una única trama retrase la transmisión de todas las tramas en la memoria debido a un puerto de destino ocupado. La memoria caché de nivel 1 es la que se utiliza en las CPU. La configuración fija se refiere a la disposición de los puertos en el hardware del switch.
```

```ad-question
title: ¿Cuáles de los siguientes son dos ejemplos de switching por método de corte? Elija dos opciones.

- [ ] Switching de almacenamiento y envío
- [ ] Switching CRC
- [ ] Switching QOS
- [x] Switching de envío rápido
- [x] Switching libre de fragmentos

**Explique:** El switching de almacenamiento y envío acepta la trama completa y realiza una verificación de errores con la CRC antes de reenviarla. A menudo, este método se requiere para el análisis de QOS. El método de envío rápido y el método libre de fragmentos son variaciones del switching por método de corte, en el que el switch solamente recibe parte de la trama antes de comenzar a reenviarla.
```

```ad-question
title: ¿En qué método de reenvío de tramas se recibe la trama completa y se realiza una comprobación de CRC para detectar errores antes de reenviarla?

- [ ] Switching libre de fragmentos
- [x] Switching de almacenamiento y envío
- [ ] Switching por método de corte
- [ ] Switching de envío rápido

**Explique:** El switching de envío rápido y el switching libre de fragmentos son variaciones del switching por método de corte, que comienza a reenviar la trama antes de recibirla por completo.
```

```ad-question
title: ¿Cuál es el propósito del campo FCS en una trama?

- [ ] Verificar la dirección lógica del nodo emisor.
- [ ] Obtener la dirección MAC del nodo emisor.
- [x] Determinar si ocurrieron errores durante la transmisión y recepción.
- [ ] Calcular el encabezado CRC para el campo de datos.

**Explique:** En una trama, el campo FCS se utiliza para detectar cualquier error en la transmisión y la recepción de una trama. Esto se hace al comparar el valor de CRC dentro de la trama con un valor de CRC computado de la trama. Si los dos valores no coinciden, se descarta la trama.
```

```ad-question
title: Un administrador de red conecta dos switches modernos mediante un cable de conexión directa. Los switches son nuevos y nunca se configuraron. ¿Cuáles son las tres afirmaciones correctas sobre el resultado final de la conexión? (Elija tres).

- [ ] La conexión no será posible a menos que el administrador reemplace el cable por un cable de conexión cruzada.
- [ ] La capacidad dúplex se debe configurar manualmente porque no puede negociarse.
- [x] El enlace entre los switches funcionará como full-duplex.
- [x] El enlace entre los switches funcionará a la máxima velocidad que admitan ambos switches.
- [ ] Si ambos switches admiten velocidades diferentes, cada switch funcionará a su propia velocidad máxima.
- [x] La característica MDIX automática configurará las interfaces, por lo que no se necesita un cable de conexión cruzada.

**Explique:** Los switches modernos pueden negociar el funcionamiento en modo full-duplex si ambos switches tienen esa capacidad. Negocian funcionar con la velocidad más alta posible, y la característica MDIX automática está habilitada de manera predeterminada, por lo que no es necesario un cambio de cable.
```

```ad-question
title: ¿Qué ventaja posee el método de switching de almacenamiento y reenvío en comparación con el método de switching por método de corte?

- [ ] Reenvío de tramas más rápido
- [ ] Reenvío de tramas utilizando la información de IPv4 de capa 3 y 4
- [ ] Detección de colisión
- [x] Verificación de errores de la trama

**Explique:** Un switch que utiliza el método de switching de almacenamiento y reenvío realiza una verificación de errores en una trama entrante comparando el valor de FCS con sus propios cálculos de FCS después de recibir la trama completa. En comparación, un switch que usa el switching por método de corte toma rápidas decisiones de reenvío e inicia el proceso de reenvío sin esperar la recepción de la trama completa. Por ende, un switch que usa el switching por método de corte puede enviar tramas no válidas a la red. El rendimiento del switching de almacenamiento y envío es más lento en comparación con el rendimiento del switching por método de corte. El dispositivo emisor controla la detección de colisiones. El switching de almacenamiento y reenvío no utiliza la información de IPv4 de capa 3 y 4 para sus decisiones de reenvío.
```

```ad-question
title: ¿Cuál de los siguientes métodos de switching utiliza el valor CRC de una trama?

- [x] Almacenamiento y envío
- [ ] Envío rápido
- [ ] Libre de fragmentos
- [ ] Método de corte

**Explique:** Cuando se utiliza el método de switching de almacenamiento y envío, el switch recibe la trama completa antes de reenviarla al destino. La porción de comprobación cíclica de redundancia (CRC) del tráiler se utiliza para determinar si la trama se modificó durante el tránsito. En cambio, un switch por método de corte reenvía la trama una vez que se lee la dirección de capa 2 de destino. Dos tipos de switching por método de corte son el método de envío rápido y el método libre de fragmentos.
```

```ad-question
title: ¿Cuáles de las siguientes son dos acciones que realiza un switch Cisco? Elija dos opciones.

- [x] Uso de la tabla de direcciones MAC para enviar tramas por medio de la dirección MAC de destino
- [ ] Reenvío de tramas con direcciones IP de destino desconocidas al gateway predeterminado
- [ ] Armado de una tabla de routing basada en la primera dirección IP en el encabezado de la trama
- [x] Uso de la dirección MAC de origen de las tramas para armar y mantener una tabla de direcciones MAC
- [ ] Revisión de la dirección MAC de destino para agregar nuevas entradas a la tabla de direcciones MAC

**Explique:** Las acciones importantes que realiza un switch son las siguientes:
Cuando llega una trama, el switch examina la dirección de origen de capa 2 para armar y mantener la tabla de direcciones MAC de capa 2.
Examina la dirección de destino de capa 2 para determinar cómo reenviar la trama. Cuando la dirección de destino se encuentra en la tabla de direcciones MAC, la trama se envía por un puerto específico. Cuando la dirección es desconocida, la trama se envía a todos los puertos que tienen dispositivos conectados a esa red.
```

```ad-question
title: ¿Qué es la función Auto-MDIX?

- [x] Permite a un dispositivo configurar automáticamente una interfaz para utilizar un cable directo o cruzado.
- [ ] Permite que un dispositivo configure automáticamente la velocidad de su interfaz.
- [ ] Permite a un switch seleccionar dinámicamente el método de reenvío.
- [ ] Permite a un dispositivo configurar automáticamente los ajustes dúplex de un segmento.

**Explique:** La función Auto-MDIX permite al dispositivo configurar su puerto de red de acuerdo con el tipo de cable que se utiliza (directo o cruzado) y el tipo de dispositivo que está conectado a ese puerto.Cuando un puerto de un switch está configurado con Auto-MDIX, este switch se puede conectar a otro switch mediante el uso de un cable directo o un cable cruzado.
```

```ad-question
title: ¿Cuál es una dirección MAC multicast?

- [ ] FF-FF-FF-FF-FF-FF
- [ ] 5C-26-0A-4B-19-3E
- [ ] 00-26-0F-4B-00-3E
- [x] 01-00-5E-00-00-03

**Explique:** Las direcciones MAC multicast comienzan con el valor especial 01-00-5E.
```

```ad-question
title: Consulte la ilustración. ¿Cuál es el problema con la terminación que se muestra?

![[Pasted image 20220317105824.png]]
- [ ] No se debería haber quitado la malla de cobre tejida.
- [ ] Se está utilizando el tipo de conector incorrecto.
- [x] La longitud de la parte sin trenzar de cada cable es demasiado larga.
- [ ] Los cables son demasiado gruesos para el conector que se utiliza.

**Explique:** uando se realiza la terminación de un cable con un conector RJ-45, es importante asegurar que los cables sin trenzar no sean demasiado largos y que el revestimiento de plástico flexible que rodea los cables esté engarzado, es decir, que no haya hilos desnudos. No se debe ver ninguno de los cables de color desde la base del conector.
```

```ad-question
title: Consulte la ilustración. La PC está conectada al puerto de consola del switch. Todas las demás conexiones se realizan con enlaces FastEthernet. ¿Qué tipos de cables UTP se pueden utilizar para conectar los dispositivos?

![[Pasted image 20220317105831.png]]
- [ ] 1: cruzado; 2: directo; 3: de consola (rollover)
- [ ] 1: de consola (rollover); 2: cruzado; 3: directo
- [ ] 1: cruzado; 2: de consola (rollover); 3: directo
- [x] 1: de consola (rollover); 2: directo; 3: cruzado

**Explique:** Por lo general, se utiliza un cable directo para interconectar un host con un switch y un switch con un router. Los cables cruzados se utilizan para interconectar dispositivos similares, como un switch con un switch, un host con un host o un router con un router. Si un switch tuviera funcionalidad MDIX, se podría utilizar un cable cruzado para conectar el switch al router; sin embargo, esa opción no está disponible. Los cables de consola (rollover) se utilizan para conectarse al puerto de consola de un router o de un switch.
```

```ad-question
title: Abra la actividad de PT. Complete las instrucciones de la actividad y luego responda la pregunta.
![[Pasted image 20220317105852.png]]
**¿Cual puerto es usado cuando Switch0 envía tramas a un host con la direccion IPv4?**

- [ ] Fa0/1
- [ ] Fa0/5
- [ ] Fa0/9
- [x] Fa0/11

**Explique:** La ejecución del comando i pconfig /all desde el símbolo del sistema PC0 muestra la dirección IPv4 y la dirección MAC. Cuando se hace ping a la dirección IPv4 10.1.1.5 desde PC0, el switch almacena la dirección MAC de origen (desde PC0) junto con el puerto al que está conectado PC0. Cuando se recibe la respuesta de destino, el switch toma la dirección MAC de destino y compara con las direcciones MAC almacenadas en la tabla de direcciones MAC. La ejecucion comando show mac-address-table en la aplicación Terminal de PC0 muestra dos entradas dinámicas de direcciones MAC. La dirección MAC y la entrada de puerto que no pertenecen a PC0 deben ser la dirección MAC y el puerto del destino con la dirección IPv4 10.1.1.5.
```

```ad-question
title: ¿Qué significa el término «atenuación» en la comunicación de datos?

- [ ] fuga de señales de un par de cables a otro
- [x] pérdida de intensidad de la señal a medida que aumenta la distancia
- [ ] fortalecimiento de una señal mediante un dispositivo de red
- [ ] tiempo para que una señal llegue a su destino

**Explique:** Los datos se transmiten en cables de cobre como impulsos eléctricos. Un detector en la interfaz de red de un dispositivo de destino debe recibir una señal que pueda decodificarse exitosamente para que coincida con la señal enviada. No obstante, cuanto más lejos viaja una señal, más se deteriora. Esto se denomina atenuación de señal.
```

```ad-question
title: ¿Qué hace que la fibra sea preferible al cableado de cobre para la interconexión de edificios? (Escoja tres opciones).

- [x] mayor potencial de ancho de banda
- [ ] fácil de terminar
- [x] mayores distancias por cable
- [ ] conexiones duraderas
- [ ] menor costo de instalación
- [x] susceptibilidad limitada a EMI/RFI

**Explique:** Transmite de datos a través de distancias más extensas y a anchos de banda mayores que cualquier otro medio de red. A diferencia de los cables de cobre, el cable de fibra óptica puede transmitir señales con menos atenuación y es totalmente inmune a las EMI y RFI.
```

```ad-question
title: ¿Qué término de capa física OSI describe la medida de la transferencia de bits a través de un medio durante un período de tiempo determinado?

- [ ] Ancho de banda
- [ ] Capacidad de transferencia útil
- [ ] Latencia
- [x] rendimiento

```

```ad-question
title: ¿Qué dos funciones se realizan en la subcapa LLC de la capa de enlace de datos OSI? (Escoja dos opciones).

- [x] Permite que IPv4 e IPv6 utilicen la misma interfaz de red y medios.
- [ ] Proporciona sincronización entre nodos de origen y de destino.
- [ ] Integra varias tecnologías físicas.
- [ ] Implementa un trailer para detectar errores de transmisión.
- [x] Agrega información de control de capa 2 a los datos de protocolo de red.

**Otro caso**

- [ ] Integra varias tecnologías físicas.
- [ ] Realiza la encapsulación de datos.
- [ ] Controla la NIC responsable de enviar y recibir datos en el medio físico.
- [x] Agrega información de control de capa 2 a los datos de protocolo de red.
- [x] Coloca en la trama información que identifica qué protocolo de capa de red se utiliza para la trama.

```

```ad-question
title: ¿Qué acción se producirá si un switch recibe una trama y tiene la dirección MAC de origen en la tabla MAC?

- [ ] El switch comparte la entrada de la tabla de direcciones MAC con cualquier switch conectado.
- [ ] El switch envía la trama a un router conectado porque la dirección MAC de destino no es local.
- [ ] El switch no reenvía la trama.
- [x] El switch actualiza el temporizador en esa entrada.

```

```ad-question
title: ¿Qué acción se producirá si un host recibe un marco con una dirección MAC de destino que no reconoce?

- [x] El host descartará la trama.
- [ ] El host reenvía la trama a todos los demás hosts.
- [ ] El host reenvía la trama al router.
- [ ] El host envía la trama al switch para actualizar la tabla de direcciones MAC.

```

```ad-question
title: Un administrador de redes mide la transferencia de bits a través de la red troncal de la compañía para una aplicación de base de datos de misión crítica. El administrador advierte que el rendimiento de la red está por debajo del ancho de banda esperado. ¿Cuáles son los tres factores que podrían afectar el rendimiento? Elija tres opciones.

- [x] La cantidad de tráfico que cruza la red en el momento
- [ ] La sofisticación del método de encapsulamiento aplicado a los datos
- [x] El tipo de tráfico que cruza la red
- [x] La latencia generada por la cantidad de dispositivos de red que atraviesan los datos
- [ ] El ancho de banda de la conexión WAN a Internet
- [ ] La confiabilidad de la infraestructura Gigabit Ethernet de la red troncal

**Explique:** En general, el rendimiento no coincide con el ancho de banda especificado de los enlaces físicos debido a varios factores. Estos factores incluyen la cantidad de tráfico, el tipo de tráfico y la latencia creada por los dispositivos de red que los datos deben atravesar.
```

```ad-question
title: ¿Cuál es la función principal de la capa física en la transmisión de datos en la red?

- [x] crear las señales que representan los bits en cada trama en el medio
- [ ] controlar el acceso a los datos a los medios
- [ ] proporcionar direccionamiento físico a los dispositivos
- [ ] Determinar las mejores rutas para los paquetes a través de la red

**Explique:** La capa física de OSI proporciona los medios de transporte de los bits que conforman una trama a través de los medios de red. Esta capa acepta una trama completa de la capa de enlace de datos y la codifica en una serie de señales para poder transmitir al medio local.
```

```ad-question
title: ¿Cuál de estas afirmaciones describe una topología en estrella extendida?

- [ ] Todos los dispositivos intermediarios y terminales se conectan entre sí en cadena.
- [ ] Las terminales se conectan entre sí por medio de un bus que se conecta a un dispositivo intermediario central.
- [x] Las terminales se conectan a un dispositivo intermediario central que se conecta a otros dispositivos intermediarios centrales.
- [ ] Cada terminal se conecta a su vecino respectivo por medio de un dispositivo intermediario.

**Explique:** En una topología en estrella extendida, los dispositivos intermediarios centrales interconectan otras topologías en estrella.
```

```ad-question
title: ¿Cuáles son las tres formas en que se utiliza el control de acceso a medios en redes? (Escoja tres opciones).

- [x] El control de acceso a medios proporciona la colocación de tramas de datos en el medio.
- [ ] El acceso basado en contención también se conoce como determinista.
- [ ] Las redes con acceso controlado han reducido el rendimiento debido a colisiones de datos.
- [ ] 802.11 utiliza CSMA/CD.
- [x] Ethernet utiliza CSMA/CD.
- [x] Los protocolos en la capa de enlace de datos definen las reglas de acceso a los diferentes medios.

**Explique:** Las redes Ethernet cableadas utilizan CSMA/CD para controlar el acceso a medios. Las redes inalámbricas IEEE 802.11 utilizan CSMA/CA, un método similar. El control de acceso a medios define la forma en que los marcos de datos se colocan en los medios. El método de acceso controlado es determinista, no un acceso basado en contencion a las redes. Dado que cada dispositivo tiene su propio tiempo para usar el medio, las redes de acceso controlado como Token Ring heredado no tienen colisiones.
```

```ad-question
title: Durante el proceso de encapsulamiento, ¿qué ocurre en la capa de enlace de datos para una PC conectada a una red Ethernet?

- [ ] Se agrega la dirección lógica.
- [x] Se agrega la dirección física.
- [ ] Se agrega una dirección IP.
- [ ] Se agrega el número de puerto del proceso.

**Explique:** La trama de Ethernet incluye las direcciones físicas de origen y de destino. El tráiler incluye un valor CRC en el campo de secuencia de verificación de trama para permitir que el dispositivo receptor determine si la trama se modificó (tiene errores) durante la transmisión.
```

```ad-question
title: ¿Qué tres elementos están contenidos en un encabezado Ethernet y un trailer? (Escoja tres opciones).

- [x] Dirección MAC de destino
- [x] información de comprobación de errores
- [ ] Dirección IP de origen
- [ ] Dirección IP de destino
- [x] Dirección MAC de origen

**Explique:** Los encabezados de capa 2 contienen lo siguiente:
Indicadores de inicio y terminación de trama que identifican los límites de inicio y terminación de la trama.
Direccionamiento: para redes Ethernet, esta parte del encabezado contiene direcciones MAC de origen y destino
Escriba el campo para indicar qué protocolo de capa 3 se está utilizando
Detección de errores para determinar si la trama llegó sin error
```

```ad-question
title: ¿Cuál de las siguientes es la característica MDIX automática en un switch?

- [ ] La capacidad de activar o desactivar una interfaz de switch, según corresponda, si se detecta una conexión activa
- [ ] La configuración automática de una interfaz para el funcionamiento a 10/100/1000 Mb/s
- [ ] La configuración automática del funcionamiento full-duplex a través de un único cable Ethernet óptico o de cobre
- [x] La configuración automática de una interfaz para una conexión por cable cruzado o directo de Ethernet

**Explique:** La función de MDIX automática permite que un switch utilice un cable cruzado o directo de Ethernet para conectarse a un dispositivo, independientemente del dispositivo que se encuentre en el otro extremo de la conexión.
```

```ad-question
title: ¿Qué método de switching tiene el nivel de latencia más bajo?

- [ ] Libre de fragmentos
- [x] Envío rápido
- [ ] Almacenamiento y envío
- [ ] Método de corte

**Explique:** El switching de envío rápido comienza a reenviar la trama cuando lee la dirección MAC de destino, lo que tiene como resultado la latencia más baja. El método libre de fragmentos lee los primeros 64 bytes antes del reenvío. El método de almacenamiento de envío tiene la latencia más alta porque lee la trama completa antes de comenzar a reenviarla. Los métodos de envío rápido y libre de fragmentos son tipos de switching por método de corte.
```

```ad-question
title: Cuando se usa el método de switching de almacenamiento y envío, ¿qué parte de la trama de Ethernet se usa para realizar una verificación de errores?

- [ ] Dirección MAC de destino en el encabezado
- [x] CRC en el tráiler
- [ ] Tipo de protocolo en el encabezado
- [ ] Dirección MAC de origen en el encabezado

**Explique:** La parte de comprobación cíclica de redundancia (CRC) del tráiler se usa para determinar si la trama se modificó durante el tránsito. Si se verifica la integridad de la trama, esta se reenvía. Si la integridad de la trama no se puede verificar, la trama se descarta.
```

```ad-question
title: ¿Cuál de las siguientes es una ventaja de utilizar el switching por método de corte en lugar del switching por almacenamiento y envío?

- [ ] Proporciona la flexibilidad para admitir cualquier combinación de velocidades de Ethernet.
- [ ] Tiene un impacto positivo en el ancho de banda debido a que se descarta la mayoría de las tramas no válidas.
- [ ] Toma decisiones de envío rápido basadas en la dirección MAC de origen de la trama.
- [x] Tiene una latencia más baja, adecuada para aplicaciones informáticas de alto rendimiento.

**Explique:** El switching por método de corte brinda un switching de menor latencia para las tecnologías informáticas de alto rendimiento (HPC). El switching por método de corte permite que más tramas no válidas crucen la red en comparación con el switching por almacenamiento y envío. El switching por método de corte puede tomar una decisión de reenvío tan pronto como busque la dirección MAC de destino de la trama.
```

```ad-question
title: Una la situación con el uso adecuado de los medios de red.

![[Pasted image 20220317110133.png]]

**Explique:** Cables de cobre: estructura de cableado horizontal y PC de escritorio en oficinas empresariales
Fibra óptica: cableado backbone en una empresa y redes de largo alcance
Inalámbrico: cafeterías y salas de espera de un hospital
```

```ad-question
title: ¿Qué tipo de regla de comunicación sería la mejor descripción de CSMA/CD?

- [x] Método de acceso
- [ ] Encapsulamiento del mensaje
- [ ] Control del flujo
- [ ] Codificación del mensaje

**Explique:** El acceso múltiple por detección de portadora con detección de colisiones (CSMA/CD) es el método de acceso que se utiliza con Ethernet. La regla de comunicación de método de acceso determina de qué forma puede un dispositivo de red ubicar una señal en la portadora. CSMA/CD determina dichas reglas en una red Ethernet, mientras que CSMA/CA lo hace en una LAN inalámbrica 802.11.
```

```ad-question
title: ¿Cuáles son las dos afirmaciones que describen las funciones o características de la subcapa de control de enlace lógico en los estándares de Ethernet? Elija dos opciones.

- [x] La capa de enlace de datos utiliza LLC para comunicarse con las capas superiores del paquete de protocolos.
- [x] El control de enlace lógico se implementa mediante software.
- [ ] La subcapa LLC agrega un encabezado y un tráiler a los datos.
- [ ] El control de enlace lógico está especificado en el estándar IEEE 802.3.
- [ ] La subcapa LLC es responsable de la ubicación y la recuperación de tramas en los medios.

**Explique:** El control de enlace lógico se implementa en el software y habilita la comunicación de la capa de enlace de datos con las capas superiores del paquete de protocolos. El control de enlace lógico está especificado en el estándar IEEE 802.2. IEEE 802.3 es un conjunto de estándares que definen los distintos tipos de Ethernet. La subcapa de control de acceso al medio (MAC) es responsable de la ubicación y la recuperación de tramas en los medios. Esta subcapa también es responsable de agregar un encabezado y un tráiler a la unidad de datos de protocolo (PDU) de la capa de red.
```

```ad-question
title: ¿Qué término de capa física OSI describe el proceso por el cual una onda modifica otra onda?

- [x] modulación
- [ ] EIA/TIA
- [ ] aire
- [ ] IEEE

```

```ad-question
title: ¿Qué acción se producirá si un host recibe una trama con una dirección MAC de destino de FF:FF:FF:FF:FF:FF?

- [ ] El host envía la trama al switch para actualizar la tabla de direcciones MAC.
- [ ] El host reenvía la trama al router.
- [ ] El host reenvía la trama a todos los demás hosts.
- [x] El host procesará la trama.

```

```ad-question
title: ¿Qué término de capa física OSI describe el medio físico que utiliza la propagación de la luz?

- [ ] rendimiento real
- [ ] latencia
- [ ] throughput
- [x] Cable de fibra óptica

```

```ad-question
title: ¿Qué dos funciones se realizan en la subcapa LLC de la capa de enlace de datos OSI? (Escoja dos opciones).

- [ ] Implementa un trailer para detectar errores de transmisión.
- [ ] Provides data link layer addressing.
- [x] Permite que IPv4 e IPv6 utilicen la misma interfaz de red y medios.
- [x] Agrega información de control de capa 2 a los datos de protocolo de red.
- [ ] Proporciona sincronización entre nodos de origen y de destino.

```

```ad-question
title: ¿Qué dos funciones se realizan en la subcapa MAC de la capa de enlace de datos OSI? (Escoja dos opciones).

- [ ] Coloca en la trama información que identifica qué protocolo de capa de red se utiliza para la trama.
- [x] Proporciona sincronización entre nodos de origen y de destino.
- [ ] Agrega información de control de capa 2 a los datos de protocolo de red.
- [x] Implementa un trailer para detectar errores de transmisión.
- [ ] Permite que IPv4 e IPv6 utilicen la misma interfaz de red y medios.

**Otro caso**

- [x] Controla la NIC responsable de enviar y recibir datos en el medio físico.
- [ ] Agrega información de control de capa 2 a los datos de protocolo de red.
- [ ] Se comunica entre el software de red en las capas superiores y el hardware del dispositivo en las capas inferiores.
- [x] Proporciona un mecanismo para permitir que varios dispositivos se comuniquen a través de un medio compartido.
- [ ] Coloca en la trama información que identifica qué protocolo de capa de red se utiliza para la trama.

```

```ad-question
title: ¿Qué acción se producirá si un switch recibe una trama con la dirección MAC de destino FF:FF:FF:FF:FF:FF?

- [x] El switch lo reenvía todos los puertos excepto el puerto de entrada.
- [ ] El switch envía la trama a un router conectado porque la dirección MAC de destino no es local.
- [ ] El switch actualiza el temporizador en esa entrada.
- [ ] El switch no reenvía la trama.

**Otro caso**

- [ ] El switch no reenvía la trama.
- [ ] El switch envía la trama a un router conectado porque la dirección MAC de destino no es local.
- [ ] El switch comparte la entrada de la tabla de direcciones MAC con cualquier switch conectado.
- [x] El switch lo reenvía a todos los puertos excepto el puerto de entrada.
```

```ad-question
title: ¿Qué declaración es verdadera sobre el método de acceso CSMA/CD que se utiliza en Ethernet?

- [x] Todos los dispositivos de red deben escuchar antes de transmitir.
- [ ] Cuando un dispositivo escucha una señal portadora y transmite, no se puede producir una colisión.
- [ ] Los dispositivos involucrados en una colisión tienen prioridad para transmitir después del período de retroceso.
- [ ] Una señal de interferencia hace que solo los dispositivos que causaron la colisión ejecuten un algoritmo de retroceso.

**Explique:** La LAN Ethernet de topología de bus heredada utiliza CSMA/CD como protocolo de control de acceso a medios de red. Funciona detectando una colisión en el medio y retrocediendo (después de transmitir una señal de atasco) según sea necesario. Cuando un host desea transmitir un fotograma, escucha en el medio para comprobar si el medio está ocupado. Después de que detecta que nadie más está transmitiendo, el host comienza a transmitir el fotograma, también monitorea el nivel actual para detectar una colisión. Si detecta una colisión, transmite una señal especial de atasco para que todos los demás hosts puedan saber que hubo una colisión. El otro host recibirá esta señal de atasco y dejará de transmitir. Después de esto, ambos hosts entran en una fase de retroceso exponencial y reintentan la transmisión.
```

```ad-question
title: ¿Qué término de capa física OSI describe la capacidad a la que un medio puede transportar datos?

- [x] Ancho de banda
- [ ] aire
- [ ] EIA/TIA
- [ ] IEEE

```

```ad-question
title: ¿Qué término de capa física OSI describe la medida de datos utilizables transferidos durante un período determinado?

- [ ] aire
- [ ] Cable de fibra óptica
- [x] goodput
- [ ] Cable de cobre

```

```ad-question
title: ¿Qué término de capa física OSI describe la cantidad de tiempo, incluidos los retrasos, para que los datos viajen de un punto a otro?

- [x] latencia
- [ ] aire
- [ ] Cable de fibra óptica
- [ ] Cable de cobre

```

```ad-question
title: ¿Qué acción se producirá si un host recibe una trama con una dirección MAC de destino que no reconoce?

- [ ] El host responde al switch con su propia dirección IP.
- [x] El host descartará la trama.
- [ ] El host reenvía la trama a todos los demás hosts.
- [ ] El host devuelve la trama al switch.

```
