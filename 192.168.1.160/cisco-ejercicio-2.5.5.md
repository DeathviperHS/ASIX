---
description: 2.5.5-packet-tracer---configure-initial-switch-settings_es-XL
---

# Cisco Ejercicio 2.5.5

Packet Tracer - Configure ajustes iniciales del interruptor .&#x20;

Objetivos&#x20;

Parte 1: Verifique la configuración predeterminada del switch &#x20;

Parte 2: Establezca una configuración básica del switch &#x20;

Parte 3: Configure un aviso de MOTD&#x20;

Parte 4: Guarde los archivos de configuración en la NVRAM&#x20;

Parte 5: Configure el S2&#x20;

Antecedentes/Escenario&#x20;

En esta actividad, realizará tareas básicas de configuración del conmutador. Protegerá el acceso a la interfaz  de línea de comandos (CLI) y a los puertos de la consola mediante contraseñas cifradas y contraseñas de  texto no cifrado. También aprenderá cómo configurar mensajes para los usuarios que inician sesión en el  switch. Estos banners de mensajes también se utilizan para advertir a los usuarios no autorizados que el  acceso está prohibido.&#x20;

Nota: En Packet Tracer, el switch Catalyst 2960 utiliza la versión 12.2 de IOS de forma predeterminada. Si  es necesario, la versión IOS se puede actualizar desde un servidor de archivos en la topología Packet  Tracer. El switch puede configurarse para arrancar a IOS versión 15.0, si esa versión es necesaria. &#x20;

Instrucciones&#x20;

Parte 1: Verifique la configuración predeterminada del switch&#x20;

Paso 1: Ingrese al modo EXEC privilegiado.&#x20;

Puede acceder a todos los comandos del switch en el modo EXEC privilegiado. Sin embargo, debido a que  muchos de los comandos privilegiados configuran parámetros operativos, el acceso privilegiado se debe  proteger con una contraseña para evitar el uso no autorizado.&#x20;

El conjunto de comandos EXEC privilegiado incluye los comandos disponibles en el modo EXEC del usuario,  muchos comandos adicionales y el comando configure a través del cual se obtiene acceso a los modos de  configuración.&#x20;

a. Haga clic en S1 y luego en la pestaña CLI. Presione Enter.&#x20;

b. Ingrese al modo EXEC privilegiado introduciendo el comando enable:&#x20;

Abra la ventana de configuración para S1&#x20;

Switch> enable&#x20;

Switch# &#x20;

Observe que la solicitud cambió para reflejar el modo EXEC privilegiado.&#x20;

Paso 2: Examine la configuración actual del switch.&#x20;

Ingrese el comando show running-config.&#x20;

Switch# show running-config&#x20;

Responda las siguientes preguntas:



¿Cuántas interfaces Fast Ethernet tiene el switch?&#x20;

&#x20;24 interfaces Fast Ethernet (de FastEthernet 0/1 a 0/24).

¿Cuántas interfaces Gigabit Ethernet tiene el switch?&#x20;

(GigabitEthernet 0/1 y 0/2 ).

¿Cuál es el rango de valores que se muestra para las líneas vty?&#x20;

De 0 a 4

¿Qué comando muestra el contenido actual de la memoria de acceso aleatorio no volátil (NVRAM)?&#x20;

show startup-config

¿Por qué el conmutador responde con "startup-config no está presente"?&#x20;

Porque el switch se encuentra con su configuración de fábrica y aún no se ha guardado ningún archivo de configuración en la NVRAM.

Parte 2: Cree una configuración básica del switch&#x20;

Paso 1: Asigne un nombre a un switch.&#x20;

Para configurar los parámetros de un switch, quizá deba pasar por diversos modos de configuración.  Observe cómo cambia la petición de entrada mientras navega por el switch.&#x20;

Switch# configure terminal&#x20;

Switch(config)# hostname S1&#x20;

S1(config)# exit&#x20;

S1#&#x20;

Paso 2: Proporcione acceso seguro a la línea de consola.&#x20;

Para proporcionar un acceso seguro a la línea de la consola, acceda al modo config-line y establezca la  contraseña de consola en letmein.&#x20;

S1# configure terminal&#x20;

Introduzca los comandos de configuración, uno por línea. End with CNTL/Z. S1(config)# line console 0&#x20;

S1(config-line)# password letmein&#x20;

S1(config-line)# login&#x20;

S1(config-line)# exit &#x20;

S1(config)# exit&#x20;

%SYS-5-CONFIG\_I: Configured from console by console <br>

Pregunta:&#x20;

S1# <br>

¿Por qué se requiere el comando login?&#x20;

Para indicarle al switch que active la solicitud y verificación de la contraseña configurada cada vez que un usuario intente acceder a la línea de consola.

Paso 3: Verifique que el acceso a la consola sea seguro.&#x20;

Salga del modo privilegiado para verificar que la contraseña del puerto de consola esté vigente. S1# exit&#x20;

Switch con0 is now available&#x20;

Press RETURN to get started.&#x20;

Verificación de acceso del usuario&#x20;

Contraseña:&#x20;

S1>&#x20;

Nota:Si el switch no le solicitó una contraseña, no configuró el parámetrologin en el Paso 2. Paso 4: Proporcione un acceso seguro al modo privilegiado.&#x20;

Establezca la contraseña de enable en c1$c0. Esta contraseña protege el acceso al modo privilegiado. &#x20;

Nota: El 0 en c1$c0 es un cero, no una O mayúscula. Esta contraseña no se calificará como correcta hasta  después de que la cifre en el Paso 8.&#x20;

S1> enable&#x20;

S1# configure terminal&#x20;

S1(config)# enable password c1$c0&#x20;

S1(config)# exit&#x20;

%SYS-5-CONFIG\_I: Configured from console by console&#x20;

S1#&#x20;

Paso 5: Verifique que el acceso al modo privilegiado sea seguro.&#x20;

a. Introduzca el comando exit nuevamente para cerrar la sesión del switch.&#x20;

b. Presione \<Enter>; a continuación, se le pedirá que introduzca una contraseña:&#x20;

Verificación de acceso del usuario&#x20;

Password:&#x20;

c. La primera contraseña es la contraseña de consola que configuró para line con 0. Introduzca esta  contraseña para volver al modo EXEC del usuario. &#x20;

d. Introduzca el comando para acceder al modo privilegiado. &#x20;

e. Introduzca la segunda contraseña que configuró para proteger el modo EXEC privilegiado. f. Verifique su configuración examinando el contenido del archivo de configuración en ejecución: S1# show running-config&#x20;

Tenga en cuenta que la consola y las contraseñas de activación están en texto plano. Esto podría  suponer un riesgo para la seguridad si alguien está mirando por encima de su hombro u obtiene acceso  a los archivos de configuración almacenados en una ubicación de copia de seguridad.&#x20;

Paso 6: Configure una contraseña encriptada para proporcionar un acceso seguro al modo  privilegiado.&#x20;

La contraseña de enable se debe reemplazar por una nueva contraseña secreta encriptada mediante el  comando enable secret. Configure la contraseña de enable secret como itsasecret.&#x20;

S1# config t&#x20;

S1(config)# enable secret itsasecret&#x20;

S1(config)# exit&#x20;

S1#&#x20;

Nota: La contraseña deenable secret sobrescribe la contraseña de enable password. Si ambos están  configurados en el conmutador, debe ingresar la contraseña enable secret para ingresar al modo EXEC  privilegiado.&#x20;

Paso 7: Verifique si la contraseña de enable secret se agregó al archivo de configuración.&#x20;

Introduzca el comando show running-config nuevamente para verificar si la nueva contraseña de enable  secret está configurada.&#x20;

Nota: Puede abreviar show running-config como  <br>

Preguntas:&#x20;

S1# show run <br>

¿Qué se muestra como contraseña de enable secret?&#x20;

Una cadena de caracteres generada mediante un algoritmo de cifrado o hash criptográfico

¿Por qué la contraseña de enable secret se ve diferente de lo que se configuró?&#x20;

Porque ha sido encriptada por seguridad mediante una función hash, lo que impide que se pueda leer a simple vista en el archivo de configuración.

Paso 8: Encripte las contraseñas de consola y de enable.&#x20;

Como notó en el Paso 7, la contraseña enable secretestaba encriptada, pero las contraseñasenable y console todavía estaban en texto plano. Ahora encriptaremos estas contraseñas de texto no cifrado con el  comando service password-encryption.&#x20;

S1# config t&#x20;

S1(config)# service password-encryption <br>

Pregunta:&#x20;

S1(config)# exit <br>

Si configura más contraseñas en el switch, ¿se mostrarán como texto no cifrado o en forma cifrada en el  archivo de configuración? Explique.&#x20;

Se mostrarán en forma cifrada, ya que el comando global service password-encryption aplica un cifrado reversible de tipo débil a todas las contraseñas que estaban previamente en texto plano.

Parte 3: Configure un aviso de MOTD&#x20;

Paso 1: Configure un aviso de mensaje del día (MOTD).&#x20;

El conjunto de comandos de Cisco IOS incluye una característica que permite configurar los mensajes que  cualquier persona puede ver cuando inicia sesión en el switch. Estos mensajes se denominan “mensajes del  día” o “avisos de MOTD”. Coloque el texto del mensaje en citas o utilizando un delimitador diferente a  cualquier carácter que aparece en la cadena de MOTD.&#x20;

S1# config t &#x20;

S1(config)# banner motd "This is a secure system. Authorized Access Only! S1(config)# exit&#x20;

%SYS-5-CONFIG\_I: Configured from console by console <br>

Preguntas:&#x20;

S1# <br>

¿Cuándo se muestra este aviso?

Se muestra inmediatamente antes de que aparezca la solicitud de inicio de sesión, cuando cualquier usuario intenta conectarse al switch (por consola, Telnet o SSH).

¿Por qué todos los switches deben tener un aviso de MOTD?&#x20;

Por motivos legales y de seguridad, para advertir explícitamente a los usuarios no autorizados que el acceso está prohibido y dejar constancia de que el acceso no autorizado puede ser procesado judicialmente.

Parte 4: Guarde y verifique archivos de configuración en NVRAM&#x20;

Paso 1: Verifique que la configuración sea precisa mediante el comando show run.&#x20;

Guarde el archivo de configuración. Usted ha completado la configuración básica del switch. Ahora haga una  copia de seguridad del archivo de configuración en ejecución a NVRAM para garantizar que los cambios que  se han realizado no se pierdan si el sistema se reinicia o se apaga.&#x20;

S1# copy running-config startup-config&#x20;

Destination filename \[startup-config]?\[Enter] &#x20;

Building configuration... &#x20;

\[OK]&#x20;

Cierre la ventana de configuración para S1&#x20;

Preguntas:&#x20;

¿Cuál es la versión abreviada más corta del comando copy running-config startup-config?

copy ru stc, o tambien se puede hacer un wr o write

Examine el archivo de configuración de inicio.&#x20;

¿Qué comando muestra el contenido de la NVRAM?&#x20;

show startup-config

¿Todos los cambios realizados están grabados en el archivo?&#x20;

No automáticamente. Solo se graban aquellos cambios que se hayan transferido explícitamente desde la memoria RAM (running-config) hacia la NVRAM (startup-config) mediante el comando de copia.

Parte 5: Configurar S2&#x20;

Ha completado la configuración en S1. Ahora configurará el S2. Si no recuerda los comandos, consulte las  partes 1 a 4 para obtener ayuda. &#x20;

Configure el S2 con los siguientes parámetros:&#x20;

Abra la ventana de configuración para S2&#x20;

a. Device name: S2&#x20;

b. Proteja el acceso a la consola con la contraseña letmein.&#x20;

c. Configure enable password como c1$c0 y una contraseña enable secret como itsasecret. d. Configure un mensaje apropiado para aquellos que inician sesión en el switch.&#x20;

e. Encripte todas las contraseñas de texto no cifrado.&#x20;

f. Asegúrese de que la configuración sea correcta.&#x20;

g. Guarde el archivo de configuración para evitar perderlo si el switch se apaga.&#x20;

h. Cierre la ventana de configuración para S2&#x20;

Fin del documento





En este ejercicio hemos aprendido a configurar los switch, hemos aprendido a poner contraseñas y configurar todos los tipos de niveles de configuracion del switch, hemos puesto contraseñas en la interfaz de usuario sin poderes y en el usuario medio donde pueden configurar algo del switch

<figure><img src=".gitbook/assets/image (21).png" alt=""><figcaption></figcaption></figure>

© 2015 - 2020 Cisco y/o sus filiales. Todos los derechos reservados. Información pública de Cisco Página 5 de 5 www.netacad.com&#x20;

\
\
\
<br>

<br>
