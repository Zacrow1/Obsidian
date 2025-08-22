---
tags:
  - Math
  - Universidad
  - Universidad/Laboratorio
Creado: 2025-05-15
Relacionado:
  - Statistics
---

# LABORATORIO DE ESTADISTICA
### DESEMPENO ACADEMICO DE ESTUDIANTES

## INTRODUCCION

Este análisis evalúa las probabilidades empiricas relacionadas con el rendimiento
académico de estudiantes en diferentes areas. Se utilizan datos reales para calcular
las probabilidades solicitadas, mostrando tanto el proceso de calculo como los
resultados finales.

## DATOS UTILIZADOS

Columnas disponibles en el conjunto de datos:
- gender
- race/ethnicity
- parental level of education
- lunch
- test preparation course
- math score
- reading score
- writing score

Total de estudiantes en la muestra: 1000

Distribución por genero:
- female: 518 estudiantes (51.8%)
- male: 482 estudiantes (48.2%)

Distribución por nivel educativo de los padres:
- some college: 226 estudiantes (22.6%)
- associate's degree: 222 estudiantes (22.2%)
- high school: 196 estudiantes (19.6%)
- some high school: 179 estudiantes (17.9%)
- bachelor's degree: 118 estudiantes (11.8%)
- master's degree: 59 estudiantes (5.9%)

## ESTADISTICAS DESCRIPTIVAS DE PUNTAJES

Puntajes en matematicas:
- Promedio: 66.09
- Mediana: 66.00
- Desviación estándar: 15.16
- Mínimo: 0
- Máximo: 100

Puntajes en lectura:
- Promedio: 69.17
- Mediana: 70.00
- Desviacion estandar: 14.60
- Minimo: 17
- Maximo: 100

Puntajes en escritura:
- Promedio: 68.05
- Mediana: 69.00
- Desviacion estandar: 15.20
- Minimo: 10
- Maximo: 100

## ANALISIS DE PROBABILIDADES

**PREGUNTA 1:** ¿Cuál es la probabilidad de que un estudiante seleccionado al azar
obtenga mas de 72 puntos en matemáticas?

**RESPUESTA:**
- Evento A: Un estudiante obtiene mas de 72 puntos en matemáticas
- Casos favorables: 347 estudiantes
- Casos posibles: 1000 estudiantes
- Formula: P(A) = Casos favorables / Casos posibles = 347 / 1000
- Probabilidad: 0.3470 o 34.70%

 La probabilidad de que un estudiante obtenga mas de 72 puntos en matematicas es del 34.70%, lo que indica que aproximadamente uno de cada tres estudiantes supera este puntaje.

**PREGUNTA 2:** ¿Cuál es la probabilidad de que un estudiante seleccionado al azar
obtenga mas de 80 puntos tanto en matemáticas como en lectura?

**RESPUESTA:**
- Evento (A y B): Un estudiante obtiene mas de 80 puntos en matematicas Y mas de 80 puntos en lectura
- Casos favorables: 131 estudiantes
- Casos posibles: 1000 estudiantes
- Formula: P(A y B) = Casos favorables / Casos posibles = 131 / 1000
- Probabilidad: 0.1310 o 13.10%

La probabilidad de que un estudiante obtenga mas de 80 puntos tanto en matematicas como en lectura es del 13.10%, lo que muestra que es un evento menos frecuente, presentandose aproximadamente en uno de cada ocho estudiantes.
   
**PREGUNTA 3:** Si se sabe que los padres del estudiante tienen como nivel educativo
"some college", determine la probabilidad de que el estudiante obtenga mas de 80
puntos en la prueba de matematicas.

**RESPUESTA:**
- Evento condicional: P(A|B) = Probabilidad de que un estudiante obtenga mas de 80 puntos
  en matematicas (A) DADO QUE sus padres tienen nivel educativo 'some college' (B)
- Estudiantes con padres con nivel 'some college' (B): 226
- Estudiantes con padres nivel 'some college' y >80 en matematicas (A y B): 39
- Formula: P(A|B) = P(A y B)/P(B) = 39 / 226
- Probabilidad condicional: 0.1726 o 17.26%

Para estudiantes cuyos padres tienen nivel educativo 'some college', la probabilidad de obtener mas de 80 puntos en matematicas es del 17.26%. Este valor es menor que la probabilidad general de obtener mas de 80 puntos en matematicas, lo que podria indicar que este nivel educativo no incrementa las probabilidades de obtener altos puntajes en matematicas.
