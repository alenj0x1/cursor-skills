# Plantilla de README para módulos

Usar esta plantilla como guía estructural. Adaptar el contenido y la extensión al tema. No es una plantilla rígida: si un módulo necesita más secciones, agregarlas. Si una sección no aplica al tema, omitirla con criterio.

---

```markdown
# Módulo [N] — [Nombre del Módulo]

> **Objetivo:** Al terminar este módulo, serás capaz de [verbo concreto + resultado esperado].

---

## 🧭 ¿Por qué importa esto?

[Motivación real. No genérica. Conectar con lo que el estudiante dijo en el diagnóstico.
¿Qué problema resuelve saber esto? ¿Qué puedes hacer que antes no podías?
Esta sección debe "enganchar" al estudiante antes de que empiece la teoría.]

---

## 🗺️ Mapa del módulo

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

### [Concepto 1]

**Analogía:** [Explicar con una metáfora del mundo real antes de la definición técnica]

**Definición:** [Definición técnica precisa, pero en lenguaje accesible]

**En detalle:**
[Desarrollo profundo del concepto. Sin saltarse pasos. Cada oración debe tener sentido
para alguien que nunca lo vio antes. Si hay sub-puntos, desarrollarlos uno a uno.]

**Ejemplo rápido:**
[Un ejemplo concreto inline, breve, para anclar el concepto]

---

### [Concepto 2]

[Misma estructura. Repetir para cada concepto del módulo.]

---

## 🔗 Cómo se relacionan estos conceptos

[Una sección que muestre cómo los conceptos del módulo interactúan entre sí.
Puede ser una tabla, un diagrama de flujo en ASCII, o prosa conectiva.]

Ejemplo de tabla comparativa:
| Concepto | Cuándo usarlo | Qué lo diferencia |
|----------|--------------|-------------------|
| A        | ...          | ...               |
| B        | ...          | ...               |

---

## ⚠️ Errores comunes

**Error 1: [Descripción del error]**
- Por qué ocurre: ...
- Cómo evitarlo: ...

**Error 2: [Descripción del error]**
- Por qué ocurre: ...
- Cómo evitarlo: ...

[Incluir al menos 3 errores frecuentes en este tema]

---

## 🧠 Resumen visual

[Una tabla, lista o diagrama que condense TODO el módulo en una vista rápida.
Esto sirve como "hoja de referencia" una vez que el estudiante avance.]

---

## 📚 Referencias y recursos

### Documentación oficial
- [Nombre del recurso](URL) — [Una línea de por qué vale la pena leerlo]

### Artículos recomendados
- [Título](URL) — [Por qué]

### Para profundizar
- [Título](URL) — [Por qué, cuándo leerlo]

---

## ➡️ Siguiente paso

Una vez que sientas que entendiste este módulo, revisa los ejemplos en `examples/`
y luego completa las prácticas en `practices/`.

Cuando termines tus soluciones, crea archivos `practice-XX-solucion.md` con tus respuestas
y avísame para revisarlas juntos.
```
