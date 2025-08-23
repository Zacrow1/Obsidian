---
materia: "{{NOMBRE_MATERIA}}"
codigo: "{{CODIGO}}"
docente: "{{PROFESOR}}"
tags: 
estado:
  completado: 0%
  ultima_actividad:
    "{ DATE:YYYY-MM-DD }":
---

```button
name 🏠 Volver al Índice
type command
action Obsidian: Open file
action params Areas/Universidad/Universidad Index.md
color blue
```


## 📊 **Progreso**
```dataview
TABLE estado.foro AS "📝 Foro", estado.tarea AS "📋 Tarea", estado.lab AS "🧪 Lab"
FROM [[{{NOMBRE_MATERIA}}]]
WHERE contains(file.folder, this.file.folder)
```

---


```button
name Nueva Semana
type command
action QuickAdd: Capturar Semana
color blue
# {{NOMBRE_MATERIA}} {{moodmoji}}
```

## 🗓️ **Semanas**
<%*
for(let semana = 1; semana <= 8; semana++) {
    tR += `[[Semana ${semana} - {{NOMBRE_MATERIA}}]]\n`;
}
%>

---


---

## 🧩 **Conexiones**
```dataview
LIST FROM outgoing([[{{NOMBRE_MATERIA}}]])
```
