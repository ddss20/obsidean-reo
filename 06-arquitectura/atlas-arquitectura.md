---
type: arquitectura
componente: atlas-core
actualizado: 2026-05-29
tags: [arquitectura, atlas, sistema]
---

# ATLAS — Arquitectura del Sistema

## Qué es ATLAS

ATLAS es el orquestador central del sistema de marketing digital para Mario Barrera Group. No es una app — es un protocolo de trabajo que combina:
- **Archivos de contexto** (markdown) como memoria persistente
- **Skills especializadas** (agentes) para cada tipo de tarea
- **Claude Code** como motor de razonamiento y ejecución
- **Obsidian vault** como interfaz de conocimiento para Mario

---

## Arquitectura de capas

```
┌─────────────────────────────────────────────┐
│              MARIO (cliente)                 │
│         Ve el vault en Obsidian iOS          │
└──────────────────┬──────────────────────────┘
                   │
┌──────────────────▼──────────────────────────┐
│           ATLAS (orquestador)                │
│    atlas_index.md + tasks_active.json        │
│    Vault Obsidian como capa de conocimiento  │
└──────────────────┬──────────────────────────┘
                   │
       ┌───────────┼───────────┐
       ▼           ▼           ▼
┌──────────┐ ┌──────────┐ ┌──────────┐
│Insurance │ │ Social   │ │   Web    │
│Marketing │ │Intellig. │ │  Funnel  │
│Strategist│ │          │ │ Builder  │
└──────────┘ └──────────┘ └──────────┘
       │           │           │
       └───────────┼───────────┘
                   ▼
┌─────────────────────────────────────────────┐
│          SEO Intelligence                    │
│    Keywords · GEO/AEO · Google Business      │
└─────────────────────────────────────────────┘
```

---

## Skills instaladas

| Skill | Archivo | Activar cuando Mario dice... |
|---|---|---|
| ATLAS | `agents/orchestrator.md` | Siempre — es el núcleo |
| Insurance Marketing | `agents/insurance_marketing_strategist.md` | "contenido", "hook", "script", "reel" |
| Social Intelligence | `agents/social_intelligence.md` | "competencia", "scraping", "analiza @" |
| Web Funnel Builder | `agents/web_funnel_builder.md` | "landing", "web", "página", "formulario" |
| SEO Intelligence | `agents/seo_intelligence.md` | "Google", "SEO", "keywords", "ChatGPT" |

---

## Infraestructura técnica

| Componente | Estado | Ubicación |
|---|---|---|
| Dashboard Kanban | ✅ Activo | http://localhost:3001 |
| Servidor Flask | ✅ Corriendo | `/tmp/dashboard.log` |
| Cloudflare Tunnel | ✅ Activo | `/tmp/tunnel.log` |
| Instagram Session | ✅ Activa | `$INSTAGRAM_SESSION` |
| Vault Obsidian | ✅ Activo | `/root/social-agent/vault/` |
| Landing page | ⏳ Pendiente | `/var/www/cotizacion/` |
| Formulario Typeform | ⏳ Pendiente | TASK-264B05 |
| Facebook presencia | ⏳ Pendiente | Sin cuenta activa |

---

## Protocolo de sesión

### Al iniciar (siempre)
1. Leer `atlas_index.md` — 1,700 tokens
2. Leer `tasks_active.json` — 300 tokens
3. Total contexto base: ~2,000 tokens

### Durante la sesión
- Activar 1 skill según intención
- Cargar 1 referencia según necesidad

### Al cerrar
1. Actualizar `tasks_active.json` si hubo cambios
2. Crear nota de sesión en vault (`01-memoria-operativa/sesiones/`)
3. Registrar decisiones en `04-decisiones/`
4. Actualizar `atlas_index.md` si hay cambios de estado

---

## Regla de tokens eficiente

```
Siempre:     atlas_index.md         ~1,700 tokens
Estado:      tasks_active.json      ~300 tokens
Skill:       1 archivo              ~1,000-1,500 tokens
Referencia:  1 archivo              ~1,000-1,300 tokens
────────────────────────────────────────────────
Sesión típica: ~4,300-5,000 tokens
```

---

*Links:* [[ATLAS-HOME]] · [[decision-001-obsidian-vault]] · [[skills-map]]
