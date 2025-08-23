## Difusión de una Película de Netflix en Tres Redes de 550 Hosts

La transmisión de una película de alta definición a 550 hosts en cada una de las tres redes presenta varios problemas significativos relacionados principalmente con la capacidad de la red y la gestión del tráfico. El ancho de banda, que es la cantidad de datos que se pueden transmitir a través de una red en un período de tiempo dado, se vería considerablemente exigido. Una película de alta calidad requiere una gran cantidad de datos, y multiplicar esto por 550 usuarios por red, y luego por tres redes, resulta en un volumen de tráfico masivo.

Esta afluencia de datos puede llevar a la saturación del ancho de banda, donde la demanda de datos excede la capacidad de la red para manejarla. En esencia, la red se convierte en un cuello de botella, ya que intenta procesar y entregar una cantidad excesiva de información simultáneamente. Esta saturación tiene un efecto dominó en todo el rendimiento de la red.

Uno de los problemas más inmediatos es la congestión de la red. Cuando demasiados dispositivos intentan enviar datos a través de la misma red al mismo tiempo, se produce una congestión. Esta congestión es similar a un embotellamiento de tráfico en una carretera; los paquetes de datos se retrasan, se ponen en cola y, en algunos casos, se descartan por completo. La congestión se manifiesta en una mayor latencia, que es el retraso entre el momento en que se envía un paquete de datos y el momento en que se recibe. Los usuarios experimentan esto como tiempos de carga más lentos, retrasos en la transmisión de video y demoras generales en la capacidad de respuesta de la red. Además, la congestión puede provocar la pérdida de paquetes, lo que obliga a retransmitir los datos y exacerba aún más el problema.

El rendimiento general de la red se degrada significativamente. Las aplicaciones y los servicios que dependen de la red, como la navegación web, el correo electrónico y la transferencia de archivos, funcionan a velocidades notablemente reducidas. Los usuarios pueden tener dificultades para acceder a sitios web, enviar y recibir correos electrónicos o descargar archivos en un tiempo razonable. La experiencia del usuario se ve comprometida, y la productividad puede verse afectada.

La calidad de servicio (QoS) es otro aspecto crítico que se ve afectado. QoS se refiere a la capacidad de una red para priorizar ciertos tipos de tráfico sobre otros. Por ejemplo, las videollamadas y la transmisión de video en tiempo real requieren una latencia baja y un ancho de banda constante para garantizar una experiencia fluida e ininterrumpida. En una red congestionada, es difícil priorizar este tipo de tráfico, lo que lleva a interrupciones, fluctuaciones y una mala calidad de imagen y sonido. Otros tipos de tráfico, como el correo electrónico y la navegación web, pueden considerarse menos sensibles al tiempo y, por lo tanto, pueden tener una prioridad más baja. Sin embargo, incluso estos servicios se ven afectados por la congestión general de la red.

Los dispositivos de red, como routers y switches, desempeñan un papel crucial en la gestión del tráfico de la red. Estos dispositivos tienen una capacidad de procesamiento y memoria finita. Cuando se enfrentan a un gran volumen de tráfico, pueden sobrecargarse. Esta sobrecarga puede resultar en un rendimiento lento, ya que los dispositivos luchan por procesar y reenviar paquetes de datos de manera eficiente. En casos extremos, la sobrecarga puede provocar fallos en los dispositivos, lo que interrumpe aún más la red y potencialmente provoca un tiempo de inactividad.

Es importante tener en cuenta que el impacto de la transmisión de la película no se limita a los usuarios que la están viendo. Todos los usuarios de la red se ven afectados por la lentitud de la red y la congestión. Esto incluye a aquellos que intentan realizar tareas simples como enviar un correo electrónico o navegar por un sitio web. Los recursos de red compartidos significan que las acciones de un grupo de usuarios pueden afectar el rendimiento de la red para todos los demás.

## Subredes para la Empresa X

Para abordar las necesidades de red de la Empresa X, es necesario implementar una estrategia de subredes. La subredes es el proceso de dividir una red más grande en varias redes más pequeñas e interconectadas, conocidas como subredes. El objetivo principal de la subredes es optimizar la asignación de direcciones IP, mejorar la seguridad de la red y mejorar la eficiencia general de la red.

La Empresa X tiene varios departamentos, cada uno con requisitos de red distintos. Estos departamentos incluyen Dirección General, Dirección de Administración, Dirección de Producción, Departamento Comercial y Dirección de Calidad. El número de hosts (dispositivos) en cada departamento varía, y es crucial tener esto en cuenta al diseñar la estrategia de subredes.

La Dirección General tiene 4 hosts, la Dirección de Administración tiene 20 hosts, la Dirección de Producción tiene 12 hosts, el Departamento Comercial tiene 24 hosts y la Dirección de Calidad tiene 2 hosts. Dado que el número de hosts en cada departamento es relativamente pequeño, se puede utilizar una máscara de subred que proporcione suficientes subredes sin desperdiciar una cantidad excesiva de direcciones IP.

Una máscara de subred /27 (255.255.255.224) es una opción adecuada para este escenario. Esta máscara divide un espacio de direcciones Clase C en subredes de 32 direcciones IP cada una. De estas 32 direcciones, 30 están disponibles para los hosts, ya que dos direcciones están reservadas para la dirección de red y la dirección de broadcast.

La estrategia de subredes da como resultado la siguiente asignación de subredes:

- Subred 1 (Dirección General): Esta subred está asignada a la Dirección General y tiene un rango de direcciones IP de 192.168.0.0/27. El rango de direcciones IP utilizables para los hosts en este departamento es 192.168.0.1 a 192.168.0.30, y la dirección de broadcast es 192.168.0.31.
    
- Subred 2 (Dirección de Administración): La Dirección de Administración está asignada a esta subred, que tiene un rango de direcciones IP de 192.168.0.32/27. El rango de direcciones IP utilizables para los hosts es 192.168.0.33 a 192.168.0.62, y la dirección de broadcast es 192.168.0.63.
    
- Subred 3 (Dirección de Producción): Esta subred está asignada a la Dirección de Producción y tiene un rango de direcciones IP de 192.168.0.64/27. El rango de direcciones IP utilizables para los hosts es 192.168.0.65 a 192.168.0.94, y la dirección de broadcast es 192.168.0.95.
    
- Subred 4 (Departamento Comercial): El Departamento Comercial está asignado a esta subred, que tiene un rango de direcciones IP de 192.168.0.96/27. El rango de direcciones IP utilizables para los hosts es 192.168.0.97 a 192.168.0.126, y la dirección de broadcast es 192.168.0.127.
    
- Subred 5 (Dirección de Calidad): Esta subred está asignada a la Dirección de Calidad y tiene un rango de direcciones IP de 192.168.0.128/27. El rango de direcciones IP utilizables para los hosts es 192.168.0.129 a 192.168.0.158, y la dirección de broadcast es 192.168.0.159.
    

La elección de la máscara de subred /27 se justifica por varias razones. En primer lugar, proporciona suficientes direcciones IP para cada departamento, incluso para el Departamento Comercial, que tiene el mayor número de hosts. En segundo lugar, crea suficientes subredes para acomodar todos los departamentos de la empresa y permite futuras expansiones de la red. En tercer lugar, la subredes mejora la seguridad de la red al aislar el tráfico entre departamentos. Esto significa que una violación de seguridad en un departamento tiene menos probabilidades de afectar a otros departamentos. En cuarto lugar, la subredes mejora el rendimiento de la red al reducir el tráfico de broadcast. El tráfico de broadcast es un tipo de tráfico de red que se transmite a todos los dispositivos en una red. Al dividir la red en subredes más pequeñas, el tráfico de broadcast se contiene dentro de cada subred, lo que reduce la cantidad de tráfico innecesario que deben procesar los dispositivos. Por último, la subredes simplifica la administración de la red al dividirla en segmentos más pequeños y manejables. Esto facilita la resolución de problemas de red, la configuración de nuevos dispositivos y la implementación de políticas de red.

## Rangos de Direcciones y Número de Bits por Clase

Las direcciones IP se dividen en cinco clases principales: Clase A, Clase B, Clase C, Clase D y Clase E. Cada clase tiene un rango específico de direcciones IP y una máscara de subred predeterminada. La clase de una dirección IP está determinada por sus primeros bits.

- Clase A: Las direcciones de Clase A tienen un primer bit de 0. El rango de direcciones IP para la Clase A es 0.0.0.0 a 127.255.255.255. La máscara de subred predeterminada para la Clase A es /8, lo que significa que los primeros 8 bits de la dirección IP se utilizan para la porción de red, y los 24 bits restantes se utilizan para la porción de host.
    
- Clase B: Las direcciones de Clase B tienen los primeros bits 10. El rango de direcciones IP para la Clase B es 128.0.0.0 a 191.255.255.255. La máscara de subred predeterminada para la Clase B es /16, lo que significa que los primeros 16 bits de la dirección IP se utilizan para la porción de red, y los 16 bits restantes se utilizan para la porción de host.
    
- Clase C: Las direcciones de Clase C tienen los primeros bits 110. El rango de direcciones IP para la Clase C es 192.0.0.0 a 223.255.255.255. La máscara de subred predeterminada para la Clase C es /24, lo que significa que los primeros 24 bits de la dirección IP se utilizan para la porción de red, y los 8 bits restantes se utilizan para la porción de host.
    
- Clase D: Las direcciones de Clase D tienen los primeros bits 1110. El rango de direcciones IP para la Clase D es 224.0.0.0 a 239.255.255.255. Las direcciones de Clase D se utilizan para multicast, que es un tipo de comunicación en red en el que un solo paquete se transmite a un grupo de dispositivos.
    
- Clase E: Las direcciones de Clase E tienen los primeros bits 1111. El rango de direcciones IP para la Clase E es 240.0.0.0 a 255.255.255.255. Las direcciones de Clase E están reservadas para experimentación e investigación.
    

## Subredes de la Dirección 222.222.22.0/24

Dado que tenemos la dirección de red 222.222.22.0/24 y el requisito de crear 16 subredes, es necesario tomar prestados bits de la porción de host de la dirección IP. La máscara /24 indica que los primeros 24 bits de la dirección IP se utilizan para la porción de red, y los 8 bits restantes se utilizan para la porción de host.

Para crear 16 subredes, necesitamos 4 bits de host (2^4 = 16). Esto da como resultado una nueva máscara de subred de /28. Los primeros 28 bits de la dirección IP se utilizan para la porción de red, y los 4 bits restantes se utilizan para la porción de host.

La máscara /28 divide el espacio de direcciones original en 16 subredes más pequeñas. Cada subred tiene 4 bits para la porción de host, lo que permite 2^4 = 16 direcciones IP por subred. Sin embargo, es importante tener en cuenta que no todas estas direcciones están disponibles para los hosts. La primera dirección en cada subred está reservada para la dirección de red, y la última dirección está reservada para la dirección de broadcast. Por lo tanto, el número de direcciones IP utilizables por subred es 16 - 2 = 14.

|   |   |   |   |
|---|---|---|---|
|Subred|Dirección de Red|Rango de Direcciones Utilizables|Dirección de Broadcast|
|1|222.222.22.0/28|222.222.22.1 - 222.222.22.14|222.222.22.15|
|2|222.222.22.16/28|222.222.22.17 - 222.222.22.30|222.222.22.31|
|3|222.222.22.32/28|222.222.22.33 - 222.222.22.46|222.222.22.47|
|4|222.222.22.48/28|222.222.22.49 - 222.222.22.62|222.222.22.63|
|5|222.222.22.64/28|222.222.22.65 - 222.222.22.78|222.222.22.79|
|6|222.222.22.80/28|222.222.22.81 - 222.222.22.94|222.222.22.95|
|7|222.222.22.96/28|222.222.22.97 - 222.222.22.110|222.222.22.111|
|8|222.222.22.112/28|222.222.22.113 - 222.222.22.126|222.222.22.127|
|9|222.222.22.128/28|222.222.22.129 - 222.222.22.142|222.222.22.143|
|10|222.222.22.144/28|222.222.22.145 - 222.222.22.158|222.222.22.159|
|11|222.222.22.160/28|222.222.22.161 - 222.222.22.174|222.222.22.175|
|12|222.222.22.176/28|222.222.22.177 - 222.222.22.190|222.222.22.191|
|13|222.222.22.192/28|222.222.22.193 - 222.222.22.206|222.222.22.207|
|14|222.222.22.208/28|222.222.22.209 - 222.222.22.222|222.222.22.223|
|15|222.222.22.224/28|222.222.22.225 - 222.222.22.238|222.222.22.239|
|16|222.222.22.240/28|222.222.22.241 - 222.222.22.254|222.222.22.255|

  