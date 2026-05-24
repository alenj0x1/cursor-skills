# Estados de progreso y criterios de evaluación

## Estados de módulos

| Emoji | Estado | Significado |
|-------|--------|-------------|
| 🔒 | Bloqueado | El módulo anterior no está completado |
| ⏳ | Pendiente | Desbloqueado, contenido no generado aún |
| 🔄 | En curso | Contenido generado, estudiante trabajando |
| ⚠️ | Requiere refuerzo | Evaluado, con puntos débiles identificados |
| ✅ | Completado | Evaluado y aprobado |

## Criterios de evaluación de prácticas

### Aprobado ✅
El estudiante demuestra que:
- Comprende el concepto central de la práctica (no solo copió del ejemplo)
- Puede aplicar el concepto en el contexto pedido
- Sus explicaciones o soluciones son coherentes, aunque no perfectas

### Requiere refuerzo ⚠️
El estudiante muestra que:
- Hay uno o más conceptos del módulo que no quedaron claros
- Las soluciones son incorrectas en aspectos fundamentales (no en detalles menores)
- Hay confusión conceptual evidente entre dos o más ideas del módulo

### Evaluación híbrida (escritas + código)

Para módulos con prácticas mixtas o de código:

| Tipo | Dónde leer | Qué evaluar |
|------|------------|-------------|
| Respuesta escrita | `solutions/practice-[NN]-[desc].md` | Comprensión conceptual, explicaciones, razonamiento |
| Código | `playground/practice-[NN]/` | Correctitud, estilo, cumplimiento de criterios de éxito del enunciado |
| Mixta | Ambas ubicaciones | Ambos criterios; la práctica no se aprueba si falla cualquiera de las partes requeridas |

### Criterio de "punto débil"
Registrar en PROGRESS.md cuando:
- Un concepto específico fue respondido incorrectamente en 2+ prácticas
- El estudiante mismo menciona que algo no le quedó claro
- Las respuestas muestran una confusión recurrente

## Formato de PROGRESS.md con links

El **título visible** (H1) debe ser `# Ruta de aprendizaje — [Tema]`, no `PROGRESS — [Tema]`. El nombre del archivo sigue siendo `PROGRESS.md`.

La tabla de módulos y la sección "Módulo Actual" deben usar links relativos. Ver `references/navigation-conventions.md`.

```markdown
# Ruta de aprendizaje — [Tema]

**Estudiante:** [nombre]
**Inicio:** [fecha]
**Última actividad:** [fecha]

---

## 📚 Módulos

| # | Módulo | Estado | Prácticas | Fecha |
|---|--------|--------|-----------|-------|
| 01 | [Fundamentos](01-fundamentos/README.md) | 🔄 En curso | [1/3](01-fundamentos/practices/) | 2026-05-23 |
| 02 | [Variables](02-variables/README.md) | 🔒 Bloqueado | [0/2](02-variables/practices/) | — |

## 📝 Módulo Actual

**[Módulo 01 — Fundamentos](01-fundamentos/README.md)**
- Estado: 🔄 En curso
- Prácticas entregadas: 1/3 — [ver prácticas](01-fundamentos/practices/) · [mis soluciones](01-fundamentos/solutions/)
- Playground: [01-fundamentos/playground/](01-fundamentos/playground/)
```

Al actualizar estados o fechas, **nunca** romper los links existentes.

## Formato de entrada en "Puntos Débiles Detectados"

```markdown
## 💡 Puntos Débiles Detectados

### [Fecha] — [Módulo 01 — Fundamentos](01-fundamentos/README.md)
- **Concepto:** [nombre del concepto]
- **Observación:** [qué confundió al estudiante]
- **Recomendación:** [qué repasar o practicar]
- **Estado:** 🔴 Sin resolver / 🟡 En refuerzo / 🟢 Superado
```

## Formato de entrada en "Historial de Feedback"

```markdown
## 📋 Historial de Feedback

### [Módulo 01 — Fundamentos](01-fundamentos/README.md) — [fecha]
**Veredicto:** ✅ Aprobado / ⚠️ Aprobado con puntos débiles

**Fortalezas:**
- [Lo que el estudiante hizo bien]

**Áreas de mejora:**
- [Lo que mejorar]

**Decisión de avance:** Avanzó a [Módulo [N+1]](02-[nombre-modulo]/README.md) / Tomó refuerzo antes de avanzar
```
