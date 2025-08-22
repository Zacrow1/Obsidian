---
tags:
  - programacion
  - proyectos
  - proyecto/idea
Creado: 2025-04-05
Relacionado:
  - Proyectos
---

Proyecto Tiklay y desarrollo del tp final

Este proyecto se esta desarrollando para el [[Espacio cultural Tiklay]] de la localidad de La plata un emprendimiento que tiene varios requisitos 

# 🗄 Base de Datos

## 📋  Tablas

| Table                  | Description                                       |
| ---------------------- | ------------------------------------------------- |
| `teachers`             | Informacion basica de los profesores              |
| `classes`              | Guarda cada clase dictada y cuánto dinero generó. |
| `teacher_payments`     | Guarda cada pago hecho a los profesores.          |
| `general_transactions` | Movimientos de dinero del espacio                 |

---

# 📊 Relational Model 

`teachers (1) ---- (n) classes teachers (1) ---- (n) teacher_payments`

- One teacher can give many classes.
    
- One teacher can receive many payments.
    

---

# 💾 New SQL (for PostgreSQL / MySQL)

sql

CopiarEditar

`-- Create database (optional) CREATE DATABASE cultural_space; USE cultural_space; -- Only needed for MySQL  -- Teachers Table CREATE TABLE teachers (     id SERIAL PRIMARY KEY,     full_name VARCHAR(100) NOT NULL,     email VARCHAR(100),     phone_number VARCHAR(20),     created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP );  -- Classes Table CREATE TABLE classes (     id SERIAL PRIMARY KEY,     teacher_id INT NOT NULL,     class_name VARCHAR(100) NOT NULL,     class_date DATE NOT NULL,     income_generated DECIMAL(10,2) NOT NULL,     created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,     FOREIGN KEY (teacher_id) REFERENCES teachers(id) ON DELETE CASCADE );  -- Teacher Payments Table CREATE TABLE teacher_payments (     id SERIAL PRIMARY KEY,     teacher_id INT NOT NULL,     payment_date DATE NOT NULL,     amount_paid DECIMAL(10,2) NOT NULL,     created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP,     FOREIGN KEY (teacher_id) REFERENCES teachers(id) ON DELETE CASCADE );  -- General Transactions Table CREATE TABLE general_transactions (     id SERIAL PRIMARY KEY,     transaction_type VARCHAR(10) NOT NULL, -- 'Income' or 'Expense'     amount DECIMAL(10,2) NOT NULL,     description TEXT,     transaction_date DATE NOT NULL,     created_at TIMESTAMP DEFAULT CURRENT_TIMESTAMP );`

---

# ✅ ¿Qué mejoras aplicamos?

|Mejoras|Explicación|
|---|---|
|Fechas normalizadas (`created_at`, `transaction_date`)|Permiten hacer consultas **por día, mes, año** de manera muy fácil en SQL.|
|Income/Expense bien separados|Evita confusiones en los reportes financieros.|
|Nombres en inglés consistentes|¡Listo para escalar o internacionalizar el proyecto!|
|Pensado para crecer|Puedes agregar más relaciones (por ejemplo: categorías de gastos, reportes automáticos) después.|

---

# 📈 ¿Cómo podrías consultar ganancias de un mes o año?

**Ejemplo en SQL:**

sql

CopiarEditar

`-- Ganancia total en enero de 2025 SELECT SUM(amount) as total_income FROM general_transactions WHERE transaction_type = 'Income'   AND EXTRACT(MONTH FROM transaction_date) = 1   AND EXTRACT(YEAR FROM transaction_date) = 2025;`

**Ganancia total (ingresos - egresos):**

sql


`SELECT      SUM(CASE WHEN transaction_type = 'Income' THEN amount ELSE 0 END) -     SUM(CASE WHEN transaction_type = 'Expense' THEN amount ELSE 0 END)  AS net_profit FROM general_transactions WHERE EXTRACT(YEAR FROM transaction_date) = 2025;`

**Ingresos generados solo por las clases:**

sql

CopiarEditar

`SELECT SUM(income_generated) as total_class_income FROM classes WHERE EXTRACT(MONTH FROM class_date) = 1   AND EXTRACT(YEAR FROM class_date) = 2025;`

**Pagos hechos a profesores en un mes:**

sql

CopiarEditar

`SELECT SUM(amount_paid) as total_payments FROM teacher_payments WHERE EXTRACT(MONTH FROM payment_date) = 1   AND EXTRACT(YEAR FROM payment_date) = 2025;`

---

# 🏗 ¿Por qué esta estructura te conviene a futuro?

- Puedes generar reportes mensuales o anuales fácilmente 🔥
    
- Puedes cruzar datos: cuánto ingreso generaron los profesores vs cuánto se les pagó.
    
- Puedes agregar categorías de ingresos/egresos si quieres más detalle.
    
- Separar "Clases" de "General Transactions" permite manejar otros ingresos o egresos que **no tienen relación directa** con las clases (donaciones, alquileres, compras de materiales, etc.).

