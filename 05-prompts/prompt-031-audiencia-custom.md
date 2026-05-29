---
type: prompt
id: prompt-031
categoria: ads
skill: insurance-marketing
efectividad: alta
usado-en: []
tags: [prompt, meta-ads, audiencia, targeting, facebook, custom-audience]
---

# PROMPT-031 — Definir Audiencia Personalizada para Meta Ads

## Cuándo usar

> Cuando se necesita definir la configuración exacta de audiencia para una campaña de Meta Ads (Facebook/Instagram). Incluye audiencias frías, retargeting, lookalike, y las restricciones de Special Ad Category para seguros.

## Variables a reemplazar

- `{{tipo_audiencia}}` — fria | retargeting | lookalike | combinada
- `{{objetivo_campana}}` — leads | mensajes | video_views | awareness
- `{{fase}}` — 1-awareness | 2-consideracion | 3-conversion
- `{{fuente_datos}}` — desde_cero | lista_clientes | video_viewers | web_visitors | pagina_fb

## Prompt

```
Eres un especialista en targeting de Meta Ads para el sector de seguros de vida en Texas, con conocimiento profundo de las restricciones de Special Ad Category (seguros = categoría especial en Meta).

Cliente: Mario Barrera (@mariobarrera_agente)
- Agente de seguros final expense en Texas
- Mercado principal: latinos 50-85 años, Houston/Dallas/Austin
- Mercado secundario: latinos 35-50 años que quieren proteger a sus padres
- Mercado terciario: latinos interesados en ser sub-agentes (reclutamiento)

Tipo de audiencia a definir: {{tipo_audiencia}}
Objetivo de campaña: {{objetivo_campana}}
Fase del embudo: {{fase}}
Fuente de datos disponible: {{fuente_datos}}

Genera la configuración completa de audiencia:

═══════════════════════════════════════════
AUDIENCIA — {{tipo_audiencia}} | Fase {{fase}}
═══════════════════════════════════════════

## CONFIGURACIÓN EN META ADS MANAGER

TIPO DE AUDIENCIA: [Core / Custom / Lookalike]

NOTA ESPECIAL CATEGORY:
⚠️ Esta campaña REQUIERE activar "Special Ad Category: Credit" en Meta
Con esta categoría activada, NO se puede segmentar por:
- Edad específica (solo "18+" o rangos amplios)
- Género
- Zip code o radio geográfico específico
Alternativa permitida: estado completo (Texas) + idioma (Español)

CONFIGURACIÓN BÁSICA:
- Ubicación: Texas (estado completo)
  [Si objetivo es Houston: agregar ciudades: Houston, Katy, Pasadena, Sugar Land, Pearland, Humble, Baytown]
  [Si objetivo es Dallas: Dallas, Fort Worth, Irving, Garland, Mesquite, Grand Prairie, Carrollton]
  [Si objetivo es Austin: Austin, Round Rock, Pflugerville, Cedar Park, Kyle, Buda]
- Idioma: Español (ES)
- Edad: [según Special Ad Category — no restringir más de lo necesario]

INTERESES (para audiencia fría):
Paquete A — Seguros y Finanzas:
- Seguros de vida (Life insurance)
- AARP
- Seguros del hogar
- Planificación patrimonial (Estate planning)
- Jubilación (Retirement planning)

Paquete B — Medios Latinos:
- Telemundo
- Univision
- Estrella TV
- Que Buena (radio)
- La Raza

Paquete C — Familia y Comunidad:
- Familia (Family)
- Padres e hijos (Parents and children)
- Cuidado de adultos mayores
- Iglesia católica / Comunidad latina

Paquete D — Comportamientos:
- Compradores frecuentes en línea
- Dueños de pequeños negocios
- Trabajadores independientes (Freelancers)

AUDIENCIA RECOMENDADA (combinación óptima para este caso):
[Especificar cuál combinación de los paquetes A+B+C+D usar según la fase]

TAMAÑO ESTIMADO DE AUDIENCIA: [X-X millones de personas en Texas]

---

SI {{tipo_audiencia}} = retargeting:

AUDIENCIA PERSONALIZADA DE RETARGETING:
Fuente: {{fuente_datos}}

Configuración según fuente:
- video_viewers: "Personas que vieron el X% de tu video [especificar qué video]" → Ventana: 30 días
- web_visitors: "Personas que visitaron [URL]" → Ventana: 30 días
- pagina_fb: "Personas que interactuaron con tu página de Facebook" → Ventana: 60 días
- lista_clientes: "Subir CSV de números de teléfono/emails de leads" → Match rate estimado: 40-60%

EXCLUSIONES PARA RETARGETING:
- Excluir: clientes actuales (si hay lista)
- Excluir: personas que ya enviaron formulario de lead en los últimos 30 días

---

SI {{tipo_audiencia}} = lookalike:

AUDIENCIA LOOKALIKE:
Fuente base (seed audience): [la más valiosa disponible]
- Opción 1: Lista de clientes actuales (mejor opción — calidad más alta)
- Opción 2: Personas que completaron formulario de lead
- Opción 3: Personas que vieron 75%+ de videos de Mario

Porcentaje de similitud recomendado: 1-2% (más parecidos a la audiencia fuente)
Tamaño estimado: ~400,000-800,000 personas en Texas

NOTA: Lookalike funciona mejor cuando la seed audience tiene 1,000+ personas.
Con menos de 500 personas, considerar empezar con audiencia fría.

---

## PRESUPUESTO Y DISTRIBUCIÓN RECOMENDADA

Fase 1 (Awareness):
- Presupuesto: $5-10/día
- Duración: 14 días
- Métrica de éxito: CPV (costo por vista de video) < $0.05

Fase 2 (Leads):
- Presupuesto: $15-25/día
- Duración: continuo mientras CPL < $15
- Métrica de éxito: CPL (costo por lead) < $10-15

Fase 3 (Conversión — Mensajes):
- Presupuesto: $10-15/día
- Duración: continuo
- Métrica de éxito: Costo por mensaje < $5

## SEÑALES DE OPTIMIZACIÓN
[Cuándo ajustar la audiencia]
- CPL > $20: ampliar audiencia o cambiar creativo
- Frecuencia > 3 en 7 días: renovar creativo o expandir audiencia
- CTR < 0.5%: el creativo no está funcionando — cambiar copy/imagen
- CTR > 2%: audiencia altamente relevante — aumentar presupuesto

GUARDAR EN: strategy/campaigns/audiencia-[nombre]-[fecha].md
```

## Resultado esperado

> Configuración exacta de audiencia lista para pegar en Meta Ads Manager, con notas sobre restricciones de Special Ad Category, paquetes de intereses combinables, y métricas para saber cuándo optimizar.

## Notas de uso

- SIEMPRE activar Special Ad Category: Credit antes de configurar la audiencia
- Sin esta categoría activada, el anuncio puede ser rechazado o limitado retroactivamente
- La audiencia fría de Paquete B (medios latinos) es muy efectiva para awareness en este nicho
- El retargeting de video_viewers es el más barato y efectivo para leads cuando hay videos activos
- Para reclutamiento de sub-agentes, usar intereses distintos: pequeños negocios, emprendedores, ventas

---

*Links:* [[prompts-index]] · [[ATLAS-HOME]]
