Disciplina que contemplando instalación, seguridad de servidor (SOS). Presenta un contenido diversificado, la base práctica del área de configuración, administración de los [[Sistemas operativos]] (SO) de servidor (SOS).

> [!help] ¿Que es un sistema distribuido?
> Es una colección de componentes de software o hardware separados e independientes llamados nodos, conectados entre sí por medio de una red, y que trabajan juntos de manera coherente al coordinarse y comunicarse a través del paso de mensajes o eventos para cumplir un objetivo final.
> Las complejidad del sistema permanecen oculta para el usuario final, ya sea un ser humano o una computadora. De manera que aparece a sus usuarios como una sola computadora.

[[Seguridad en Sistemas distribuidos]]

En ausencia de un reloj compartido, se logra un reloj lógico mediante sincronización y coordinación.
**Uso compartido de recursos:** un sistema distribuido puede compartir hardware, software o datos.
**Procesamiento simultáneo:** varias máquinas pueden procesar la misma función al mismo tiempo.
**Escalabilidad:** la capacidad de cómputo y procesamiento se puede escalar según sea necesario cuando se extiende máquinas adicionales.

### Computación distribuida:
Es la construcción y establecimiento de modelos
computacionales para los sistemas distribuidos, un
ejemplo de estos es lo que hoy conocemos como [[Cloud computing]] o Computación en la nube.

Ejemplos: Paas, Iaas, Serverless, etc

### Sistemas distribuidos:
Existen varios criterios para clasificar los sistemas
distribuidos, entre ellos:
De acuerdo al Acoplamiento y escala tenemos
- Cluster computing
- Grid computing
De acuerdo al Modelo de arquitectura tenemos
- Layered model
- Object—based Model
- Data-Centered Model
- Event-Based Model (uno de los más comunes)

### Ventajas y desventajas de los sistemas distribuidos

CUADROOOOOOOOOOOOOOOOOOOOOOOOOOOOOOO

VENTAJAS
- Confiabilidad
- Escalabilidad
- Tolerancia a fallos (fault tolerance)
- Rendimiento agrandado
DESVENTAJAS
- Dificultad de detectar fallas
- Redundancia— Un asunto a tener en cuenta
- Inconsistencia
- Cuellos de botella de rendimiento (performance)

![[Pasted image 20240701133343.png]]

![[Pasted image 20240701133739.png]]

### EXPLICACIONES:
Un sistemas operativo de servidor (SOS) tiene la función de atender las solicitudes provenientes de varias estaciones, ya sean remotas o locales, gestionando varias tareas de diferente tipo al mismo tiempo.
Un servidor proporciona varios servicios a la rede a la que está conectado, tales como: base de datos, proxy de internet, almacenamiento de archivos, firewall y muchos otros.

Un entorno cliente-servidor es un modelo de arquitectura de red en el que las tareas se distribuyen entre dos tipos de programas: **clientes** y **servidores**. Los clientes inician las solicitudes a los servidores, que a su vez responden proporcionando los datos o servicios solicitados.

Para tales funciones, el SOS necesita de más recursos que un S.O de escritorio como:
- + memorias;
- > velocidad de acceso al disco e memoria;
- + espacio en disco de almacenamiento;
- > velocidad de procesamiento;

Importante: El SOS consiste en un ambiente que, además de las funciones básicas de un S.O de escritorio, también debe responder a las solicitudes provenientes de otras estaciones.

### FUNCIONAMIENTO
**S.O CLIENTE:** Existe un proceso cliente que envía diversas solicitudes a un
proceso servidor.
- Iniciar solicitudes;
- Esperar respuestas;
- Recibir respuestas;
- Conectarse a un número limitado de servidores simultáneamente;
- Interactuar directamente con los usuarios finales;
- Usar los recursos de la red.

**S.O SERVIDOR:** Retorna al cliente los resultados de las solicitudes realizadas.
- Esperar por las solicitudes de los clientes;
- Responder a los datos solicitados por los clientes;
- Comunicarse con otros servidores;
- Proporcionar recursos a la red;

> [!tip]
> Los procesos son ejecutados bajo la gestión del sistema operativo, que también coordina sus recursos.

### COMUNICACION EN EL MODELO CLIENTE-SERVIDOR:

- Uso de [[sockets]] para el paso de mensajes.
- Llamadas a Procedimientos Remotos (RPC Produre Calls).
- Invocación a Procedimientos Remotos RMI Method Invocation).

### Arquitectura cliente-servidor

CUADROOOOOOOOOOOOOOOOOO

VENTAJAS DEL MODELO
**Centralización de los recursos:** el servidor debe gestionar los recursos comunes a todos los
usuarios;
**Mejor seguridad:** la concentración de datos en un único punto facilita la gestión y compartición adecuada;
**Administración:** a través del servidor es posible administrar toda la red;
**Escalabilidad e paralelismo:** es posible agregar o quitar clientes de una manera sencilla y interrumpir el funcionamiento de la red;

DESVENTAJAS DEL MODELO

**Costo:** los costos pueden ser elevados, dependiendo del servicio;
**Confiabilidad:** el servidor es el único responsable por mantener funcionamiento. En caso de que ocurran problemas en el servidor, los servicios dejaran de ser proporcionados;
**Mantenimiento:** las diversas partes involucradas no siempre funcionan bien juntas;
**Gestión:** la gestión del ambiente es compleja.

###### Intercambio de recursos;
- Administración y gestión;
- Siempre en funcionamiento;
- Sistema de seguridad rígido;
- Funciones de protección de la memoria;
- Mecanismos avanzados de respaldo para evitar Ia pérdida de datos en caso de fallas.

###### La elección de un SOS se basa en varios factores, tales como:
- Costo;
- Requisitos del hardware del sistema;
- Aplicaciones que se ejecutarán
- Eficiencia del hardware y del sistema;
- Escalabilidad;
- Estabilidad;
- Seguridad.