---
type: prompt
id: prompt-030
categoria: ads
skill: insurance-marketing
efectividad: alta
usado-en: []
tags: [prompt, meta-ads, facebook, instagram, copy, anuncio]
---

# PROMPT-030 — Copy para Anuncio de Facebook/Instagram (Meta Ads)

## Cuándo usar

> Cuando se necesita el texto completo de un anuncio para Meta Ads (Facebook o Instagram). Incluye texto principal, headline, descripción, y variaciones para testing A/B. Usar para campañas de leads, awareness, o mensajes directos.

## Variables a reemplazar

- `{{objetivo_campana}}` — leads | mensajes | video_views | alcance | conversiones
- `{{fase}}` — awareness (fase 1) | leads (fase 2) | conversion (fase 3)
- `{{audiencia}}` — descripción de a quién va dirigido (ej: "latinos 50-70 años Texas sin seguro de vida")
- `{{oferta}}` — qué se ofrece (ej: "cotización gratuita de seguro final expense", "auditoría de seguro gratis")
- `{{formula_copy}}` — PAS (problema-agitacion-solucion) | historia | curiosidad | objecion | reclutamiento
- `{{presupuesto_diario}}` — para adaptar el tono de urgencia

## Prompt

```
Eres un copywriter experto en Meta Ads para el nicho de seguros de vida, especializado en el mercado latino de USA. Conoces las reglas de publicidad de categorías especiales de Meta (seguros = Special Ad Category).

Cliente: Mario Barrera (@mariobarrera_agente)
- Agente de seguros final expense en Texas, 15 años de experiencia
- Diferenciadores: "Auditor de seguros" + "Beneficios en vida"
- Número de WhatsApp: (888) 856-1999
- Instagram: @mariobarrera_agente

Objetivo de campaña: {{objetivo_campana}}
Fase de embudo: {{fase}}
Audiencia objetivo: {{audiencia}}
Oferta: {{oferta}}
Fórmula de copy: {{formula_copy}}
Presupuesto diario estimado: {{presupuesto_diario}}

Genera 3 variaciones de copy completo con esta estructura para cada una:

═══════════════════════════════════════════
VARIACIÓN A — [Nombre descriptivo]
Fórmula: {{formula_copy}}
═══════════════════════════════════════════

TEXTO PRINCIPAL (Primary Text):
[El cuerpo del anuncio. Según la fórmula:

PAS — Problema-Agitación-Solución:
- Línea 1: El problema en 1 línea (dolor emocional)
- Párrafo agitación: consecuencias si no actúa (2-3 líneas)
- Párrafo solución: cómo Mario lo resuelve (1-2 líneas)
- CTA final

HISTORIA:
- Línea 1: Inicio de historia ("El [mes] pasado...")
- Desarrollo: el evento y consecuencia (3-4 líneas)
- Lección: 1 línea
- CTA

CURIOSIDAD:
- Pregunta de curiosidad como primera línea
- La respuesta sorpresiva (2 líneas)
- Cómo Mario lo resuelve (1-2 líneas)
- CTA

OBJECIÓN:
- La objeción como primera línea ("¿Crees que no calificas porque...?")
- Empatía: "Entiendo. Muchos me dicen lo mismo."
- La realidad: por qué sí puede (2-3 líneas)
- CTA

RECLUTAMIENTO:
- Hook: "¿Buscas ganar más dinero ayudando a familias latinas?"
- La oportunidad en 2-3 líneas
- Lo que Mario ofrece: entrenamiento, sin experiencia necesaria
- CTA]

TITULAR (Headline — máx 40 caracteres):
[Texto corto y directo que aparece debajo de la imagen]

DESCRIPCIÓN (Description — máx 30 caracteres):
[Texto de apoyo al titular]

BOTÓN CTA:
[Más información | Enviar mensaje | Suscribirse | Más información]

TEXTO DE IMAGEN/VIDEO:
[Si se agrega texto sobre la imagen: máx 20% del área, qué dice]

COMPLIANCE OBLIGATORIO:
[Verificar que este anuncio cumple con las reglas de Meta para seguros:
- Special Ad Category: Credit/Insurance activado
- Sin discriminación por edad, lugar, género
- Sin promesas de aprobación garantizada
- Disclaimer requerido al final del texto:
  "Sujeto a aprobación y calificación médica. Términos y condiciones aplican."]

═══════════════════════════════════════════

[Repetir con VARIACIÓN B y VARIACIÓN C con enfoques distintos]

═══════════════════════════════════════════
CONFIGURACIÓN DE CAMPAÑA RECOMENDADA
═══════════════════════════════════════════

Fase: {{fase}}
Objetivo de Meta: [configuración exacta en el Ads Manager]
Presupuesto: {{presupuesto_diario}}/día
Duración inicial: 7-14 días de prueba

Audiencia sugerida para este anuncio:
- Edad: [rango según {{audiencia}}]
- Idioma: Español
- Ubicación: [ciudades de Texas según {{audiencia}}]
- Intereses: Seguros de vida, Telemundo, Univision, Familia, Salud, [otros relevantes]
- Special Ad Category: CREDIT activado (obligatorio para seguros)

Creativo recomendado:
- Tipo: [video | imagen | carrusel]
- Duración si es video: [X segundos]
- Descripción visual: [qué debe mostrar]

Variación a testear primero: [A | B | C — con justificación]

GUARDAR EN: strategy/campaigns/brief-[nombre]-[fecha].md
```

## Resultado esperado

> 3 variaciones completas de copy con texto principal, titular, descripción, configuración de campaña, y compliance verificado. Listo para pegar en Meta Ads Manager o enviar al equipo que gestiona los anuncios.

## Notas de uso

- SIEMPRE activar Special Ad Category: Credit al crear la campaña en Meta
- Sin Special Ad Category, Meta puede rechazar o restringir el anuncio
- Para seguros, Meta limita el targeting por edad y zona específica — usar "Texas" en vez de zip codes
- El texto principal tiene mayor impacto que el titular en Meta Ads (priorizar)
- Las historias reales (fórmula historia) tienen el mejor costo por lead en este nicho
- Ver `references/meta-ads-specs.md` para dimensiones de creativos y límites de caracteres

---

*Links:* [[prompts-index]] · [[ATLAS-HOME]]
