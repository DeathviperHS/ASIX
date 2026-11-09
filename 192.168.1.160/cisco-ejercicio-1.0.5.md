---
description: 1.0.5-packet-tracer---logical-and-physical-mode-exploration_es-XL
---

# Cisco Ejercicio 1.0.5

<img src=".gitbook/assets/unknown.png" alt="" height="84" width="272">

Packet Tracer - Exploración de Modo Lógico y Físico&#x20;

Objetivos&#x20;

Parte 1: Investigar la Barra de Herramientas Inferior&#x20;

Parte 2: Investigar Dispositivos en un Armario de Cableado&#x20;

Parte 3: Conectar Dispositivos Finales a Dispositivos de Red&#x20;

Parte 4: Instalar un Router de Respaldo&#x20;

Parte 5: Configurar un Nombre de Host&#x20;

Parte 6: Explora el resto de la Red&#x20;

Aspectos básicos/Situación&#x20;

El modelo de red de esta actividad Packet Tracer Physical Mode (PTPM) incorpora muchas de las  tecnologías que puede dominar en los cursos de Cisco Networking Academy. Y representa una versión  simplificada de la forma en que podría verse una red de pequeña o mediana empresa. &#x20;

La mayoría de los dispositivos de la sucursal de Seward y del Centro de Datos de Warrenton ya están  implementados y configurados. Usted acaba de ser contratado para revisar los dispositivos y redes  implementados. No es importante que comprenda todo lo que vea y haga en esta actividad. Siéntase libre de  explorar la red por usted mismo. Si desea hacerlo de manera más sistemática, siga estos pasos. Responda  las preguntas lo mejor que pueda.&#x20;

Nota: Esta actividad se abre y se centra en el modo Físico . Muchas de las actividades de Packet Tracer que  encuentre en los cursos de Cisco Networking Academy utilizarán el modo Lógico . Puede cambiar entre  estos modos en cualquier momento para comparar las diferencias haciendo clic en los botones Lógico (Shift+L) y Físico (Shift+P). Sin embargo, en otras actividades de este curso puede estar bloqueado de un  modo u otro.&#x20;

Instrucciones&#x20;

Parte 1: Investigar la Barra de Herramientas Inferior&#x20;

La barra de herramientas de iconos en la esquina inferior izquierda tiene varias categorías de componentes  de red. Debería ver categorías que corresponden a Dispositivos de Red, Dispositivos Finales, y  Componentes. La cuarta categoría (con el icono del rayo) es Conexiones y representa los medios de red  compatibles con Packet Tracer. Las dos últimas categorías son Miscelánea y Conexión multiusuario.&#x20;

¿Cuáles son las subcategorías de Dispositivos de Red?&#x20;

<br>

Routers, Switches, Hubs, Dispositivos inalámbricos, seguridad y Simulador de Wan&#x20;

Parte 2: Investigar Dispositivos en un Armario de Cableado&#x20;

a. Si fuiste a explorar, vuelve a modo Físico e Intercity ahora. En la barra azul superior, haga clic en  Físico y, a continuación, utilice los botones Panel de Navegación o Nivel Atrás para desplazarse a  Intercity.&#x20;

b. Haga clic en Seward y, a continuación, haga clic en la Sucursal. &#x20;

c. Haga clic en el Armario de Cableado de la Sucursal. Observe que el armario de cableado tiene un  Rack, un Tablero de Cables, una Mesa y un Estante.&#x20;

♥ 2021 – 2021 Cisco y/o sus filiales. Todos los derechos reservados. Información pública de Cisco Página 1 de 4 www.netacad.com&#x20;

Packet Tracer - Exploración de Modo Lógico y Físico&#x20;

El Rack contiene dispositivos que se pueden montar en rack. Si amplía el rack (herramienta de zoom o  Ctrl+rueda de desplazamiento), puede ver que los dispositivos están atornillados (montados) en el rack.  Debajo del dispositivo de distribución de energía, encontrará un router. Los routers conectan redes  diferentes. &#x20;

d. Debajo del router hay dos switches. Estos switches proporcionan conexiones por cable para conectarse  a otros dispositivos. Observe que los dispositivos tienen un nombre asignado por el administrador de red.  ¿Qué dispositivos utilizan una conexión por cable para conectarse al switch ALS2?&#x20;

Un acces point, un webserver y el ALS1

\
<br>

e. Debajo de los switches del Rack se encuentra un punto de acceso inalámbrico denominado  Access\_Point. Los puntos de acceso inalámbricos utilizan una conexión inalámbrica para conectarse a  otros dispositivos. Cambie al modo Lógico. ¿Qué dispositivo está conectado a Access\_Point?&#x20;

La laptop

f. Cambie al modo Físico. Deberías estar de vuelta en el Armario de Cableado de la Sucursal. ¿Dónde  se encuentra físicamente el dispositivo conectado a Access\_Point? &#x20;

Se encuentra físicamente conectado al ASL2

Parte 3: Conectar Dispositivos Finales a Dispositivos de Red&#x20;

Los dispositivos se pueden conectar de varias maneras. Para la conectividad de red, los dispositivos  normalmente se conectan mediante un cable directo de cobre o de forma inalámbrica. Para la conectividad  de administración, los dispositivos normalmente se conectan mediante un cable de consola o un cable USB.&#x20;

Nota: Packet Tracer calificará el resto de esta actividad. En cualquier momento, puede hacer clic en  Comprobar resultados en la parte inferior de la ventana Tareas. A continuación, haga clic en Elementos  de evaluación para ver qué elementos aún no ha completado.&#x20;

a. Investigue el Tablero de Cables. Incluye dos cables de Consola, diez cab les directos de cobre, cuatro  cables de Fibra, dos cables Coaxiales y dos cables USB. Observe que las representaciones de cable en  modo Físico son más representativas de sus homólogos del mundo real. Cambie al modo Lógico. Observe que las representaciones de cable son diferentes en este modo.&#x20;

b. Cambie al modo Físico. Haga clic en un cable directo de cobre del Tablero de Cables. &#x20;

c. Mueva el ratón sobre los puertos de PC\_1 hasta que vea la ventana emergente FastEthernet0. El otro puerto RS232 es para conectar cables de Consola.&#x20;

d. Con el cable directo de cobre todavía seleccionado, haga clic en el puerto FastEthernet0 para conectar  el cable. Ahora el puerto debe estar resaltado en verde.&#x20;

e. Conecte el otro extremo del cable al switch ALS2 haciendo clic en un puerto Fast Ethernet vacío. El  cable ahora debería colgar entre la PC\_1 y el puerto de ALS2.&#x20;

f. Las PCs y los portátiles también se pueden conectar a dispositivos de red mediante un cable de consola  o un cable USB. Esta conexión proporciona acceso de administración. Haga clic en un cable de Consola del Tablero de Cables. &#x20;

g. Haga clic en el puerto RS232 en PC\_1. Ahora el puerto debe estar resaltado en verde. &#x20;

h. Pase el ratón sobre el Edge\_Router y busque el puerto de Consola. Puede hacer clic con el botón  derecho en > Inspeccionar Frente para ampliar y facilitar la búsqueda del puerto.&#x20;

i. Haga clic en el puerto de consola en Edge\_Router para conectar el cable de Consola. El cable ahora  debería colgar entre PC\_1 y el puerto de Consola en el Edge\_Router.

♥ 2021 – 2021 Cisco y/o sus filiales. Todos los derechos reservados. Información pública de Cisco Página 2 de 4 www.netacad.com&#x20;

Packet Tracer - Exploración de Modo Lógico y Físico&#x20;

Parte 4: Instalar un Router de Respaldo&#x20;

A los modelos más nuevos de dispositivos de red se puede acceder a través de un puerto USB para la  configuración de la administración. Esto es necesario porque los portátiles y los PC más recientes  normalmente no incluyen un puerto RS232 para las conexiones de cables de consola. &#x20;

a. Investigue el Estante. Esto incluye un inventario de dispositivos de la Sucursal de Seward que no están  instalados actualmente. &#x20;

b. Haga clic y arrastre Backup\_Router a un lugar vacío en el Rack.&#x20;

c. Algunos dispositivos no se encienden automáticamente cuando se instalan en el Rack. Haga clic en  Backup\_Router > Inspeccionar parte trasera. Busque el botón de encendido y encienda el router.&#x20;

d. En el Tablero de Cables, elija un cable USB. Vuelva a la vista trasera de Backup\_Router y encuentre el  puerto deconsola USB en el extremo izquierdo. Haga clic en el puerto para conectar el cable USB.  Ahora el puerto debe estar resaltado en verde.&#x20;

e. Conecte el otro extremo del cable USB a cualquiera de los puertos USB de la Laptop\_1. El cable no  colgará como lo hicieron los cables para las conexiones a PC\_1.&#x20;

Parte 5: Configuración de un Nombre de Host&#x20;

Los administradores de red suelen asignar un nombre a los dispositivos de red. Para hacer esto, utilizará la  conexión de consola al Backup\_Router.&#x20;

a. Haga clic enLaptop\_1 > pestaña deDesktop > Terminal. &#x20;

b. La configuración de la Terminal ya está definida con la configuración de puerto necesaria. Haga clic en  Aceptar.&#x20;

c. Ahora está en la línea de comandos para Backup\_Router y debería ver lo siguiente.  \<output omitted>&#x20;

cisco ISR4331/K9 (1RU) processor with 1795999K/6147K bytes of memory.&#x20;

Processor board ID FLM232010G0&#x20;

3 Gigabit Ethernet interfaces&#x20;

2 Serial interfaces&#x20;

32768K bytes of non-volatile configuration memory.&#x20;

4194304K bytes of physical memory.&#x20;

3207167K bytes of flash memory at bootflash:.&#x20;

0K bytes of WebUI ODM Files at webui:.&#x20;

&#x20;\--- System Configuration Dialog ---&#x20;

Would you like to enter the initial configuration dialog? \[yes/no]: no&#x20;

d. Responda no a la pregunta y luego presione ENTRAR para obtener el símbolo del sistema Router. Press RETURN to get started!&#x20;

\<ENTER>&#x20;

Router>&#x20;

e. Introduzca los siguientes comandos para nombrar al router Edge\_Router\_Backup. Router> enable

♥ 2021 – 2021 Cisco y/o sus filiales. Todos los derechos reservados. Información pública de Cisco Página 3 de 4 www.netacad.com&#x20;

Packet Tracer - Exploración de Modo Lógico y Físico&#x20;

Router#configure terminal&#x20;

Enter configuration commands, one per line. End with CNTL/Z.&#x20;

Router (config) # hostname Edge\_Router\_Backup&#x20;

Edge\_Router\_Backup (config) # end&#x20;

Edge\_Router\_Backup#&#x20;

Observe que el nombre de host cambió de Router a Edge\_Router\_Backup.&#x20;

f. Cierre la ventana de Laptop\_1 y vuelva al Armario de Cableado de la Sucursal. &#x20;

g. Observe que el nombre para mostrar de Backup\_Router no ha cambiado. Haga clic en Backup\_Router > pestaña Config. En Configuración global, observe que Packet Tracer mantiene dos nombres para el  dispositivo: un nombre para mostrar y un nombre de host. &#x20;

Parte 6: Explora el resto de la Red&#x20;

Tómese un tiempo para explorar el resto de la red. Familiarícese con las representaciones de red en los  modos Lógico y Físico. En el modo Físico, vaya a otras áreas, como el Centro de Datos de Wellington y  el hogar de Teleworker. Las tecnologías utilizadas en estos lugares se analizan con mayor detalle en los  cursos de Cisco Networking Academy. Por ahora, vea lo que puede descubrir por su cuenta. No se preocupe  por romper nada. Siempre puede cerrar Packet Tracer y abrir una copia nueva para empezar a explorar de  nuevo.&#x20;

\
\
<br>

En este ejercicio he aprendido a navegar por dentro del sistema cisco, los dispositivos que hay y cómo se conectan entre ellos. He tenido que mover un router, conozco mejor el entorno gráfico, he descubierto que hay 2 entornos, unos fisico y uno lógico

\
<br>

Lo que he hecho ha sido conectar un PC a un switch por cable ethernet, también lo he conectado por consola  al router que hay, he movido el router de repuesto por si se estropea el otro, y lo he conectado por usb al laptop para poder cambiarle el nombre&#x20;

♥ 2021 – 2021 Cisco y/o sus filiales. Todos los derechos reservados. Información pública de Cisco Página 4 de 4 www.netacad.com

<br>

<figure><img src=".gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>
