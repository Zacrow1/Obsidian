### Venis de [[2.3 Programación 3]]

# Ecosistema de .NET 
.NET es una plataforma gratuita para desarrolladores, multiplataforma y de código abierto diseñada para compilar muchos tipos diferentes de aplicaciones. 
.NET se basa en un entorno de ejecución de alto rendimiento que muchas aplicaciones a gran escala usan en producción. 

El ecosistema de .NET brinda soluciones en diferentes campos, por ejemplo: 
![[Pasted image 20250106160230.png]]

Microsoft ofrece 3 lenguajes en la plataforma .NET: C#, F# y Visual Basic. C# es un lenguaje multiplataforma de propósito general que permite a los desarrolladores ser productivos al escribir código altamente eficiente. Con millones de desarrolladores, C# es el lenguaje .NET más popular. Basado en principios de programación orientada a objetos, incorpora muchas características de otros paradigmas, incluyendo la programación funcional.
![[Pasted image 20250106160301.png]]




### Implementaciones de .NET
Hay varias variantes de .NET, cada una de las cuales admite un tipo diferente de aplicación. La razón de las múltiples variantes es en parte histórica y en parte técnica.

![[Pasted image 20250106160526.png]]

.NET Framework: proporciona acceso a las amplias funcionalidades de Windows y Windows Server. El lenguaje .NET original. Mono: una implementación multiplataforma de .NET Framework. Es de código abierto. Se usa para aplicaciones Android, iOS y WASM. .NET (Core): una implementación multiplataforma y de código abierto de .NET, reformulada para trabajar con la nube sin dejar de ser significativamente compatible con .NET Framework. Se usa en aplicaciones de Linux, macOS y Windows.

![[Pasted image 20250106160613.png]]

### Common Language Infrastructure

Es un conjunto de estándares que definen cómo se compilan, ejecutan y administran las aplicaciones .NET. Es la base de la plataforma .NET y proporciona una serie de beneficios, como la portabilidad, la seguridad y la escalabilidad. Pongamos la siguiente analogía: Imagine que se está construyendo una casa. El Common Language Infrastructure es como el plano de la casa. Es un conjunto de instrucciones que le dicen cómo construir la casa.

![[Pasted image 20250106160939.png]]

### Intermediate Language
Es un lenguaje de programación de bajo nivel que se genera al compilar código fuente
escrito en un lenguaje de alto nivel, como C# o Visual Basic. 
Es independiente de la plataforma, puede ser ejecutado en cualquier máquina que tenga instalado el .NET Framework o el .NET Core. Es un lenguaje de programación de bajo nivel, pero no tan bajo como el lenguaje ensamblador.

![[Pasted image 20250106161328.png]]

### Common Language Runtime
Es el entorno responsable de cargar y ejecutar el código escrito en diferentes lenguajes
.NET, como C#, F#, etc.
Cuando un programa es compilado, el código ejecutable de resultado esta en el IL. Este código solo puede ser ejecutado por cualquier plataforma que utilice el CLR. 
El CLR se encarga de compilar el código a código maquina y así pueda ser ejecutado por el procesador.

![[Pasted image 20250106161411.png]]

Adicionalmente el CLR provee un marco de trabajo para desarrollar aplicaciones y un conjunto de librerías base BCL (Base Class Libraries) que tienen un gran abanico de funcionalidades básicas. En resumen, el CLR es un entorno de ejecución que se utiliza para ejecutar aplicaciones .NET. Proporciona una serie de beneficios, como la portabilidad, la seguridad, la eficiencia y la gestión de memoria.
![[Pasted image 20250106161429.png]]


### Compilador Just in time

Funcionamiento del compilador JIT: el compilador JIT es necesario para acelerar la ejecución del código y brindar soporte para múltiples plataformas. Su funcionamiento se da de la siguiente manera: El compilador JIT convierte el lenguaje intermedio de Microsoft (MSIL) o el lenguaje intermedio común (CIL) en código de máquina. Esto se hace antes de que se pueda ejecutar. Es decir, el compilador JIT compila el MSIL o CIL según sea necesario en lugar de hacerlo en su totalidad. El MSIL o CIL compilado se almacena para que esté disponible para llamadas posteriores si es necesario

![[Pasted image 20250106161511.png]]


### Procesos de Compilación y ejecución
Compilación 
- El compilador de C#: Traduce el código fuente de C# a CIL. 
- Produce archivos .dll y .exe. 
- Se produce compilación justo a tiempo (JIT): Traducción de CIL a código máquina. Ejecución 
- Usando compilación JIT intercalada. 
- En Mono: Activación explícita del intérprete. 
- En Windows: Activación transparente del intérprete.

![[Pasted image 20250106161609.png]]

### Comparación entre CLR y JVM

El CLR y el JVM son dos máquinas virtuales de procesos que tienen muchas similitudes, pero también algunas diferencias importantes. El CLR es neutral en cuanto al lenguaje y ahora es compatible con diferentes sistemas operativos al igual que el JVM aun que este es específico de Java. El CLR utiliza un compilador JIT, mientras que el JVM utiliza un compilador JIT especializado llamado Java HotSpot.

El CLR incluye instrucciones para cierres, corrutinas y declaración/manipulación de punteros, mientras que el JVM no. El JVM es compatible con herramientas de resolución de errores y monitoreo de producción más robustas.

![[Pasted image 20250106161715.png]]

Proceso de Soporte La información sobre el tipo de cada versión está codificado en el número de versión con el formato principal.secundaria.revisión. Por ejemplo: 
- .NET 6 y NET 7 son versiones principales. 
- .NET Core 3.1 es la primera versión secundaria después de la versión principal de .NET Core 3.0. 
- .NET Core 5.0.15 es la decimoquinta revisión de .NET 5.
![[Pasted image 20250106161852.png]]

Proceso de Soporte Existen dos tipos de soporte técnico para las versiones de .NET: • Soporte Técnico a Corto Plazo (STS): Soporte durante 6 meses después del lanzamiento de la siguiente versión principal o secundaria. Por ejemplo.NET 7 tiene soporte hasta mayo de 2024. • Soporte Técnico a Largo Plazo (LTS): Soporte durante al menos 3 años o 1 año después del lanzamiento de la siguiente versión LTS, lo que sea posterior. Por ejemplo.NET 6, otra versión LTS, tiene soporte hasta noviembre de 2024 desde su lanzamiento en noviembre de 2021.