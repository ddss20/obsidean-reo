---
type: prompt
id: prompt-010
categoria: analisis
skill: social-intelligence
efectividad: alta
usado-en: []
tags: [prompt, analisis, instagram, competencia, scraping]
---

# PROMPT-010 — Analizar Perfil de Competidor en Instagram

## Cuándo usar

> Cuando se necesita analizar un perfil de Instagram de un competidor (otro agente de seguros o cuenta del nicho). Usar con los datos scrapeados de `cache/profiles/` o con datos copiados manualmente del perfil.

## Variables a reemplazar

- `{{username}}` — handle de Instagram sin @ (ej: insuredbykourt)
- `{{datos_perfil}}` — bloque de datos del perfil (bio, seguidores, posts, últimos posts con sus métricas)
- `{{objetivo_analisis}}` — aprender | detectar_gaps | hooks | estrategia_completa
- `{{contexto_mario}}` — qué necesita Mario específicamente de este análisis

## Prompt

```
Eres un analista de marketing digital especializado en el nicho de seguros de vida para el mercado latino en USA.

Tu cliente es Mario Barrera (@mariobarrera_agente), agente de seguros final expense en Texas con 15 años de experiencia. Sus diferenciadores: "Auditor de seguros" y "Beneficios en vida" (se cobra en vida). Su mercado: latinos 50-85 años en Houston, Dallas y Austin.

Vas a analizar el siguiente perfil de Instagram de la competencia:

PERFIL: @{{username}}
DATOS:
{{datos_perfil}}

OBJETIVO DEL ANÁLISIS: {{objetivo_analisis}}
QUÉ NECESITA MARIO: {{contexto_mario}}

Produce el análisis con esta estructura exacta:

═══════════════════════════════════════════
ANÁLISIS @{{username}} — [fecha]
═══════════════════════════════════════════

## 1. DATOS BÁSICOS
- Seguidores: X
- Posts totales: X
- Ratio seguidores/posts: X (bueno si >100)
- Frecuencia estimada de publicación: X veces/semana
- Bio (texto exacto): "..."
- Idioma dominante: Español | Inglés | Mixto
- ¿Tiene cara visible en contenido?: Sí | No
- ¿Usa video (reels)?: Sí | No | Poco

## 2. POSICIONAMIENTO
- ¿Qué promesa central hace? (en 1 línea)
- ¿A quién le habla específicamente?
- ¿Se posiciona como experto, amigo, o vendedor?
- ¿Menciona Texas o región específica?
- ¿Habla de beneficios en vida? ¿De auditoría?

## 3. ESTRATEGIA DE CONTENIDO
- Formato dominante: Reels X% | Carruseles X% | Posts X%
- Temas más frecuentes: [lista]
- Temas con más engagement (comentarios/likes): [lista]
- ¿Usa hashtags estratégicos? ¿Cuáles?
- ¿Tiene consistencia de publicación?

## 4. LO QUE HACE BIEN (para aprender)
[Mínimo 3 puntos con dato concreto cada uno]
1. [Patrón + por qué funciona + dato]
2. [Patrón + por qué funciona + dato]
3. [Patrón + por qué funciona + dato]

## 5. LO QUE HACE MAL (oportunidades para Mario)
[Mínimo 3 puntos]
1. [Error o gap + cómo Mario puede aprovecharlo]
2. [Error o gap + cómo Mario puede aprovecharlo]
3. [Error o gap + cómo Mario puede aprovecharlo]

## 6. HOOKS MÁS EFECTIVOS DETECTADOS
[Copiar los hooks exactos de los posts con más engagement]
- "[hook exacto]" — X likes/comentarios — Por qué funcionó: [explicación]
- "[hook exacto]" — X likes/comentarios — Por qué funcionó: [explicación]
- "[hook exacto]" — X likes/comentarios — Por qué funcionó: [explicación]

## 7. ESPACIOS QUE DEJA LIBRES
[Lo que este competidor NO está haciendo y Mario puede hacer]
- Tema sin cubrir: [explicación + oportunidad concreta]
- Audiencia sin atender: [descripción]
- Formato sin usar: [cuál y por qué sería efectivo]

## 8. VEREDICTO Y AMENAZA
- Nivel de amenaza para Mario (1-10): X
- ¿Por qué?: [explicación en 2 líneas]
- ¿Debe Mario monitorear este perfil regularmente?: Sí | No | Ocasionalmente

## 9. ACCIONES CONCRETAS PARA MARIO (esta semana)
1. [Acción específica basada en lo que hace bien este competidor]
2. [Acción específica para llenar un gap detectado]
3. [Acción específica para diferenciarse]
═══════════════════════════════════════════

GUARDAR EN: output/reports/analisis-{{username}}-[fecha].md
ACTUALIZAR: data/competitors.json con nuevos datos
```

## Resultado esperado

> Análisis completo con datos concretos, 3 acciones inmediatas para Mario, lista de hooks efectivos que puede adaptar, y veredicto de nivel de amenaza. Listo para leer en 5 minutos y tomar decisiones.

## Notas de uso

- Para obtener los datos del perfil, usar primero: `python3 /root/social-agent/scripts/scrape_instagram.py {{username}} 10`
- Si no hay sesión de Instagram activa, copiar datos manualmente del perfil
- No re-analizar si hay reporte de menos de 7 días en `output/reports/`
- Los competidores principales ya están en `data/competitors.json`
- Guardar siempre el reporte antes de terminar la sesión

---

*Links:* [[prompts-index]] · [[ATLAS-HOME]]
