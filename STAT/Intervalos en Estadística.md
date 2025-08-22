---
tags:
  - Math
  - Universidad
Creado: 2025-05-05
Relacionado:
  - Statistics
---
## Intervalos en Estadística

Los intervalos (también llamados **clases** o **bins**) son rangos de valores que se utilizan para agrupar datos cuantitativos continuos o discretos en categorías. Son fundamentales para organizar grandes conjuntos de datos y facilitar su análisis.

---

### **¿Para qué sirven?**  
1. Simplificar datos numéricos continuos.  
2. Crear tablas de frecuencias agrupadas.  
3. Visualizar distribuciones mediante histogramas.  

---

### **Componentes de un Intervalo**  
Cada intervalo se define por:  
1. **Límite inferior (LI):** Valor mínimo del intervalo.  
2. **Límite superior (LS):** Valor máximo del intervalo.  
3. **Amplitud (A):** Tamaño del intervalo, calculado como \( A = LS - LI \).  
4. **Marca de clase (MC):** Punto medio del intervalo:  
   $$
   MC = \frac{LI + LS}{2}
   $$

**Ejemplo:**  
- Intervalo: `10-19`  
- LI = 10, LS = 19  
- Amplitud: \( 19 - 10 = 9 \) (si los datos son enteros).  
- Marca de clase: $( \frac{10 + 19}{2} = 14.5 )$.

---

### **Pasos para Crear Intervalos**  
1. **Calcular el rango:**  
   \[
   Rango = \text{Valor máximo} - \text{Valor mínimo}
   \]  
   Ejemplo: Si los datos van de 5 a 50 → Rango = 45.  

2. **Decidir el número de intervalos:**  
   - **Regla de Sturges:** $( k = 1 + 3.322 \cdot \log_{10}(n) )$, donde $( n )$ = total de datos.  
   - Por convención, se usan entre 5 y 20 intervalos.  

3. **Calcular la amplitud aproximada:**  
   $$
   A = \frac{\text{Rango}}{k}
   $$ 
   Ejemplo: Si \( k = 5 \) y rango = 45 → \( A = 9 \).  

4. **Definir los intervalos:**  
   - Comenzar desde el valor mínimo.  
   - Asegurarse de que no haya superposición.  

**Ejemplo:**  
- Datos: `5, 10, 15, ..., 50`  
- Intervalos:  
  `5-14`,  
  `15-24`,  
  `25-34`,  
  `35-44`,  
  `45-54`.  

---

### **Tipos de Intervalos**  
1. **Abiertos vs. Cerrados:**  
   - **Cerrados:** Ambos límites están incluidos (ej: `[10-20]`).  
   - **Abiertos:** Un límite no está incluido (ej: `10-20`, donde 20 es excluido).  

2. **De igual vs. desigual amplitud:**  
   - **Igual amplitud:** Recomendado para datos uniformes.  
   - **Desigual amplitud:** Útil cuando hay valores atípicos o distribuciones asimétricas.  

---

### **Aplicación en Tablas de Frecuencia**  
Ejemplo de **tabla de frecuencias agrupadas**:  

| Intervalo   | Frecuencia Absoluta (FA) | Marca de Clase (MC) |  
|-------------|---------------------------|---------------------|  
| 10-19       | 8                         | 14.5                |  
| 20-29       | 12                        | 24.5                |  
| 30-39       | 5                         | 34.5                |  

---

### **Errores Comunes**  
1. **Intervalos superpuestos:** Ej: `10-20` y `20-30` (el 20 aparece en ambos).  
2. **Amplitud demasiado grande:** Oculta patrones en los datos.  
3. **Amplitud demasiado pequeña:** Genera intervalos vacíos o poco informativos.  

---

### **Consideraciones Clave**  
- Los intervalos deben ser **mutuamente excluyentes** y **colectivamente exhaustivos**.  
- La elección de intervalos afecta la interpretación de histogramas y medidas estadísticas.  

## Marcas de Clase  

### **¿Qué son?**  
La **marca de clase** (también llamada *punto medio del intervalo*) es el valor central de un intervalo en una tabla de datos agrupados. Representa numéricamente a todo el intervalo y se usa para cálculos estadísticos como la media o la varianza.  

---

### **Fórmula**  
\[
\text{Marca de Clase} = \frac{\text{Límite inferior} + \text{Límite superior}}{2}
\]  

---

### **Ejemplo Práctico**  
**Datos agrupados:**  
- Intervalo: `10-19`  
- Límite inferior (LI) = 10  
- Límite superior (LS) = 19  

**Cálculo:**  
$$
\text{Marca de Clase} = \frac{10 + 19}{2} = 14.5
$$

---

### **Características**  
1. **Representatividad:** Es el valor que "sustituye" a todo el intervalo en operaciones matemáticas.  
2. **Amplitud constante:** Si los intervalos tienen la misma amplitud, las marcas de clase estarán equidistantes.  
3. **Uso en gráficos:** Se usan como eje horizontal en histogramas para mostrar la distribución.  

---

### **Tabla de Ejemplo con Marcas de Clase**  
| Intervalo   | Límite Inferior | Límite Superior | Marca de Clase | Frecuencia |  
|-------------|-----------------|-----------------|----------------|------------|  
| 10-19       | 10              | 19              | 14.5           | 8          |  
| 20-29       | 20              | 29              | 24.5           | 12         |  
| 30-39       | 30              | 39              | 34.5           | 5          |  

---

### **Pasos para Calcular Marcas de Clase**  
1. **Identificar los límites:**  
   - Asegúrate de que los intervalos estén bien definidos (ej: `10-19`, `20-29`, etc.).  
2. **Aplicar la fórmula:**  
   - Suma los límites y divide entre 2.  
3. **Verificar consistencia:**  
   - Si hay intervalos con distinta amplitud, recalcula cada marca individualmente.  

---

### **Errores Comunes**  
- **Confundir límites reales con aparentes:**  
  - Si el intervalo es `10-19`, los límites reales son 10 y 19 (si son enteros).  
  - En datos continuos, los límites reales podrían ser `10 ≤ x < 20`.  
- **Usar la marca de clase como dato real:**  
  - Es una aproximación, no el valor exacto de los datos originales.  

---

### **Aplicaciones Clave**  
1. **Cálculo de la media aritmética para datos agrupados:**  
   \[
   \bar{x} = \frac{\sum (MC \cdot F_i)}{N}
   \]  
   Donde:  
   - \( MC \) = Marca de Clase.  
   - \( F_i \) = Frecuencia del intervalo.  
   - \( N \) = Total de datos.  

2. **Cálculo de varianza y desviación estándar:**  
   \[
   \sigma^2 = \frac{\sum (MC^2 \cdot F_i)}{N} - \bar{x}^2
   \]  

---

### **Ejemplo Completo**  
**Datos agrupados (edades):**  
| Intervalo   | Frecuencia (F_i) | Marca de Clase (MC) | MC · F_i |  
|-------------|-------------------|---------------------|----------|  
| 10-19       | 8                 | 14.5                | 116      |  
| 20-29       | 12                | 24.5                | 294      |  
| 30-39       | 5                 | 34.5                | 172.5    |  
| **Total**   | 25                |                     | **582.5**|  

**Media (\(\bar{x}\)):**  
$$
\bar{x} = \frac{582.5}{25} = 23.3 \text{ años}
$$  



---
#### Referencias
