[[1.2 Sistemas Operativos ]]

---

# Semana 5

---
![[Pasted image 20240205121559.png]]
![[Pasted image 20240205121609.png]]
El primer disco comercial
• En 1956, IBM introdujo la 305 RAMAC  (Random Access Method of Accounting and Control), que fue revolucionaria por ser la primera computadora en ofrecer un sistema de almacenamiento en disco magnético integrado. 
• El IBM Model 350 Disk File fue la unidad de disco que acompañaba a la 305 RAMAC.  
• Ofrecía una capacidad total de almacenamiento de alrededor de 5 millones de caracteres de seis bits (aproximadamente 3.75 MB).

### Memoria de estado solido 
  
Memoria no volátil utilizada como un disco duro solid state disks (SSDs)  
• Muchas variaciones tecnológicas Puede ser más fiable que los discos  
duros Más caro por MB  
• Tal vez tenga una vida útil más corta menor capacidad, pero mucho más rápido.
• Los buses pueden ser demasiado lentos -> conectarse directamente a PCI, por ejemplo  
• Sin piezas móviles, por lo que no hay tiempo de búsqueda ni latencia de rotación

### Cinta magnetica
  
- Fue un medio de almacenamiento secundario temprano
	- Evolucionado de carretes abiertos a cartuchos  
- Relativamente permanente y contiene grandes cantidades de datos  
- Tiempo de acceso lento  
- Acceso aleatorio 1000 veces más lento que el disco  
- Se utiliza principalmente para copias de seguridad, almacenamiento de datos de uso poco frecuente, medio de transferencia entre sistemas.
- Mantenido en el carrete y enrollado o rebobinado más allá del cabezal de lectura y escritura.
- Una vez que los datos están bajo la cabeza, las tasas de transferencia son comparables a las del disco 140 MB/seg y más
- Almacenamiento típico de 200 GB a 1,5 TB.

### Disk Attachment
Conexión a la Computadora
• Los dispositivos de almacenamiento se conectan a la computadora a través del bus de Entrada/Salida (E/S).
• Diversos tipos de buses se utilizan para la conexión, como ATA, SATA, USB, Fibre Channel (FC), SCSI, SAS y Firewire.

Comunicación a través de Controladores
- El controlador de host en la computadora utiliza el bus para comunicarse con el controlador de disco integrado en el dispositivo de almacenamiento o en el arreglo de almacenamiento

### Métodos de Conexión al Almacenamiento
Las computadoras acceden al almacenamiento de tres maneras: 
- Host Local 
	• Acceso directo a través de puertos de E/S locales. 
	• Utiliza tecnologías como SATA, PCIe. 
	
- Conexión de Red
	- Acceso a través de la red, como almacenamiento en la nube.
	- Conexiones de Buses de Almacenamiento 
	- Para múltiples dispositivos, se utilizan buses como USB, Firewire y Thunderbolt
### Storage Area Network
- Común en grandes entornos de almacenamiento 
- Múltiples hosts conectados a múltiples arreglos de almacenamiento: flexible
![[Pasted image 20240205122506.png]]

- SAN es una o Más arreglos de almacenamiento Conectado a uno o mas switches Fibre Channel  
- Los hosts también se conectan a los switches.
- Fácil de agregar o quitar almacenamiento, agregue un nuevo host y asígnele almacenamiento.

### Almacenamiento conectado a la red
- El almacenamiento conectado a la red ( NAS ) es un almacenamiento disponible a través de una red en lugar de una conexión local (como un bus) 
- Conexión remota a sistemas de archivos  
- NFS y CIFS son protocolos comunes  
- Implementado a través de llamadas a procedimientos remotos  
(RPC) entre el host y el almacenamiento a través de TCP o UDP en la red IP.  
- iSCSI utiliza una red IP para llevar el protocolo SCSI

![[Pasted image 20240205122820.png]]

### RAID 
- Es un término utilizado en informática, cuyas siglas vienen del inglés «Redundant Array of Independent Disks»  
- Es un proceso utilizado para combinar varios discos duros y que éstos  funcionen de manera coordinada para formar una única unidad lógica en la que almacenar los datos.  
- A nivel empresarial, es muy utilizado a la hora de configurar el almacenamiento de servidores NAS y aplicaciones. Ofrece mayor tolerancia a fallos y más altos niveles de rendimiento que un sólo disco duro o un grupo de discos duros independientes.
#### RAID 0
- Se necesitan mínimo 2 discos. Cuenta la Suma de tamaños de todos los HDD.
- Un RAID 0, conocido como striping, utiliza como mínimo 2 discos y reparte los datos entre ambos.
- Ofrece un mayor rendimiento.
- No debe utilizarse con datos críticos.
- El inconveniente es que no hay redundancia y tolerancia a fallos, por lo que cualquier fallo o avería en uno de los discos conlleva una pérdida total de los datos.
- Recomendado. Si priorizamos el rendimiento del sistema y el acceso a la información (diseño gráfico, en 3D y edición de video), y contamos con un presupuesto muy ajustado. Ofrece un alto rendimiento, especialmente para archivos grandes.
#### RAID 1  
- Se necesitan mínimo 2 discos. En el caso de más unidades, solo cuenta el disco de menor tamaño. 
- Es conocido como “espejo” o “mirroring“. El raid 1 utiliza 2 discos y duplica todos los datos de la primera unidad de forma sincronizada a una segunda unidad de almacenamiento. De esta forma, si el primer disco se estropea, el sistema seguirá  funcionando y trabajando con el segundo disco sin problemas y sin perder datos.  
- Rápida recuperación. 
- Recomendado para servidores de nivel básico.
#### RAID 5 
- Se necesitan mínimo 2 discos. En el caso de más unidades, solo cuenta el disco de menor tamaño. Es conocido como “espejo” o “mirroring“. El raid 1 utiliza 2 
- Se necesitan como mínimo 3 discos (se puede romper un disco sin perder los datos) El espacio disponible en el RAID 5 será de n-1, siendo n el número de discos del raid. Si utilizamos 5 discos de 1TB tendremos: 5 discos – 1 = 4 discos -> 4TB disponibles.
- Suele ser el RAID más usado en servidores, ya que aporta la velocidad y rendimiento del RAID 0 (uso eficiente de la unidad, alto rendimiento en escritura y lectura) y la seguridad del RAID 1 ante la pérdida de datos. 
- El RAID 5 utiliza la paridad para recuperar los datos. Se dividen los datos en bloques en los diferentes discos, de forma qué si hay un fallo en uno de ellos, esa parte de los datos se subsana con los datos almacenados en el resto de los discos, permitiendo al usuario continuar (aunque funciona más lenta) con su trabajo.

¿Cuáles son sus desventajas? 
- Hay un impacto medio de los fallos del disco y la reconstrucción es más larga por la necesidad de volver a calcular la paridad. El rendimiento tanto de lectura como de escritura sufre un gran impacto si la matriz del RAID 5 se ha degradado. Para discos SATA de gran capacidad (de 500GB a 1TB) los tiempos de reconstrucción son muy largos y conllevan una degradación del rendimiento del controlador. 
- Importante: Si se produce un fallo en un segundo disco mientras se está realizando la reconstrucción del primero, se perderán todos los datos.
- Lo recomendamos para un gran número de aplicaciones, pequeños servidores, proporciona alto rendimiento, redundancia de datos y además éste aprovecha mejor el espacio.
#### RAID 6
- Se necesitan como mínimo 4 discos. Puede tolerar dos fallos de discos duros (N-2)
- El Raid6 es similar al Raid 5 e incluye un disco de reserva que entra en funcionamiento una vez que uno de los discos se estropea (en este caso hasta que sustituimos el disco averiado, a todos los efectos tenemos un Raid 5).
- Proporciona por tanto una elevada redundancia de datos y rendimiento de lectura.
- El rendimiento en tareas de escritura es menor que el de Raid 5 debido a los dos cálculos de paridad. Requiere hacer un gasto adicional ya quededicamos dos discos a la paridad, (si tenemos 4 discos de 1TB disponemos sólo de 2TB de espacio ya que los otros 2 TB se dedican a paridad).
- El Raid 6 resulta aconsejable cuando queramos soportar varios fallos de unidades y ofrece una mayor redundancia para la protección de datos.

#### Raid10 (Raid 1+0)
- Se necesitan un mínimo de cuatro discos
- En el RAID 1+0—> Se hace un Raid 1 y sobre ellos un RAID 0
- Se necesitan un mínimo de cuatro o más unidades, por lo que el coste es más elevado que en otras configuraciones.

![[Pasted image 20240205123916.png]]

- Se obtiene un alto rendimiento de lectura (gracias al Raid 0), a la vez que se proporciona tolerancia a los fallos (gracias al Raid1). P.e. si usamos 4 discos, se pueden romper hasta dos sin perder información (N-2), siempre que nos sean del mismo subgrupo.
- Aunque su precio es más elevado, el RAID 10 es ideal para aplicaciones tipo servidores de bases de datos. Proporciona un elevado rendimiento, redundancia de datos completa y una rápida recuperación ante fallos de los discos.

#### Raid 50 (Raid 5+0) 
- Se necesitan como mínimo 6 discos. s*( n-1). con la posibilidad de que se puedan estropear hasta 3 discos sin perder datos.
- En el Raid 5+0—> Se hace un Raid 5 y sobre ellos un RAID 0.
- Con el RAID 50 conseguiremos un volumen muy robusto, un mayor rendimiento de lectura en comparación con la RAID 5 estándar, y un rendimiento de escritura de medio a alto.
- Presenta las mismas desventajas que el RAID 5 (impacto medio ante los fallos de disco y tiempos de reconstrucción más largos al ser necesario volver a calcular la paridad), y un precio más elevado.
#### Raid 60 (Raid 6+0) 
- Se necesitan como mínimo 8 discos, con la posibilidad de que se puedan estropear hasta 4 discos sin perder datos.
- En el Raid 6+0—> Se hace un Raid 6 y sobre ellos un RAID 0.
- Obtenemos un alto rendimiento sobre todo en tareas de lectura.
- Las desventajas son las mismas a las del RAID6 (rendimiento más bajo en escritura debido a los dos cálculos de paridad, y mayor gasto en hardware).

#### Raid 0+1
- Necesitaremos 4 discos duros.
- Los discos se agrupan por parejas para que cada una de éstas forme un RAID 0 y sobre estos 2 bloques montamos un Raid 1. Esta configuración es menos segura que la RAID 10, ya que no tolera dos fallos simultáneos.

#### Hot Swap, intercambio de discos
- A la hora de configurar nuestro servidor hay que evaluar el impacto que tiene una posible parada de nuestros sistemas. Por ello, recomendamos incluir los elementos críticos del hardware por duplicado. Los más importantes con: 
	- Fuentes de alimentación y ventiladores redundantes
	- Hot Swap para intercambio en caliente de discos. Muy importante, ya que nos permitirá sustituir el disco averiado por uno nuevo, sin necesidad de desconectar o apagar el servidor, para luego poder reconstruir la información.

#### Controladora RAID
- Una controladora RAID es una tarjeta de hardware o una aplicación de software que se utiliza con el objetivo de gestionar varios discos duros en un mismo servidor.
- La controladora RAID puede darse por software o por hardware. Nuestra experiencia nos dice que es más recomendable escoger las controladoras por hardware, ya que son más fiables y ofrecen mayores niveles de rendimiento. 

#### Raid por software vs Raid por hardware 
- Un sistema RAID puede ser controlado por hardware o por software, y aquí es donde también existe diferencia tanto de funcionamiento como de rendimiento. Como ahora veremos cada sistema tiene sus pros y contras.
- ##### **RAID por software** 
	- Los discos se conectan a la placa o a una controladora, y es el procesador y el sistema operativo quienes hacen las operaciones necesarias para controlar el RAID y los discos.
	- Ventajas. Es fácilmente ampliable con la cantidad de discos que se necesiten, realmente la única limitación es la que ofrezca la placa base. También es más fácil de configurar.
	- Inconvenientes. Para aquellos RAID que necesiten más recursos, el rendimiento general del sistema puede verse afectado. Además en el caso de que se degrade el RAID, es más complicado volver a recuperarlo y se puede perder información. 
- ##### RAID por hardware
	- Los discos se conectan a una controladora RAID que es la encargada de realizar todas las operaciones de control del RAID y los discos. 
	- Ventajas 
		- El RAID por hardware es más fiable que el RAID por software ya que es más independiente del resto de componentes.
		- Ofrece un mayor rendimiento, que sobre todo se notará en RAID 5 y RAID 6 donde se realizan operaciones de paridad y se consumen más recursos.
	- Inconvenientes 
		- Es necesario realizar actualizaciones del firmware. 
		- Puede haber incompatibilidades del hardware con la placa base del servidor o que no existan drivers apropiados —> por ello aconsejamos que tarjeta y servidor sean del mismo fabricante (IBM, Dell, HP).
		- Dependiendo del modelo de tarjeta que escojamos, será compatible con un determinado hardware y soportará determinados niveles de RAID.

### Qué es virtualización
- La virtualización es una tecnología que permite crear versiones virtuales de recursos físicos, como servidores, dispositivos de almacenamiento, redes y dispositivos de entrada/salida. Se utiliza para optimizar el uso de los recursos físicos, mejorar la eficiencia, facilitar la administración y proporcionar aislamiento entre diferentes sistemas operativos y aplicaciones.
 
#### Tipos de virtualización
- Virtualización de servidores
- Virtualización de almacenamiento
- Virtualización de red
- Virtualización de escritorio
- Virtualización de aplicaciones
- Virtualización de datos

#### Virtualización Completa
- Tecnología que permite a un software (hipervisor) emular completamente el hardware de una computadora, creando un entorno en el que los sistemas operativos pueden ejecutarse como si estuvieran en hardware físico real, sinmodificaciones.
- Características:
	- Independencia del SO: Capacidad para ejecutar cualquier sistema operativo sin necesidad de modificaciones.
	- Aislamiento completo: Cada máquina virtual es independiente y aislada de las demás.
	- Flexibilidad: Fácil migración de VMs entre hosts físicos.
- Usos Comunes:
	- Entornos de desarrollo y pruebas.
	- Consolidación de servidores. 
	- Simulación de entornos de hardware variados.
#### Paravirtualización
- Método de virtualización en el que el sistema operativo huésped es modificado para trabajar en conjunto con el hipervisor, mejorando la eficiencia y el rendimiento al reducir la sobrecarga de la emulación.
- Características:
	- Conciencia del entorno virtualizado: Los SOs huéspedes están optimizados para un hipervisor específico.
	- Menor sobrecarga: Interacción directa con el hipervisor reduce la necesidad de emulación de hardware.
	- Mejor rendimiento: Optimizaciones específicas para entornos virtualizados mejoran la velocidad y eficiencia.
- Usos Comunes:
	- Optimización de recursos en centros de datos.
	- Ambientes de hosting de alta densidad.
	- Escenarios donde se prioriza el rendimiento sobre la flexibilidad.
#### Hipervisores en la Virtualización
- Qué es un Hipervisor
	- Software, firmware o hardware que crea y gestiona máquinas virtuales (VMs).
	- Proporciona una capa de abstracción entre el hardware físico y los sistemas operativos virtuales.
	- Permite la ejecución simultánea de múltiples sistemas operativos en un solo sistema físico.
#### Tipos de Hipervisores
- Tipo 1 (Bare Metal)
	- Se ejecutan directamente en el hardware del host.
	- Ofrecen mejor rendimiento y seguridad.
	
	- Ejemplos: VMware ESXi, Microsoft Hyper-V, Xen, KVM.
- Tipo 2 (Alojados)
	- Se ejecutan sobre un sistema operativo existente. 
	- Fáciles de instalar y usar, ideales para desarrollo y pruebas.
	
	- Ejemplos: VMware Workstation, Oracle VM VirtualBox, Parallels Desktop.
#### Ventajas de la Virtualización
- Consolidación de servidores
- Obtener los recursos necesarios con medios existentes
- Centros de tolerancia a Fallos
- Alargar la vida de entornos antiguos
- Entornos de prueba y desarrollo flexibles
- Virtualización de puestos de trabajo