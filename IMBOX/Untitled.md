## Modelo OSI

El Modelo OSI (Open Systems Interconnection) es un modelo conceptual que estandariza las funciones de telecomunicaciones y computación en un sistema de transmisión, permitiendo la interoperabilidad de diversos sistemas de comunicación. Divide el proceso de comunicación en siete capas abstractas, cada una con funciones específicas:

Capa Física (Physical Layer):

Se ocupa de la transmisión y recepción de datos sin procesar a través de un medio físico. Define las características del medio de transmisión (cables, fibra óptica, ondas de radio), los niveles de voltaje, la sincronización de bits y las velocidades de transmisión de datos. Unidades de datos: bits.

Capa de Enlace de Datos (Data Link Layer):

Proporciona la transferencia de datos entre nodos adyacentes en una red. Divide los datos en tramas (frames) y se ocupa del direccionamiento físico (direcciones MAC), la detección y corrección de errores, y el control de flujo. Subcapas: Control de Enlace Lógico (LLC) y Control de Acceso al Medio (MAC). Unidades de datos: tramas.

Capa de Red (Network Layer):

Es responsable del enrutamiento de paquetes de datos a través de una red. Utiliza direcciones lógicas (direcciones IP) para identificar dispositivos y determinar la mejor ruta para la transferencia de datos. Protocolos clave: IP, ICMP, ARP. Unidades de datos: paquetes.

Capa de Transporte (Transport Layer):

Proporciona servicios de transferencia de datos confiables o no confiables entre procesos que se ejecutan en diferentes dispositivos. Se ocupa de la segmentación de datos, el control de flujo, el control de errores y la multiplexación/demultiplexación de aplicaciones. Protocolos clave: TCP (confiable), UDP (no confiable). Unidades de datos: segmentos (TCP), datagramas (UDP).

Capa de Sesión (Session Layer):

Gestiona y coordina las comunicaciones entre aplicaciones. Establece, gestiona y finaliza sesiones entre aplicaciones, controlando el diálogo (quién transmite y cuándo), la sincronización y el establecimiento de puntos de control para la recuperación de errores.

Capa de Presentación (Presentation Layer):

Se ocupa de la representación de los datos. Realiza funciones como la conversión de formatos de datos (por ejemplo, ASCII a EBCDIC), la compresión de datos, el cifrado y el descifrado. Asegura que los datos sean compatibles entre diferentes sistemas.

Capa de Aplicación (Application Layer):

Proporciona interfaces para que las aplicaciones de red accedan a los servicios de la red. Ofrece servicios de red directamente a las aplicaciones de usuario, como correo electrónico (SMTP), transferencia de archivos (FTP), acceso web (HTTP) y resolución de nombres de dominio (DNS). Protocolos clave: HTTP, FTP, SMTP, DNS, DHCP. Unidades de datos: datos.

## Analogía del Modelo OSI en 1990

Imaginemos el envío de una carta en 1990, antes de la omnipresencia de Internet como la conocemos hoy:

- **Capa 7 (Aplicación):** Tú, escribiendo la carta con un procesador de textos como WordPerfect o Microsoft Word. La aplicación (WordPerfect) te permite crear el mensaje.
    
- **Capa 6 (Presentación):** Imprimes la carta. La carta está ahora en un formato estandarizado (papel) que el destinatario puede leer, y podrías haber usado un sobre especial o cifrado (aunque menos común en 1990 para el correo regular).
    
- **Capa 5 (Sesión):** Abres un "canal de comunicación" con el sistema postal al preparar tu envío. Es el acto de preparar la carta para el envío.
    
- **Capa 4 (Transporte):** Pones la carta en un sobre, escribes la dirección, y pones una estampilla. Esto asegura que la carta llegue a su destino, y si es certificada, tienes acuse de recibo (similar a TCP). Si usas el correo regular, es menos confiable (similar a UDP).
    
- **Capa 3 (Red):** El sistema de enrutamiento del correo postal (oficinas de correos regionales, etc.) determina la ruta para que tu carta llegue a la oficina de correos correcta cerca del destinatario. Se usa el código postal para encaminar la carta.
    
- **Capa 2 (Enlace de Datos):** El cartero que recoge tu carta y la lleva a la oficina de correos local, y el cartero que la entrega al destinatario. Es la entrega física de un punto al siguiente.
    
- **Capa 1 (Física):** El papel de la carta, el sobre, el camión de correo, las calles por las que viaja el cartero. Es el medio físico que transporta la información.
    

## Capa del Modelo OSI y Direcciones de Red

La dirección de red se encuentra en la **Capa 3: Capa de Red**. Específicamente, las direcciones IP se utilizan en esta capa para identificar redes y dispositivos.

## Porción de Red y Porción de Host

Para determinar la porción de red y la porción de host de una dirección IP, necesitamos conocer la máscara de subred o la notación CIDR. Asumiré máscaras de subred predeterminadas para las clases de direcciones dadas:

- **192.168.10.5:**
    
    - Clase C (máscara predeterminada: 255.255.255.0 o /24)
        
    - Porción de red: 192.168.10
        
    - Porción de host: 5
        
- **10.0.0.8:**
    
    - Clase A (máscara predeterminada: 255.0.0.0 o /8)
        
    - Porción de red: 10
        
    - Porción de host: 0.0.8
        
- **172.16.24.200:**
    
    - Clase B (máscara predeterminada: 255.255.0.0 o /16)
        
    - Porción de red: 172.16
        
    - Porción de host: 24.200