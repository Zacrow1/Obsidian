1. Buenas tardes a todos Somos TEST MASTERS, vamos a presentarles nuestro análisis y resultados del testing de la plataforma Actio. Nuestro equipo está conformado por Agustín De Luca, Guido Mamaní, Mateo Escobar, Mateo Olarte, Richard Choque, Santiago Uribe y Thiago Hinojosa.
2. Aca tenemos un vistazo general de lo que vamos a cubrir hoy. Iniciaremos explicando qué es Actio, luego pasaremos a los objetivos de nuestro testing y la estrategia que implementamos. También detallaremos nuestro alcance. Finalmente, presentaremos los reportes de features, el reporte general y el reporte de bugs y mejoras ahora mi compañero Guido les contara que es actio
3. -
4. -
5. -
6. -
7. Nuestras pruebas cubrieron aspectos funcionales críticos como la creación de eventos, el registro y el inicio de sesión de usuarios, la administración de Workspace y la funcionalidad de búsqueda de eventos. También nos centramos en aspectos no funcionales como el rendimiento y la seguridad. Verificamos la interfaz de usuario, prestando especial atención a validaciones de campos obligatorios, gestión de permisos, consistencia de mensajes de error y restricciones de acceso. Además, realizamos pruebas de rendimiento para asegurar tiempos de respuesta adecuados y la resiliencia del sistema ante interrupciones. Nuestro objetivo final es garantizar que Actio funcione según las especificaciones, ofreciendo una experiencia de usuario estable, segura y predecible en diversos escenarios.
8. -
9. -
10. Para la creación de eventos múltiples, este tipo de evento consta de varias actividades con un calendario establecido. En basic info, ingresamos el nombre del evento en la sección de 'Details' se solicita una descripción, si el evento es público o privado, y una imagen, siendo todos estos campos opcionales. Finalmente, en un evento múltiple, la creación de actividades que tienen un nombre, una descripcion una imagen. Los resultados muestran 20 casos pasados, 3 bloqueados y 1 fallido.

> [!bug]
    > Uno de los bugs críticos que encontramos se relaciona con la creación de actividades dentro del formulario de un evento múltiple. Al hacer clic de forma repetida y rápida en el botón 'Guardar Actividad', el sistema crea la misma actividad dos veces, generando duplicados exactos dentro del evento. Se espera que, sin importar la cantidad o velocidad de clics, la actividad se cree solo una vez. Pueden ver los pasos detallados para reproducirlo en la diapositiva.


🔹 Scripted Testing
Definición: pruebas guionadas, con pasos y datos definidos por adelantado.

Objetivo: confirmar que el software cumple los requerimientos.

Características: predecibles, repetibles, ideales para testers sin experiencia.

🧪 Ejemplo: seguir un paso a paso para crear un usuario y verificar mensaje de éxito.

🔹 Exploratory Testing (repaso)
Pruebas no estructuradas, más libres e intuitivas.

Se descubren errores explorando el sistema sin un guion fijo.

🔹 Test Case (caso de prueba)
Contiene: ID, título, descripción, requerimientos, pasos, resultados esperados, estado.

Organizados en Test Suites.

🔹 Tipos de pruebas
Funcionales: confirman funciones.

No funcionales: rendimiento, seguridad, usabilidad.

Positivas: entradas válidas.

Negativas: entradas inválidas para probar robustez.

🗓 Semana 3 – Risk-Based Testing (RBT)
📄 Documento: SQE2_Week3.pdf

🔹 Riesgo
Riesgo = probabilidad × impacto de que algo falle.

Se prioriza lo más riesgoso para probarlo primero.

🔹 RBT (Testing basado en riesgos)
Objetivo: optimizar recursos y encontrar defectos críticos temprano.

Tipos de riesgo:

Del producto: errores, mal rendimiento, bugs visibles.

Del proyecto: retrasos, mal uso de herramientas, falta de gente.

🧪 Ejemplo: si falla la creación de eventos, tiene alto impacto → se testea con prioridad.

🔹 Proceso RBT
Identificar riesgos

Analizar impacto y probabilidad

Priorizar

Mitigar o prevenir

Crear test cases dirigidos al riesgo

Repetir y ajustar

🗓 Semana 4 – Domain Testing
📄 Documento: SQE2_Week4_v3.pdf

🔹 Domain Testing
Método para reducir la cantidad de pruebas necesarias dividiendo entradas en clases.

Se enfoca en entradas y límites.

🔹 Partición de Equivalencia (EC)
Divide valores de entrada en grupos válidos/invalidos.

Se testea un valor representativo por grupo.

🧪 Ejemplo: edad aceptada (18–65) → testear 20 y -1.

🔹 Boundary Value Analysis (BVA)
Se prueban los valores en el límite de aceptación.

🧪 Ejemplo: para nombre de usuario (5–20 letras) → probar 4, 5, 20, 21.

🔹 Tipos de variables
Numéricas (int, float)

Categóricas (colores, roles)

Booleanas (sí/no)

Ordinales (nivel: bajo, medio, alto)

🔹 Escalas de medición
Nominal: sin orden (navegador)

Ordinal: con orden (satisfacción)

Intervalo: sin cero absoluto (temperatura)

Razón: con cero absoluto (tamaño archivo)

🗓 Semana 5 – Combinatorial Testing
📄 Documento: SQE2_Week5_v3.pdf

🔹 ¿Qué es?
Técnica para probar múltiples combinaciones de valores de entrada.

Se enfoca en fallas por interacción entre variables.

🔹 Pairwise Testing
Asegura que cada par de valores posibles sea testeado al menos una vez.

Reduce cantidad de test cases manteniendo buena cobertura.

🔹 Diseño ortogonal
Método para seleccionar combinaciones de valores de forma balanceada.

🔹 Ventajas
Reduce esfuerzo sin perder calidad.

Detecta errores que solo ocurren cuando se combinan valores específicos.

🧪 Ejemplo: reserva de vuelos:
Origen × Destino × Clase × Método de pago

En vez de probar las 81 combinaciones posibles, usás 10–15 seleccionadas inteligentemente.

🗓 Semana 6 – Introducción a los Errores (Parte I)
📄 Documento: SQE2_Week6_v4.pdf

🔹 Términos clave
Error: humano (ej. mal interpretar un requerimiento).

Defecto: problema en el código.

Falla: consecuencia en el sistema.

Bug: cuando el software se comporta mal por alguno de los anteriores.

🔹 Bug Advocacy
Habilidad de comunicar bien un bug para que se corrija.

Debe ser claro, con evidencia, reproducible, y mostrar impacto.

🔹 Reporte de bug
Contiene:

Título

Descripción clara

Requerimientos (ambiente, navegador, cuenta usada)

Pasos detallados

Resultado real vs esperado

Archivos adjuntos (capturas, logs)

🗓 Semana 7 – Gestión de Casos y Bugs (Parte II)
📄 Documento: SQE2_Week7_v3.pdf

🔹 Gestión de Test Cases
Planificar, organizar, ejecutar y registrar pruebas.

Agrupar test cases en Suites según propósito:

Smoke: pruebas básicas rápidas.

Regression: verificar que nada se rompió.

Hotfix/Patch: validar cambios urgentes o específicos.

🔹 Ciclo de vida de un test case
Diseñado

Ejecutado

Asociado a bug si falla

Validado y cerrado

🔹 Herramientas (TCMS)
Permiten gestionar test cases, ejecución y trazabilidad.

🔹 Gestión de Bugs
Ciclo de vida: nuevo → asignado → en progreso → resuelto → cerrado.

Cada bug se relaciona con uno o más test cases fallidos.

Se registra validación con evidencia.