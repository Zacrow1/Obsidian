---
materia: "<% tp.system.prompt('Nombre exacto de la materia (Ej: Desarrollo Software 2)', '') %>"
semana: <% tp.system.prompt('Número de semana (1-8)', '1') %>
fecha_inicio: <% tp.date.now('YYYY-MM-DD') %>
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
- [ ] #foro Completar foro sobre [[{{TEMA}}]] 📅 <% tp.date.now("YYYY-MM-DD", 3) %>
- [ ] #tarea Entregar {{TAREA}} 📅 <% tp.date.now("YYYY-MM-DD", 5) %>
- [ ] #lab Finalizar laboratorio 📅 <% tp.date.now("YYYY-MM-DD", 7) %>

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