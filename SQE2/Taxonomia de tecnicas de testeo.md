---
tags:
  - Universidad
  - Testing
  - SQE2
Creado: 2025-05-06
Relacionado:
  - SQE2
---

Una taxonomía de técnicas de testeo de software permite clasificar los diversos métodos y enfoques utilizados para evaluar la calidad de un producto de software. Estas clasificaciones ayudan a comprender el propósito, el alcance y la aplicación de cada técnica, facilitando la selección adecuada en diferentes contextos del ciclo de vida del desarrollo.

Si bien no existe una única taxonomía universalmente aceptada, las técnicas de testeo suelen agruparse en función de distintos criterios clave:

**1. Por el Nivel de Prueba:** Este criterio se basa en la granularidad y el alcance de las pruebas dentro de la arquitectura del software.

- **Testeo Unitario (Unit Testing):** Se enfoca en probar componentes individuales o módulos pequeños y aislados del código fuente (por ejemplo, funciones, métodos, clases). Generalmente es realizado por los desarrolladores.
- **Testeo de Integración (Integration Testing):** Verifica la interacción y comunicación entre diferentes unidades o módulos que han sido previamente testeados de forma unitaria. Busca descubrir defectos en las interfaces y la integración entre componentes.
- **Testeo de Sistema (System Testing):** Prueba el sistema completo e integrado para evaluar su conformidad con los requisitos funcionales y no funcionales especificados. Se realiza en un entorno que simula el entorno de producción lo más fielmente posible.
- **Testeo de Aceptación (Acceptance Testing):** Es un nivel formal de testeo donde se valida si el sistema cumple con los requisitos del usuario, cliente o negocio. Puede incluir Testeo Alfa (realizado internamente por el equipo de desarrollo o testers) y Testeo Beta (realizado por usuarios finales en un entorno real).

**2. Por el Conocimiento de la Estructura Interna:** Esta clasificación se basa en si las pruebas se diseñan con o sin conocimiento del código interno, diseño o estructura del sistema.

- **Testeo de Caja Negra (Black-Box Testing):** Se enfoca en la funcionalidad del software basándose en los requisitos y especificaciones, sin tener conocimiento de la estructura interna del código. Las pruebas se diseñan a partir de las entradas y salidas esperadas.
- **Testeo de Caja Blanca (White-Box Testing):** Se basa en el conocimiento de la estructura interna del código, el diseño y la implementación del software. Las pruebas se diseñan para cubrir rutas de código específicas, sentencias, decisiones y condiciones. También conocido como testeo estructural.
- **Testeo de Caja Gris (Gray-Box Testing):** Combina aspectos del testeo de caja negra y caja blanca. El tester tiene un conocimiento parcial de la estructura interna, lo que le permite diseñar pruebas más informadas que en caja negra, pero sin tener acceso completo al código fuente como en caja blanca.

**3. Por el Propósito del Testeo:** Este criterio clasifica las técnicas en función del tipo de requisito que buscan validar.

- **Testeo Funcional:** Verifica que el software se comporta de acuerdo con los requisitos funcionales especificados, es decir, qué hace el sistema. Incluye pruebas de funcionalidades, usabilidad, accesibilidad, entre otras relacionadas con el comportamiento observable por el usuario.
- **Testeo No Funcional:** Evalúa características del software que no están directamente relacionadas con su funcionalidad específica, sino con su calidad y desempeño. Incluye:
    - **Testeo de Rendimiento (Performance Testing):** Evalúa la velocidad, capacidad de respuesta y estabilidad del sistema bajo diferentes cargas de trabajo (ej. testeo de carga, testeo de estrés, testeo de volumen).
    - **Testeo de Seguridad (Security Testing):** Identifica vulnerabilidades y riesgos de seguridad en el software para proteger los datos y recursos del acceso no autorizado.
    - **Testeo de Usabilidad (Usability Testing):** Mide la facilidad con la que los usuarios pueden utilizar el sistema para lograr sus objetivos de manera efectiva, eficiente y satisfactoria.
    - **Testeo de Compatibilidad (Compatibility Testing):** Verifica que el software funciona correctamente en diferentes entornos (sistemas operativos, navegadores, dispositivos, bases de datos).
    - **Testeo de Fiabilidad (Reliability Testing):** Evalúa la capacidad del software para mantener su rendimiento en condiciones específicas durante un período de tiempo determinado.
    - **Testeo de Mantenibilidad (Maintainability Testing):** Evalúa la facilidad con la que el software puede ser modificado, corregido o adaptado.
    - **Testeo de Portabilidad (Portability Testing):** Verifica la capacidad del software para ser transferido de un entorno a otro.

**4. Por la Ejecución:** Se refiere a cómo se llevan a cabo las pruebas.

- **Testeo Manual:** Las pruebas son ejecutadas manualmente por un tester sin la ayuda de herramientas de automatización.
- **Testeo Automatizado:** Se utilizan herramientas de software para ejecutar casos de prueba, comparar los resultados con los esperados e informar sobre los resultados. Es especialmente útil para pruebas repetitivas como las de regresión.

**5. Por la Asociación con el Cambio:** Este criterio se relaciona con las pruebas realizadas después de realizar modificaciones en el software.

- **Testeo de Regresión (Regression Testing):** Consiste en re-ejecutar pruebas existentes para asegurar que los cambios realizados en el software no han introducido nuevos defectos en funcionalidades que antes funcionaban correctamente o no han afectado negativamente a otras partes del sistema.
- **Testeo de Confirmación (Re-testing):** Se realiza después de que se ha corregido un defecto para confirmar que el defecto ha sido eliminado satisfactoriamente y que la corrección no ha causado efectos secundarios no deseados.

**6. Por el Enfoque o Experiencia:** Algunas técnicas dependen en gran medida de la habilidad y el conocimiento del tester.

- **Testeo Exploratorio (Exploratory Testing):** Es un enfoque donde el diseño, la ejecución y el aprendizaje de las pruebas se realizan de forma simultánea. El tester utiliza su experiencia y creatividad para explorar el software, identificar áreas de riesgo y diseñar pruebas sobre la marcha.

Es importante destacar que estas categorías no son mutuamente excluyentes y una técnica de testeo particular puede clasificarse bajo varios criterios simultáneamente. Por ejemplo, un test unitario puede ser de caja blanca y manual o automatizado. La elección de las técnicas de testeo a aplicar dependerá de diversos factores como los requisitos del proyecto, el modelo de desarrollo adoptado, el presupuesto, el cronograma y los riesgos identificados.

![[Pasted image 20250506131016.png]]
---
#### Referencias
