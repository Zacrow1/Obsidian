---
tags:
  - Math
  - Universidad
Creado: 2025-05-07
Relacionado:
  - Statistics
  - Programacion
completado:
---
# Estadística - MATH-233
### Tarea Semana 2
#### AGUSTIN DE LUCA

## **Análisis de Hábitos de Sueño y Estudio en Estudiantes**

## 1. Tabla de Frecuencias de Datos Agrupados de la Variable sleep_hours por Género

Para el análisis de la variable `sleep_hours`, se elaboraron tablas de frecuencias agrupadas por género, utilizando intervalos determinados a partir de los valores mínimos y máximos observados en los datos. Se utilizó una distribución uniforme de intervalos para garantizar una representación clara de los datos. Cada intervalo incluye la frecuencia absoluta y la correspondiente marca de clase, que representa el punto medio de cada rango.

### Tabla de Frecuencias para Female:

|     |  Interval   | Frequency | Midpoint |
| :-: | :---------: | :-------: | :------: |
|  0  | 3.2, 4.05)  |    10     |  3.625   |
|  1  | 4.05, 4.9)  |    36     |  4.475   |
|  2  | 4.9, 5.75)  |    91     |  5.325   |
|  3  | 5.75, 6.6)  |    129    |  6.175   |
|  4  | 6.6, 7.45)  |    106    |  7.025   |
|  5  | 7.45, 8.3)  |    69     |  7.875   |
|  6  | 8.3, 9.15)  |    33     |  8.725   |
|  7  | 9.15, 10.0) |     6     |  9.575   |

### Tabla de Frecuencias para Male:

|     |   Interval    | Frequency | Midpoint |
| :-: | :-----------: | :-------: | :------: |
|  0  |  3.3, 4.138)  |    16     |  3.7190  |
|  1  | 4.138, 4.975) |    41     |  4.5565  |
|  2  | 4.975, 5.813) |    107    |  5.3940  |
|  3  | 5.813, 6.65)  |    110    |  6.2315  |
|  4  | 6.65, 7.488)  |    94     |  7.0690  |
|  5  | 7.488, 8.325) |    81     |  7.9065  |
|  6  | 8.325, 9.163) |    19     |  8.7440  |
|  7  | 9.163, 10.0)  |     9     |  9.5815  |

## 2. Gráfico Adecuado para Visualizar la Tabla de Frecuencias

Con el propósito de representar gráficamente la distribución de las horas de sueño en cada grupo, se construyeron histogramas separados para mujeres y hombres. Estos gráficos permiten visualizar de manera intuitiva las frecuencias asociadas a cada intervalo de sueño. En el histograma correspondiente a las mujeres, se observa una distribución con un claro pico entre las 5.75 y 7.45 horas de sueño, mientras que el histograma de los hombres muestra una forma similar, aunque con una leve variación en la concentración de datos.

**Histograma por los géneros**
![[histogram_gender_comparison.png]]

El análisis comparativo entre hombres y mujeres en cuanto a sus hábitos de sueño permite observar tanto semejanzas como pequeñas diferencias. La media de horas de sueño en mujeres fue de 6.47 horas, mientras que en hombres fue de 6.44 horas. . Sin embargo, al observar la mediana, se nota que las mujeres presentan un valor de 6.40 horas, mientras que los hombres alcanzan una mediana de 6.50 horas, lo cual indica una leve tendencia a que los hombres duerman un poco más en términos de valor central.

 En ambos casos, la mayor parte de los estudiantes duerme entre cinco y ocho horas, sin diferencias significativas en la forma general de la distribución, aunque pueda haber ligeras variaciones individuales, los patrones de sueño entre géneros son altamente comparables dentro de esta muestra.

## 4. Diagrama de Dispersión y Correlación con Otra Variable Cuantitativa

Se seleccionó la variable `study_hours_per_day` como posible factor asociado a las horas de sueño. Se construyó un diagrama de dispersión que representa a cada estudiante como un punto en el plano, considerando en el eje horizontal las horas de sueño y en el eje vertical las horas de estudio. Este gráfico se utilizó para determinar si existe alguna relación visual o estadística entre ambas variables.

El diagrama de dispersión generado muestra una distribución de puntos bastante dispersa, sin una tendencia clara en ninguna dirección. Este resultado indica que no existe una relación lineal significativa entre el tiempo que los estudiantes dedican al sueño y el tiempo que invierten en el estudio.

**Diagrama de dispersión:**  
![Diagrama de dispersión](study_vs_sleep.png)
## Conclusiones

El análisis realizado permitió concluir que los hábitos de sueño entre hombres y mujeres en la muestra estudiada son prácticamente iguales, tanto en términos de media como de mediana, y muestran distribuciones similares. La mayoría de los estudiantes, sin importar el género, duerme entre cinco y ocho horas por noche. Por otro lado, al analizar la relación entre las horas de sueño y las horas de estudio, no se encontró evidencia de una correlación lineal significativa. Esto implica que ambas variables, dentro del contexto de esta muestra, pueden considerarse independientes.