---
tags:
  - Universidad
  - Testing
  - SQE2
Creado: 2025-05-06
Relacionado:
  - SQE2
---
![[Pasted image 20250602202258.png]]## Pruebas Guiadas (Scripted Testing): Un Enfoque Estructurado para la Verificación de Software

Las pruebas guiadas (scripted testing) son un método formal de prueba de software donde los casos de prueba son diseñados y documentados en detalle _antes_ de que la ejecución de la prueba tenga lugar. Este enfoque implica seguir un conjunto predefinido de pasos, entradas y resultados esperados para verificar que una aplicación de software funciona de acuerdo con sus requisitos.

En esencia, las pruebas guiadas se centran en la precisión y la repetibilidad. Los evaluadores siguen un "guion" – un caso de prueba o script de prueba – que describe las acciones exactas a realizar y el resultado esperado en cada etapa. Esto contrasta con métodos más libres como las pruebas exploratorias, donde los evaluadores tienen más flexibilidad para desviarse y explorar la aplicación basándose en su intuición y hallazgos.

**Características Clave de las Pruebas Guiadas:**

- **Casos de Prueba Predefinidos:** Los escenarios de prueba se analizan y se crean casos de prueba detallados por adelantado. Estos casos especifican el objetivo de la prueba, las precondiciones, los datos de entrada, los procedimientos paso a paso y los resultados esperados.
- **Ejecución Paso a Paso:** Los evaluadores siguen los pasos documentados rigurosamente, asegurando que cada acción se realice exactamente como se describe.
- **Resultados Esperados Claros:** Para cada paso o secuencia de pasos, se define claramente la respuesta o salida esperada del sistema, lo que permite una comparación directa entre los resultados reales y los esperados.
- **Documentación:** Las pruebas guiadas dependen en gran medida de la documentación, incluyendo planes de prueba, casos de prueba y scripts de prueba. Esta documentación sirve como guía para la ejecución y como registro de las actividades y resultados de las pruebas.
- **Repetibilidad:** Debido a la naturaleza estructurada y la documentación detallada, las pruebas guiadas pueden repetirse fácilmente, lo cual es crucial para las pruebas de regresión para asegurar que los nuevos cambios en el código no hayan introducido defectos en la funcionalidad existente.

**Las Pruebas Guiadas en la Práctica:**

Las pruebas guiadas pueden realizarse tanto manualmente como a través de la automatización.

- **Pruebas Guiadas Manuales:** Los evaluadores humanos ejecutan los pasos predefinidos descritos en los casos de prueba, interactuando manualmente con la aplicación y verificando los resultados frente a los resultados esperados.
- **Pruebas Guiadas Automatizadas:** Los scripts de prueba se traducen a código que puede ser ejecutado por herramientas de automatización. Estas herramientas interactúan con la aplicación de forma programática, realizan los pasos y comparan los resultados reales con los resultados esperados, a menudo reportando las discrepancias automáticamente.

**Ventajas de las Pruebas Guiadas:**

- **Claridad y Consistencia:** Proporciona instrucciones claras, reduciendo la ambigüedad y asegurando que las pruebas se ejecuten de manera consistente independientemente del evaluador.
- **Repetibilidad:** Facilita la fácil repetición de las pruebas, esencial para las pruebas de regresión y la verificación de correcciones.
- **Cobertura Medible:** Permite un mejor seguimiento de la cobertura de las pruebas en relación con los requisitos.
- **Adecuado para Principiantes:** Los evaluadores nuevos pueden seguir fácilmente las pruebas guiadas con un conocimiento mínimo del dominio.
- **Bueno para Funcionalidades Críticas:** Ideal para probar a fondo características centrales o críticas donde la verificación precisa es primordial.
- **Base para la Automatización:** Los casos de prueba guiados bien definidos sirven como una base sólida para desarrollar scripts de prueba automatizados.

**Desventajas de las Pruebas Guiadas:**

- **Pueden Ser Rígidas:** La estricta adherencia a los guiones puede limitar la capacidad de un evaluador para explorar más allá de los caminos definidos y potencialmente pasar por alto defectos inesperados.
- **Preparación que Requiere Mucho Tiempo:** La creación de casos de prueba y scripts detallados por adelantado requiere una cantidad significativa de tiempo y esfuerzo.
- **Sobrecarga de Mantenimiento:** Las pruebas guiadas deben actualizarse cada vez que cambian los requisitos de la aplicación o la interfaz de usuario.
- **Puede No Descubrir Problemas de Usabilidad:** El enfoque principal está en la verificación funcional basada en los requisitos, lo que podría pasar por alto problemas de usabilidad o comportamiento inesperado del usuario.

**Comparación con las Pruebas Exploratorias:**

Las pruebas guiadas y las pruebas exploratorias a menudo se consideran enfoques complementarios. Mientras que las pruebas guiadas se centran en la _verificación_ contra requisitos conocidos, las pruebas exploratorias enfatizan el _descubrimiento_ y el aprendizaje a través de la interacción práctica con el software. Una estrategia de prueba equilibrada a menudo incorpora ambos métodos para lograr una cobertura integral.

---
#### Referencias
