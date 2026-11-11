# Router Cisco 2810 Series

> **Nota sobre el nombre:** esta página conserva el título solicitado, «Router Cisco 2810 Series». El equipo de las fotografías está identificado en su etiqueta como **Cisco 2811** (PID: CISCO2811), perteneciente a la familia Cisco 2800. No debe confundirse con un modelo 2810.

## 1. Identificación del equipo

| Dato                          | Información                                                                                                  |
| ----------------------------- | ------------------------------------------------------------------------------------------------------------ |
| Fabricante                    | Cisco Systems                                                                                                |
| Modelo identificado           | Cisco 2811 Integrated Services Router                                                                        |
| Familia                       | Cisco 2800 Series                                                                                            |
| PID visible                   | CISCO2811                                                                                                    |
| Número de serie visible       | FHK1042U04W                                                                                                  |
| Fecha estimada de fabricación | Semana 42 de 2010 (interpretación del código de serie; confirmar con Cisco si se necesita una fecha oficial) |
| Sistema operativo             | Cisco IOS                                                                                                    |
| Versión exacta de IOS         | Pendiente de comprobar con `show version`                                                                    |
| Tipo                          | Router modular de servicios integrados                                                                       |
| Formato                       | Chasis para rack de 19 pulgadas, aproximadamente 1U                                                          |

La serie Cisco 2800 se presentó en 2004. Esa es la fecha de lanzamiento de la familia, no la fecha de fabricación de esta unidad.

## 2. Componentes internos observados

En la fotografía del interior se distinguen los siguientes elementos. La identificación funcional de los circuitos sin referencia legible es orientativa; no se debe asignar una función concreta a un chip únicamente por su forma o posición.

| Elemento                          | Función                                                                                   |
| --------------------------------- | ----------------------------------------------------------------------------------------- |
| Placa base (PCB)                  | Interconecta los componentes y módulos del router                                         |
| Módulo AIM-VPN/EPII-PLUS          | Módulo de aceleración criptográfica para operaciones VPN compatibles                      |
| Conectores y ranuras de expansión | Permiten instalar módulos compatibles                                                     |
| Cable plano (ribbon)              | Conecta internamente placas o conjuntos del equipo                                        |
| Fuente y blindajes metálicos      | Alojan/protegen circuitos y partes de alimentación                                        |
| Condensadores                     | Filtrado y estabilización de la alimentación                                              |
| Bobinas/inductores                | Parte de los circuitos de regulación de tensión                                           |
| Circuitos integrados              | Realizan funciones de procesamiento y control; la función exacta depende de su referencia |
| Tarjeta/módulo inferior           | Requiere leer las referencias de sus chips para identificar con certeza su función        |

**Aclaración:** no se puede confirmar visualmente la capacidad instalada de RAM o Flash ni la referencia exacta de la CPU en las fotografías disponibles. Se debe comprobar con los comandos del apartado 9.

## 3. Interfaces físicas

### Interfaces integradas

En el panel fotografiado se identifican dos puertos RJ-45 Fast Ethernet:

| Interfaz         | Cantidad | Función                                                         |
| ---------------- | -------: | --------------------------------------------------------------- |
| FastEthernet 0/0 |        1 | Interfaz Ethernet 10/100 para LAN o WAN                         |
| FastEthernet 0/1 |        1 | Interfaz Ethernet 10/100 para LAN o WAN                         |
| Console          |        1 | Administración local por línea de comandos                      |
| AUX              |        1 | Acceso de administración auxiliar, habitualmente mediante módem |

El equipo también dispone de opciones de expansión. La disponibilidad real depende de los módulos instalados:

* Ranuras HWIC/WIC para interfaces WAN o de conectividad compatibles.
* Ranura de red para módulos compatibles (NME).
* Ranuras AIM para módulos de integración/aceleración.
* Conectores PVDM para módulos DSP de voz.
* Almacenamiento CompactFlash para IOS y archivos.

No se debe asumir que todas las ranuras están ocupadas ni que todos los módulos están instalados. La lista exacta se comprueba con `show inventory` y `show diag`.

### Puertos ASYNC 0–7 y 8–15

Cuando están presentes en un módulo de interfaz asíncrona, estos conectores proporcionan líneas serie asíncronas numeradas del 0 al 15. Se utilizan para conectar terminales, módems u otros equipos serie mediante el cableado/adaptador apropiado.

No son puertos Ethernet ni equivalen al puerto Console. Su disponibilidad depende del módulo instalado y de su configuración.

### Diferencia entre Console y ASYNC

* **Console:** permite administrar el propio router y acceder a Cisco IOS.
* **ASYNC:** permite que el router se comunique por líneas serie con dispositivos externos. No es, por sí mismo, el acceso de consola local del router.

## 4. Enrutamiento (routing)

Según la imagen de Cisco IOS y las funciones/licencias disponibles, la familia puede trabajar con:

| Tecnología/protocolo | Uso                                                            |
| -------------------- | -------------------------------------------------------------- |
| Rutas estáticas      | Rutas introducidas manualmente por el administrador            |
| RIP/RIPv2            | Enrutamiento dinámico de vector distancia                      |
| OSPF                 | Enrutamiento dinámico de estado de enlace                      |
| EIGRP                | Protocolo de enrutamiento avanzado de Cisco                    |
| BGP                  | Enrutamiento entre sistemas autónomos, si la imagen lo soporta |

Otras funciones de red habituales en la plataforma incluyen NAT/PAT, DHCP, VLAN 802.1Q, subinterfaces, ACL y QoS, sujetas a la versión de IOS y al hardware instalado.

**Importante:** la lista anterior describe capacidades posibles de la plataforma; no demuestra que estén habilitadas o configuradas en este router.

## 5. TRUST y UNTRUST

TRUST y UNTRUST son roles o zonas lógicas de seguridad, no nombres físicos impresos en los puertos del Cisco 2811.

* **TRUST:** zona considerada de confianza, normalmente la LAN interna con ordenadores, servidores e impresoras.
* **UNTRUST:** zona externa o de menor confianza, normalmente la conexión hacia Internet o una red de proveedor.

Ejemplo de diseño (no es la configuración confirmada de este equipo):

| Interfaz de ejemplo | Rol propuesto | Conexión                      |
| ------------------- | ------------- | ----------------------------- |
| FastEthernet 0/0    | TRUST         | LAN interna                   |
| FastEthernet 0/1    | UNTRUST       | Router del proveedor/Internet |

La asignación real depende de la configuración. En IOS clásico se pueden aplicar ACL y, si la imagen lo admite, Cisco IOS Zone-Based Firewall para controlar el tráfico entre zonas.

## 6. Seguridad y VPN

Entre las funciones que pueden estar disponibles según IOS y módulos:

* ACL: filtran tráfico por dirección IP, protocolo y puertos.
* NAT/PAT: traducen direcciones privadas y públicas.
* Firewall IOS / Zone-Based Firewall: aplican políticas de inspección entre interfaces o zonas.
* VPN IPsec: crean túneles cifrados entre redes o usuarios compatibles.
* SSH: administración remota cifrada.
* AAA: autenticación, autorización y accounting.
* QoS: clasificación y priorización del tráfico.

En la placa fotografiada se lee la referencia **AIM-VPN/EPII-PLUS**. Este módulo proporciona aceleración criptográfica para funciones VPN compatibles. Su presencia no significa que exista una VPN configurada.

## 7. Memoria y almacenamiento

Las capacidades exactas de RAM y Flash de esta unidad no se han confirmado. Pueden variar según la configuración y las ampliaciones realizadas por propietarios anteriores.

Consultar:

* `show version`: memoria y versión de IOS.
* `show flash:` o `dir flash:`: archivos y capacidad del almacenamiento Flash.
* `show inventory`: inventario de hardware reconocido.

No utilizar cifras genéricas de una ficha comercial como si fueran las capacidades instaladas en esta unidad.

## 8. Restablecimiento de configuración de fábrica

**Advertencia:** estos pasos eliminan la configuración de inicio del router. Antes de continuar, asegúrate de que tienes autorización y de que no necesitas conservar la configuración del anterior propietario.

Si puedes entrar en modo privilegiado:

```
enable
erase startup-config
reload
```

Si el router pregunta si deseas guardar la configuración antes de reiniciar, responde `no`. Confirma el reinicio cuando lo solicite. Al arrancar, si aparece el asistente inicial, responde `no` para entrar después a la CLI.

También puede utilizarse `write erase` para borrar la configuración de inicio.

El borrado de startup-config no elimina Cisco IOS de la memoria Flash ni equivale a formatear el almacenamiento. No ejecutes `format flash:` ni borres archivos IOS para hacer un restablecimiento normal.

Si solicita una contraseña de enable que no tienes, será necesario realizar el procedimiento de recuperación de contraseña específico del Cisco 2811 antes de borrar la configuración.

## 9. Comandos útiles de comprobación

| Comando                   | Qué permite comprobar                                                                   |
| ------------------------- | --------------------------------------------------------------------------------------- |
| `show version`            | Modelo, versión de IOS, uptime y memoria detectada                                      |
| `show ip interface brief` | Interfaces, direcciones IP y estado                                                     |
| `show interfaces`         | Detalles y estadísticas de interfaces                                                   |
| `show ip route`           | Tabla de enrutamiento                                                                   |
| `show running-config`     | Configuración activa                                                                    |
| `show startup-config`     | Configuración guardada para el próximo arranque                                         |
| `show inventory`          | Inventario de módulos y componentes reconocidos                                         |
| `show diag`               | Información de hardware y ranuras, si está soportado                                    |
| `show access-lists`       | Listas de control de acceso                                                             |
| `show ip nat statistics`  | Estadísticas de NAT                                                                     |
| `show zone security`      | Zonas de seguridad, si Zone-Based Firewall está configurado y el comando está soportado |

## 10. Datos pendientes de verificar en la unidad

Para cerrar el inventario técnico, ejecutar los comandos del apartado anterior y anotar:

* Versión exacta de Cisco IOS y feature set.
* RAM y Flash realmente instaladas.
* Módulos presentes en las ranuras de expansión.
* Estado y direccionamiento de FastEthernet 0/0 y 0/1.
* Protocolos de routing activos.
* Existencia de ACL, NAT, VPN o políticas de firewall.
* Asignación efectiva de interfaces a TRUST y UNTRUST.

## 11. Resumen

El equipo identificado es un **Cisco 2811 Integrated Services Router**, de la familia Cisco 2800, con dos interfaces Fast Ethernet integradas y arquitectura modular. La etiqueta muestra el número de serie **FHK1042U04W**, cuya codificación apunta a la semana 42 de 2010. En el interior se ha identificado un módulo **AIM-VPN/EPII-PLUS**.

La versión exacta de IOS, las memorias instaladas, los módulos adicionales y la configuración actual deben confirmarse conectándose al router y ejecutando los comandos de diagnóstico.
