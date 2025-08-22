[[1.8 Software Development 1]]

## Dominio del problema
![[Pasted image 20240506180703.png]]

## Fases de desarrollo de software
![[Pasted image 20240506180252.png]]

### Fases Iteraciones y flujos de trabajo

![[Pasted image 20240506180344.png]]
![[Pasted image 20240506180544.png]]

[[Requisitos e Historias de usuarios]]

![[Pasted image 20240506181117.png]]

![[Pasted image 20240506183908.png]]

### Importancia de RE en el desarrollo de software
No tiene sentido ser preciso si no se sabe de que se está hablando [[von Neumann]]

Cuanto más tarde en el ciclo de vida se detecta un error, más cuesta repararlo.
Muchos errores permanecen latentes y no son detectados hasta bastante después de la etapa en que se cometieron. Muchos podrían detectarse tempranamente

Se cometen muchos errores de requisitos Impacto de los errores en la etapa de requisitos
- EI software resultante puede no satisfacer a los usuarios.
- Las interpretaciones múltiples de los requisitos pueden causar desacuerdos entre clientes y desarrolladores.
- Es imposible que a través del testeo el software satisfaga sus requisitos.
- Puede gastarse tiempo y dinero construyendo el sistema erróneo.

¿Qué es un requisito?
- Es una condición o capacidad que debe cumplir o poseer un sistema o componente de un sistema para satisfacer un contrato, Standard, o especificación o algún otro documento impuesto.
- El conjunto de requisitos forma la base para el desarrollo de un sistema o una componente de sistema.

### Rol de los requisitos
• Acuerdo desarrolladores - stakeholders (comunicación con el equipo de desarrollo)
• Aspecto contractual
• Multipartes (comunicación, conflicto y cambio de visiones)
• Base para el diseño del software
• Minimizar defectos tanto como sea posible
• Proyecto Técnicamente factible
Soporte para verificación y validación
Soporte a la evolución del sistema

University
¿Qué es un requisito?
Un requisito podría describir:
- Una facilidad a nivel usuario
	Ej.: el procesador de palabras debe incluir un verificador de ortografla y un comando de corrección.
- Una propiedad muy general del sistema
	Ej.: el sistema debe asegurar que la información personal nunca se haga disponible sin autorización
- Una restricción específica del sistema
	Ej.: el sensor debe ser activado 10 veces por segundo.
- Una restricción para el desarrollo del sistema
	Ej.: 'el sistema debe ser desarrollado usando Ada.
- Cómo llevar a cabo algún cálculo
	Ej.: tla nota final debe ser calculada sumando las notas del examen, proyecto y cursada el estudiante basado en Ia siguiente fórmula nota final nota_examen  * nota_proy + 2/3 * nota_cursada.
	
#### Requisitos funcionales: describen lo que el sistema
debería hacer 
	Ej.: el sistema debe proveer autenticación de la identidad de un usuario
	Ej.: el sistema debe emitir una factura
#### Requisitos no funcionales: establecen restricciones
de cómo estos requisitos funcionales son implementados.
	EJ. : proceso de autenticación debería completarse en menos de 4 segundos.
	EJ. : la emisión de factura debe poder hacerse desde cualquier terminal de trabajo.
• Seguridad
— permiso de acceso
— niveles de seguridad
políticas de confiabilidad
distribución de los datos
• Interface
help
— lookup de tablas
— restricciones de entrada/visualización de datos
— amigable
• Mantenible
• Portabilidad
• Interoperabilidad
• Restricciones particulares de Ia tecnología de implementación

![[Pasted image 20240506185052.png]]
 ![[Pasted image 20240506185640.png]]
[[Glosario]]

![[Pasted image 20240506185659.png]]

![[Pasted image 20240506185820.png]]

[[Documento de requisitos]]

![[Pasted image 20240506190838.png]]ha

#### Chequeo de Requerimientos
- Validez. ¿Provee al sistema las funciones que mejor soporta las necesidades del cliente?
- Consistencia. ¿Existen conflictos en los requerimientos?
- Completitud. ¿Están incluidas todas las funciones requeridas por el cliente
- Realismo. ¿Pueden los requerimientos ser implementados con la tecnología y el presupuesto disponible?

![[Pasted image 20240506191824.png]]

Reporte de requerimiento == backlog

![[Pasted image 20240506192413.png]]