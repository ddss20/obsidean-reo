---
type: prompt
id: prompt-001
categoria: contenido
skill: insurance-marketing
efectividad: alta
usado-en: []
tags: [prompt, hook, reel, instagram, contenido]
---

# PROMPT-001 — Generar Hook de 3 Segundos para Reel

## Cuándo usar

> Cuando necesites la primera frase de un reel de Instagram. Es lo único que decide si la persona se queda o hace scroll. Usar antes de escribir el guión completo.

## Variables a reemplazar

- `{{tema}}` — el tema del reel (ej: "beneficios en vida", "qué pasa si mueres sin seguro", "seguros para trabajadores independientes")
- `{{tipo_hook}}` — el tipo de palanca emocional: familia | miedo_carga | barrera | urgencia | curiosidad | autoridad | historia
- `{{audiencia}}` — quién es el receptor exacto (ej: "papá latino de 50 años en Houston", "mujer latina de 60 años en Dallas")
- `{{formato_salida}}` — video (máx 8 palabras) | caption (primera línea completa, máx 125 chars)

## Prompt

```
Eres un experto en hooks de video para el mercado latino en Texas, USA.

Cliente: Mario Barrera, agente de seguros final expense, 15 años de experiencia, Houston/Dallas/Austin.
Diferenciadores únicos: "Auditor de seguros" y "Beneficios en vida" (dinero que se cobra en vida).
Audiencia: Latinos de 50-85 años, muchos trabajadores independientes, familias con hijos adultos.

Tema del reel: {{tema}}
Tipo de palanca emocional: {{tipo_hook}}
Audiencia específica: {{audiencia}}
Formato de salida: {{formato_salida}}

Genera 5 hooks distintos usando las siguientes reglas:

REGLAS PARA HOOKS DE VIDEO (formato_salida = video):
- Máximo 6-8 palabras habladas
- Debe crear tensión o curiosidad en los primeros 2 segundos
- Debe conectar con miedo, orgullo familiar, o curiosidad del latino en Texas
- No usar palabras corporativas ni promesas de montos específicos
- Puede ser pregunta, afirmación impactante, o inicio de historia

REGLAS PARA HOOKS DE CAPTION (formato_salida = caption):
- Máximo 125 caracteres (lo que Instagram muestra antes de "ver más")
- Debe hacer que la persona quiera tocar "ver más"
- Terminar con "..." o con pregunta que crea tensión

PALANCAS POR TIPO:
- familia: miedo a dejar desprotegidos a los hijos, orgullo de ser proveedor
- miedo_carga: no querer que la familia pida dinero prestado, gastos del funeral ($12,000+)
- barrera: responder objeción ("sí calificas aunque seas trabajador independiente")
- urgencia: cada año que esperan el seguro cuesta más, la salud puede cambiar
- curiosidad: secreto del seguro, lo que el agente no te dice, beneficio que no conocen
- autoridad: 15 años de experiencia, auditor de seguros, diferencia entre agente y auditor
- historia: situación real de cliente (anónima), empieza "el mes pasado...", "nunca olvidaré..."

Para cada hook, incluir:
1. El hook exacto
2. Por qué funciona para este mercado (1 línea)
3. Puntuación estimada 1-10 para latinos en Texas

COMPLIANCE: Ningún hook debe prometer montos específicos de cobertura ni garantías de aprobación.
```

## Resultado esperado

> 5 hooks distintos con puntuación y explicación de por qué cada uno funciona para el mercado latino en Texas. El mejor hook debe poder usarse directamente en el reel sin editar.

## Notas de uso

- Siempre generar al menos 5 para elegir el mejor
- El tipo "historia" (10/10) requiere que Mario tenga una historia real del caso
- El tipo "autoridad" funciona mejor cuando Mario aparece en cámara
- Para avatar digital, preferir hooks tipo "barrera" o "curiosidad" (no requieren historia propia)
- Ver biblioteca completa en `references/hook-patterns.md`

---

*Links:* [[prompts-index]] · [[ATLAS-HOME]]
