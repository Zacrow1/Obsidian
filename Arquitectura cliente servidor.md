# Arquitectura Cliente Servidor

Cada computadora conectada a una red comúnmente es denominada como host.
Los servidores son computadoras que brindan información a los hosts.
Los clientes son computadoras que envían solicitudes a los servidores para recuperar cierta información requerida, ej: email.

Dispositivos intermediarios
Este tipo de dispositivo interconecta terminales en una red, por ej: Routers, switches, puntos de acceso inalámbricos, etc.
Tareas que realizan los dispositivos intermediarios:
- En caso de error generan y re transmiten los datos.
- Almacenar información acerca de las rutas que existen a través de la red y la internet.
- En caso de fallas de comunicación estos notifican a otros dispositivos.
- Dirigir los datos a lo largo de rutas alternativas cuando hay una falla en el enlace.
- De acuerdo a las prioridades clasifican y dirigen los mensajes (datagramas)
- En función a los parámetros de seguridad denegar flujo de datos.

Se utiliza un medio para la comunicación a través de una red, este proporcionara el canal por el cual viaja el mensaje desde el origen hacia el destino final.

Hoy en día las redes normalmente utilizan tres tipos de medios para interconectar los dispositivos y transmitir los datos.
- Hilos metálicos dentro de cables: los datos se codifican en impulsos eléctricos.
- Cable de fibra óptica: los datos se codifican como pulsos de luz.
- Transmisión inalámbrica: los datos se codifican con longitudes de onda.

## términos importantes:
- Tarjeta de interfaz de red: NIC o adaptador de LAN, proporciona la conexión física a la red en la computadora (u otro tipo de dispositivo). Los medios que realizan la conexión del computador al dispositivo de red se conectan directamente a la NIC
- Puerto físico: punto de conexión en un dispositivo de red donde se conectan los medios a una computadora u otro dispositivo de red.
- Interfaz: son puertos especializados en un dispositivo de red, por ejemplo un Router, que se conecta a redes individuales. Los puertos de un router se denominan interfaces de red.