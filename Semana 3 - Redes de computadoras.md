---
materia: "Redes de computadoras"
semana: 3
fecha_inicio: 2025-03-17
tags:
---

```button
name 🏠 Volver a Materia
type command
action Obsidian: Open file
params "{{materia}}"
color purple
```

# Semana {{SEMANA}} - {{NOMBRE_MATERIA}}

## 🎯 **Objetivos**
- [ ] #foro Completar foro sobre [[{{TEMA}}]] 📅 2025-03-20
- [ ] #tarea Entregar {{TAREA}} 📅 2025-03-22
- [ ] #lab Finalizar laboratorio 📅 2025-03-24

---

## 📚 **Temas Cubiertos**
```button
name ➕ Nuevo Tema
type command
action QuickAdd: Capturar Tema
color blue
```


---

## 💬 **Foro**
> [!question] {{TITULO_PREGUNTA}}
> {{CONTENIDO_PREGUNTA}}

**Mi Respuesta:**  
<% tp.file.cursor() %>

---

## 📋 **Tareas**
```tasks
not done
path includes {{NOMBRE_MATERIA}}
tags include #tarea
```

**Tipos de Entrega de Mensajes**  
Existen tres tipos de entrega de mensajes en redes: unicast, multicast y broadcast. El unicast consiste en la comunicación directa entre un emisor y un receptor específico, como el envío de un correo electrónico a una persona determinada. El multicast permite enviar información a un grupo seleccionado de dispositivos, utilizado en aplicaciones como videoconferencias donde varios participantes reciben el mismo flujo de datos. El broadcast transmite mensajes a todos los dispositivos en una red, similar a una señal de televisión abierta que llega a todos los televisores sintonizados en un canal específico.

**Protocolos TCP y UDP: Uso en Descarga de Archivos y Juegos en Línea**  
El protocolo TCP (Transmission Control Protocol) garantiza la entrega ordenada y sin errores de los datos mediante confirmaciones y retransmisiones, lo que lo hace ideal para descargas de archivos donde la integridad es crítica. Por otro lado, el protocolo UDP (User Datagram Protocol) prioriza la velocidad al no verificar la recepción de paquetes, siendo adecuado para juegos en línea que requieren baja latencia, incluso si algunos paquetes se pierden. Por ejemplo, en un juego multijugador, UDP permite actualizaciones rápidas de posiciones, mientras que TCP podría usarse para transacciones seguras dentro del juego.

**Capa del Modelo OSI para Protocolos**  
En el Modelo OSI, los protocolos se distribuyen de la siguiente manera: TCP y UDP corresponden a la capa de transporte. IP, ICMP y ARP pertenecen a la capa de red, aunque ARP también opera en la capa de enlace de datos al relacionar direcciones IP con MAC. FTP, DNS y HTTP funcionan en la capa de aplicación, ya que gestionan servicios directos al usuario, como transferencia de archivos, resolución de nombres y acceso a páginas web.

**Importancia de ARPANET y su Primera Aplicación**  
ARPANET fue fundamental para el desarrollo de Internet actual al introducir la conmutación de paquetes y sentar las bases de los protocolos de comunicación, como TCP/IP. Esta red permitió la conexión descentralizada de computadoras, un concepto revolucionario que evitaba puntos únicos de fallo. La primera aplicación utilizada en ARPANET fue el correo electrónico, creado en 1971 por Ray Tomlinson, que permitió el intercambio de mensajes entre usuarios, marcando un hito en la comunicación digital.

---

## 🧪 **Laboratorio**
**Instrucciones:**  
{{DESCRIPCION_LAB}}


---

## 📝 **Cuestionario**
```tasks
not done
path includes {{NOMBRE_MATERIA}}
tags include #quiz
```

---

## 🔗 **Relación con Otras Semanas**
```dataview
LIST FROM #semana/{{SEMANA-1}} OR #semana/{{SEMANA+1}}
WHERE file != this
```

---

## 📌 **Recursos**
```dataview
LIST FROM #recurso AND [[{{NOMBRE_MATERIA}}]]
```