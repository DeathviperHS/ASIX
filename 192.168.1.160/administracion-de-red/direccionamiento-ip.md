# Direccionamiento IP

Un direccionamiento IP se clasifica por rangos

A --> BIG --> 0 hasta la 127\
B --> MEDIO --> 128 hasta la 191 \
C --> PEQUEÑO --> 192 hasta la 223\
D --> ??? --> 224 hasta la 239\
E --> ??? --> 240 hasta la 255

Una IP se divide en 32 bits, es decir $$2^{8}$$ , que da 256, en la IP no ponemos es el numero 255, ya que se considera la puerta de salida o broadcast, y la xxx.xxx.xxx.xx0 donde es la puerta del red, es la que queremos que nos de la conectividad a la red, y la xxx.xxx.xxx.xx1 es la primera IP que se nos asocia, el dispositivo mas comun que tiene esta IP es el router, ya que es el gateway, la IP a la que nos conectamos para poder conectarnos al dispositivo que nos da la conectividad, la ultima IP valida que podemos usar es la xxx.xxx.xxx254 y la primera sin quitar la IP al router, es la IP xxx.xxx.xxx.xx2.&#x20;

Las IP se rigen en 4 grupos, es decir se separan los 32 bits en 4 grupos de 8, donde cada bit es un 1 o un 0, cada numero se transforma a 2 elevado a la posicion en la que esta, para transformarlo en numeros decimales.

Cuando llegamos a&#x20;

PUERTOS

22 --> SSH

23 --> TELNET

53 --> DNS

80 --> HTTP

443 --> HTTPS
