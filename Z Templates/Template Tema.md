---
tema: "{{NOMBRE_TEMA}}"
semana:
  "{ SEMANA }": 
materia: "{{MATERIA}}"
tags:
  - 
  - 
aliases:
  - Z-Templates/Tema.md
---

# {{NOMBRE_TEMA}}

## 📌 Definición Clave
{{CONTENIDO}}

## 💡 Aplicación Práctica
```button
name Ejemplo Relacionado
type link
action [[Proyecto: {{MATERIA}} - Semana {{SEMANA}}]]
color green
```

## 🔄 Conexiones
```dataview
LIST FROM outgoing([[{{NOMBRE_TEMA}}]])
WHERE !contains(file.name, "Semana")
```

---

## 📚 Recursos Adicionales
- [[Clase {{SEMANA}}]]
- ![[_Attachments/@Documents/{{MATERIA}}-Semana-{{SEMANA}}.pdf]]