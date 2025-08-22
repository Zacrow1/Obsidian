entender los principios de la comunicación de mensajes sobre redes en entornos [[Concepto de sistemas distribuidos]]{Cliente-servidor}.

## Redes y dispositivos de red:
- **Hosts:** En un sentido general son todos los dispositivos enlazados en una red, como ser computadoras, teléfonos móviles, servidores, impresoras, televisores inteligentes, etc.). Cada uno de ellos se identifica a través de una IP. 

- **Red (Network):** Una red se define como una agrupación lógica de hosts que requieren conectividad similar apoyada en la existencia de una infraestructura de comunicación.

- **Repetidores, Hubs, Switches y Routers:** Son elementos que forman parte de la infraestructura que garantiza la conectividad y son parte de las redes.

## Direccion IP — Internet Protocol

Las IPs identifican los hosts en una red y se componen tradicionalmente de números de 32 bits normalmente presentados como cuatro "octetos" de bits. Una dirección IP común tiene el siguiente formato:
![[Pasted image 20240708122029.png]]

Los cuatro números en una dirección IP se denominan octetos, porque pueden tener valores entre 0 y 255 ($2^8 = 256$ posibilidades por octeto). 
Es decir, los valores binarios pueden veriar entre 000000000, siendo que el primero que presenta la red y el último que presenta el broadcast de la red, no podemos utilizar para los hosts.

#### Comando 

En windows el comando `ipconfig` nos muestra la configuración de IP de Windows el Adaptador de Ethernet donde se nos muestra:

![[Pasted image 20240708122536.png]]

El comando `ip` en Linux:

El comando `nslookup` en Linux es una herramienta de línea de comandos que te permite **obtener información, realizar consultas y solucionar problemas relacionados con el Sistema de Nombres de Dominio (DNS)**

**¿Qué puedes hacer con nslookup?**

- Resolver nombres de dominio:
- Resolver nombres de dominio en modo inverso
- Obtener información sobre registros DNS específicos
- Especificar un servidor DNS para las consultas
- Cambiar entre modo interactivo y no interactivo

**Ejemplos:**

- **Resolver google.com:**

```
nslookup google.com
```

- **Resolver la dirección IP en modo inverso:**

```
nslookup 8.8.8.8
```

.255 esta reservada para el broadcast

### Dirección IP — Internet Protocol

![[Pasted image 20240708130137.png]]

- Con el crecimiento explosivo de Internet la versión 4 se vio amenazada con agotar el stock de direcciones IP (Pronóstico inicial - 2008) 
- Algunas técnicas para evitar este posible agotamiento:
	- El direccionamiento privado (RFC 1918);
	- Las sub redes (RFC 950);
	- La división en clases para definir pequenias
	- La división en clases para definir redes pequeñas, medianas y grandes;
	- Enruteamiento sin clases entre dominios (Classless Interdomain Routing — CIDR);
	- Máscara de subred con longitud variable (Variable Length Subnet Mask— VLSM);
	- Traducción de direcciones de red (NAT Network Address Translation).
### INFORMACIONES RELEVANTES IP

La demanda por nuevos números IP se há reducido drásticamente a través de esta técnica y otras tecnologías creadas, y aún nose ha producido el agotamiento de las direcciones IPv4. Como el agotamiento ciertamente ocurrirá, una forma de direccionamiento llamada IP versión 6 comenzó a ser desarrollada en la década de 1990.

El IPv6 tiene como objetivo serla solucion definitiva para el direccionamiento de internet
La principal diferencia es el espacio de direccionamiento, aumentado de 32 bits a 128 bits.
Las direcciones IPv6 están compuestos de ocho grupos de 4 dígitos hexadecimales, como se muestra en el siguiente ejemplo,
![[Pasted image 20240708130233.png]]
Por fin, la IP versión 6 resuelve la limitación de direccionamiento actual en internet.

### NAT - Network Address Translation
Un NAT (Network Address Translation, o Traducción de Direcciones de Red) es una técnica que consiste en transcribir la dirección IP de un paquete de una red interna que pasa por un enruteador para que ese paquete tenga acceso a otra red externa.
Un NAT solo reconoce paquetes TCP y no siendo posible hacer el puente de otros paquetes.
Conectar una red que usa direcciones privadas a Internet requiere convertir direcciones privadas en direcciones públicas. Este proceso de conversión se llama NAT.

![[Pasted image 20240708130434.png]]

### NAT-Entendimiento
Se puede decir que NAT no es más que una "conversión" de IP público a IP privado, pudiendo así acceder a otros servidores fuera de la red interna.

### Protocolos de internet
En terminos generales un protocolo es un conjunto de reglas que norman la
comunicación en internet, es decir, definen la forma de comunicación entre los nodos
de una red (note que internet significa entre redes).
Veamos ARP (Address Resolution Protocol) como ejemplo de un protocolo. El estándar
que define el funcionamiento de ARP esta normado por la RFC 826. Existen muchos protocolos dependiendo del tipo de servicio, IP es uno de ellos, además de TCP, UDP, FTP SMTP, DNS, etc.

![[Pasted image 20240708133421.png]]

### DNS - Domain Name System

Es un sistema jerárquico y distribuído de traducción de nombres.

El DNS traduce nombres a direcciones IP y vice-versa.
	Ejemplo: www.atlaspapelaria.com.br 
	IP:35.199.85.145

Como base de datos es distribuida, su tamaño es virtualmente ilimitado y el rendimiento no se degrada tanto cuando se adiciona más servidores a ese servicio. 

Un servidor DNS secundario es una copia de seguridad del servidor DNS primario, proyectada para el caso de una eventual falla del servidor primario.

##### JUSTIFICACIONES
- Hay miles de millones de direcciones IP en uso actualmente y la mayoria de las máquinas tienen un nombre legible;
- Diariamente son realizados miles de millones de solicitudes de DNS;
- Nombres de dominios y direcciones IP cambian constantemente;
- Nuevos nombres de dominio son creados diariamente;
- El servicio DNS facilita el acceso a los recursos de la red, porque es mas fácil recordar nombre que secuencias numéricas.

![[Pasted image 20240708134615.png]]

### DHCP - Dynamic Host Configuration Protocol
Es un protocolo de servicio TCP/IP proporciona que configuración dinámica terminales, con concesión de direcciones IP de host y otros es de configuración para clientes de red. Este protocolo es el sucesor del BOOTP, que se há vuelto limitado para las exigencias actuales. El DHCP apareció como estándar en 1993.

![[Pasted image 20240708135057.png]]

### EL MODELO OSI:
De acuerdo a la ISO (International Organization for Standardization), el modelo OSI (Open
Systems Interconnection model) es un modelo conceptual que "proporciona una base común para la coordinación del desarrollo de estándares con el propósito de la interconexión de sistemas".

![[Pasted image 20240708135607.png]]
![[Pasted image 20240708140120.png]]