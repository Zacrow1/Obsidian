---
materia: "2.4 Redes de computadoras"
semana: 2
fecha_inicio: 2025-03-11
tags:
---

```button
name 🏠 Volver a Materia
type command
action Obsidian: Open file
params "{{materia}}"
color purple
```

# Semana {{SEMANA}} - {{NOMBRE_MATERIA}}

## 🎯 **Objetivos**
- [ ] #foro Completar foro sobre [[{{TEMA}}]] 📅 2025-03-14
- [ ] #tarea Entregar {{TAREA}} 📅 2025-03-16
- [ ] #lab Finalizar laboratorio 📅 2025-03-18

---

## 📚 **Temas Cubiertos**
```button
name ➕ Nuevo Tema
type command
action QuickAdd: Capturar Tema
color blue
```


---

## 💬 **Foro**
> [!question] {{TITULO_PREGUNTA}}
> {{CONTENIDO_PREGUNTA}}

**Mi Respuesta:**  
<% tp.file.cursor() %>

---

## 📋 **Tareas**
```tasks
not done
path includes {{NOMBRE_MATERIA}}
tags include #tarea
```

---

## 🧪 **Laboratorio**
**Instrucciones:**  
{{DESCRIPCION_LAB}}


---

## 📝 **Cuestionario**
```tasks
not done
path includes {{NOMBRE_MATERIA}}
tags include #quiz
```

---

## 🔗 **Relación con Otras Semanas**
```dataview
LIST FROM #semana/{{SEMANA-1}} OR #semana/{{SEMANA+1}}
WHERE file != this
```

---

## 📌 **Recursos**
```dataview
LIST FROM #recurso AND [[{{NOMBRE_MATERIA}}]]
```

[[Escalabilidad en redes]]