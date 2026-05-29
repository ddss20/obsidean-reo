---
type: dashboard
titulo: Dashboard con Dataview
tags: [home, dataview]
---

# Dashboard Dinámico ATLAS

> Este archivo usa **Dataview** para mostrar tablas automáticas desde el vault.
> Los datos se actualizan solos cada vez que editas una nota.

---

## Tareas activas por responsable

```dataview
TABLE titulo, prioridad, fecha_limite
FROM "03-trazabilidad"
WHERE type = "tarea" AND estado != "completada"
SORT fecha_limite ASC
```

---

## Decisiones tomadas

```dataview
TABLE fecha, area, impacto
FROM "04-decisiones"
WHERE type = "decision"
SORT fecha DESC
```

---

## Sesiones recientes

```dataview
TABLE temas, estado
FROM "01-memoria-operativa/sesiones"
WHERE type = "sesion"
SORT fecha DESC
LIMIT 5
```

---

## Prompts por categoría

```dataview
TABLE categoria, efectividad
FROM "05-prompts"
WHERE type = "prompt"
SORT categoria ASC
```
