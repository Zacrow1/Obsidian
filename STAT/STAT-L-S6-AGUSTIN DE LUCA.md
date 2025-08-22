# Análisis de Distribución de Pesos y Teorema del Límite Central

Se realizó analizando la variable Weight (Peso). Para el análisis, se tomaron 1000 muestras aleatorias con reemplazo para cada uno de los siguientes tamaños muestrales: n = 5, n = 10 y n = 50. Esto permite observar cómo evoluciona la distribución de las medias muestrales a medida que aumenta el tamaño de la muestra.

## Análisis de la Distribución Original
La distribución original de los pesos muestra una distribución asimétrica, lo cual es esperado en datos de peso corporal. Esta distribución inicial servirá como base para comparar cómo evoluciona la forma de la distribución al tomar muestras de diferentes tamaños.

![Distribución Original](histograma_original.png)

## Análisis de Muestras
### Muestras de tamaño n = 5
Con muestras de tamaño pequeño (n=5), la distribución de las medias muestrales aún mantiene cierta asimetría, aunque menos pronunciada que la distribución original. Esto sugiere que con muestras tan pequeñas, el Teorema del Límite Central aún no ha tenido un efecto significativo en la forma de la distribución.

![Distribución n=5](histograma_n5.png)

### Muestras de tamaño n = 10
Al aumentar el tamaño muestral a n=10, se observa una tendencia hacia la simetría en la distribución de las medias muestrales. La forma de la distribución comienza a mostrar características más cercanas a una distribución normal, aunque aún mantiene algunas desviaciones.

![Distribución n=10](histograma_n10.png)

### Muestras de tamaño n = 50
Con muestras de tamaño n=50, la distribución de las medias muestrales muestra una clara tendencia hacia la normalidad, evidenciando el Teorema del Límite Central en acción. La forma de la distribución se ha vuelto notablemente simétrica y presenta las características típicas de una distribución normal.

![Distribución n=50](histograma_n50.png)

## Se utilizaron las siguientes fórmulas:

La media muestral se calculó utilizando la fórmula:
$$
\bar{x} = \frac{1}{n}\sum_{i=1}^{n} x_i
$$

Para la desviación estándar muestral se empleó:
$$ 
s = \sqrt{\frac{1}{n-1}\sum_{i=1}^{n} (x_i - \bar{x})^2}
$$

## Conclusiones
El análisis realizado proporciona una evidencia clara y contundente del Teorema del Límite Central en acción. A medida que aumentamos el tamaño de las muestras, observamos una transformación gradual en la distribución de las medias muestrales. Con muestras pequeñas (n=5), la distribución mantiene una asimetría notable, reflejando aún las características de la distribución original. Sin embargo, al incrementar el tamaño muestral a n=10, comienza a manifestarse una tendencia hacia la simetría, aunque con algunas desviaciones.

El cambio más significativo se observa con muestras de tamaño n=50, donde la distribución de las medias muestrales se aproxima notablemente a una distribución normal. Esta transformación no solo se manifiesta en la forma de la distribución, sino también en la reducción de la variabilidad, lo cual es consistente con la fórmula

$$\sigma_{\bar{x}} = \frac{\sigma}{\sqrt{n}}$$

La prueba de Shapiro-Wilk confirma esta aproximación a la normalidad, mostrando valores de p-valor que aumentan con el tamaño muestral, indicando una mayor compatibilidad con la distribución normal. Este comportamiento tiene importantes implicaciones prácticas para la inferencia estadística, ya que nos permite realizar inferencias sobre la media poblacional incluso cuando la distribución original no es normal.

Este análisis demuestra de manera empírica la importancia fundamental del Teorema del Límite Central en la estadística inferencial. Proporciona una base teórica sólida para la construcción de intervalos de confianza y la realización de pruebas de hipótesis, herramientas esenciales en el análisis estadístico moderno.

