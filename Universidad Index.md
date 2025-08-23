---
breadcrumbs: "[[Home]] > [[Áreas]] > [[Universidad]]"
tags: universidad/index
---



```button
name 🆕 Nueva Materia
type command
action Templater: Create new note from template
params: "Template-Materia2", {{Nombre}}, {{Fecha}}
color green
```

# 🏛️ Universidad Índex 

## 📈 Progreso Global
```dataview
TABLE WITHOUT ID
  file.link AS Materia,
  choice(estado.completado >= 90, "✅", choice(estado.completado >= 50, "⏳", "🛑")) AS Progreso,
  estado.ultima_actividad AS "📅 Última Actividad"
FROM "Universidad/Materias"
WHERE contains(tags, "#materia")
SORT estado.ultima_actividad DESC
```

---

## 🎯 Acceso Rápido
```button
name 📚 Glosario
type link
action [[Diccionario Glosario Index]]
color blue
```

```button
name 🧠 Técnicas Estudio
type link
action [[0.1 Tecnicas de estudio]]
color purple
```

---

## 📚 Plan de Estudios
### Primer Año
```dataview
TABLE WITHOUT ID file.link AS Materia, estado.completado AS "%"
FROM #primer-año 
WHERE !contains(tags, "#template")
SORT file.name ASC
```

### Segundo Año
```dataview
TABLE WITHOUT ID file.link AS Materia, estado.completado AS "%"
FROM #segundo-año 
WHERE !contains(tags, "#template")
SORT file.name ASC
```

---
[[Diccionario Glosario Index]]

--- 
[[0.1 Tecnicas de estudio]]
[[0.2 Curso de admisión]]
[[0.3 preuniversitario]]

---


# Primer año

#### Modulo 1

[[1.1 Logica]]
[[1.2 Sistemas Operativos 0]]
[[1.3 Programación 1]]

#### Modulo 2

[[1.4 Base de datos]]
[[1.5 Matemáticas discretas]]

#### Modulo 3

[[1.6 Calculo 1]]
[[1.7 Comunicación 1]]
[[1.8 Sistemas operativos 1]]

[[Notas momentáneas]]

#### Modulo 4

[[1.9 Algebra Lineal]]
[[1.10 Sistemas operativos 2]] 
[[1.11 Programación 2]]

#### Modulo 5

[[1.12 Base de datos 2]]
[[1.13 Desarrollo de Software 2]]


#### Modulo 6

[[1.14 Historia de la Ingeniería de Software]]
[[1.15 Comunicación 2]]


# Segundo año
#### Modulo 1

[[2.1 Ingeniería de calidad de software 1]]
[[2.2 Calculo 2]]
[[2.3 Programación 3]]
#### Modulo 2
[[2.4 Redes de computadoras]]
[[2.5 Desarrollo de Software 3]]
#### Modulo 3
#### Modulo 4
#### Modulo 5
#### Modulo 6
