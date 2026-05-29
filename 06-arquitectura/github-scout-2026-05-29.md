# GitHub Scout — Herramientas para ATLAS
**Fecha:** 2026-05-29
**Propósito:** Investigación de herramientas en GitHub para mejorar el sistema ATLAS de marketing de seguros

---

## 1. Tabla de Hallazgos por Categoría

### 1.1 Plugins de Obsidian

| Herramienta | Repo URL | Estrellas | Qué hace | Relevancia ATLAS |
|---|---|---|---|---|
| **Dataview** | [blacksmithgu/obsidian-dataview](https://github.com/blacksmithgu/obsidian-dataview) | ~9,000 | Query tipo SQL sobre notas Markdown; genera tablas/listas dinámicas desde metadatos YAML | **ALTA** — ver leads, campañas, métricas como base de datos |
| **Templater** | [SilentVoid13/Templater](https://github.com/SilentVoid13/Templater) | ~7,000 | Templates con variables dinámicas y JS; fecha automática, variables de contexto | **ALTA** — crear notas de leads, posts, reportes con estructura uniforme |
| **Obsidian Git** | [Vinzent03/obsidian-git](https://github.com/Vinzent03/obsidian-git) | ~4,500 | Commit/push/pull automático al vault desde dentro de Obsidian | **MEDIA** — backup automático del vault en GitHub |
| **Kanban** | [mgmeyers/obsidian-kanban](https://github.com/mgmeyers/obsidian-kanban) | ~6,000 | Tableros Kanban respaldados en Markdown dentro de Obsidian | **ALTA** — pipeline de contenido: Idea → Redactar → Revisar → Publicado |

### 1.2 Skills de Claude Code para Marketing

| Herramienta | Repo URL | Skills incluidas | Relevancia ATLAS |
|---|---|---|---|
| **alirezarezvani/claude-skills** | [GitHub](https://github.com/alirezarezvani/claude-skills) | 329 skills: social-media-analyzer, content-creator, x-twitter-growth, marketing-psychology | **ALTA** — social-media-analyzer cubre Facebook/Instagram/metrics |
| **OpenClaudia/openclaudia-skills** | [GitHub](https://github.com/OpenClaudia/openclaudia-skills) | 34 skills: SEO, content, email, ads, analytics, growth | **ALTA** — skills listos para instalar, incluye SEO + content |
| **coreyhaines31/marketingskills** | [GitHub](https://github.com/coreyhaines31/marketingskills) | CRO, copywriting, SEO, analytics, growth engineering | **ALTA** — CRO y copywriting útil para landing pages de seguros |
| **zubair-trabzada/ai-marketing-claude** | [GitHub](https://github.com/zubair-trabzada/ai-marketing-claude) | 15 skills: auditoría web, copy, email sequences, ad campaigns, content calendars | **ALTA** — content calendars y email sequences para leads |
| **sales-skills/sales** | [GitHub](https://github.com/sales-skills/sales) | CRM, outbound, email marketing, influencer marketing, social listening | **MEDIA** — social listening útil para monitorear competencia |
| **kostja94/marketing-skills** | [GitHub](https://github.com/kostja94/marketing-skills) | 160+ skills: SEO, social, influencer, 40+ tipos de páginas | **MEDIA** — muy amplio, seleccionar los específicos |

### 1.3 Herramientas de Análisis de Instagram (Python)

| Herramienta | Repo URL | Requiere login | Qué hace | Relevancia ATLAS |
|---|---|---|---|---|
| **instagrapi** | [subzeroid/instagrapi](https://github.com/subzeroid/instagrapi) | Sí (privado) | Wrapper Instagram Private API 2026; analytics, upload, DM, stories | **ALTA** — el más completo y actualizado para 2026 |
| **aiograpi** | [subzeroid/aiograpi](https://github.com/subzeroid/aiograpi) | Sí (privado) | Versión async de instagrapi; ideal para scrapers en background | **MEDIA** — útil si ATLAS crece a múltiples cuentas |
| **drawrowfly/instagram-scraper** | [GitHub](https://github.com/drawrowfly/instagram-scraper) | No requerido | Scraping de posts/hashtags/locations sin credenciales | **MEDIA** — limitado en 2026 por defensas de Instagram |
| **MmdUnion/instagram-scraper** | [GitHub](https://github.com/MmdUnion/instagram-scraper) | No requerido | API FastAPI wrapper para scraping básico sin login | **BAJA** — funcionalidad limitada en entorno 2026 |

### 1.4 Automatización de Publicación de Contenido

| Herramienta | Repo URL | Qué hace | Relevancia ATLAS |
|---|---|---|---|
| **ayrshare/social-post-api-python** | [GitHub](https://github.com/ayrshare/social-post-api-python) | API para publicar en Instagram/FB/Twitter/LinkedIn con scheduling | **ALTA** — publicación multi-plataforma desde Python |
| **ArthurFDLR/instagram-post-scheduler** | [GitHub](https://github.com/ArthurFDLR/instagram-post-scheduler) | Scheduler via AWS Lambda + Meta Graph API | **MEDIA** — requiere AWS, más complejo |
| **VAggarwal97/AutoReelUpload** | [GitHub](https://github.com/VAggarwal97/AutoReelUpload) | Download Reel + publicar automáticamente via Meta API | **MEDIA** — útil para repurposing de contenido |
| **lajosdeme/instagram-scheduler** | [GitHub](https://github.com/lajosdeme/instagram-scheduler) | Scheduler simple de fotos para Instagram | **BAJA** — menos mantenimiento activo |

### 1.5 Generadores de Contenido con IA

| Herramienta | Repo URL | Qué hace | Relevancia ATLAS |
|---|---|---|---|
| **claude-code-skill-factory** | [alirezarezvani/claude-code-skill-factory](https://github.com/alirezarezvani/claude-code-skill-factory) | Factory para generar skills de Claude Code; incluye social-media-analyzer | **ALTA** — puede generar skills personalizados para seguros |
| **thatrebeccarae/claude-marketing** | [GitHub](https://github.com/thatrebeccarae/claude-marketing) | 56 skills especializados para equipos de marketing; paid media, e-commerce, content | **MEDIA** — enfocado en e-commerce pero adaptable |

---

## 2. Top 5 Instalaciones Recomendadas

### #1 — Dataview (Obsidian Plugin)
**Por qué primero:** Transforma el vault Obsidian de colección de notas a base de datos consultable. Permite ver todos los leads, campañas activas y métricas en tablas dinámicas.

**Instalación manual en Linux:**
```bash
# Crear directorio del plugin
mkdir -p /root/social-agent/vault/.obsidian/plugins/dataview

# Descargar última release (verificar versión actual en GitHub)
cd /root/social-agent/vault/.obsidian/plugins/dataview
wget https://github.com/blacksmithgu/obsidian-dataview/releases/latest/download/main.js
wget https://github.com/blacksmithgu/obsidian-dataview/releases/latest/download/manifest.json
```

**Luego en Obsidian:**
- Settings → Community plugins → Habilitar "Community plugins"
- Habilitar "Dataview" en la lista

**Uso en ATLAS:**
```dataview
TABLE cliente, estado, fecha_contacto FROM "03-leads"
WHERE estado != "cerrado"
SORT fecha_contacto DESC
```

---

### #2 — Templater (Obsidian Plugin)
**Por qué segundo:** Crea templates con fecha automática, nombre del agente, y variables. Esencial para notas de leads y posts uniformes.

**Instalación:**
```bash
mkdir -p /root/social-agent/vault/.obsidian/plugins/templater-obsidian
cd /root/social-agent/vault/.obsidian/plugins/templater-obsidian
wget https://github.com/SilentVoid13/Templater/releases/latest/download/main.js
wget https://github.com/SilentVoid13/Templater/releases/latest/download/manifest.json
wget https://github.com/SilentVoid13/Templater/releases/latest/download/styles.css
```

**Template de lead para ATLAS** (guardar en `/root/social-agent/vault/templates/nuevo-lead.md`):
```
---
cliente: <% tp.file.title %>
fecha: <% tp.date.now("YYYY-MM-DD") %>
estado: prospecto
fuente: instagram
agente: Mario Barrera
---
# Lead: <% tp.file.title %>

## Información de contacto
- Nombre: 
- Teléfono: 
- Ciudad (Texas): 

## Notas de conversación
<% tp.date.now("YYYY-MM-DD HH:mm") %> — 
```

---

### #3 — instagrapi (Python)
**Por qué tercero:** La biblioteca más actualizada (2026) para acceder a Instagram Private API. Reemplaza/mejora el scraping actual con soporte para analytics, subida de media, y gestión de sesión.

**Instalación:**
```bash
pip install instagrapi

# O en el entorno del servidor
cd /root/social-agent
pip install instagrapi
```

**Integración con script existente** (`/root/social-agent/scripts/scrape_instagram.py`):
```python
from instagrapi import Client

cl = Client()
cl.login("usuario_instagram", "password")

# Analizar competidor
profile = cl.user_info_by_username("competidor_seguros_texas")
medias = cl.user_medias(profile.pk, amount=20)

for post in medias:
    print(f"Likes: {post.like_count} | Comentarios: {post.comment_count} | Caption: {post.caption_text[:100]}")
```

**Nota importante:** Guardar sesión para evitar re-login constante:
```python
cl.dump_settings("session_instagram.json")
# Siguiente vez: cl.load_settings("session_instagram.json")
```

---

### #4 — alirezarezvani/claude-skills (marketing-skill)
**Por qué cuarto:** Incluye `social-media-analyzer` que analiza campañas en Instagram/Facebook con métricas de engagement, ROI y benchmarking competitivo — exactamente lo que necesita ATLAS.

**Instalación:**
```bash
# Clonar solo el directorio de marketing skills
git clone --depth=1 --filter=blob:none --sparse https://github.com/alirezarezvani/claude-skills.git
cd claude-skills
git sparse-checkout set marketing-skill/skills

# Copiar skills relevantes al directorio de ATLAS
cp -r marketing-skill/skills/social-media-analyzer /root/social-agent/agents/
cp -r marketing-skill/skills/content-creator /root/social-agent/agents/
```

**O via npm (más simple):**
```bash
npx ai-agent-skills install alirezarezvani/claude-skills/marketing-skill/social-media-analyzer
```

---

### #5 — Kanban (Obsidian Plugin)
**Por qué quinto:** Pipeline visual de contenido dentro del mismo vault. Tarjetas Markdown con Dataview integrado — ver el estado de cada post en tablero visual.

**Instalación:**
```bash
mkdir -p /root/social-agent/vault/.obsidian/plugins/obsidian-kanban
cd /root/social-agent/vault/.obsidian/plugins/obsidian-kanban
wget https://github.com/mgmeyers/obsidian-kanban/releases/latest/download/main.js
wget https://github.com/mgmeyers/obsidian-kanban/releases/latest/download/manifest.json
wget https://github.com/mgmeyers/obsidian-kanban/releases/latest/download/styles.css
```

**Uso:** Crear archivo `pipeline-contenido.md` con sintaxis Kanban para ver el estado de cada post de Instagram/Facebook por columnas: Idea → Redactando → Revisión → Programado → Publicado.

---

## 3. Plan de Instalación — Orden y Razonamiento

### Semana 1: Infraestructura Obsidian (Días 1-3)
```
Día 1: Dataview + Templater
  → Son los plugins fundacionales; Dataview requiere activar "Community plugins" en Obsidian
  → Probar con query básico sobre /03-leads/
  
Día 2: Kanban
  → Crear pipeline-contenido.md para pipeline visual
  → Conectar con Dataview para que cards muestren métricas

Día 3: Obsidian Git (opcional pero recomendado)
  → Configurar git repo en GitHub para backup automático del vault
  → Requiere Personal Access Token de GitHub
```

### Semana 1: Python — Instagram (Días 4-5)
```
Día 4: Instalar instagrapi
  → pip install instagrapi
  → Migrar/actualizar scrape_instagram.py
  → Probar login y guardar sesión en JSON

Día 5: Integrar con Flask dashboard
  → Endpoint /api/instagram-analytics que use instagrapi
  → Mostrar métricas de competidores en dashboard
```

### Semana 2: Skills de Claude Code (Días 6-7)
```
Día 6: Instalar social-media-analyzer de alirezarezvani
  → Copiar a /root/social-agent/agents/
  → Probar invocando desde Claude Code

Día 7: Instalar content-creator skill
  → Adaptar templates para marketing de seguros final expense Texas
  → Crear skill personalizada: insurance-content-creator.md
```

---

## 4. Archivos a Copiar para Plugins Obsidian

Cada plugin requiere exactamente estos archivos en su subdirectorio:

```
/root/social-agent/vault/.obsidian/plugins/
├── dataview/
│   ├── main.js           ← desde: github.com/blacksmithgu/obsidian-dataview/releases
│   └── manifest.json
├── templater-obsidian/
│   ├── main.js           ← desde: github.com/SilentVoid13/Templater/releases
│   ├── manifest.json
│   └── styles.css
├── obsidian-kanban/
│   ├── main.js           ← desde: github.com/mgmeyers/obsidian-kanban/releases
│   ├── manifest.json
│   └── styles.css
└── obsidian-git/         ← opcional
    ├── main.js           ← desde: github.com/Vinzent03/obsidian-git/releases
    └── manifest.json
```

**Comando de descarga automatizado:**
```bash
#!/bin/bash
# Script: /root/social-agent/scripts/install-obsidian-plugins.sh

VAULT="/root/social-agent/vault/.obsidian/plugins"

install_plugin() {
    local name=$1
    local repo=$2
    mkdir -p "$VAULT/$name"
    for file in main.js manifest.json styles.css; do
        url="https://github.com/$repo/releases/latest/download/$file"
        wget -q --spider "$url" 2>/dev/null && wget -q -O "$VAULT/$name/$file" "$url" || true
    done
    echo "Instalado: $name"
}

install_plugin "dataview" "blacksmithgu/obsidian-dataview"
install_plugin "templater-obsidian" "SilentVoid13/Templater"
install_plugin "obsidian-kanban" "mgmeyers/obsidian-kanban"
install_plugin "obsidian-git" "Vinzent03/obsidian-git"

echo "Plugins instalados. Habilitar en Obsidian Settings → Community plugins"
```

---

## 5. Skills de Claude Code Encontradas — Adaptación para ATLAS

### 5.1 Social Media Analyzer (alirezarezvani)
Skill encontrado en: `github.com/alirezarezvani/claude-code-skill-factory/blob/dev/generated-skills/social-media-analyzer/SKILL.md`

**Funcionalidades del skill original:**
- Análisis de rendimiento de campañas en Facebook, Instagram, Twitter, LinkedIn, TikTok
- Métricas de engagement, ROI, insights de audiencia
- Detección de tendencias y benchmarking competitivo

**Adaptación recomendada para ATLAS** — crear `/root/social-agent/agents/instagram-competitor-analyzer.md`:
```markdown
# Skill: Instagram Competitor Analyzer para Seguros Texas

## Propósito
Analizar perfiles de competidores de seguros final expense en Texas usando los datos
obtenidos por instagrapi. Identificar qué contenido genera más engagement.

## Métricas a analizar
- Engagement rate por post (likes + comments / followers)
- Tipos de contenido más efectivos (carrusel vs reel vs foto)
- Horarios de mayor interacción
- Hashtags con mejor rendimiento en seguros Texas
- Temas que resuenan con la audiencia hispana 55+

## Output esperado
Tabla comparativa de competidores + recomendaciones de contenido para Mario Barrera
```

### 5.2 Content Creator Skill
Skill base: `github.com/alirezarezvani/claude-skills/tree/main/marketing-skill/skills`

**Adaptar para seguros** — agregar al skill content-creator existente en ATLAS:
- Prompts específicos para final expense insurance
- Audiencia objetivo: hispanos 55+ en Texas
- Tono: confianza, familia, tranquilidad financiera
- Call-to-action: "Llama a Mario" / "Cotización gratis"
- Cumplimiento: no hacer promesas de cobertura sin verificación

---

## 6. Notas Adicionales

### Sobre Instagram scraping en 2026
Los scrapers sin login (drawrowfly, MmdUnion) tienen limitaciones severas en 2026 porque Instagram implementó:
- Mandatory login walls
- GraphQL obfuscation
- IP flagging agresivo

**Recomendación:** Usar `instagrapi` con cuenta real, rotación de user-agents, y delays entre requests. Guardar sesión en JSON para evitar challenges frecuentes.

### Sobre Meta Graph API oficial
Para publicación oficial (no scraping), la Graph API requiere:
1. Cuenta de Instagram Business (Mario ya debería tenerla)
2. Facebook App con permisos `instagram_content_publish`
3. Access token de larga duración

Costo: Gratis hasta 200 llamadas/hora. Suficiente para ATLAS.

### Recursos adicionales encontrados
- [Guía completa Instagram Platform API 2024](https://gist.github.com/PrenSJ2/0213e60e834e66b7e09f7f93999163fc) — implementación con httpx y asyncio
- [SocialMediaAnalytics wrapper Meta Graph API](https://github.com/ckoutavas/SocialMediaAnalytics) — analytics de Facebook + Instagram Business
- [Dataview example vault](https://github.com/s-blu/obsidian_dataview_example_vault) — ejemplos de queries para aprender Dataview

---

*Scout generado por agente de investigación ATLAS — 2026-05-29*
