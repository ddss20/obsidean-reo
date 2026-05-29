---
type: prompt
id: prompt-020
categoria: seo
skill: seo-intelligence
efectividad: alta
usado-en: []
tags: [prompt, seo, keywords, hispano, texas, google]
---

# PROMPT-020 — Investigar Keywords para el Nicho Hispano de Seguros en Texas

## Cuándo usar

> Cuando se necesita identificar palabras clave que los latinos en Texas usan para buscar seguros de vida, final expense, o beneficios en vida. Usar antes de crear artículos SEO, optimizar la landing page, o planear contenido orgánico de Google.

## Variables a reemplazar

- `{{tema_central}}` — tema a investigar (ej: "final expense", "beneficios en vida", "agente de seguros en español Houston")
- `{{tipo_keywords}}` — transaccional | informacional | local | todas
- `{{ciudad}}` — Houston | Dallas | Austin | Texas (general) | todas
- `{{profundidad}}` — rapido (top 10) | completo (con long tails y preguntas)

## Prompt

```
Eres un especialista en SEO para el mercado hispanohablante en USA, con experiencia en nichos de servicios financieros y seguros.

Cliente: Mario Barrera — agente de seguros de vida y final expense en Texas
Website objetivo: [dominio de Mario cuando esté activo]
Mercado: Latinos que hablan español o español/inglés en Texas
Audiencia: 50-85 años, trabajadores independientes, familias con hijos adultos

Tema central a investigar: {{tema_central}}
Tipo de keywords: {{tipo_keywords}}
Ciudad/Región foco: {{ciudad}}
Profundidad del análisis: {{profundidad}}

Genera la investigación de keywords con esta estructura:

═══════════════════════════════════════════
KEYWORD RESEARCH — {{tema_central}}
Ciudad: {{ciudad}} | Tipo: {{tipo_keywords}}
═══════════════════════════════════════════

## KEYWORDS PRIMARIAS (alta intención, mayor competencia)

| Keyword | Idioma | Intención | Competencia est. | Oportunidad Mario |
|---------|--------|-----------|-----------------|-------------------|
| [keyword] | ES/EN | T/I/L | Alta/Media/Baja | Alta/Media/Baja |
[completar tabla]

## KEYWORDS DE COLA LARGA (long tail — más fáciles de posicionar)

Formato: "keyword exacta" | intención | por qué es valiosa para Mario

Transaccionales (alguien listo para contactar):
- "[keyword]" | Transaccional | [razón]
- ...

Informacionales (alguien buscando aprender):
- "[keyword]" | Informacional | [razón]
- ...

Locales (búsquedas con ciudad o "cerca de mí"):
- "[keyword]" | Local | [razón]
- ...

## PREGUNTAS QUE HACEN LOS LATINOS EN TEXAS (para GEO/AEO)
[Estas aparecen en Google como "La gente también pregunta" y en las IAs]

- ¿[pregunta exacta]?
- ¿[pregunta exacta]?
- ¿[pregunta exacta]?
[mínimo 10 preguntas]

## KEYWORDS DE OPORTUNIDAD ÚNICA PARA MARIO
[Keywords donde Mario puede posicionarse como único — baja competencia + intención alta]

1. "auditor de seguros texas" — competencia: casi cero — Mario es el único con este concepto
2. "beneficios en vida seguro español" — vacío en contenido en español
3. [otras keywords únicas identificadas]

## KEYWORDS A EVITAR
[Las que tienen alta competencia pero bajo ROI para Mario]
- "[keyword]" — por qué evitar: [razón]

## MAPA DE CONTENIDO RECOMENDADO
[Cómo agrupar estas keywords en páginas/artículos]

Página principal (landing):
- Keyword primaria: [keyword]
- Keywords secundarias: [lista]

Artículo 1:
- Título optimizado: "[título con keyword]"
- Keyword objetivo: [keyword]
- Keywords de soporte: [lista]

Artículo 2:
[mismo formato]

[continuar según profundidad]

## KEYWORDS PARA GOOGLE MY BUSINESS
[Las que deben aparecer en la descripción del perfil de Google Business]
- [lista de 8-10 keywords para GMB]

## KEYWORDS PARA META ADS (targeting por intereses)
[Términos de intereses en Facebook/Instagram que corresponden a estas búsquedas]
- [lista de 5-8 intereses para Meta]

## TOP 5 KEYWORDS PARA EMPEZAR HOY
[Las de mayor impacto vs menor esfuerzo]
1. Keyword: [keyword] | Artículo sugerido: [título] | Tiempo estimado para posicionar: [X semanas]
2. ...
═══════════════════════════════════════════

NOTAS PARA EL ANÁLISIS:
- Priorizar keywords en español — la competencia es mucho menor que en inglés
- El mercado objetivo busca en "Spanglish": mezcla español con términos en inglés como "life insurance", "final expense", "beneficios"
- Keywords con "en español", "habla español", "agente hispano" tienen altísima intención y baja competencia
- Las búsquedas locales "Houston", "Dallas", "Austin" tienen mucho menos competencia que keywords nacionales
- El concepto "auditor de seguros" es único de Mario — cero competencia, crear contenido primero

GUARDAR EN: data/seo/keywords/research-[tema]-[fecha].md
```

## Resultado esperado

> Lista organizada de keywords por tipo e intención, tabla de oportunidad vs competencia, mapa de contenido para aprovecharlas, y top 5 para empezar esta semana. Incluye keywords para GMB y Meta Ads.

## Notas de uso

- La base de keywords ya existente está en `references/keyword-database.md` — leer antes de ejecutar este prompt
- Keywords con intención local (Houston, Dallas, Austin) tienen 5-10x menos competencia que keywords nacionales
- Actualizar la base de keywords cada trimestre
- Para validar volumen real: usar Google Keyword Planner o Semrush (si hay acceso)
- GEO/AEO: las preguntas en formato "¿Cómo...?" y "¿Cuánto...?" son las que responden ChatGPT y Perplexity

---

*Links:* [[prompts-index]] · [[ATLAS-HOME]]
