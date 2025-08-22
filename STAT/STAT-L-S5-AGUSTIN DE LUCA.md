---
tags:
  - Math
  - Universidad
  - Universidad/Laboratorio
Creado: 2025-05-27
Relacionado:
  - Statistics
completado:
---
# Informe de Análisis del Rendimiento Académico de Estudiantes

## 1. Histograma de 'math score'
Se creó un histograma de los puntajes en matemáticas para visualizar su distribución. El histograma muestra una forma que se asemeja a una campana, con la mayoría de los puntajes concentrados alrededor de la media.

  ![[histograma_math_score 2.png]]

### Análisis de la distribución:
La distribución de los puntajes en matemáticas se puede considerar aproximadamente normal debido a las siguientes razones:

*   Forma de campana: El histograma se asemeja a la forma de campana característica de una distribución normal.

*   Simetría: La distribución es aproximadamente simétrica alrededor de la media, lo que indica que los puntajes se distribuyen de manera similar por encima y por debajo de la media.

*   Concentración central: La mayoría de los puntajes se concentran alrededor de la media, lo que es otra característica de una distribución normal.

El histograma se generó utilizando la biblioteca `matplotlib.pyplot` de Python. Se utilizó la función `hist()` para crear el histograma y la función `plot()` para superponer la curva de distribución normal. La curva de distribución normal se ajustó a los datos utilizando la función `norm.fit()` de la biblioteca `scipy.stats`.

Se generó un archivo de imagen llamado `histograma_math_score.png` que contiene el histograma con la curva de distribución normal superpuesta.

## 2. Estadísticos descriptivos
Se calcularon los siguientes estadísticos descriptivos para la variable 'math score':

*   Media: 66.09

*   Desviación estándar: 15.16

La media se calculó utilizando la función `mean()` de la biblioteca `pandas`. La desviación estándar se calculó utilizando la función `std()` de la biblioteca `pandas`.

## 3. Cálculo de probabilidades  
Se definió la variable aleatoria X como el puntaje en matemáticas y se asumió una distribución normal con los parámetros obtenidos en el paso anterior (media = 66.09, desviación estándar = 15.16). Con base en esta suposición, se calcularon las siguientes probabilidades:

*   P(x <= 70): 0.6018 (probabilidad de que un estudiante saque 70 puntos o menos)

*   P(80 <= x <= 90): 0.1220 (probabilidad de que un estudiante tenga una calificación entre 80 y 90 puntos)

Las probabilidades se calcularon utilizando la función `norm.cdf()` de la biblioteca `scipy.stats`. Esta función calcula la función de distribución acumulativa (CDF) de una distribución normal. La probabilidad P(x <= 70) se calculó como `norm.cdf(70, mu, std)`, donde `mu` es la media y `std` es la desviación estándar. La probabilidad P(80 <= x <= 90) se calculó como la diferencia entre `norm.cdf(90, mu, std)` y `norm.cdf(80, mu, std)`.

## 4. Puntaje mínimo para beca
Se calculó el puntaje mínimo requerido para estar en el percentil 90 o superior, que corresponde a los estudiantes que recibirán becas. El puntaje mínimo requerido es:

*   Puntaje mínimo para beca (percentil 90): 85.51

El puntaje mínimo para la beca se calculó utilizando la función `norm.ppf()` de la biblioteca `scipy.stats`. Esta función calcula la función de percentil (o función inversa de la CDF) de una distribución normal. El puntaje mínimo para la beca se calculó como `norm.ppf(0.90, mu, std)`, que devuelve el valor de x para el cual la CDF es igual a 0.90 (es decir, el percentil 90).