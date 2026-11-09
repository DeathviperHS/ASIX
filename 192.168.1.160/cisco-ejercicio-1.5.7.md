---
description: 1.5.7-packet-tracer---network-representation_es-XL
---

# Cisco Ejercicio 1.5.7



<img src=".gitbook/assets/unknown (5).png" alt="" height="84" width="272">

Packet Tracer: Representación de la red&#x20;

Objetivos&#x20;

El modelo de red en esta actividad incluye muchas de las tecnologías que llegará a dominar en sus estudios  en CCNA y representa una versión simplificada de la forma en que podría verse una red de pequeña o  mediana empresa. Siéntase libre de explorar la red por usted mismo. Cuando esté listo, siga estos pasos y  responda las preguntas.&#x20;

Nota: No es importante que comprenda todo lo que vea y haga en esta actividad. Siéntase libre de explorar  la red por usted mismo. Si desea hacerlo de manera más sistemática, siga estos pasos. Responda las  preguntas lo mejor que pueda.&#x20;

Instrucciones&#x20;

Paso 1: Identifique los componentes comunes de una red según se los  representa en Packet Tracer.&#x20;

La barra de herramientas de íconos en la esquina inferior izquierda tiene diferentes categorías de  componentes de red. Debería ver las categorías que corresponden a los dispositivos intermediarios, los  terminales y los medios. La categoría Conexiones (su ícono es un rayo) representa los medios de red que  admite Packet Tracer. También hay una categoría llamada Terminales y dos categorías específicas de  Packet Tracer: Dispositivos personalizados y Conexión multiusuario.&#x20;

Preguntas:&#x20;

Enumere las categorías de los dispositivos intermediarios.&#x20;

Sin ingresar en la nube de Internet o de intranet, ¿cuántos íconos de la topología representan dispositivos de  terminales (solo una conexión conduce a ellos)?&#x20;

Las categorías de dispositivos intermediarios incluyen routers, switches, switches multicapa, puntos de acceso inalámbrico, dispositivos de seguridad (firewalls) y módems.

\
<br>

Sin contar las dos nubes, ¿cuántos íconos de la topología representan dispositivos intermediarios (varias  conexiones conducen a ellos)?&#x20;

15&#x20;

¿Cuántos terminales no son PC de escritorio?&#x20;

8

<br>

¿Cuántos tipos diferentes de conexiones de medios se utilizan en esta topología de red?&#x20;

13

&#x20;

Paso 2: Explique la finalidad de los dispositivos.&#x20;

Preguntas:

a. En Packet Tracer, solo el dispositivo Server-PT puede funcionar como servidor. Las PC de escritorio o  portátiles no pueden funcionar como servidores. Según lo que estudió hasta ahora, explique el modelo  cliente-servidor.&#x20;

El modelo cliente-servidor es una estructura de red en la que los clientes solicitan servicios o recursos y los servidores los proporcionan. Por ejemplo, un ordenador puede solicitar una página web a un servidor, que procesa la petición y envía la información solicitada.

<br>

b. Enumere, al menos, dos funciones de los dispositivos intermediarios.&#x20;

1. Conectar dispositivos y redes diferentes para permitir la comunicación.
2. Determinar la mejor ruta para transmitir los datos hacia su destino.
3. Filtrar el tráfico y aplicar medidas de seguridad.
4. Regenerar y retransmitir las señales de datos.

<br>

c. Enumere, al menos, dos criterios para elegir un tipo de medio de red.&#x20;

1. La distancia que deben recorrer los datos.
2. La velocidad de transmisión necesaria.
3. El coste de instalación y mantenimiento.
4. Las condiciones ambientales y las posibles interferencias.

\
\
\
\
<br>

Paso 3: Compare las redes LAN y WAN.&#x20;

Preguntas:

a. Explique la diferencia entre una LAN y una WAN, y dé ejemplos de cada una. Una LAN (red de área local) conecta dispositivos dentro de un área geográfica pequeña, como una vivienda, una oficina o un centro educativo. Una WAN (red de área amplia) conecta redes situadas en áreas geográficas más extensas, como diferentes ciudades o países. Por ejemplo, la red de ordenadores de una escuela es una LAN, mientras que una red que conecta las sucursales de una empresa en distintas ciudades es una WAN.

<br>

b. ¿Cuántas WAN ve en la red de Packet Tracer?&#x20;

Hay 2 WAN, representadas por las nubes de Internet e intranet.

<br>

c. ¿Cuántas LAN ve?&#x20;

Hay 3 LAN, identificables por los límites y las etiquetas de la topología.

<br>

d. En esta red de Packet Tracer, Internet está simplificada en gran medida y no representa ni la estructura  ni la forma de Internet propiamente dicha. Describa Internet brevemente.&#x20;

Internet es una red mundial de redes interconectadas que permite la comunicación entre dispositivos y el intercambio de información mediante protocolos comunes, como TCP/IP.

e. ¿Cuáles son algunas de las formas más comunes que utiliza un usuario doméstico para conectarse a  Internet?&#x20;

Las formas más comunes son la fibra óptica, el cable, el ADSL o DSL, las redes móviles (4G y 5G) y las conexiones por satélite.

f. ¿Cuáles son algunos de los métodos más comunes que utilizan las empresas para conectarse a Internet  en su área?&#x20;

Las empresas suelen utilizar fibra óptica, líneas dedicadas, conexiones Ethernet metropolitanas, cable, DSL y conexiones por satélite, dependiendo de sus necesidades y de la disponibilidad del servicio.

<br>

Pregunta de desafío&#x20;

Ahora que tuvo la oportunidad de explorar la red representada en esta actividad de Packet Tracer, es posible  que haya adquirido algunas habilidades que quiera poner en práctica o tal vez desee tener la oportunidad de  analizar esta red en mayor detalle. Teniendo en cuenta que la mayor parte de lo que ve y experimenta en  Packet Tracer supera su nivel de habilidad en este momento, los siguientes son algunos desafíos que tal vez  quiera probar. No se preocupe si no puede completarlos todos. Muy pronto se convertirá en un usuario y  diseñador de redes experto en Packet Tracer.&#x20;

• Agregue un dispositivo final a la topología y conéctelo a una de las LAN con una conexión de medios.  ¿Qué otra cosa necesita este dispositivo para enviar datos a otros usuarios finales? ¿Puede  proporcionar la información? ¿Hay alguna manera de verificar que conectó correctamente el dispositivo?&#x20;

Necesita una dirección IP, una máscara de subred y, si desea comunicarse con otras redes, una puerta de enlace predeterminada. También debe conectarse mediante el medio adecuado. Para comprobar la conexión, puede utilizar el comando “ping” desde la consola del dispositivo y verificar si recibe respuestas.

<br>

• Agregue un nuevo dispositivo intermediario a una de las redes y conéctelo a uno de las LAN o WAN con  una conexión de medios. ¿Qué otra cosa necesita este dispositivo para funcionar como intermediario de  otros dispositivos en la red?&#x20;

Necesita una conexión física adecuada y una configuración correcta. Por ejemplo, un router debe disponer de direcciones IP en sus interfaces y, cuando corresponda, de rutas para dirigir el tráfico hacia otras redes.

<br>

• Abra una nueva instancia de Packet Tracer. Cree una nueva red con, al menos, dos redes LAN  conectadas mediante una WAN. Conecte todos los dispositivos. Investigue la actividad de Packet Tracer  original para ver qué más necesita hacer para que la nueva red esté en condiciones de funcionamiento.  Registre sus comentarios y guarde el archivo de Packet Tracer. Tal vez desee volver a acceder a la red  cuando domine algunas habilidades más.&#x20;

Debe conectar los dispositivos finales a los switches, conectar los switches a los routers y enlazar los routers mediante una conexión WAN. También debe configurar las direcciones IP, las máscaras de subred, las puertas de enlace predeterminadas y el enrutamiento. Finalmente, debe comprobar la conectividad mediante “ping” y guardar el archivo de Packet Tracer.

\
![](<.gitbook/assets/image (20).png>)

© 2013 - aa Cisco y/o sus filiales. Todos los derechos reservados. Información pública de Cisco Página 3 de 3 www.netacad.com

<br>
