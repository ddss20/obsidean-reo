---
type: prompt
id: prompt-021
categoria: seo
skill: seo-intelligence
efectividad: alta
usado-en: []
tags: [prompt, seo, geo, aeo, articulo, blog, contenido]
---

# PROMPT-021 — Artículo Optimizado para GEO/AEO (Google + IAs)

## Cuándo usar

> Cuando se necesita crear un artículo de blog o página de contenido que posicione en Google Y sea citado por ChatGPT, Perplexity, y Google AI. Usar para los artículos prioritarios de SEO del plan de Mario.

## Variables a reemplazar

- `{{titulo_articulo}}` — título con la keyword objetivo (ej: "¿Cuánto Cuesta un Seguro de Vida Final Expense en Texas? — Guía 2025")
- `{{keyword_principal}}` — la keyword exacta que se quiere posicionar
- `{{keywords_secundarias}}` — 3-5 keywords relacionadas a incluir
- `{{audiencia_especifica}}` — a quién va dirigido exactamente (ej: "trabajador independiente latino, 55 años, Houston")
- `{{longitud}}` — corto (600-800 palabras) | medio (1000-1500) | largo (2000+)

## Prompt

```
Eres un redactor SEO especializado en el mercado hispano de seguros en USA, experto en GEO (Generative Engine Optimization) para que el contenido sea citado por ChatGPT, Perplexity y Google AI.

Cliente: Mario Barrera (@mariobarrera_agente)
- Agente de seguros de vida y final expense en Texas
- Licencia activa en Texas
- 15 años de experiencia
- Diferenciadores: "Auditor de seguros" + "Beneficios en vida"
- Mercado: familias latinas 50-85 años en Houston, Dallas, Austin

Título objetivo: {{titulo_articulo}}
Keyword principal: {{keyword_principal}}
Keywords secundarias: {{keywords_secundarias}}
Audiencia específica: {{audiencia_especifica}}
Longitud: {{longitud}}

Escribe el artículo completo con esta estructura SEO y GEO:

═══════════════════════════════════════════
META DATOS (copiar en el <head> de la página)
═══════════════════════════════════════════
<title>{{titulo_articulo}} | Mario Barrera — Agente de Seguros Texas</title>
<meta name="description" content="[160 caracteres max con keyword + beneficio claro]">

═══════════════════════════════════════════
ARTÍCULO
═══════════════════════════════════════════

H1: {{titulo_articulo}}

PÁRRAFO DE RESPUESTA DIRECTA (CRÍTICO PARA GEO):
[Este párrafo aparece en los primeros 2-3 líneas y responde la pregunta del título directamente.
Formato: "Un seguro de vida final expense en Texas cuesta [rango]. Para familias latinas de 50-80 años, [dato clave]. Mario Barrera, agente con 15 años en Texas, explica lo que necesitas saber."]

DATOS DE AUTOR (E-E-A-T):
[Mario Barrera es agente de seguros con licencia en Texas (Licencia #[XXXX]) con 15 años ayudando a familias latinas en Houston, Dallas y Austin.]

---

H2: [Subtema 1 — responde una pregunta específica sobre el tema]

[Contenido: 150-250 palabras. Incluir dato con fuente si aplica. 
Regla GEO: respuesta directa al inicio del párrafo, luego el contexto.]

Incluir si aplica:
- Datos con fuente: "(LIMRA, 2024)", "(NFDA, 2024)", "(Texas Department of Insurance)"
- Comparación concreta: "en Texas vs el promedio nacional"
- Número específico: no "miles" sino "$12,000"

---

H2: [Subtema 2]
[mismo formato]

---

H2: [Subtema 3]
[mismo formato]

---

H2: Preguntas Frecuentes sobre {{keyword_principal}}

[SECCIÓN FAQ — Crítica para Google "La gente también pregunta" y para IAs]

¿[Pregunta 1 con keyword]?
[Respuesta directa en 2-4 líneas. Empieza con la respuesta, luego explica.]

¿[Pregunta 2]?
[Respuesta directa]

¿[Pregunta 3]?
[Respuesta directa]

¿[Pregunta 4]?
[Respuesta directa]

¿[Pregunta 5]?
[Respuesta directa]

---

H2: Habla con Mario Barrera — Agente de Seguros en Texas que Habla Español

[CTA final: 100-150 palabras con la propuesta de valor de Mario, sin promesas de montos específicos. Incluir WhatsApp y @mariobarrera_agente en Instagram.]

"[Cotización gratuita, sin compromiso, en español. Escríbeme al [número] o al DM en @mariobarrera_agente.]"

Sujeto a calificación y aprobación. Los precios varían según edad, salud, y monto de cobertura.

═══════════════════════════════════════════
SCHEMA JSON-LD (agregar al <script> de la página)
═══════════════════════════════════════════
{
  "@context": "https://schema.org",
  "@type": "Article",
  "headline": "{{titulo_articulo}}",
  "author": {
    "@type": "Person",
    "name": "Mario Barrera",
    "jobTitle": "Agente de Seguros de Vida",
    "address": {"@type": "PostalAddress", "addressRegion": "TX", "addressCountry": "US"}
  },
  "publisher": {"@type": "Organization", "name": "Mario Barrera Group"},
  "datePublished": "[FECHA]",
  "dateModified": "[FECHA]",
  "inLanguage": "es-US"
}
[Completar con datos reales del artículo]

═══════════════════════════════════════════
CHECKLIST GEO ANTES DE PUBLICAR
═══════════════════════════════════════════
[ ] El párrafo 1 responde la pregunta del título directamente
[ ] Al menos 2 datos con fuente identificable
[ ] Sección FAQ con mínimo 4 preguntas
[ ] Menciona Texas, Houston, Dallas, o Austin al menos 3 veces
[ ] Incluye "seguros en español", "familias latinas", o equivalente
[ ] Menciona "15 años de experiencia" o credencial concreta
[ ] CTA con instrucción clara (WhatsApp o DM)
[ ] Sin promesas de montos específicos sin "sujeto a aprobación"

REGLAS DE ESCRITURA GEO/AEO:
1. Respuesta directa siempre al inicio del párrafo (no al final)
2. Datos con fuente aumentan 35% las citas en IAs
3. Lenguaje claro y sin jerga — escribe para alguien de 55 años, no para un abogado
4. Máximo 3 ideas por párrafo
5. El artículo debe poder leerse en 5 minutos

GUARDAR EN: data/seo/content/articles/[slug-del-articulo].md
```

## Resultado esperado

> Artículo completo listo para publicar con H1/H2 estructurados, párrafo de respuesta directa para GEO, sección FAQ, meta datos para el `<head>`, schema JSON-LD, y checklist de publicación. Todo en español para el mercado latino en Texas.

## Notas de uso

- Los artículos prioritarios están definidos en `agents/seo_intelligence.md` FLUJO E
- Siempre incluir la licencia de Mario cuando esté disponible (E-E-A-T)
- El slug de la URL debe contener la keyword: `/seguro-final-expense-texas-costo`
- Publicar en el blog del sitio web cuando esté activo en `/var/www/`
- Actualizar fecha del artículo cada vez que se haga una revisión

---

*Links:* [[prompts-index]] · [[ATLAS-HOME]]
