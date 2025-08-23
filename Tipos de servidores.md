- Una mirada a los Sistemas Distribuidos
- Servidores Web
- Servidores de Bases de Datos
- Servidores de Correo electrónico.
- Servidor DNS
- Servidor FTP

Un sistema distribuido es una colección de componentes de software o hardware separados e independientes llamados nodos, conectados entre sí por medio de una red, y que trabajan juntos de manera coherente al coordinarse y comunicarse a través del paso de mensajes o eventos para cumplir un objetivo final.
Las complejidad del sistema permanecen oculta para el usuario final, ya sea un ser humano o una computadora. De manera que aparece a sus usuarios como una sola computadora.
En un sistema distribuido actúan programas, procesos, computadoras, una red(es), aplicaciones distribuidas, protocolos.
- Un programa es un conjunto de instrucciones.
- Un proceso es un programa en ejecución.
- Se tiene una red de computadores interconectadas.
- Los sistemas distribuidos requieren la interconexión que paveen las redes.
- Las aplicaciones distribuidas son un conjunto de procesos que se ejecutan en más de una computadora comunicándose a través del intercambio de mensajes.
- Un protocolo es un conjunto de reglas e instrucciones para la comunicación en un sistema distribuido.
- Se cuenta con múltiples componentes autónomos.
- Los programas se ejecutan de forma concurrente.
- Existe una única forma de comunicación y sincronización: paso de mensajes.
- Los errores o fallos son independientes.
- El sistema de software es complejo.

![[Pasted image 20240805123436.png]]

## SERVIDORES WEB:
Un servidor web es un software y un hardware que hace uso del protocolo HTTP y otros protocolos para responder a las solicitudes que los clientes realizan a través de Internet. Su principal función es mostrar el contenido de un sitio web almacenando, procesando y entregando las páginas web a los clientes.
El hardware del servidor web está conectado a Internet y permite el intercambio de datos con otros dispositivos conectados, por otro lado el software del servidor web controla Como un cliente accede a los archivos alojados en el servidor.
![[Pasted image 20240805123503.png]]
![[Pasted image 20240805124156.png]]
### Peticón/Respuesta HTTP
Por simplicidad veremos el modelo del protocolo de comunicación del protocolo HTTP a pesar que en nuestros días se usa más el protocolo HTTPS.

![[Pasted image 20240805124232.png]]
## Arquitectura de 1 nivel
En esta arquitectura la presentación, la lógica empresarial y las capas de datos se almacenan en un solo dispositivo. Por ejemplo pensemos en una aplicación de escritorio que funciona sin conexión a internet y almacena todos sus datos en la misma computadora desde donde se ejecuta.
![[Pasted image 20240805124412.png]]

## Arquitectura de 2 niveles
la arquitectura de 2 niveles, el cliente se encuentra en el primer nivel. 1 En el segundo nivel, se encuentran el servidor de bases de datos y el servidor de aplicaciones web. Este segundo nivel proporciona la información (los datos) y ejecuta la lógica empresarial para la aplicación web. Este nivel es el responsable
de proporcionar las características de disponibilidad, escalabilidad y rendimiento para el entorno web de la organización.
Como ejemplo podemos imaginarnos cuando iniciamos sesión en nuestra cuenta de Correo electrónico.
![[Pasted image 20240805124558.png]]

## Arquitectura de 3 niveles
En un arquitectura de tres niveles, el servidor de bases
reside en un servidor diferente al servidor de
aplicaciones web.
El cliente se encuentra en el primer nivel, igual que en
una arquitectura de dos niveles.
El servidor de aplicaciones reside en el segundo nivel. El
servidor de aplicaciones maneja la parte de la lógica
empresarial y que hará las llamadas/consultas necesarias al servidor de bases de datos.
En el tercer nivel, el servidor de bases de datos provee la
información requerida.
En esta arquitectura, tanto el hardware y software del
segundo y tercer nivel llegan a compartir la responsabilidad de disponibilidad, escalabilidad y rendimiento de todo el entorno web.

![[Pasted image 20240805124838.png]]

![[Pasted image 20240805132224.png]]

### Tipos de Servidores Web
- Apache
- Nginx
- LiteSpeed
- Microsoft IIS
- Lighttpd
- Caddy
- GWS
- Cherokee
- NodeJS
- Sun Java System Web Server
![[Pasted image 20240805132525.png]]

## SERVIDORES DE BASES DE DATOS:
Los servidores de bases de datos se utilizan para almacenar y administrar las bases de datos almacenadas en el servidor y para proporcionar acceso a los datos a los usuarios autorizados. Este tipo de servidor mantiene los datos en una ubicación central de
la que se puede hacer una copia de seguridad cada cierto tiempo. También permite que los usuarios y las aplicaciones accedan de forma centralizada a los datos a través de la red.

El Servidor de Base de datos es un componente clave en un
arquitectura cliente/servidor, este alberga dentro de si sistema de gestión de bases de datos (DBMS) y las Bases de datos.

En el contexto de la base de datos, el cliente toma la solicitud del usuario, verifica la sintaxis y genera solicitudes de base de datos en SQL (u otro lenguaje de base de datos).
Posteriormente se transmite el mensaje hacia el servidor, se espera una respuesta y se da formato a la respuesta para el usuario final.
El servidor acepta y procesa las solicitudes de la base de datos, y finalmente transmite los resultados al cliente. Este proceso implica verificar la autorización, garantizar la integridad de los datos, mantener actualizado el catálogo o de datos del sistema.

La arquitectura de 1 nivel en DBMS es la arquitectura más simple de la base de datos
en la ue el Cliente, el Servidor y la Base de datos viven en una misma computadora.
Un ejemplo muy común sería como cuando instalamos un DBMS(mysql, etc) en nuestra
computadora, la cual actuaría como servidor, se tendría el DBMS y se podrían hacer
consultas SQL para una aplicación que se desarrolla en el misma computadora. 

[[XAMPP]] MySQL/MariaDB: XAMPP cuenta con uno de los sistemas relacionales de gestión de bases de datos más populares del mundo. En combinación con el servidor web Apache y el lenguaje PHP, MySQL sirve para el almacenamiento de datos para servicios web. En las versiones actuales de XAMPP esta base de datos se ha sustituido por MariaDB.

![[Pasted image 20240805133055.png]]

![[Pasted image 20240805133243.png]]

Arquitectura de 2 niveles
Un arquitect ra de 2 niveles en DBMS es una
arquitecturúe base de datos donde la capa de
presentación (User Interface) se ejecuta en un
cliente (PC, smartphone, etc.)
y los datos se
almacenan en un servidor llamado
nivel.
seguridad
arquitectura proporciona
Esta
adicional al DBMS, ya que no está expuesto
directamente
al usuario final. También
proporciona una comunicación directa y más
rápida.

![[Pasted image 20240805133327.png]]
### Arquitectura de 3 niveles
Una arquitectura de 3 niveles en DBMS es la arquitectura de servidor de cliente más popular y usada que los procesos funcionales, lógica del en DBMS negocio, acceso a datos, almacenamiento de datos e interfaz de usuario se realiza de forma independiente como módulos separados.
Esta arquitectura de tres niveles contiene una capa de presentación, una capa de aplicación y un servidor de base de datos.
Esta ar uitectura es una extensión de la arquitectura cliente-servidor de 2 niveles. Una arquitectura de 3 niveles tiene las siguientes capas:
Capa de presentación (PC, Smartphone, etc.)
Capa de aplicación (servidor)
Servidor de base de datos
![[Pasted image 20240805133406.png]]

## SERVIDORES DE CRREO ELECTONICO
Un servidor de correo electrónico (también llamado servidor de correo), es en esencia un sistema informático que envía y recibe correos electrónicos. Cuando enviamos un correo electrónico, este pasa por una serie de servidores hasta llegar al destinatario final.
Aunque este es un proceso súper rápido, hay una cantidad significativa de complejidad detrás del cómo se envían y reciben los correos electrónicos.
La comunicación por correo electrónico implica protocolos y procesos complejos. Según el tipo de acción que realizan, los servidores de correo electrónico se pueden clasificar en servidores de correo electrónico entrantes y salientes.

![[Pasted image 20240805133509.png]]

### Servidores de Correo Electrónico - SMTP

SMTP es a abreviatura de Simple Mail Transfer Protocol y es el servidor de correo saliente.
Cuando presionamos el botón de "Enviar/Send" en cualquier programa de correo electrónico (Gmail, Outlook, etc), este programa se va a conectar a un servidor en la red/lnternet que se llama servidor SMTP y este se encargará de enviar el correo electrónico.
SMTP es un protocolo que se utiliza cuando los correos electrónicos se entregan de clientes a servidores y de servidores a otros servidores.

Servidores de Correo Electrónico - POP3, IMAP

Respecto a los servidores de correo entrante existen de dos tipos: POP3 e IOP.
os servidores POP3(Post Office Protocol) versión 3, son conocidos por poner el
contenido de la Bandeja de entrada en el disco duro de su computadora.
Los servidores IMAP(Internet Message Access Protocol), se utilizan para Ia
sincronización directa de todo el buzón.
En la actualidad POP3 sigue siendo el protocolo mas usado porque es simple,
tiene una alta tasa de éxito y hace el trabajo con un mínimo de errores. Incluso le
permite descargar sus correos electrónicos y leerlos sin conexión.

## SERVIDORES DNS:
o El sistema de nombres de dominio (Domain Name System o DNS) es un gestor de nombres de sitios Web públicos y otros dominios de Internet. El DNS te permite escribir nombres de paginas web en un navegador web y que la computadora encuentre
automáticamente su dirección en Internet. Un elemento fundamental para que un DNS funcione es el servidor DNS y la colección mundial de servidores DNS.
o DNS se basa en la arquitectura cliente-servidor. Por ejemplo un navegador web actúa como un cliente DNS que hace solicitudes al servidor de DNS del ISP que tengamos contratado.

### Servidore DNS — Root Servers o Servidores raiz

Existe una jerarquía entre los DNS servers.
En la parte mas alta de esta jerarquía se encuentran los Root Servers que tienen por objetivo almacenar una base de datos completa de Nombres d9_dominio de Internet y sus correspondientes direcciones IP.
principalmente tiene 13 Internet root servers https://www.iana.org/domains/root/servers
![[Pasted image 20240805134605.png]]

 Root Servers existen otros servidores DYS que se encuentran por debajo de los Root servers, estos mantienen ciertas partes dflp_base de datos global. La mayoría de estos servidores DNS de bajo nivel pertenecen a empresas o proveedores de servicios de Internet (ISP). Veamos por ejemplo Google mantiene varios servidores DNS de todo
el mundo que se encargan de dar vida a google.com, google.com.bc google.com.mx, etc,
los ISP de igual forma.

## SERVIDORES FTP:
Un servidor FTP se utiliza para la transferencia de archivos y que también permite subdirectorios, iniciar sesión y varios comandos para manejar los archivos, por ejemplo: crear y eliminar archivos en el servidor FTP, cambiar el nombre de los archivos, crear
folders y subfolders, listar folders, etc.
El Protocolo de transferencia de archivos (FTP) es un protocolo de red que se utiliza para intercambiar y manipular archivos a través de una red basada en TCP/IP.
FTP se basa en una arquitectura cliente-servidor y utiliza conexiones de datos y control separadas entre las aplicaciones cliente y servidor. FTP se utiliza con autenticación de contraseña basada en el usuario o con acceso de usuario anónimo.

FTP puede orrer en modo activo o pasivo, que controlan cómo se abre la conexión de datos, y este modo de operación estará definido por el comando que ejecute el cliente.
Modo activo, el Cliente FTP envía al servidor la dirección IP y el número de puerto que el cliente utilizará para la conexión de datos, y el servidor abre la conexión.
Modo pasivo, el servidor envía al cliente una dirección IP y un número de puerto para que el cliente pueda establecer la conexión con el servidor. Este modo se usa cuando el cliente está ubicado detrás de un firewall y no puede aceptar la conexión TCP entrante.Serv•dor 

### FTP - Cómo funciona

servicio FT es un protocolo basado en TCP, o sea, es un protocolo de transferencia de archivos. Por defecto utiliza dos puertos: el puerto 20 (puerto de datos) y el puerto 21 (puerto para comandos).
Un usuario envía una solicitud de servicio al servidor en la red. Después de eso, la solicitud es recibida por el servidor, que responde a la solicitud del usuario y le proporciona al usuario el servicio de transferencia de archivos solicitado.
![[Pasted image 20240805135304.png]]