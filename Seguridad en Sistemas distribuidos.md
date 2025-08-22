Venis de:[[Concepto de sistemas distribuidos]]

## Aspectos de la seguridad
- ### Integridad
	- Los datos envidos no son alterados y llegan al destino sin sufrir cambios o perdidas.
- ### Confidencialidad 
	- Los datos no pueden ser obtenidos, leídos e interpretados por terceros.
- ### Autenticidad
	- El emisor y el receptor son quienes dicen ser
- ### Credibilidad
	- Una entidad confiable valida la identidad e integridad de: individuos, organizaciones, dispositivos, sitios web, emails y otros documentos electrónicos involucrados en la comunicación.

## Tipos de ataques de seguridad

Cuando hablamos de ataques en entornos informáticos lo podemos definir como "Cualquier acción que compromete la seguridad de la información y los intereses de un individuo u organizacion".
### Tipos de ataques:
- **Ataques pasivos:** Su objetivo es conocer o hacer uso de información del sistema. No afecta los recursos del sistema, ni modifica los mensajes o datos, pero accede a ellos de forma no autorizada.
- **Ataques activos:** Involucra la modificación o destrucción del flujo de mensajes (datos) o la creación de mensajes (datos) falsos.
* **Control de acceso:** Implementar controles de acceso para restringir el acceso a los recursos del sistema. |

| Característica                      | Ataque pasivo                                                  | Ataque activo                                                                 |
| ----------------------------------- | -------------------------------------------------------------- | ----------------------------------------------------------------------------- |
| Interacción con el sistema objetivo | No modifica los datos ni el sistema objetivo.                  | Modifica los datos o el sistema objetivo.                                     |
| Dificultad                          | Más fácil de realizar.                                         | Más difícil de realizar.                                                      |
| Detección                           | Más difícil de detectar.                                       | Más fácil de detectar.                                                        |
| Impacto                             | Puede robar información.                                       | Puede robar información, interrumpir el servicio o causar daños.              |
| Ejemplos                            | Interceptación, análisis de tráfico, interferencia de señales. | Suplantación de identidad, re-actuación, modificación de mensajes, denegación |
![[Pasted image 20240715125022.png]]![[Pasted image 20240715125052.png]]
### ATAQUES ACTIVOS
![[Pasted image 20240715125245.png]]
![[Pasted image 20240715125408.png]]
![[Pasted image 20240715125505.png]]
![[Pasted image 20240715125626.png]]
![[Pasted image 20240715125943.png]]

### Algoritmos o funciones Hash
Hash es la manera en Ia que nos referimos al resultado de aplicar una función o algoritmo especifico a un dato para obtener otro que lo representa de una forma resumida y cifrada. (También
se suele llama Hash a la propia función o algoritmo y digest o
réSumen al resultado).
Actividad: Invente una forma o algoritmo para cifrar el nombre
"Esteban" a un código numérico de 3 dígitos decimal

### Características de un buen algoritmo Hash:
- Unidireccionalidad: No es posible obtener el dato original aplicando el mismo algoritmo Hash o su inverso si existiera.
- Compresión: El tamaño del valor resultante\después de aplicar el algoritmo Hash al dato, es mucho menor que el tamaño del dato de original.
- Unicidad: No se puede tener el mismo Hash resultante para datos diferentes de partida (Aunque pueden existir "colisiones").
- Tamaño fijo: El hash resultante (digest) tiene longitud fija.
-  Diferencia: Un pequeño cambio en el dato original provoca una gran diferencia en los Hashes de ambos valores.
O Ejemplos de algoritmos Hash: MD5 (roto), SHAI (roto), SHA256 (standard de hoy), SHA512. 

> [!NOTE]
>  Ejecute el comando: echo "Hola mundo" | md5sum) 
>  | md5sum esto encripta el codigoIntegridad con Checksum

#### Checksum
Checksum: Es una forma de verificación de la integridad de los datos: Del lado del emisor se hace la suma binaria de las "palabras"* del mensaje a enviar (checksum). Esta suma es enviada al receptor junto con el mensaje. En el lado del receptor se hace la suma de las palabras del mensaje recibido. Si el complemento a 1 de la suma (en el lado del receptor) más el checksum es igual a 0 entonces Se deduce que el mensaje de origen igual al del destino, o sea que no se degrado ni se modifico la información.
#### Integridad con Hash
La verificación de la integridad con Checksum es deficiente porque no es lo suficientemente
segurapara prevenir los ataques activos como muestran las imágenes

![[Pasted image 20240715133157.png]]
#### Keys
El uso de Keys y Hashes previene, de manera más segura, que los ataques activos atenten
contra la integridad de los datos como muestran las imágenes
![[Pasted image 20240715133336.png]]

# Conlidencialidad con cifrado de datos o "Encryptlon "
Hash es un mecanismo que no permite descifrar el mensaje riginal. El mensaje original debe ser acompañado del Hash con el único propósito es garantizar la integridad del mensaje Si el mensaje se envía en "texto plano", puede estar sujeto a ataques como los que vinos anteriormente. Por esta razón se requieren mecanismos como el cifrado de datos que veremos a continuación.

- La confidencialidad se logra enviando el me aje cifrado o "encriptado" de manera que solo el receptor pueda interpretar o "desencriptar" el mensaje original a partir del mensaje cifrado.
- Los algoritmos que permiten el cifrado se conocen como algoritmos de encriptación muestra el ejemplo.

![[Pasted image 20240715133601.png]]ara garantizar la eficacia de un algoritmo de cifrado este no debe ser simple, es decir, que no debe producir la misma cadena cada vez que envía un mensaje especifico. A continuación se ilustra lo que se conoce como Encriptación basada en llaves o Key based Encryption:
![[Pasted image 20240715133630.png]]
###
existen dos tipos de "keys": Algoritmos de encriptación usando llaves o keys
- encriptación Simétricos: En los que la misma llave o key sirve tanto para encriptar como para desencriptar el mensaje
- Algoritmos de encriptación Asimétricos: No se puede usar la misma llave o "key" que encripto el mensaje para desencriptarlo, debe usarse otra. Estas dos versiones de llaves se conocen como llaves publicas y privadas respectivamente, o "public and private keys" o llaves asimétricas.

![[Pasted image 20240715134106.png]]
Los pares de llaves publica y privada, conocidas como "Asymmetric Key Pairs" permiten no solo encriptar los datos si no también verificar la identidad del emisor; esto es lo que se conoce como firmas digitales (el uso de las llaves asimétricas provee autenticación e
integridad). En la tarea de esta semana podrá investigar cómo se logra esto dos propósitos con el uso de las llaves publicas y privadas.

Existen dos tipos de ataques en particular que originaron la necesidad de la creación de Certificados digitales y Autoridades de Certificación, estos son el phishing y el ataque conocido como man-in-the-midd/e o ataques de intermediario.
El objetivo de los Certificados digitales es el de garantizar que el portador de este documento electrónico es quien dice ser. Las Autoridades de Certificación, por otro lado,
o notarios de fe publica que garantizan la validez y legitimidad de un certificado digital.

- Un certificado digital contiene: La clave publica de la entidad (persona, organización o servicio) País, estado, ciudad, empresa, departamento, propósito, vigencia y correo electrónico.

- Los certificados permiten la Autenticación, Integridad y no-repudio o irrenunciabilidad.

- La Autoridad de Certificación (CA por sus siglas en inglés): Emite, revoca, almacena y distribuye los certificados.

Los protocolos de comunicación en Internet han evolucionado hacia versiones más seguras a través de la implementación de los mecanismos de seguridad que hemos estudiado, algunos ejemplos más sobresalientes son:

![[Pasted image 20240715135908.png]]

#### Firewalls
Además de los mecanismos de seguridad que implementan los protocolos de comunicación en las redes, en los sistemas distribuidos se pueden implementar firewalls, ya sea como parte de los sistema operativos de los servidores, o como servidores o servicios independientes.

Los firewalls permiten estableces reglas sobre que tipo de paquetes se pueden ingresar al sistema que protegen. 

En los sistemas operativos de escritorio y servidor se pueden administrar los firewalls a través de la apertura o cierre de puertos específicos. Esto se verá de forma práctica en la clase de tutoría.