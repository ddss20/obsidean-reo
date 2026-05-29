---
type: decision
id: decision-001
fecha: 2026-05-29
estado: activa
impacto: alto
area: sistema
tags: [decision, infraestructura, obsidian, atlas]
---

# DECISION-001 — Usar Obsidian vault como capa de conocimiento de ATLAS

## Contexto

ATLAS trabajaba con archivos dispersos (`atlas_index.md`, `tasks.json`, reportes en `output/`). Sin una capa de conocimiento estructurada, cada sesión requería recargar contexto desde cero y las decisiones, aprendizajes y prompts no estaban conectados.

## Opciones consideradas

| Opción | Pro | Contra |
|---|---|---|
| Seguir con markdown plano | Simple, ya existía | Sin links, sin trazabilidad, sin grafo |
| Notion | Visual, bases de datos | Requiere cuenta, no local, lento |
| **Obsidian vault** | Local, markdown, grafo, gratis, iOS sync | Necesita app en cliente |

## Decisión tomada

**Elegimos:** Obsidian vault en `/root/social-agent/vault/`

**Razón principal:** Los archivos son markdown puro — ATLAS puede leerlos y escribirlos directamente sin intermediarios. Obsidian solo es la interfaz visual para Mario.

## Estructura adoptada

```
00-home/          → Panel de control
01-memoria-operativa/ → Sesiones con trazabilidad
02-contexto/      → Perfil, mercado, conocimiento estable
03-trazabilidad/  → Tareas con [[links]] entre sí
04-decisiones/    → Log ADR de decisiones
05-prompts/       → Librería de prompts reutilizables
06-arquitectura/  → Sistema vivo de ATLAS
07-aprendizaje/   → Insights y patrones aprendidos
08-docs/          → Documentación auto-generada
_templates/       → Plantillas para cada tipo de nota
```

## Consecuencias esperadas

- ✅ Contexto de sesión cargable en ~1,500 tokens desde vault
- ✅ Decisiones trazables con fecha y razonamiento
- ✅ Prompts reutilizables sin reescribir
- ✅ Mario puede consultar el vault desde iPhone/iPad
- ⚠️ Requiere disciplina para mantener vault actualizado al final de cada sesión

---

*Sesión:* [[sesion-2026-05-29-s4]] · *Links:* [[ATLAS-HOME]] · [[atlas-arquitectura]]
