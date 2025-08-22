[[1.2 Arquitectura Computacional]]

### Un sistema operativo ejecuta una variedad de programas:
- Sistema por lotes — trabajos
- Sistemas de tiempo compartido: [[programas]] o [[tareas de usuario]]
El libro de texto usa los términos **trabajo** y **proceso ** casi indistintamente.
[[Proceso]] : un programa en ejecución; la ejecución del proceso debe progresar en forma secuencial
Múltiples partes
- El código del programa, también llamado sección de texto.
- Actividad actual incluyendo [[programa contador]] , registros del
procesador
- Pila que contiene datos temporales
	- Parámetros de función, direcciones de retorno, variables locales
- Sección de datos que contiene variables globales
- Montón que contiene memoria asignada dinámicamente durante el tiempo de ejecución

El programa es una entidad pasiva almacenada en el disco (archivo ejecutable), el proceso está activo
- El programa se convierte en proceso cuando el archivo ejecutable se carga en la memoria
La ejecución del programa se inició a través de clics del mouse en la GUI, la entrada de la línea de comando de su nombre, etc.
Un programa puede ser varios procesos
- Considere múltiples usuarios ejecutando el mismo programa

El código del programa, también llamado sección de texto
Sección de datos que contiene variables
globales
Pila(stack) que contiene datos temporales
Parámetros de funciones, variables locales,
retorno
valores, direcciones de retorno
Heap que contiene memoria asignada
dinámicamente durante el tiempo de
ejecución

![[Pasted image 20240115121222.png]]

### Estado del proceso
A medida que se ejecuta un proceso, cambia de **estado**
- **new **: El proceso se está creando
- **En ejecución (running)** : las instrucciones se están ejecutando.
- **Esperando (waiting)** : el proceso está esperando que ocurra algún evento
- **Listo (ready)** : el proceso está esperando a ser asignado a un procesador
- **Terminado** : El proceso ha terminado de ejecutarse.

![[Pasted image 20240115121325.png]]

### Bloque de control de procesos (PCB)
Información asociada a cada proceso
(también llamado [[bloque de control de tareas]] )

- Estado del proceso: en ejecución, en espera, etc.
- Contador de programa: ubicación de la instrucción para la próxima ejecución
- Registros de [[ CPU]]: contenido de todos los registros centrados en procesos
- Información de programación de [[CPU]]: prioridades, punteros de cola de programación
- Información de gestión de memoria: memoria asignada al proceso
- Información contable: [[CPU]] utilizada, tiempo de reloj transcurrido desde el inicio, límites de tiempo
- Información de estado de E/S: dispositivos de EIS asignados al proceso, lista de archivos abiertos

![[Pasted image 20240115121601.png]]

### Cambio de [[CPU]] de proceso a proceso
![[Pasted image 20240115122159.png]]

### Hilos
- Hasta ahora, el proceso tiene un solo hilo de ejecución.
- Considere tener múltiples contadores de programa por proceso
- Múltiples ubicaciones pueden ejecutarse a la vez
	- Múltiples hilos de control -> hilos
- Luego debe tener almacenamiento para detalles de subprocesos, múltiples contadores de programas en PCB
- Ver el próximo capítulo

### Programación de procesos
- Maximice el uso de la [[CPU]], cambie rápidamente los procesos a la [[CPU]] para compartir el tiempo
- El [[programador de procesos]] selecciona entre los procesos disponibles para la próxima ejecución en la [[CPU]]
- Mantiene la [[programación de colas]] de procesos.
	- Cola de trabajo : conjunto de todos los procesos en el sistema
	- Cola lista : conjunto de todos los procesos que residen en la memoria principal, listos y esperando para ejecutarse
	- Colas de dispositivos : conjunto de procesos que esperan un dispositivo de E/S
	- Los procesos migran entre las distintas colas

### Cola lista y varias colas de dispositivos de E/S
![[Pasted image 20240115125712.png]]

### El diagrama de colas representa colas, recursos, flujos
![[Pasted image 20240115125834.png]]

 ### Programadores
- **Programador a corto** plazo (o [[programador de CPU]] ): selecciona qué proceso debe ejecutarse a continuación y asigna la [[CPU]]
	- A veces, el único programador en un sistema
	- El planificador a corto plazo se invoca con frecuencia (milisegundos) ==> (debe ser rápido)
- Programador a largo plazo (o [[programador de trabajos]] ): selecciona qué procesos deben ponerse en la cola lista
	 - El planificador a largo plazo se invoca con poca frecuencia (segundos, minutos) (puede ser lento)
	- El planificador a largo plazo controla el grado de multiprogramación
- Los procesos se pueden describir como:
	- Proceso enlazado a EIS —dedica más tiempo a EIS que a cálculos, muchas ráfagas breves de [[CPU]]
	- Proceso vinculado a la [[CPU]] : pasa más tiempo haciendo cálculos; pocas ráfagas de [[CPU]] muy largas
- El programador a largo plazo se esfuerza por lograr una buena **combinación de procesos**

### Adición de Programación a Mediano Plazo 
- un programador a mediano plazo si es necesario reducir el grado de programación múltiple
	- Eliminar el proceso de la memoria, almacenarlo en el disco, recuperarlo del disco para continuar con la ejecución: intercambio
![[Pasted image 20240115130813.png]]
### Multitarea en Sistemas Móviles

- Algunos sistemas móviles (por ejemplo, la versión anterior de iOS) permiten que solo se ejecute un proceso, otros se suspenden 
- Debido al estado real de la pantalla, los límites de la interfaz de usuario iOS proporciona una
	- de primer plano único controlado a través de la interfaz de usuario
	- Múltiples procesos en segundo plano : en la memoria, en ejecución, pero no en la pantalla y con límites 
	- Los límites incluyen una sola tarea corta, recibir notificaciones de eventos, tareas específicas de larga duración como la reproducción de audio. Android se ejecuta en primer plano y en segundo plano, con menos límites El proceso en segundo plano utiliza un servicio para realizar tareas El servicio puede seguir ejecutándose incluso si se suspende el proceso en segundo plano El servicio no tiene interfaz de usuario, uso de memoria pequeño