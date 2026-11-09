---
description: 9.2.9-packet-tracer---examine-the-arp-table_es-XL
---

# Cisco Ejercicio 9.2.9

<img src=".gitbook/assets/unknown (6).png" alt="" height="84" width="272">

Packet Tracer: Revisión de la tabla ARP&#x20;

Tabla de asignación de direcciones&#x20;

<table data-header-hidden><thead><tr><th></th><th></th><th></th><th></th></tr></thead><tbody><tr><td>Dispositivo </td><td>Interfaz </td><td>Dirección MAC </td><td>Interfaz del switch</td></tr><tr><td rowspan="2"><p>Router0 </p><p>Router0</p></td><td>Gg0/0 </td><td>0001.6458.2501 </td><td>G0/1</td></tr><tr><td>S0/0/0 </td><td>N/A </td><td>N/A</td></tr><tr><td rowspan="2"><p>Router1 </p><p>Router1</p></td><td>G0/0 </td><td>00E0.F7B1.8901 </td><td>G0/1</td></tr><tr><td>S0/0/0 </td><td>N/A </td><td>N/A</td></tr><tr><td>10.10.10.2 </td><td>Inalámbrica </td><td>0060.2F84.4AB6 </td><td>F0/2</td></tr><tr><td>10.10.10.3 </td><td>Inalámbrica </td><td>0060.4706.572B </td><td>F0/2</td></tr><tr><td>172.16.31.2 </td><td>F0 </td><td>000C.85CC.1DA7 </td><td>F0/1</td></tr><tr><td>172.16.31.3 </td><td>F0 </td><td>0060.7036.2849 </td><td>F0/2</td></tr><tr><td>172.16.31.4 </td><td>G0 </td><td>0002.1640.8D75 </td><td>F0/3</td></tr></tbody></table>

\
<br>

Objetivos&#x20;

Parte 1: Examinar una solicitud de ARP&#x20;

Parte 2: Examinar una tabla de direcciones MAC del switch&#x20;

Parte 3: Examinar el proceso ARP en comunicaciones remotas&#x20;

Aspectos básicos&#x20;

Esta actividad está optimizada para la visualización de PDU. Los dispositivos ya están configurados. Reunirá  información de PDU en el modo de simulación y responderá una serie de preguntas sobre los datos que  obtenga.&#x20;

Instrucciones&#x20;

Parte 1: Examinar una solicitud de ARP&#x20;

Paso 1: Generar solicitudes de ARP haciendo ping a 172.16.31.3 en 172.16.31.2. Abra un símbolo del sistema.&#x20;

a. Haga click en172.16.31.2 y abra el Command Prompt.&#x20;

b. Introduzca el comando arp -d para borrar la tabla ARP.&#x20;

Cierre símbolo del sistema&#x20;

c. Ingrese al modo Simulation (Simulación) e introduzca el comando ping 172.16.31.3. Se generan dos  PDU. El comando ping no puede completar el paquete ICMP sin conocer la dirección MAC del destino.  Por lo tanto, la PC envía una trama de difusión de ARP para encontrar la dirección MAC del destino.&#x20;

d. Haga clic en Capture/Forward (Capturar/Adelantar) una vez. La PDU ARP mueve el Switch1, mientras  que la PDU ICMP desaparece y espera la respuesta de ARP. Abra la PDU y registre la dirección MAC de  destino.

\
<br>

¿Esta dirección se indica en la tabla anterior?&#x20;

<br>

No, la que sale es la direccion MAC de difusion, la FFFF.FFFF.FFFF

e. Haga clic en Capture/Forward (Capturar/Adelantar) para mover la PDU al siguiente dispositivo. Pregunta:&#x20;

¿Cuántas copias de la PDU realizó el Switch1?

<br>

Hizo 3 copias

<br>

¿Cuál es la dirección IP del dispositivo que aceptó la PDU?&#x20;

La 172.16.31.3

f. Abra la PDU y examine la capa 2.&#x20;

Pregunta:&#x20;

¿Qué sucedió con las direcciones MAC de origen y destino?&#x20;

<br>

Se invirtieron las MAC de los equipos con IP 172.16.31.3 con la del 172.16.31.2

<br>

g. Haga clic en Capture/Forward (Capturar/Adelantar) hasta que la PDU regrese a 172.16.31.2. Pregunta:&#x20;

¿Cuántas copias de la PDU realizó el switch durante la respuesta de ARP?&#x20;

<br>

Solo 1

<br>

Paso 2: Examinar la tabla ARP.&#x20;

a. Observe que vuelve a aparecer el paquete ICMP. Abra la PDU y examine las direcciones MAC. Pregunta:&#x20;

¿Las direcciones MAC de origen y destino coinciden con sus direcciones IP?&#x20;

<br>

Si, la de destino es la 172.16.31.3 y la de origen es la 172.16.31.2

b. Vuelva a cambiar al modo Realtime (Tiempo real); el ping se completa.&#x20;

c. Haga clic en 172.16.31.2 e introduzca el comando arp -a.&#x20;

Pregunta:&#x20;

¿A qué dirección IP corresponde la entrada de la dirección MAC?&#x20;

A la 172.16.31.3

<br>

En general, ¿cuándo emite una terminal una solicitud de ARP?&#x20;

Cuando necesita enviar datos a alguien de la misma red local, pero no conoce la dirección MAC asociada a la IP destino

<br>

Parte 2: Examinar una tabla de direcciones MAC del switch&#x20;

Paso 1: Generar tráfico adicional para completar la tabla de direcciones MAC del switch. Abra un símbolo del sistema.&#x20;

a. Desde 172.16.31.2, introduzca el 172.16.31.4 comando ping.&#x20;

b. Haga clic en 10.10.10. 2 y abra el símbolo del sistema .&#x20;

c. Introduzca el comando ping 10.10.10.3.&#x20;

Pregunta:&#x20;

¿Cuántas respuestas se enviaron y se recibieron?&#x20;

4 paquetes

<br>

Paso 2: Examinar la tabla de direcciones MAC en los switches.&#x20;

a. Haga clic en Switch1 y, a continuación, en la ficha CLI. Introduzca el comando show mac-address table.&#x20;

Pregunta:&#x20;

¿Las entradas corresponden a las de la tabla de arriba?

Si, la direcciones MAC asociadas a las interfaces coinciden con la tabla

<br>

b. Haga clic en Switch0 y, a continuación, en la ficha CLI. Introduzca el comando show mac-address table.&#x20;

Preguntas:&#x20;

¿Las entradas corresponden a las de la tabla de arriba?

SI&#x20;

<br>

¿Por qué hay dos direcciones MAC asociadas a un puerto?&#x20;

Porque está conectado al puerto F0/2 a un puerto inalámbrico o a un dispositivo intermediario, por lo cual, transitan múltiples dispositivos wireless

<br>

Pq&#x20;

Parte 3: Examinar el proceso ARP en comunicaciones remotas&#x20;

Paso 1: Generar tráfico para producir tráfico ARP.&#x20;

Abra un símbolo del sistema.&#x20;

a. Haga click 172.16.31.2 y abra el Command Prompt.&#x20;

b. Introduzca el comando ping 10.10.10.1.&#x20;

c. Escriba arp -a.&#x20;

Pregunta:&#x20;

¿Cuál es la dirección IP de la nueva entrada de la tabla ARP?&#x20;

172.16.31.1, es la gateway

d. Escriba arp -d para borrar la tabla ARP y cambiar al modo Simulation (Simulación).&#x20;

e. Repita el ping a 10.10.10.1.&#x20;

Pregunta:&#x20;

¿Cuántas PDU aparecen?&#x20;

2

<br>

f. Haga clic en Capture/Forward (Capturar/Adelantar). Haga clic en la PDU que ahora se encuentra en el  Switch1.&#x20;

Pregunta:&#x20;

¿Cuál es la dirección IP de destino objetivo de la solicitud de ARP?

172.16.31.1&#x20;

<br>

g. La dirección IP de destino no es 10.10.10.1.&#x20;

Pregunta:&#x20;

¿Por qué?&#x20;

Porque el destino objetivo está en una red remota diferente

Paso 2: Examinar la tabla ARP en el Router1.&#x20;

a. Cambie al modo Realtime. Haga click en el Router1 y luego en la pestaña CLI&#x20;

b. Ingrese al modo EXEC privilegiado y, a continuación, introduzca el comando show mac-address-table. Pregunta:&#x20;

¿Cuántas direcciones MAC figuran en la tabla? ¿Por qué?&#x20;

Muestra 0, porque los routers operan en 3 capas y no mantienen una tabla de direcciones MAC del switch

<br>

c. Introduzca el comando show arp.&#x20;

Preguntas:&#x20;

¿Existe una entrada para 172.16.31.2?&#x20;

No, porque pertenece a otra red conectada a otro router

<br>

¿Qué sucede con el primer ping en una situación en la que el router responde a la solicitud de ARP?&#x20;

El primero falla, ya que esta lejos y tiene que buscarlo, y en la segunda, ya lo suele encontrar

En este ejercicio hemos aprendido a ver el trazado de los paquetes, mediante pings a direcciones IP y toda la configuración que pueden guardar los dispositivos de red para poder facilitarse los siguientes trazados a diferentes dispositivos

Fin del documento

© 2013 - 2020 Cisco y/o sus filiales. Todos los derechos reservados. Información pública de Cisco Página 3 de 3 www.netacad.com&#x20;

\
\
<br>
