# Plantilla de README para módulos

Usar esta plantilla como guía estructural. Adaptar el contenido y la extensión al tema. No es una plantilla rígida: si un módulo necesita más secciones, agregarlas. Si una sección no aplica al tema, omitirla con criterio.

**Criterios de profundidad:** cumplir los mínimos de [`content-quality-checklist.md`](content-quality-checklist.md) antes de dar el módulo por terminado.

Ver `references/navigation-conventions.md` para reglas de enlaces.

---

```markdown
# Módulo [N] — [Nombre del Módulo]

> **Objetivo:** Al terminar este módulo, serás capaz de [verbo concreto + resultado esperado].

## Navegación

← [Progreso general](../PROGRESS.md) · [Ejemplos](examples/) · [Prácticas](practices/) · [Mis soluciones](solutions/) · [Playground](playground/)

_(Omitir link a Playground si el módulo no tiene prácticas de código.)_

---

## 🧭 ¿Por qué importa esto?

**Mínimo:** ≥2 párrafos; conectar con el diagnóstico del estudiante (objetivo, trabajo, proyecto). Sin frases genéricas vacías.

[Motivación real. ¿Qué problema resuelve saber esto? ¿Qué puedes hacer que antes no podías?
Esta sección debe "enganchar" al estudiante antes de que empiece la teoría.]

---

## 🗺️ Mapa del módulo

**Mínimo:** diagrama ASCII o jerarquía que incluya todos los conceptos que se desarrollarán abajo.

[Diagrama ASCII o lista jerárquica que muestre cómo se relacionan los conceptos del módulo]

Ejemplo:
```
[Concepto A]
    ├── [Sub-concepto A1]
    │       └── [Detalle]
    └── [Sub-concepto A2]
[Concepto B]
    └── [depende de A]
```

---

## 📖 Conceptos Fundamentales

**Mínimo:** por cada concepto — analogía + definición + ≥3 párrafos de desarrollo + ejemplo rápido inline.

### [Concepto 1]

**Analogía:** [Explicar con una metáfora del mundo real antes de la definición técnica]

**Definición:** [Definición técnica precisa, pero en lenguaje accesible]

**En detalle:**
[Desarrollo profundo del concepto. Sin saltarse pasos. Cada oración debe tener sentido
para alguien que nunca lo vio antes. Si hay sub-puntos, desarrollarlos uno a uno.]

**Ejemplo rápido:**
[Un ejemplo concreto inline, breve, para anclar el concepto. Si hay código: comentarios en español.]

---

### [Concepto 2]

[Misma estructura. Repetir para cada concepto del módulo.]

---

## 🔗 Cómo se relacionan estos conceptos

**Mínimo:** tabla o diagrama que relacione al menos dos conceptos del módulo.

[Una sección que muestre cómo los conceptos del módulo interactúan entre sí.
Puede ser una tabla, un diagrama de flujo en ASCII, o prosa conectiva.]

Ejemplo de tabla comparativa:
| Concepto | Cuándo usarlo | Qué lo diferencia |
|----------|--------------|-------------------|
| A        | ...          | ...               |
| B        | ...          | ...               |

---

## ⚠️ Errores comunes

**Mínimo:** ≥3 errores; cada uno con causa y cómo evitarlo.

**Error 1: [Descripción del error]**
- Por qué ocurre: ...
- Cómo evitarlo: ...

**Error 2: [Descripción del error]**
- Por qué ocurre: ...
- Cómo evitarlo: ...

---

## 🧠 Resumen visual

**Mínimo:** condensar todos los conceptos del módulo en una vista de referencia.

[Una tabla, lista o diagrama que condense TODO el módulo en una vista rápida.
Esto sirve como "hoja de referencia" una vez que el estudiante avance.]

---

## 📂 Contenido de este módulo

### Ejemplos
- [Ejemplo 01 — [descripción]](examples/ejemplo-01-[desc].md)
- [Ejemplo 02 — [descripción]](examples/ejemplo-02-[desc].md)

### Prácticas
- [Practice 01 — [descripción]](practices/practice-01-[desc].md) → [solución](solutions/practice-01-[desc].md) · [playground](playground/practice-01/)
- [Practice 02 — [descripción]](practices/practice-02-[desc].md) → [solución](solutions/practice-02-[desc].md)

_(Incluir link a playground solo en prácticas de código.)_

---

## 📚 Referencias y recursos

**Mínimo:** URLs reales verificables.

### Documentación oficial
- [Nombre del recurso](URL) — [Una línea de por qué vale la pena leerlo]

### Artículos recomendados
- [Título](URL) — [Por qué]

### Para profundizar
- [Título](URL) — [Por qué, cuándo leerlo]

---

## ➡️ Siguiente paso

1. Revisa los [ejemplos](examples/) para ver los conceptos en acción
2. Completa las [prácticas](practices/):
   - Respuestas escritas → [solutions/](solutions/)
   - Ejercicios de código → [playground/](playground/) _(si aplica)_
3. Cuando termines, avísame en el chat para revisar tus soluciones juntos
```

---

## Plantilla de archivo de ejemplo (`examples/ejemplo-01-[desc].md`)

Nomenclatura: `ejemplo-XX`, nunca `example-XX`. Título siempre `# Ejemplo [N] — ...`.

**Código:** comentarios en español en bloques de código.

```markdown
# Ejemplo [N] — [Título descriptivo]

## Navegación

← [Progreso general](../../PROGRESS.md) · [Módulo](../README.md) · [Ejemplos](.) · [Prácticas](../practices/) · [Mis soluciones](../solutions/)

---

## ¿Qué problema resuelve este ejemplo?

[Contexto breve]

---

[Contenido del ejemplo con explicaciones; comentarios en español en el código]
```
