---
materia: "[[2.4 Redes de computadoras]]"
tags:
  - universidad
fecha_inicio: 2025-03-03
estado: '"foro":"pending","tarea":"done","lab":"pending","quiz":"pending"'
breadcrumbs: "[[2.4 Redes de computadoras]]"
---
```button
name 🏠 Volver a Materia
type command
action Obsidian: Open file
params 2.4 Redes de computadoras
color purple
```

TEMAS
[[Arquitectura cliente servidor]]

# Semana 1 - 2.4 Redes de computadoras

## 🎯 Objetivos
- [ ] #foro Completar foro sobre [[{{TEMA}}]] 📅 2025-03-06
- [x] #tarea Entregar T1-S1-CN1 📅 2025-03-17 ✅ 2025-03-03
- [ ] #lab Finalizar laboratorio 📅 2025-03-10

---

## 💬 Foro
> [!question] {{TITULO_PREGUNTA}}
> {{CONTENIDO_PREGUNTA}}

**Mi Respuesta:**  
<% tp.file.cursor() %>

---

## 📋 Tarea
```tasks
not done
path includes 2.4 Redes de computadoras
tags include #tarea
```

1. Describa cómo funciona la Arquitectura Cliente-Servidor, cuales son sus ventajas y desventajas, que elementos son necesarios para esta arquitectura?
2.  ¿Podría su celular funcionar como Servidor? Justifique su respuesta dando ejemplos.
3. ¿Qué diferencias existen entre un hub, switch y router? También describa cómo funciona cada uno de los dispositivos mencionados. 
4. Haga un listado de los dispositivos que puedan formar parte de una red LAN y mencione qué características/requisitos deberían cumplir estos dispositivos.

### **1. Arquitectura Cliente-Servidor**

En este modelo, existen roles claramente definidos por un lado tenemos el **Cliente** que es quien solicita servicios o recursos que pueden ser un navegador web, app móvil por otro lado tenemos el **Servidor** es el proveedor de los recursos o servicios solicitados como un servidor web o servidor de correo como algunos ejemplos.

El servidor deberá exponer un mecanismo que permite a los clientes conectarse conectarse, por lo general es **TCP/IP** (Cuando los datos llegan al destino, TCP/IP los recorre en orden inverso para volver a ensamblarlos.) lo que proporciona una comunicación continua y bidireccional. En esta arquitectura el cliente no sirve para absolutamente nada si el servidor no está disponible, mientras que el servidor por sí solo no tendría motivo de ser, pues no habría nadie que lo utilice. En este sentido, las dos partes son mutuamente dependientes, pues una sin la otra no tendría motivo de ser.

Es considerada una arquitectura distribuida debido a que el servidor y el cliente se encuentran distribuidos en diferentes equipos (aunque podrían estar en la misma máquina) y se comunican únicamente por medio de la RED o Internet.

La idea central de separar al cliente del servidor radica en la idea de centralizar la información y la separación de responsabilidades, por una parte, el servidor será la única entidad que tendrá acceso a los datos y los servirá solo a los clientes del cual el confía, y de esta forma, protegemos la información y la lógica detrás del procesamiento de los datos, además, el servidor puede atender simultáneamente a varios clientes, por lo que suele ser instalado en un equipo con muchos recursos. Por otro lado, el cliente suele ser instalado en computadoras con bajos recursos, pues desde allí no se procesa nada, simplemente actúa como un visor de los datos y delega las operaciones pesadas al servidor.

Es normal tener 3 artefactos, el Cliente, el Servidor y una tercera librería que contiene Objetos comunes entre el servidor y el cliente, esta librería tiene por lo general los Objetos de Entidad, DTO, interfaces y clases base que se usan para compartir la información, es decir, objetos que se utilizan en las dos aplicaciones y se separan para no repetir código (Principio DRY – Don’t repeat yourself), sin embargo, este tercer componente no es obligatorio que exista, sobre todo si el cliente y el servidor utilizan tecnologías diferentes o son implementados con diferentes proveedores.

![[Pasted image 20250303191833.png]]

#### Ventajas
- Centralización: El servidor funcionara como única fuente de la verdad, lo que impide que los clientes conserven información desactualizada.
- Seguridad: El servidor por lo general está protegido por firewall o subredes que impiden que los atacantes pueden acceder a la base de datos o los recursos sin pasar por el servidor.
- Fácil de instalar (cliente): El cliente es por lo general una aplicación simple que no tiene dependencias, por lo que es muy fácil de instalar.
- Separación de responsabilidades: La arquitectura cliente-servidor permite implementar la lógica de negocio de forma separada del cliente.
- Portabilidad: Una de las ventajas de tener dos aplicaciones es que podemos desarrollar cada parte para correr en diferentes plataformas, por ejemplo, el servidor solo en Linux, mientras que el cliente podría ser multiplataforma.
#### Desventajas
- Actualizaciones (clientes): Una de las complicaciones es gestionar las actualizaciones en los clientes, pues puede haber muchos terminales con el cliente instalado y tenemos que asegurar que todas sean actualizadas cuando salga una nueva versión.
- Concurrencia: Una cantidad no esperada de usuarios concurrentes puede ser un problema para el servidor, quien tendrá que atender todas las peticiones de forma simultánea, aunque se puede mitigar con una estrategia de escalamiento, siempre será un problema que tendremos que tener presente.
- Todo o nada: Si el servidor se cae, todos los clientes quedarán totalmente inoperables.
- Protocolos de bajo nivel: Los protocolos más utilizados para establecer comunicación entre el cliente y el servidor suelen ser de bajo nivel, como Sockets, HTTP, RPC, etc. Lo que puede implicar un reto para los desarrolladores.
- Depuración: Es difícil analizar un error, pues los clientes están distribuidos en diferentes máquinas, incluso, equipos a los cuales no tenemos acceso, lo que hace complicado recopilar la traza del error.

---

### **2. ¿Puede un celular funcionar como servidor?**

Si, podes configurar un servidor web en cualquier smartphone moderno (o incluso antiguo) con unas sencillas manipulaciones. El uso del sitio web como plataforma móvil universal permite el uso de aplicaciones P2P (peer to peer), como mensajería y almacenamiento de archivos. Además, el sitio web actúa como una tarjeta de presentación digital que te identifica dentro de una red P2P que funciona independientemente de Internet. 
Esto se puede realizar usando Termux que es un emulador de Linux para Android tiene limitaciones Batería, RAM y CPU no están diseñados para cargas prolongadas, La IP pública suele ser dinámica (requiere servicios como _No-IP_ para acceder desde internet) y cuenta con una seguridad menos robusta que un servidor tradicional. pero funciona para pequeños proyectos como:

- **Servidor web**:  hostear sitios simples en Android.
    
- **Servidor de archivos**: Usando aplicaciones como _FTP Server_ para compartir archivos en la red local.
    
- **Servidor de juegos**: _Minecraft Pocket Edition_ permite crear mundos multijugador.    

---

### **3. Diferencias entre Hub, Switch y Router**

| **Dispositivo** | **Capa OSI**    | **Funcionamiento**                                                               | **Diferencias clave**                           |
| --------------- | --------------- | -------------------------------------------------------------------------------- | ----------------------------------------------- |
| **Hub**         | Capa 1 (Física) | Retransmite datos a **todos** los puertos, sin inteligencia.                     | Ineficiente, causa colisiones. Obsoleto.        |
| **Switch**      | Capa 2 (Enlace) | Direcciona tráfico usando **MAC addresses**. Crea tablas de direcciones.         | Eficiente, reduce colisiones. Usado en LANs.    |
| **Router**      | Capa 3 (Red)    | Enruta paquetes entre redes usando **IP addresses** (ej: de una LAN a internet). | Conecta redes diferentes, maneja NAT, firewall. |

---

### **4. Dispositivos en una red LAN y sus requisitos**

1. **Router** Conecta la LAN a otras redes (ej: Internet) y dirige el tráfico entre ellas.
    - **Características/Requisitos**:        
        - Soporte para NAT (Traducción de Direcciones de Red).
        - Funcionalidad DHCP para asignar direcciones IP automáticamente.
        - Capacidad de gestión de seguridad (firewall básico, filtrado de puertos).
        - Interfaces WAN y LAN (ej: puertos Ethernet, fibra óptica).
2. **Switch** Interconecta dispositivos dentro de la LAN y gestiona el tráfico mediante direcciones MAC.
    - **Características/Requisitos**:
        - Número suficiente de puertos (8, 16, 24, 48).
        - Velocidad de puertos (ej: 10/100/1000 Mbps, 10 Gbps).
        - Soporte para VLANs (en switches gestionados).
        - Calidad de Servicio (QoS) para priorizar tráfico crítico.
3. **Hub (Concentrador)** Conecta dispositivos en una LAN, pero sin inteligencia (envía datos a todos los puertos).
    - **Características/Requisitos**:
        - Tecnología obsoleta, pero aún presente en redes antiguas.
        - Funciona en la capa física (Layer 1 del modelo OSI).
4. **Punto de Acceso Inalámbrico (WAP)** Permite conexiones Wi-Fi a la LAN.
    - **Características/Requisitos**:        
        - Soporte para estándares Wi-Fi (ej: Wi-Fi 6, 802.11ac).
        - Seguridad avanzada (WPA3, cifrado AES).
        - Capacidad de manejar múltiples clientes simultáneamente.
5. **Tarjeta de Red (NIC)** Permite a dispositivos (PCs, servidores) conectarse físicamente a la red.
    - **Características/Requisitos**:        
        - Compatibilidad con estándares (Ethernet, Wi-Fi).
        - Velocidad acorde a la red (ej: Gigabit Ethernet).
        - Drivers actualizados para el sistema operativo.
6. **Firewall** Protege la red filtrando tráfico no autorizado.
    - **Características/Requisitos**:
		- Filtrado de paquetes y detección de intrusiones (IDS/IPS).
        - Soporte para VPN (conexiones seguras remotas).
        - Actualizaciones periódicas de reglas de seguridad.
7. **Servidor** Aloja servicios compartidos (archivos, correo, aplicaciones).
    - **Características/Requisitos**:
        - Alto rendimiento de CPU, RAM y almacenamiento.
        - Redundancia (discos en RAID, fuentes de poder duales).
        - Sistema operativo de servidor (ej: Windows Server, Linux).
8. **Dispositivos Finales** PCs, laptops, impresoras de red, teléfonos IP.
    - **Características/Requisitos**:
        - Dirección IP configurada (estática o vía DHCP).
        - Conectividad física o inalámbrica (NIC integrada).
9. **NAS (Almacenamiento en Red)** Almacenamiento centralizado accesible por la red.
    - **Características/Requisitos**:
	    - Capacidad de almacenamiento escalable (ej: discos HDD/SSD).
        - Protocolos de acceso (SMB, NFS, FTP).
        - RAID para redundancia de datos.
10. **Repetidor/Extensor de Red** Amplía la cobertura de la señal inalámbrica.
    - **Características/Requisitos**:
        - Compatibilidad con el estándar Wi-Fi de la red principal.
        - Baja latencia para no degradar la velocidad.
11. **Puente de Red (Bridge)** Conecta segmentos de red distintos (ej: Ethernet y Wi-Fi).
    - **Características/Requisitos**:
        - Soporte para protocolos de conversión (ej: Ethernet a Wi-Fi).
        - Gestión de colisiones de tráfico.

---

## 🧪 Laboratorio

**Instrucciones:**  
{{DESCRIPCION_LAB}}

---

## 📝 Cuestionario
```tasks
not done
path includes [[2.4 Redes de computadoras]]
tags include #quiz
```

---

## 🔗 Recursos
```dataview
LIST FROM #recurso AND [[2.4 Redes de computadoras]]
```
