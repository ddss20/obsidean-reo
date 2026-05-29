---
type: prompt
id: prompt-011
categoria: analisis
skill: social-intelligence
efectividad: media
usado-en: []
tags: [prompt, ranking, comparacion, instagram, competencia]
---

# PROMPT-011 — Comparar y Rankear Múltiples Cuentas de Instagram

## Cuándo usar

> Cuando se tienen 3 o más perfiles analizados y se necesita un ranking comparativo para saber quiénes son los competidores más fuertes, qué estrategias dominan el nicho, y dónde está parado Mario vs el mercado.

## Variables a reemplazar

- `{{lista_perfiles}}` — lista de usernames a comparar (incluir @mariobarrera_agente)
- `{{metricas_disponibles}}` — qué datos se tienen de cada perfil (seguidores, posts, engagement, etc.)
- `{{objetivo}}` — benchmark | detectar_lider | oportunidades_nicho | posicionamiento_mario
- `{{fecha_datos}}` — fecha en que se tomaron los datos

## Prompt

```
Eres un analista estratégico de marketing digital. Vas a comparar y rankear múltiples perfiles de Instagram del nicho de seguros de vida para el mercado latino en Texas.

El cliente es Mario Barrera (@mariobarrera_agente). El objetivo es entender dónde está parado Mario vs la competencia y qué debe hacer diferente.

PERFILES A COMPARAR:
{{lista_perfiles}}

DATOS DISPONIBLES:
{{metricas_disponibles}}

OBJETIVO: {{objetivo}}
FECHA DE LOS DATOS: {{fecha_datos}}

Produce el análisis comparativo con esta estructura:

═══════════════════════════════════════════
RANKING DE CUENTAS — Seguros Latinos Texas
Fecha: {{fecha_datos}}
═══════════════════════════════════════════

## TABLA COMPARATIVA GENERAL

| Perfil | Seguidores | Posts | Ratio S/P | Freq/sem | Idioma | Video | Cara | Español |
|--------|-----------|-------|-----------|----------|--------|-------|------|---------|
| @perfil1 | X | X | X | X | | ✓/✗ | ✓/✗ | ✓/✗ |
[completar para todos los perfiles]

## RANKING POR CRITERIO

### Por alcance potencial (seguidores):
1. @perfil — X seguidores — [fortaleza principal en 1 línea]
2. ...

### Por engagement estimado (likes+comentarios/post):
1. @perfil — X engagement rate — [por qué]
2. ...

### Por calidad de estrategia de contenido (evaluación 1-10):
1. @perfil — X/10 — [razón]
2. ...

### Por posicionamiento hispano (qué tan bien sirve al mercado latino):
1. @perfil — [evaluación]
2. ...

## ANÁLISIS DEL LÍDER DEL NICHO
Perfil #1: @[perfil]
- Por qué lidera: [3 razones concretas]
- Su estrategia dominante: [descripción]
- Su punto débil que Mario puede explotar: [oportunidad concreta]

## MAPA DE POSICIONAMIENTO

Eje X: Alcance (pequeño ← → grande)
Eje Y: Especialización en mercado hispano (genérico ↑ → específico ↓)

[Describir en texto dónde cae cada perfil en este mapa]

## DÓNDE ESTÁ MARIO vs COMPETENCIA

Fortalezas únicas que Mario tiene y nadie más:
1. "Auditor de seguros" — [explicar si algún competidor usa este concepto]
2. "Beneficios en vida" — [qué tan bien lo comunica vs la competencia]
3. 15 años de experiencia — [cómo se compara con los demás]

Brechas de Mario vs el líder:
1. [Brecha + acción para cerrarla]
2. [Brecha + acción para cerrarla]
3. [Brecha + acción para cerrarla]

## TÁCTICAS QUE DOMINAN EL NICHO (patrones repetidos en los top 3)
1. [Táctica + quién la usa + por qué funciona]
2. [Táctica + quién la usa + por qué funciona]
3. [Táctica + quién la usa + por qué funciona]

## OPORTUNIDADES BLANCAS (lo que nadie está haciendo)
1. [Oportunidad + cómo Mario la puede capitalizar]
2. [Oportunidad + cómo Mario la puede capitalizar]
3. [Oportunidad + cómo Mario la puede capitalizar]

## RECOMENDACIONES PARA MARIO (en orden de prioridad)

PRIORIDAD ALTA (hacer esta semana):
- [Acción específica con formato y tema]

PRIORIDAD MEDIA (hacer este mes):
- [Acción específica]

PRIORIDAD BAJA (considerar este trimestre):
- [Acción de largo plazo]

## PERFIL A MONITOREAR MÁS DE CERCA
- Perfil: @[username]
- Por qué: [razón en 1 línea]
- Frecuencia de monitoreo recomendada: semanal | quincenal | mensual
═══════════════════════════════════════════

GUARDAR EN: output/reports/ranking-cuentas-[fecha].md
ACTUALIZAR: data/competitors.json
```

## Resultado esperado

> Tabla comparativa de todos los perfiles, ranking por múltiples criterios, posicionamiento claro de Mario vs el mercado, oportunidades vacías en el nicho, y 3-5 acciones concretas ordenadas por prioridad.

## Notas de uso

- Requiere haber corrido prompt-010 para cada perfil primero (o tener datos en cache)
- Incluir siempre a @mariobarrera_agente en la comparación para que el ranking sea útil
- Actualizar el ranking cada 30-45 días máximo
- Los reportes anteriores están en `output/reports/`
- Para datos frescos: correr `python3 /root/social-agent/main.py compare @user1 @user2 @user3`

---

*Links:* [[prompts-index]] · [[ATLAS-HOME]]
