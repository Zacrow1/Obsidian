---
tags:
  - Universidad
  - Universidad/Laboratorio
  - Math
Creado: 2025-05-27
Relacionado:
  - Statistics
completado:
---
# Informe de Análisis de Partidas de League of Legends

Este informe presenta un análisis detallado de partidas de League of Legends, utilizando la base de datos "LeagueofLegends.csv". Se exploran diversos aspectos del juego, incluyendo la duración de las partidas, las tasas de victoria, los patrones de selección de campeones, la dinámica de la diferencia de oro y se aplican conceptos básicos de probabilidad.

---

## 1. Histograma de Duración de Partidas

![[gamelength_histogram.png]]

**Uso:**
El histograma visualiza la distribución de la duración de las partidas, mostrando la frecuencia de juegos para diferentes rangos de tiempo.

**Análisis:**
La duración promedio de una partida es de aproximadamente 37.01 minutos. La mayoría de los juegos se concentran notablemente entre los 30 y 45 minutos. La forma del histograma sugiere que, si bien hay una duración típica, existen partidas que se desvían hacia tiempos más cortos o más largos, aunque con menor frecuencia. Esto indica una duración estándar competitiva pero con variabilidad.

---

## 2. Diagrama de Barras de Campeones Más Elegidos

![[top_champions_barchart.png]]

**Uso:**
Este gráfico identifica a los campeones más populares basándose en su frecuencia de selección en las partidas analizadas.

**Análisis:**
Gragas fue el campeón más elegido con una frecuencia de 2555 apariciones, representando un 3.35% del total de selecciones. Le siguen RekSai (3.06%) y Braum (2.78%). La prominencia de estos campeones en el top 10 sugiere que eran opciones particularmente fuertes o muy valoradas dentro del metajuego competitivo durante el período cubierto por este conjunto de datos.

---

## 3. Diagrama Circular de Tasas de Victoria

![[win_rate_piechart.png]]

**Uso:**
El diagrama circular ilustra la distribución porcentual de las victorias entre el equipo azul y el equipo rojo.

**Análisis:**
El equipo azul ganó el 54.41% de las partidas analizadas, mientras que el equipo rojo ganó el 45.59%. Esta diferencia indica una ligera ventaja histórica para el equipo que juega en el lado azul del mapa en este conjunto de datos. Esta disparidad podría estar influenciada por el diseño simétrico pero no idéntico del mapa de League of Legends o por factores estratégicos relacionados con la elección de lado en el formato competitivo.

---

## 4. Diagrama de Cajas de Duración por Liga

![[gamelength_by_league_boxplot.png]]

**Uso:**
Este diagrama compara la distribución de la duración de las partidas en las ligas con mayor representación en el conjunto de datos, mostrando medianas, cuartiles y valores atípicos para cada liga.

**Análisis:**
Las medianas de duración de partida son bastante consistentes entre las principales ligas representadas (LCK, NALCS, EULCS, LMS, TCL). Sin embargo, los rangos intercuartílicos y la extensión de los "bigotes" de las cajas varían, lo que indica diferencias en la dispersión de la duración de las partidas entre regiones. Esto podría reflejar distintos estilos de juego o enfoques estratégicos que llevan a partidas ligeramente más rápidas o más lentas en ciertas ligas, así como una mayor o menor predictibilidad en la duración del juego.

---

## 5. Gráfico de Dispersión de Asesinatos

![[kills_blue_vs_red_scatterplot.png]]

**Uso:**
El scatterplot muestra la relación entre el número de asesinatos conseguidos por el equipo azul y el equipo rojo en cada partida individual.

**Análisis:**
El gráfico revela una fuerte correlación positiva entre los asesinatos de ambos equipos. Los puntos tienden a agruparse a lo largo de una línea diagonal, lo que indica que las partidas con un alto número de asesinatos para un equipo suelen ser también partidas con un alto número de asesinatos para el equipo contrario. Esto sugiere que los juegos agresivos o con muchas peleas son una característica de la partida en sí, en lugar de ser el resultado de la dominación unilateral de un equipo. No se observan muchos puntos donde un equipo tiene una cantidad extremadamente alta de asesinatos y el otro una cantidad muy baja.

---

## 6. Diagrama de Barras de Tipos de Dragones

![[dragon_types_barchart.png]]

**Uso:**
Este gráfico de barras muestra la frecuencia con la que el equipo azul obtuvo cada tipo de dragón elemental y el Dragón Ancestral.

**Análisis:**
El análisis de este gráfico dependerá de los resultados visuales obtenidos. Si los colores y el orden son correctos, se describirá la frecuencia de cada tipo de dragón, identificando cuáles fueron los más o menos obtenidos. Esto puede reflejar prioridades estratégicas en el control de objetivos durante el metajuego del período de los datos, o simplemente la distribución natural de la aparición de dragones elementales.

---

## 7. Análisis de la Diferencia de Oro en Momentos Clave

**Uso:**
Este análisis se centra en la diferencia de oro entre los equipos en puntos específicos de la partida, como el minuto 10, proporcionando una métrica temprana del estado del juego.

**Análisis:**
La diferencia de oro en el minuto 10 (`golddiff_at_10`) tiene una media de 86.89, lo que sugiere que, en promedio, los equipos están bastante igualados en términos de oro al inicio de la partida. Sin embargo, la desviación estándar extremadamente alta (1295.16) y el amplio rango de valores (de -7300 a 7307) son indicadores clave. Esto demuestra que, aunque el punto de partida sea equilibrado en promedio, las partidas pueden divergir significativamente muy pronto, con un equipo obteniendo una ventaja de oro sustancial o cayendo en una desventaja considerable a los 10 minutos. Esto resalta la importancia del juego temprano y la volatilidad potencial en las primeras etapas.

---

## 8. Aplicación de Conceptos de Probabilidad

Utilizando las frecuencias observadas en los datos, se calcularon varias probabilidades que ofrecen una perspectiva cuantitativa sobre ciertos eventos del juego. La probabilidad general de que el equipo azul gane una partida se estima en un 54.41%, mientras que para el equipo rojo es del 45.59%. Un hallazgo interesante de la probabilidad condicional es que si el equipo azul consigue la primera sangre del juego, su probabilidad de victoria aumenta notablemente al 65.61%. Además, la probabilidad de que el campeón Gragas, identificado como el más común, sea elegido en una oportunidad de selección particular es del 3.35%. Estas cifras ilustran cómo ciertos eventos o selecciones están asociados con diferentes probabilidades de éxito o aparición basándose en este conjunto de datos histórico.

---

## Conclusiones Detalladas

Este análisis estadístico de las partidas de League of Legends, basado en el conjunto de datos "LeagueofLegends.csv", ha revelado varios patrones y características importantes del juego. La duración de las partidas muestra una clara concentración alrededor de la media de 37 minutos, aunque con suficiente variabilidad para incluir juegos más rápidos o más largos. La distribución de victorias presenta una ligera inclinación hacia el equipo azul. Los datos sobre la selección de campeones destacan a Gragas como el más popular, reflejando probablemente su fuerza o relevancia en el metajuego analizado. Aunque la diferencia de oro inicial tiende a ser baja en promedio, la alta dispersión indica que es común que se establezcan ventajas económicas significativas temprano en la partida. La correlación positiva en los asesinatos subraya que los juegos con mucha acción involucran activamente a ambos equipos. Finalmente, la aplicación de conceptos de probabilidad cuantifica hallazgos como la ventaja del lado azul y el impacto positivo de obtener la primera sangre en la probabilidad de victoria. Estos resultados proporcionan una visión valiosa sobre la dinámica competitiva y los factores que pueden influir en el resultado de una partida de League of Legends dentro de este conjunto de datos.
