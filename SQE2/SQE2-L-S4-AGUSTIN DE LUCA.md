#### Create Activity

You can add as many activities as you need.
##### Activity name

Pick a name that tells what your activity is about.

Title *

- Caractereres especiales no permitidos
- <= 15 >=100

## 📊 Tabla de Dominio: Activity Name (Agus)

> **Tipo:** Categórica Nominal

### Dimensión Primaria
| Variable             | Equivalencia de clases Caso válido | Equivalencia de clases Caso Inválido | Límites y casos especiales        |     |
| -------------------- | ---------------------------------- | ------------------------------------ | --------------------------------- | --- |
| Activity Name (Agus) | Cualquier cadena de texto no vacía | Vacío                                | 1 carácter, texto largo, espacios |     |
|                      |                                    |                                      |                                   |     |

### Dimensión Secun

|Variable|Equivalencia de clases Caso válido|Equivalencia de clases Caso Inválido|Límites y casos especiales|
|---|---|---|---|
|Activity Name (Agus)|Sin espacios extra|Solo espacios en blanco|Espacio al inicio o al final, doble espacio entre palabras|

## 📊 Tabla de Dominio: Presentation Level (Agus)

> **Tipo:** Categórica Ordinal

### Dimensión Primaria

|Variable|Equivalencia de clases Caso válido|Equivalencia de clases Caso Inválido|Límites y casos especiales|
|---|---|---|---|
|Presentation Level (Agus)|"Básico", "Intermedio", "Avanzado"|Cualquier otro valor, o vacío|Diferencias de mayúsculas/minúsculas (ej: "básico", "BASICO")|

### Dimensión Secundaria

|Variable|Equivalencia de clases Caso válido|Equivalencia de clases Caso Inválido|Límites y casos especiales|
|---|---|---|---|
|Presentation Level (Agus)|Sin espacios extra|Solo espacios en blanco, caracteres especiales|Espacio al inicio o al final, tabulaciones, salto de línea|


| Variable      | Equivalencia de clases Caso válido                                                                 | Equivalencia de clases Caso Inválido                                                | Límites y casos especiales                                     |
| ------------- | -------------------------------------------------------------------------------------------------- | ----------------------------------------------------------------------------------- | -------------------------------------------------------------- |
|               | **Dimensión Primaria**                                                                             |                                                                                     |                                                                |
| Activity Name | Cadena alfanumérica y los caracteres permitidos `[]()~_.-@¿?!#"` de longitud **15-100 caracteres** | Cadena con longitud menor a 15 o mayor a 100 caracteres, o caracteres no permitidos | Longitud mínima: **15**, máxima: **100**                       |
|               | **Dimensión Secundaria**                                                                           |                                                                                     |                                                                |
| Activity Name | Sin espacios al inicio ni al final. Solo caracteres válidos                                        | Cadena vacía, solo espacios, caracteres especiales no permitidos                    | Ejemplo inválido: `¿ ñ Ñ 12` — Ejemplo válido: `Actividad 123` |

| Variable               | Equivalencia de clases Caso válido          | Equivalencia de clases Caso Inválido    | Límites y casos especiales                           |
| ---------------------- | ------------------------------------------- | --------------------------------------- | ---------------------------------------------------- |
|                        | **Dimensión Primaria**                      |                                         |                                                      |
| **Presentation Level** | `None`, `Basic`, `Intermediate`, `Advanced` | Cualquier otro valor diferente a estos  | Insensible a mayúsculas/minúsculas (`None` = `none`) |
|                        |                                             | **Dimensión Secundaria**                |                                                      |
| **Presentation Level** | Sin espacios al inicio ni al final          | Espacios antes o después de los valores | `" None"` o `"Advanced "` inválidos                  |


|ID|TC-AN-01|
|---|---|
|**Título**|Validate valid activity name input|
|**Status**|Draft|
|**Requerimientos**|The system must accept names with allowed characters and a minimum of 15 characters|
|**Descripción**|Verify that the system accepts a valid activity name with at least 15 characters and allowed symbols|
|**Prioridad**|High|
|**Labels**|ActivityName, Positive|
|**Owner**|[Tu nombre]|
|**Tiempo Estimado**|5 min|
|**Resultados Esperados**|The system accepts the value without error|
|**Steps**|1. Go to the activity creation form  <br>2. Enter a valid activity name with 20 alphanumeric characters and allowed symbols  <br>3. Submit the form|

---

### TC-AN-02

|ID|TC-AN-02|
|---|---|
|**Título**|Validate activity name minimum length enforcement|
|**Status**|Draft|
|**Requerimientos**|The system must reject names shorter than 15 characters|
|**Descripción**|Verify that the system displays an error message when the activity name is shorter than 15 characters|
|**Prioridad**|High|
|**Labels**|ActivityName, Negative|
|**Owner**|[Tu nombre]|
|**Tiempo Estimado**|5 min|
|**Resultados Esperados**|The system displays an error: "Minimum 15 characters required"|
|**Steps**|1. Go to the activity creation form  <br>2. Enter an activity name with only 10 characters  <br>3. Submit the form|

---

## 📑 LLTC para `Presentation Level`

### TC-PL-01

|ID|TC-PL-01|
|---|---|
|**Título**|Validate valid Presentation Level selection|
|**Status**|Draft|
|**Requerimientos**|The system must accept only predefined values from the Presentation Level dropdown|
|**Descripción**|Verify that selecting a valid Presentation Level option allows proceeding|
|**Prioridad**|Medium|
|**Labels**|PresentationLevel, Positive|
|**Owner**|[Tu nombre]|
|**Tiempo Estimado**|3 min|
|**Resultados Esperados**|The system accepts the selection and proceeds|
|**Steps**|1. Go to the activity creation form  <br>2. Open the Presentation Level dropdown  <br>3. Select 'Intermediate'  <br>4. Submit the form|

---

### TC-PL-02

| ID                       | TC-PL-02                                                                                                                           |
| ------------------------ | ---------------------------------------------------------------------------------------------------------------------------------- |
| **Título**               | Validate rejection of invalid Presentation Level input                                                                             |
| **Status**               | Draft                                                                                                                              |
| **Requerimientos**       | The system must restrict Presentation Level input to predefined values                                                             |
| **Descripción**          | Verify that entering a non-listed value like 'Expert' is rejected                                                                  |
| **Prioridad**            | Medium                                                                                                                             |
| **Labels**               | PresentationLevel, Negative                                                                                                        |
| **Owner**                | [Tu nombre]                                                                                                                        |
| **Tiempo Estimado**      | 3 min                                                                                                                              |
| **Resultados Esperados** | The system displays an error or disallows the selection                                                                            |
| **Steps**                | 1. Go to the activity creation form  <br>2. Try to manually input 'Expert' in the Presentation Level field  <br>3. Submit the form |


|ID|TC-AN-01|
|---|---|
|**Título**|Validate valid activity name input|
|**Status**|Draft|
|**Requerimientos**|The system must accept names with allowed characters and a minimum of 15 characters|
|**Descripción**|Verify that the system accepts a valid activity name with at least 15 characters and allowed symbols|
|**Prioridad**|High|
|**Labels**|ActivityName, Positive|
|**Owner**|[Tu nombre]|
|**Tiempo Estimado**|5 min|
|**Resultados Esperados**|The system accepts the value without error|
|**Steps**|1. Go to the activity creation form  <br>2. Enter a valid activity name with 20 alphanumeric characters and allowed symbols  <br>3. Submit the form|

---

### TC-AN-02

|ID|TC-AN-02|
|---|---|
|**Título**|Validate activity name minimum length enforcement|
|**Status**|Draft|
|**Requerimientos**|The system must reject names shorter than 15 characters|
|**Descripción**|Verify that the system displays an error message when the activity name is shorter than 15 characters|
|**Prioridad**|High|
|**Labels**|ActivityName, Negative|
|**Owner**|[Tu nombre]|
|**Tiempo Estimado**|5 min|
|**Resultados Esperados**|The system displays an error: "Minimum 15 characters required"|
|**Steps**|1. Go to the activity creation form  <br>2. Enter an activity name with only 10 characters  <br>3. Submit the form|

---

## 📑 LLTC para `Presentation Level`

### TC-PL-01

|ID|TC-PL-01|
|---|---|
|**Título**|Validate valid Presentation Level selection|
|**Status**|Draft|
|**Requerimientos**|The system must accept only predefined values from the Presentation Level dropdown|
|**Descripción**|Verify that selecting a valid Presentation Level option allows proceeding|
|**Prioridad**|Medium|
|**Labels**|PresentationLevel, Positive|
|**Owner**|[Tu nombre]|
|**Tiempo Estimado**|3 min|
|**Resultados Esperados**|The system accepts the selection and proceeds|
|**Steps**|1. Go to the activity creation form  <br>2. Open the Presentation Level dropdown  <br>3. Select 'Intermediate'  <br>4. Submit the form|

---

### TC-PL-02

|ID|TC-PL-02|
|---|---|
|**Título**|Validate rejection of invalid Presentation Level input|
|**Status**|Draft|
|**Requerimientos**|The system must restrict Presentation Level input to predefined values|
|**Descripción**|Verify that entering a non-listed value like 'Expert' is rejected|
|**Prioridad**|Medium|
|**Labels**|PresentationLevel, Negative|
|**Owner**|[Tu nombre]|
|**Tiempo Estimado**|3 min|
|**Resultados Esperados**|The system displays an error or disallows the selection|
|**Steps**|1. Go to the activity creation form  <br>2. Try to manually input 'Expert' in the Presentation Level field  <br>3. Submit the form|
