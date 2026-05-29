---
type: prompt
id: prompt-004
categoria: contenido
skill: insurance-marketing
efectividad: alta
usado-en: []
tags: [prompt, carrusel, slides, instagram, contenido]
---

# PROMPT-004 — Texto de Cada Slide de Carrusel

## Cuándo usar

> Cuando se necesita el texto completo de cada slide de un carrusel de Instagram. Los carruseles son el formato con mayor ratio de guardados. Usar martes y viernes según el calendario editorial.

## Variables a reemplazar

- `{{tema}}` — tema del carrusel (ej: "5 errores al contratar seguro en USA", "guía de beneficios en vida para latinos")
- `{{numero_slides}}` — cantidad de slides: 5 | 6 | 7 | 8
- `{{objetivo}}` — guardados | compartidos | leads | educar
- `{{pilar}}` — educacion | auditoria | conversion | viral
- `{{cta_slide_final}}` — dm | whatsapp | seguir | guardar

## Prompt

```
Eres un diseñador de contenido experto en carruseles de Instagram para el mercado latino de seguros en Texas.

Cliente: Mario Barrera (@mariobarrera_agente)
- Agente de seguros final expense, 15 años de experiencia, Texas
- Diferenciadores: "Auditor de seguros" + "Beneficios en vida"
- Audiencia: Latinos 50-85 años, Houston/Dallas/Austin
- Colores de marca: Azul navy (#1B3A6B) + dorado (#C9A84C)
- Tono: claro, sin jerga técnica, como si explicaras a un familiar

Tema del carrusel: {{tema}}
Número de slides: {{numero_slides}}
Objetivo principal: {{objetivo}}
Pilar de contenido: {{pilar}}
CTA del último slide: {{cta_slide_final}}

Escribe el texto de cada slide con este formato:

═══════════════════════════════════════════
CARRUSEL — [TÍTULO DEL TEMA]
Slides: {{numero_slides}} | Objetivo: {{objetivo}}
═══════════════════════════════════════════

SLIDE 1 — HOOK (el más importante)
TÍTULO: [máx 8 palabras — debe crear curiosidad o urgencia]
SUBTÍTULO: [máx 15 palabras — amplía el gancho, promete el valor]
VISUAL: [descripción para el diseñador: qué imagen, ícono, o dato mostrar]
NOTA DISEÑO: Incluir foto de Mario o ícono impactante. Color de fondo: navy.

SLIDE 2 — [PUNTO 1]
TÍTULO: [máx 6 palabras]
CUERPO: [máx 20 palabras — 1 idea completa]
DATO/ÍTEM: [si aplica — número, estadística, o bullet específico]
VISUAL: [descripción para el diseñador]
NOTA DISEÑO: Ícono representativo. Fondo: blanco o gris suave.

SLIDE 3 — [PUNTO 2]
[misma estructura]

[continuar según número de slides...]

SLIDE PENÚLTIMO — RESUMEN o LECCIÓN
TÍTULO: [recapitulación en máx 6 palabras]
CUERPO: [mensaje central del carrusel en 1-2 líneas]
VISUAL: [descripción]

SLIDE FINAL — CTA
TÍTULO: [llamado a acción directo]
CUERPO: [instrucción específica según {{cta_slide_final}}]:
  - dm: "Escríbeme al DM — te respondo en español"
  - whatsapp: "📲 Escríbeme al WhatsApp: wa.me/18888561999"
  - seguir: "Sígueme para más consejos de seguros en español"
  - guardar: "💾 Guarda este carrusel — lo vas a necesitar"
VISUAL: Logo de Mario + foto profesional + datos de contacto
NOTA DISEÑO: Fondo navy. Incluir @mariobarrera_agente visible.

═══════════════════════════════════════════
BRIEF PARA DISEÑADOR:
- Fuente: Inter o similar — limpia, legible en móvil
- Tamaño mínimo de texto: equivalente a 16sp en móvil
- Máximo 20 palabras por slide (regla de oro de carruseles)
- Consistencia visual en todos los slides (mismos colores, tipografía)
- Relación de aspecto: 1:1 (1080x1080) o 4:5 (1080x1350)
═══════════════════════════════════════════

ESTRUCTURAS POR PILAR:

EDUCACIÓN (martes):
Slide 1: Pregunta o dato impactante
Slides 2-6: Un concepto o paso por slide
Slide 7: Resumen + lección
Slide 8: CTA + contacto

AUDITORÍA (viernes):
Slide 1: "¿Tu seguro tiene estos errores?"
Slides 2-6: Un error o cosa a verificar por slide
Slide 7: "Si tienes alguno de estos errores..."
Slide 8: CTA para auditoría gratuita

CONVERSIÓN (cualquier día):
Slide 1: El problema/dolor
Slides 2-4: Consecuencias de no actuar
Slides 5-6: La solución (beneficios del seguro)
Slide 7: Testimonio o prueba social
Slide 8: CTA directo

VIRAL (mitos y realidades):
Slide 1: "X mitos sobre seguros que debes conocer"
Slides pares: MITO (en rojo o contraste)
Slides impares: REALIDAD (en verde o positivo)
Slide final: CTA

COMPLIANCE OBLIGATORIO EN TODOS LOS CARRUSELES:
- No prometer coberturas específicas sin calificación
- No usar cifras de beneficios sin "sujeto a aprobación"
- Agregar en slide final: "Sujeto a calificación y aprobación"
```

## Resultado esperado

> Texto completo de cada slide listo para entregar al diseñador, con instrucciones visuales claras, jerarquía de información correcta (máx 20 palabras/slide), y CTA en el último slide. El diseñador solo necesita este brief para crear el carrusel.

## Notas de uso

- El slide 1 es el más importante — si no para el scroll, nadie ve el resto
- Máximo 20 palabras por slide (regla no negociable para legibilidad en móvil)
- Los carruseles de "errores" o "mitos" tienen el mayor ratio de guardados
- El slide final siempre debe incluir logo y @mariobarrera_agente
- Herramienta de diseño recomendada: Canva Pro (plantillas ya en la cuenta)

---

*Links:* [[prompts-index]] · [[ATLAS-HOME]]
