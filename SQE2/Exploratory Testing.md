---
tags:
  - Universidad
  - Testing
  - SQE2
Creado: 2025-05-06
Relacionado:
  - SQE2
---
## Pruebas Exploratorias (Exploratory Testing): Descubrimiento y Aprendizaje en Tiempo Real

Las pruebas exploratorias son un enfoque de prueba de software que se describe a menudo como el aprendizaje, el diseño de pruebas y la ejecución de pruebas que ocurren _simultáneamente_. A diferencia de las pruebas guiadas (scripted testing), donde los pasos se definen meticulosamente por adelantado, las pruebas exploratorias se centran en la libertad y la responsabilidad del evaluador individual para explorar la aplicación, descubrir cómo funciona y encontrar defectos sobre la marcha.

En este método, el evaluador no sigue un script predefinido, sino que utiliza su conocimiento, experiencia, creatividad e intuición para navegar por el software. El proceso es dinámico: el evaluador aprende sobre el sistema mientras lo prueba y usa la información obtenida para diseñar y realizar sus siguientes pruebas.

**Características Clave de las Pruebas Exploratorias:**

- **Aprendizaje Continuo:** El evaluador está constantemente aprendiendo sobre la aplicación, sus funcionalidades y su comportamiento a medida que interactúa con ella.
- **Diseño y Ejecución Simultáneos:** Las ideas para nuevas pruebas surgen durante la ejecución, basándose en las observaciones y descubrimientos del evaluador.
- **Dependencia del Evaluador:** El éxito de las pruebas exploratorias depende en gran medida de las habilidades, la experiencia y la curiosidad del evaluador.
- **Enfoque en el Descubrimiento:** El objetivo principal es descubrir fallas, comportamientos inesperados, problemas de usabilidad y riesgos que podrían no estar cubiertos por pruebas más estructuradas.
- **Flexibilidad y Adaptabilidad:** El enfoque es altamente adaptable a cambios en los requisitos o en la aplicación misma.
- **Documentación Límida o Ad-hoc:** La documentación suele ser menos formal y puede incluir notas sobre hallazgos, ideas de prueba o grabaciones de sesiones, en lugar de scripts detallados paso a paso.

**Metodología (Sesiones Exploratorias):**

Aunque es menos estructurado que las pruebas guiadas, el testing exploratorio a menudo se realiza dentro de un marco para mantener el enfoque y la productividad. Un enfoque común es el uso de "sesiones exploratorias" o "charters de prueba":

1. **Definir la Misión (Charter):** Establecer un objetivo claro para la sesión de exploración (ej: "Explorar la funcionalidad de carrito de compras y la finalización de la compra", "Investigar la gestión de errores en la subida de archivos").
2. **Asignar un Tiempo (Timeboxing):** Limitar la sesión a un período de tiempo específico (ej: 60-90 minutos) para mantener el enfoque.
3. **Explorar y Registrar:** El evaluador explora la aplicación siguiendo la misión, documentando ideas, observando el comportamiento, identificando problemas y registrando los hallazgos relevantes (bugs, preguntas, ideas para futuras pruebas).
4. **Revisar los Resultados:** Al final de la sesión, se revisan y analizan los hallazgos.

**Ventajas de las Pruebas Exploratorias:**

- **Descubre Defectos Inesperados:** Es excelente para encontrar errores sutiles, de borde o aquellos que involucran interacciones complejas entre diferentes partes del sistema, que podrían pasarse por alto en scripts predefinidos.
- **Respuesta Rápida a Cambios:** Ideal en entornos Ágiles o donde los requisitos cambian frecuentemente, ya que no requiere una extensa reelaboración de scripts.
- **Simula Mejor el Uso Real:** Los evaluadores pueden interactuar con la aplicación de una manera más similar a como lo haría un usuario final real.
- **Aprovecha la Habilidad del Evaluador:** Permite a los evaluadores experimentados aplicar su conocimiento y intuición para encontrar problemas de manera eficiente.
- **Proporciona Retroalimentación Rápida:** Permite obtener información rápida sobre la calidad y usabilidad de una nueva funcionalidad o una versión.

**Desventajas de las Pruebas Exploratorias:**

- **Menor Repetibilidad:** Es difícil repetir exactamente la misma ejecución de prueba, lo que puede complicar la verificación de correcciones o la regresión precisa.
- **Documentación Potencialmente Incompleta:** La falta de scripts detallados puede hacer que sea más difícil tener un registro completo de todas las pruebas realizadas.
- **Dependencia de la Experiencia:** Su efectividad varía mucho según la habilidad y el conocimiento del dominio del evaluador. Un evaluador inexperto puede ser menos efectivo.
- **Cobertura Difícil de Medir:** Es más complicado cuantificar la cobertura de la prueba de manera formal.

**¿Cuándo Utilizar Pruebas Exploratorias?**

Las pruebas exploratorias son particularmente útiles en los siguientes escenarios:

- Cuando los requisitos no están claros, están incompletos o cambian con frecuencia.
- Para complementar las pruebas guiadas, explorando áreas que no están cubiertas por los scripts formales.
- En fases tempranas del desarrollo para obtener retroalimentación rápida.
- Para probar nuevas características o áreas de alto riesgo.
- Para realizar pruebas de usabilidad y experiencia del usuario.
- Cuando se tiene poco tiempo para la planificación formal y la creación de scripts detallados.
- Para aprovechar la experiencia y el conocimiento de evaluadores altamente calificados.