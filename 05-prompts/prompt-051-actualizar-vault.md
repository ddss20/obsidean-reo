---
type: prompt
id: prompt-051
categoria: sistema
skill: atlas
efectividad: alta
usado-en: []
tags: [prompt, vault, cierre-sesion, atlas, memoria]
---

# PROMPT-051 — Actualizar Vault al Cerrar Sesión

## Cuándo usar

> Al final de cada sesión de trabajo importante. Asegura que todo el conocimiento generado en la sesión quede guardado en el vault y que el sistema esté listo para la próxima sesión. Toma 5-10 minutos pero evita perder trabajo.

## Variables a reemplazar

- `{{resumen_sesion}}` — qué se hizo en esta sesión (en bullet points)
- `{{decisiones_tomadas}}` — decisiones que Mario tomó (aunque sean pequeñas)
- `{{archivos_creados_modificados}}` — lista de archivos que se crearon o modificaron
- `{{tareas_completadas}}` — IDs o nombres de tareas que se cerraron
- `{{tareas_nuevas}}` — nuevas tareas identificadas durante la sesión
- `{{proxima_sesion}}` — si Mario mencionó qué quiere hacer la próxima vez

## Prompt

```
Eres ATLAS, el orquestador de Mario Barrera Group. La sesión de trabajo va a terminar.

Tu trabajo es asegurarte de que NADA se pierda y que el sistema quede listo para la próxima sesión.

DATOS DE ESTA SESIÓN:
- Resumen: {{resumen_sesion}}
- Decisiones tomadas: {{decisiones_tomadas}}
- Archivos creados/modificados: {{archivos_creados_modificados}}
- Tareas completadas: {{tareas_completadas}}
- Tareas nuevas identificadas: {{tareas_nuevas}}
- Próxima sesión: {{proxima_sesion}}

Ejecuta el protocolo de cierre completo:

PASO 1 — VERIFICAR QUE TODO ESTÉ GUARDADO:
```bash
# Verificar archivos creados en esta sesión
ls -la /root/social-agent/strategy/content-plans/ | tail -5
ls -la /root/social-agent/strategy/campaigns/ | tail -5
ls -la /root/social-agent/output/reports/ | tail -5
ls -la /root/social-agent/vault/05-prompts/ | tail -5
```

PASO 2 — ACTUALIZAR TASKS (si hubo cambios):
[Si hubo tareas completadas o nuevas, actualizar tasks_active.json]
```bash
# Ver estado actual
cat /root/social-agent/data/tasks_active.json
# Actualizar si es necesario via API o edición directa
```

PASO 3 — CREAR NOTA DE SESIÓN EN EL VAULT:
Crear archivo: `/root/social-agent/vault/01-memoria-operativa/sesiones/sesion-[FECHA].md`

Contenido de la nota de sesión:
---
type: sesion
fecha: [FECHA]
duracion: [X minutos]
skills-usadas: [lista]
---

# Sesión [FECHA]

## Qué se hizo
{{resumen_sesion}}

## Decisiones tomadas
{{decisiones_tomadas}}

## Archivos generados
{{archivos_creados_modificados}}

## Tareas cerradas
{{tareas_completadas}}

## Tareas nuevas creadas
{{tareas_nuevas}}

## Para la próxima sesión
{{proxima_sesion}}

PASO 4 — ACTUALIZAR atlas_index.md SI HAY CAMBIOS DE ESTADO:
[Solo si algo importante cambió: nueva landing activa, nueva campaña, nuevo análisis, etc.]
```bash
# Ver estado actual del índice
cat /root/social-agent/data/atlas_index.md
# Editar solo si hay cambio de estado real
```

PASO 5 — REGISTRAR DECISIONES IMPORTANTES:
[Si Mario tomó una decisión estratégica importante, crear archivo en vault/04-decisiones/]
Crear: `/root/social-agent/vault/04-decisiones/decision-[FECHA]-[tema].md`

PASO 6 — CHECKLIST FINAL:

[ ] Todos los briefs de contenido guardados en strategy/content-plans/
[ ] Todos los informes de análisis en output/reports/
[ ] tasks_active.json actualizado
[ ] Nota de sesión creada en vault/01-memoria-operativa/sesiones/
[ ] atlas_index.md refleja el estado actual
[ ] Próxima sesión documentada

PASO 7 — MENSAJE DE CIERRE PARA MARIO:

━━━━━━━━━━━━━━━━━━━━━━━━━━━
SESIÓN CERRADA ✓
━━━━━━━━━━━━━━━━━━━━━━━━━━━
Lo que quedó guardado:
[lista en bullet points de lo más importante]

Para la próxima sesión:
[lo más urgente en 1-2 líneas]

Puedes cerrar Claude Code.
━━━━━━━━━━━━━━━━━━━━━━━━━━━

---

REGLAS DEL PROTOCOLO DE CIERRE:
- Si no hubo decisiones importantes, no crear archivo en vault/04-decisiones (evitar ruido)
- Solo actualizar atlas_index.md si algo cambió de estado realmente
- La nota de sesión es siempre obligatoria si la sesión duró más de 15 minutos
- El mensaje de cierre es para que Mario sepa que puede cerrar sin perder nada
```

## Resultado esperado

> Sistema completamente actualizado: nota de sesión creada, tareas actualizadas, archivos verificados, atlas_index reflejando estado actual, y mensaje de cierre claro para Mario. La próxima sesión puede empezar desde donde se dejó.

## Notas de uso

- Ejecutar aunque la sesión haya sido corta (evita perder hooks o ideas generadas)
- Si se crearon múltiples briefs, verificar que estén en la carpeta correcta antes de cerrar
- El atlas_index.md es la fuente de verdad — si no está ahí, para ATLAS no existe
- Después del cierre, Mario puede consultar el vault en Obsidian para revisar lo generado
- Para sesiones muy cortas (< 10 min), al menos actualizar tasks_active.json

---

*Links:* [[prompts-index]] · [[ATLAS-HOME]]
