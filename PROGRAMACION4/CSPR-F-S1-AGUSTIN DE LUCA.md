# CSPR-F-S1-AGUSTIN DE LUCA

## Discusión 1

### Definiciones previas

**Backend**: Es la parte de una aplicación o sistema que se encarga de procesar la lógica de negocio, acceder a bases de datos, gestionar usuarios, seguridad y servir datos al frontend. No es visible directamente para el usuario final.

**Rendimiento (en sistemas de software)**: Se refiere a la capacidad de un sistema para responder rápidamente a las solicitudes de los usuarios, procesar grandes volúmenes de datos o transacciones por segundo, y utilizar eficientemente los recursos del servidor (CPU, memoria, red, etc.).

**Escalable (en sistemas de software)**: Un sistema es escalable si puede aumentar su capacidad de procesamiento (más usuarios, más datos, más transacciones) añadiendo más recursos (hardware, instancias, nodos) sin perder rendimiento ni estabilidad.

### Debate concreto: ¿C# o JavaScript para sistemas backend de alto rendimiento y escalables?

Si el sistema requiere procesamiento intensivo, cálculos complejos o máxima eficiencia de recursos, **C#** Si el sistema es principalmente I/O, APIs, tiempo real, microservicios y se prioriza la escalabilidad horizontal y rapidez de desarrollo, **JavaScript/Node.js** es una mejor opción la elección depende del contexto y los requisitos específicos del proyecto.

---

## Discusión 2

### Definiciones previas

**Arquitectura monolítica**: Es un modelo donde toda la funcionalidad del sistema está contenida en una sola aplicación o despliegue.

**Arquitectura de microservicios**: Consiste en dividir el sistema en pequeños servicios independientes, cada uno responsable de una funcionalidad específica, que se comunican entre sí mediante APIs.

**Sistemas mantenibles**: Son aquellos que pueden ser modificados, corregidos, ampliados o adaptados fácilmente a lo largo del tiempo, con bajo riesgo de introducir errores y sin grandes esfuerzos.

### Debate concreto: ¿Monolito o microservicios para backend escalable y mantenible con JavaScript?

**Respuesta concreta:**
- Para proyectos pequeños o en etapas iniciales, un **monolito** puede ser más práctico.
- Para sistemas grandes, con necesidades de escalabilidad y mantenibilidad, la **arquitectura de microservicios** con JavaScript/Node.js es más adecuada, aunque requiere mayor madurez técnica y organizacional. 