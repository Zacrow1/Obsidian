## 1. Construcción de la Tabla de Distribución de Probabilidad

### 1.1. Frecuencia de Cada Valor de X
La frecuencia de cada valor de la variable aleatoria discreta X (nivel educativo de los padres) se calculó contando el número de ocurrencias de cada nivel educativo en el conjunto de datos. Esto se realizó utilizando la función `value_counts()` de Pandas.
  
```python

education_counts = df['education_level'].value_counts().sort_index()

``` 

La frecuencia representa la cantidad de veces que un valor específico de la variable X aparece en el conjunto de datos. Es un paso fundamental para entender la distribución de los datos.

### 1.2. Frecuencia Relativa (Probabilidad) de Cada Valor de X
La frecuencia relativa, o probabilidad, de cada valor de X se calculó dividiendo la frecuencia de cada valor por el número total de observaciones en el conjunto de datos. Esto se realizó dividiendo la serie `education_counts` por la longitud del DataFrame `df`.

```python

education_probabilities = education_counts / len(df)

```

La frecuencia relativa representa la proporción de veces que un valor específico de la variable X aparece en el conjunto de datos. Es una estimación de la probabilidad de observar ese valor en una muestra aleatoria de la misma población.

### 1.3. Verificación de la Suma de Probabilidades
Se verificó que la suma de las probabilidades sea igual a 1 para asegurar que la distribución de probabilidad sea válida.

```python

probability_sum = probability_table['P(X)'].sum()

```

Una distribución de probabilidad válida debe cumplir con la condición de que la suma de las probabilidades de todos los posibles valores de la variable aleatoria sea igual a 1. Esto asegura que se cubren todos los posibles resultados.

## 2. Representación Gráfica de la Distribución de Probabilidad
Se utilizó un diagrama de barras para representar visualmente la distribución de probabilidad. El eje X representa los niveles educativos (valores de X) y el eje Y representa las probabilidades (frecuencias relativas).

![[education_probability_distribution.png]]
## 3. Cálculo del Valor Esperado E(X) 
El valor esperado E(X) se calculó como la suma de los productos de cada valor de X por su probabilidad correspondiente.

```python

expected_value = (probability_table['X'] * probability_table['P(X)']).sum()

```

El valor esperado representa el promedio ponderado de los posibles valores de la variable aleatoria. En este contexto, representa el nivel educativo promedio de los padres en el conjunto de datos, ponderado por la probabilidad de cada nivel.

## 4. Cálculo de la Varianza Var(X)
La varianza Var(X) se calculó como la suma de los productos de los cuadrados de las diferencias entre cada valor de X y el valor esperado, por su probabilidad correspondiente.

```python

variance = ((probability_table['X'] - expected_value)**2 * probability_table['P(X)']).sum()

```

La varianza mide la dispersión de los valores de la variable aleatoria alrededor del valor esperado. En este contexto, representa la variabilidad en los niveles educativos de los padres en el conjunto de datos.
  
## 5. Cálculo de la Probabilidad P(X ≤ 3)
La probabilidad de que X sea menor o igual a 3 se calculó sumando las probabilidades de todos los valores de X que son menores o iguales a 3.

```python

probability_lte_3 = probability_table[probability_table['X'] <= 3]['P(X)'].sum()

```

Esta probabilidad representa la proporción de padres en el conjunto de datos que tienen un nivel educativo de "some college", "associate's degree", "high school" o "some high school".

## 5. Resultados del Análisis
### 5.1. Tabla de Distribución de Probabilidad:
|   X |   P(X) |
| --: | -----: |
|   1 |  0.226 |
|   2 |  0.222 |
|   3 |  0.196 |
|   4 |  0.179 |
|   5 |  0.118 |
|   6 |  0.059 |
### 5.2. Suma de Probabilidades: 1.0
### 5.3. Valor Esperado E(X): 2.918
### 5.4. Varianza Var(X): 2.301276
### 5.5. Probabilidad P(X ≤ 4): 0.644


