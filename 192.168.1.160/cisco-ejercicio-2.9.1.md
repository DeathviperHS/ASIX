---
description: 2.9.1-packet-tracer---basic-switch-and-end-device-configuration_es-XL
---

# Cisco Ejercicio 2.9.1

<img src=".gitbook/assets/unknown (1).png" alt="" height="84" width="272">

Packet Tracer — Configuración básica del switch y del dispositivo  final&#x20;

Tabla de asignación de direcciones&#x20;

| Dispositivo    | Interfaz  | Dirección IP  | Máscara de subred |
| -------------- | --------- | ------------- | ----------------- |
| \[\[S1Name]]   | VLAN 1    | \[\[S1Add]]   | 255.255.255.0     |
| \[\[S2Name]]   | VLAN 1    | \[\[S2Add]]   | 255.255.255.0     |
| \[\[PC1Name]]  | NIC       | \[\[PC1Add]]  | 255.255.255.0     |
| \[\[PC2Name]]  | NIC       | \[\[PC2Add]]  | 255.255.255.0     |

\
<br>

Objetivos&#x20;

• Configure los nombres de host y las direcciones IP en dos switches con sistema operativo Internetwork  (IOS) de Cisco mediante la interfaz de línea de comandos (CLI).&#x20;

• Utilice comandos de Cisco IOS para especificar o limitar el acceso a las configuraciones de dispositivos.  • Utilice comandos de IOS para guardar la configuración en ejecución.&#x20;

• Configure dos dispositivos host con direcciones IP.&#x20;

• Verifique la conectividad entre dos terminales PC.&#x20;

Escenario&#x20;

Como técnico de LAN contratado recientemente, el administrador de red le solicitó que demuestre su  habilidad para configurar una LAN pequeña. Sus tareas incluyen la configuración de parámetros iniciales en  dos switches mediante Cisco IOS y la configuración de parámetros de dirección IP en dispositivos host para  proporcionar conectividad completa. Debe utilizar dos switches y dos hosts/PC en una red conectada por  cable y con alimentación. &#x20;

Instrucciones&#x20;

Configure los dispositivos para que cumplan los requisitos que se indican a continuación.&#x20;

Requisitos&#x20;

• Utilice una conexión de consola para acceder a cada switch.&#x20;

• Nombre los switches \[\[S1Name]] y \[\[S2Name]].&#x20;

• Utilice la contraseña \[\[LinePW]] para todas las líneas. &#x20;

• Utilice la contraseña secreta \[\[SecretPW]].&#x20;

• Encripte todas las contraseñas de texto no cifrado.&#x20;

• Configure un aviso apropiado para el mensaje del día (MOTD).&#x20;

• Configure el direccionamiento para todos los dispositivos de acuerdo con la tabla de direccionamiento. • Guarde las configuraciones.

• Verifique la conectividad entre todos los dispositivos.&#x20;

Nota: Hag clic en Check Results para ver su progreso. Haga clic en Reset Activity para generar un nuevo  conjunto de requisitos. Si hace clic en esto antes de completar la actividad, se perderán todas las  configuraciones.&#x20;

ID: \[\[indexNames]]\[\[indexPWs]]\[\[indexAdds]]\[\[indexTopos]]&#x20;

Fin del documento

| Dispositivo  | Interfaz         | Dirección                | Máscara de subred        |
| ------------ | ---------------- | ------------------------ | ------------------------ |
| pc1          | NIC              | <p><br>128.107.20.25</p> | <p>255.255.255.0<br></p> |
| pc2          | <p><br>NIC</p>   | <p>128.107.20.30<br></p> | <p>255.255.255.0<br></p> |
| ASw1         | VLAN1            | <p>128.107.20.10<br></p> | <p>255.255.255.0<br></p> |
| ASw2         | <p>VLAN1<br></p> | <p><br>128.107.20.15</p> | <p><br>255.255.255.0</p> |

\
<br>

<img src=".gitbook/assets/unknown (2).png" alt="" height="147" width="409">

<img src=".gitbook/assets/unknown (3).png" alt="" height="212" width="443">

<img src=".gitbook/assets/unknown (4).png" alt="" height="320" width="241">

© 2013 - 2020 Cisco y/o sus filiales. Todos los derechos reservados. Información pública de Cisco Página 3 de 3 www.netacad.com

<br>

<figure><img src=".gitbook/assets/image (19).png" alt=""><figcaption></figcaption></figure>
