> [!info] Definition
> En un sentido amplio, el riesgo se refiere a la posibilidad de que ocurra un evento adverso o indeseado que puede resultar en una pérdida o un resultado negativo. Esta definición es aplicable en diversos contextos, como financiero, de seguridad, empresarial, entre otros.
> El riesgo se caracteriza generalmente por dos componentes:Probabilidad: La posibilidad de que ocurra el evento indeseado.
> - Impacto: La gravedad de las consecuencias si el evento efectivamente ocurre.
> - Es fundamental en la toma de decisiones, ya que permite anticipar y gestionar posibles peligros o incertidumbres.

# Riesgos y Gestión de riesgos en Software Testing

- El **ISTQB** (International Software Testing Qualifications Board) define riesgo en el contexto de pruebas de software como la posibilidad de que un evento adverso ocurra, y el impacto negativo que dicho evento tendría sobre los objetivos del proyecto, como la calidad, el cronograma, el presupuesto, la reputación, etc. 

- Este concepto es fundamental en la planificación y ejecución de las pruebas, ya que permite identificar y priorizar áreas críticas del sistema que requieren una mayor atención durante el proceso de pruebas.

- La gestión del riesgo en las pruebas implica la identificación, evaluación y control de los riesgos para minimizar su impacto en la calidad del software.

- La gestión de riesgos incluye la identificación, análisis, planificación de respuesta y control de los riesgos.


## Nivel de riesgo

- La importancia de un riesgo según lo definido por sus características, impacto y probabilidad. 
- El nivel de riesgo puede utilizarse para determinar la intensidad de las pruebas que tienen que ejecutarse.
- Cuanto mayor es el nivel de riesgo, más importante es su tratamiento.
- Un nivel de riesgo puede ser expresado ya sea cualitativamente (e.g. alto, medio, bajo) o cuantitativamente.

# Risk Based Testing (RBT)

- Las pruebas basadas en riesgos son un enfoque de prueba que prioriza las características y funciones más críticas y riesgosas de un sistema en función de la probabilidad del impacto de la falla de las mismas. Son pruebas en las que la gestión, selección, priorización y uso de actividades y recursos de prueba se basan en los tipos y niveles de riesgo correspondientes.
- RBT o las pruebas basadas en riesgos son la idea de que podemos organizar los esfuerzos de prueba de una manera que reduzca el nivel residual de riesgo del producto cuando se entrega el sistema.

> [!success] Beneficios
    > - Priorizar las pruebas para encontrar los defectos más críticos lo antes posible. Permiten al equipo en áreas de alta criticidad y alto riesgo.
    > - Ayudar a detectar problemas críticos temprano en el ciclo de vida del desarrollo de software, lo cual implícitamente reduce costos asociados al testing y corrección de errores post-lanzamlento.
    > - A centrarse en áreas críticas del sistema, las pruebas basadas en riesgos utilizan recursos de manera más efectiva y eficiente.
    > - Determinar si se podrían emplear otras actividades para reducir el riesgo, como brindar capacitación en diseño y pruebas a desarrolladores sin experiencia.
    > - El equipo de prueba se enfoca en tareas que agregan valor real al proyecto, mejorando la gestión del tiempo y evitando esfuerzos innecesarios en áreas que presentan menos riesgo o importancia.
    > - Determinar los niveles y tipos de pruebas que se realizarán (ej. Pruebas funcionales, seguridad, rendimiento)

# Riesgos del Proyecto
Los riesgos del proyecto están relacionados con la gestión y control del proyecto. Los riesgos del
proyecto incluyen:

> [!danger]
> - Desviaciones del cronograma: por ejemplo, retrasos con el cumplimiento de milestones del Proyecto, estimaciones incorrectas.
> - Problemas relacionados con las personas: por ejemplo, habilidades insuficientes, conflictos, problemas de comunicación, escasez de personal o pérdida de personal clave.
> - Cambios en el Alcance: Modificaciones en los requisitos del proyecto o adición de nuevas características después de haber comenzado el desarrollo, lo que puede llevar a la expansión del trabajo y a complicaciones en la gestión del proyecto.
> - Problemas técnicos: por ejemplo, variación del alcance, soporte deficiente de las herramientas u obsolecencia de herramientas o fallos en productos de terceros. 
> - Problemas con proveedores: por ejemplo, fallas en la entrega de terceros, quiebra de la empresa de soporte.
> - Los riesgos del proyecto, cuando ocurren, pueden tener un impacto El cronograma, retrasar la entrega e incluso en su comercialización perdiendo oportunidades de mercado o inflando del presupuesto.
> - Los retrasos o la calidad disminuida pueden afectar la aceptación del usuario y las ventas, impactando directamente el retorno de la inversión.
> - Los cambios no controlados en el alcance del proyecto, pueden afectar la capacidad del proyecto para lograr sus objetivos, causar retrasos y elevación de costos.

# Riesgos del Producto
Los riesgos del producto están relacionados con las características de calidad del producto
(por ejemplo, descritas en el modelo de calidad ISO 25010).

> [!danger]
> Algunos ejemplos de riesgos del producto pueden ser:
> - Funcionalidad faltante o incorrecta
> - Cálculos incorrectos
> - Defectos de calidad, errores de codificación , fallos en la integración de componentes.
> - Arquitectura deficiente
> - Algoritmos ineficientes
> - Problemas de rendimiento: tiempo de respuesta inadecuado , consumo excesivo de recursos, problemas de escalabilidad.
> - Dificultades en la interfaz de usuario que pueden hacer que el software sea difícil de entender, aprender o utilizar por los usuarios finales 
> - Vulnerabilidades de seguridad.

Las pruebas que revelan defectos ayudan a mitigar los riesgos de calidad pues es posible repararlos antes de la entrega. Incluso en algunas ocasiones permite descubrir riesgos del proyecto

![[Pasted image 20250512123551.png]]

![[Pasted image 20250512124833.png]]

![[Pasted image 20250512125205.png]]

# ¿Como escribir un riesgo?
**Riesgo de que** _{Indicar la falta de manera especifica}_ **cuando** _{describir la causa que podria desencadenarlo}_ Ej. valor de una variable, una acción, etc.

Riesgo de que la pagina web incremente su tiempo de respuesta. cuando mas de 500 usuarios acceden a la misma de manera concurrente
![[Pasted image 20250513124021.png]]

Riesgo de que el performance de actio baje cuando las imágenes subidas por los usuarios se almacenen de manera ineficiente.